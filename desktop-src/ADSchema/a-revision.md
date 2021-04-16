---
title: Атрибут Revision
description: Уровень редакции для дескриптора безопасности или другое изменение. Используется только в объектах SAM-Server и DS-UI-Settings.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Revision
- Схема AD атрибута Revision
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8948bd865db776c52ac021d296792a6f7d0720dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535903"
---
# <a name="revision-attribute"></a><span data-ttu-id="814f9-106">Атрибут Revision</span><span class="sxs-lookup"><span data-stu-id="814f9-106">Revision attribute</span></span>

<span data-ttu-id="814f9-107">Уровень редакции для дескриптора безопасности или другое изменение.</span><span class="sxs-lookup"><span data-stu-id="814f9-107">The revision level for a security descriptor or other change.</span></span> <span data-ttu-id="814f9-108">Используется только в объектах SAM-Server и DS-UI-Settings.</span><span class="sxs-lookup"><span data-stu-id="814f9-108">Only used in the sam-server and ds-ui-settings objects.</span></span>



| <span data-ttu-id="814f9-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-109">Entry</span></span> | <span data-ttu-id="814f9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="814f9-111">CN</span><span class="sxs-lookup"><span data-stu-id="814f9-111">CN</span></span>                | <span data-ttu-id="814f9-112">Редакция</span><span class="sxs-lookup"><span data-stu-id="814f9-112">Revision</span></span>                             |
| <span data-ttu-id="814f9-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="814f9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="814f9-114">revision</span><span class="sxs-lookup"><span data-stu-id="814f9-114">revision</span></span>                             |
| <span data-ttu-id="814f9-115">Размер</span><span class="sxs-lookup"><span data-stu-id="814f9-115">Size</span></span>              | <span data-ttu-id="814f9-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="814f9-116">4 bytes</span></span>                              |
| <span data-ttu-id="814f9-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="814f9-117">Update Privilege</span></span>  | <span data-ttu-id="814f9-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="814f9-118">This value is set by the system.</span></span>     |
| <span data-ttu-id="814f9-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="814f9-119">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="814f9-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-120">Attribute-Id</span></span>      | <span data-ttu-id="814f9-121">1.2.840.113556.1.4.145</span><span class="sxs-lookup"><span data-stu-id="814f9-121">1.2.840.113556.1.4.145</span></span>               |
| <span data-ttu-id="814f9-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="814f9-122">System-Id-Guid</span></span>    | <span data-ttu-id="814f9-123">bf967a21-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="814f9-123">bf967a21-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="814f9-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="814f9-124">Syntax</span></span>            | [<span data-ttu-id="814f9-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="814f9-125">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="814f9-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="814f9-126">Implementations</span></span>

-   [<span data-ttu-id="814f9-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="814f9-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="814f9-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="814f9-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="814f9-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="814f9-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="814f9-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="814f9-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="814f9-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="814f9-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="814f9-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="814f9-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="814f9-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="814f9-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="814f9-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="814f9-134">Windows 2000 Server</span></span>



| <span data-ttu-id="814f9-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-135">Entry</span></span> | <span data-ttu-id="814f9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-136">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814f9-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-137">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-138">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-139">System-Only</span></span>            | <span data-ttu-id="814f9-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-140">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-141">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-142">True</span><span class="sxs-lookup"><span data-stu-id="814f9-142">True</span></span>                                                                                  |
| <span data-ttu-id="814f9-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-143">Is Indexed</span></span>             | <span data-ttu-id="814f9-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-144">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-145">In Global Catalog</span></span>      | <span data-ttu-id="814f9-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-146">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-148">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="814f9-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-149">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-150">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-151">Search-Flags</span></span>           | <span data-ttu-id="814f9-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-152">0x00000000</span></span>                                                                            |
| <span data-ttu-id="814f9-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-153">System-Flags</span></span>           | <span data-ttu-id="814f9-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-154">0x00000010</span></span>                                                                            |
| <span data-ttu-id="814f9-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-155">Classes used in</span></span>        | [<span data-ttu-id="814f9-156">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="814f9-156">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="814f9-157">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="814f9-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="814f9-158">Windows Server 2003</span></span>



| <span data-ttu-id="814f9-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-159">Entry</span></span> | <span data-ttu-id="814f9-160">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-160">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814f9-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-161">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-162">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-163">System-Only</span></span>            | <span data-ttu-id="814f9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-164">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-165">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-166">True</span><span class="sxs-lookup"><span data-stu-id="814f9-166">True</span></span>                                                                                  |
| <span data-ttu-id="814f9-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-167">Is Indexed</span></span>             | <span data-ttu-id="814f9-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-168">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-169">In Global Catalog</span></span>      | <span data-ttu-id="814f9-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-170">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-172">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="814f9-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-173">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-174">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-175">Search-Flags</span></span>           | <span data-ttu-id="814f9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-176">0x00000000</span></span>                                                                            |
| <span data-ttu-id="814f9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-177">System-Flags</span></span>           | <span data-ttu-id="814f9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-178">0x00000010</span></span>                                                                            |
| <span data-ttu-id="814f9-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-179">Classes used in</span></span>        | [<span data-ttu-id="814f9-180">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="814f9-180">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="814f9-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="814f9-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="814f9-182">ADAM</span></span>



| <span data-ttu-id="814f9-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-183">Entry</span></span> | <span data-ttu-id="814f9-184">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="814f9-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="814f9-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="814f9-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-187">System-Only</span></span>            | <span data-ttu-id="814f9-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-188">False</span></span>                           |
| <span data-ttu-id="814f9-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-189">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-190">True</span><span class="sxs-lookup"><span data-stu-id="814f9-190">True</span></span>                            |
| <span data-ttu-id="814f9-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-191">Is Indexed</span></span>             | <span data-ttu-id="814f9-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-192">False</span></span>                           |
| <span data-ttu-id="814f9-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-193">In Global Catalog</span></span>      | <span data-ttu-id="814f9-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-194">False</span></span>                           |
| <span data-ttu-id="814f9-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="814f9-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="814f9-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="814f9-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-199">Search-Flags</span></span>           | <span data-ttu-id="814f9-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-200">0x00000000</span></span>                      |
| <span data-ttu-id="814f9-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-201">System-Flags</span></span>           | <span data-ttu-id="814f9-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-202">0x00000010</span></span>                      |
| <span data-ttu-id="814f9-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-203">Classes used in</span></span>        | [<span data-ttu-id="814f9-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="814f9-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="814f9-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="814f9-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-206">Entry</span></span> | <span data-ttu-id="814f9-207">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-207">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814f9-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-208">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-209">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-210">System-Only</span></span>            | <span data-ttu-id="814f9-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-211">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-212">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-213">True</span><span class="sxs-lookup"><span data-stu-id="814f9-213">True</span></span>                                                                                  |
| <span data-ttu-id="814f9-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-214">Is Indexed</span></span>             | <span data-ttu-id="814f9-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-215">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-216">In Global Catalog</span></span>      | <span data-ttu-id="814f9-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-217">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-219">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="814f9-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-220">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-221">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-222">Search-Flags</span></span>           | <span data-ttu-id="814f9-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-223">0x00000000</span></span>                                                                            |
| <span data-ttu-id="814f9-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-224">System-Flags</span></span>           | <span data-ttu-id="814f9-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-225">0x00000010</span></span>                                                                            |
| <span data-ttu-id="814f9-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-226">Classes used in</span></span>        | [<span data-ttu-id="814f9-227">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="814f9-227">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="814f9-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="814f9-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="814f9-229">Windows Server 2008</span></span>



| <span data-ttu-id="814f9-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-230">Entry</span></span> | <span data-ttu-id="814f9-231">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-231">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814f9-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-232">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-233">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-234">System-Only</span></span>            | <span data-ttu-id="814f9-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-235">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-236">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-237">True</span><span class="sxs-lookup"><span data-stu-id="814f9-237">True</span></span>                                                                                  |
| <span data-ttu-id="814f9-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-238">Is Indexed</span></span>             | <span data-ttu-id="814f9-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-239">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-240">In Global Catalog</span></span>      | <span data-ttu-id="814f9-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-241">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-243">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="814f9-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-244">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-245">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-246">Search-Flags</span></span>           | <span data-ttu-id="814f9-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-247">0x00000000</span></span>                                                                            |
| <span data-ttu-id="814f9-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-248">System-Flags</span></span>           | <span data-ttu-id="814f9-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-249">0x00000010</span></span>                                                                            |
| <span data-ttu-id="814f9-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-250">Classes used in</span></span>        | [<span data-ttu-id="814f9-251">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="814f9-251">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="814f9-252">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="814f9-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="814f9-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="814f9-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-254">Entry</span></span> | <span data-ttu-id="814f9-255">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-255">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814f9-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-256">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-257">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-258">System-Only</span></span>            | <span data-ttu-id="814f9-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-259">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-260">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-261">True</span><span class="sxs-lookup"><span data-stu-id="814f9-261">True</span></span>                                                                                  |
| <span data-ttu-id="814f9-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-262">Is Indexed</span></span>             | <span data-ttu-id="814f9-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-263">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-264">In Global Catalog</span></span>      | <span data-ttu-id="814f9-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-265">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-267">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="814f9-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-268">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-269">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-270">Search-Flags</span></span>           | <span data-ttu-id="814f9-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-271">0x00000000</span></span>                                                                            |
| <span data-ttu-id="814f9-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-272">System-Flags</span></span>           | <span data-ttu-id="814f9-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-273">0x00000010</span></span>                                                                            |
| <span data-ttu-id="814f9-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-274">Classes used in</span></span>        | [<span data-ttu-id="814f9-275">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="814f9-275">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="814f9-276">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="814f9-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="814f9-277">Windows Server 2012</span></span>



| <span data-ttu-id="814f9-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="814f9-278">Entry</span></span> | <span data-ttu-id="814f9-279">Значение</span><span class="sxs-lookup"><span data-stu-id="814f9-279">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814f9-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="814f9-280">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="814f9-281">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="814f9-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="814f9-282">System-Only</span></span>            | <span data-ttu-id="814f9-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-283">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="814f9-284">Is-Single-Valued</span></span>       | <span data-ttu-id="814f9-285">True</span><span class="sxs-lookup"><span data-stu-id="814f9-285">True</span></span>                                                                                  |
| <span data-ttu-id="814f9-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="814f9-286">Is Indexed</span></span>             | <span data-ttu-id="814f9-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-287">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="814f9-288">In Global Catalog</span></span>      | <span data-ttu-id="814f9-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="814f9-289">False</span></span>                                                                                 |
| <span data-ttu-id="814f9-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="814f9-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="814f9-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="814f9-291">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="814f9-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="814f9-292">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="814f9-293">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="814f9-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-294">Search-Flags</span></span>           | <span data-ttu-id="814f9-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="814f9-295">0x00000000</span></span>                                                                            |
| <span data-ttu-id="814f9-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="814f9-296">System-Flags</span></span>           | <span data-ttu-id="814f9-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="814f9-297">0x00000010</span></span>                                                                            |
| <span data-ttu-id="814f9-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="814f9-298">Classes used in</span></span>        | [<span data-ttu-id="814f9-299">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="814f9-299">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> [<span data-ttu-id="814f9-300">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="814f9-300">**Top**</span></span>](c-top.md)<br/> |



 

 





