---
title: Атрибут MS-DS-целостности-дочерних элементов
description: Этот атрибут используется для проверки согласованности между каталогом и другим объектом, базой данных или приложением путем сравнения количества дочерних объектов.
ms.assetid: f7d6e8f0-963b-45a9-86af-8e51d6de32bb
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута "Active-DS-согласованность-дочерняя-Count"
- Схема AD атрибута mS-DS-Консистенцичилдкаунт
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Child-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b9c46d1c4519550a91d92d0a82f726a20572490
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138239"
---
# <a name="ms-ds-consistency-child-count-attribute"></a><span data-ttu-id="bdf69-105">Атрибут MS-DS-целостности-дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="bdf69-105">MS-DS-Consistency-Child-Count attribute</span></span>

<span data-ttu-id="bdf69-106">Этот атрибут используется для проверки согласованности между каталогом и другим объектом, базой данных или приложением путем сравнения количества дочерних объектов.</span><span class="sxs-lookup"><span data-stu-id="bdf69-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing a count of child objects.</span></span>



| <span data-ttu-id="bdf69-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-107">Entry</span></span> | <span data-ttu-id="bdf69-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="bdf69-109">CN</span><span class="sxs-lookup"><span data-stu-id="bdf69-109">CN</span></span>                | <span data-ttu-id="bdf69-110">MS-DS-целостность-дочерняя — количество</span><span class="sxs-lookup"><span data-stu-id="bdf69-110">MS-DS-Consistency-Child-Count</span></span>        |
| <span data-ttu-id="bdf69-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bdf69-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bdf69-112">mS-DS-Консистенцичилдкаунт</span><span class="sxs-lookup"><span data-stu-id="bdf69-112">mS-DS-ConsistencyChildCount</span></span>          |
| <span data-ttu-id="bdf69-113">Размер</span><span class="sxs-lookup"><span data-stu-id="bdf69-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="bdf69-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bdf69-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="bdf69-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bdf69-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="bdf69-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-116">Attribute-Id</span></span>      | <span data-ttu-id="bdf69-117">1.2.840.113556.1.4.1361</span><span class="sxs-lookup"><span data-stu-id="bdf69-117">1.2.840.113556.1.4.1361</span></span>              |
| <span data-ttu-id="bdf69-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bdf69-118">System-Id-Guid</span></span>    | <span data-ttu-id="bdf69-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="bdf69-119">178b7bc2-b63a-11d2-90e1-00c04fd91ab1</span></span> |
| <span data-ttu-id="bdf69-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdf69-120">Syntax</span></span>            | [<span data-ttu-id="bdf69-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="bdf69-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="bdf69-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bdf69-122">Implementations</span></span>

-   [<span data-ttu-id="bdf69-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bdf69-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bdf69-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bdf69-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bdf69-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bdf69-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bdf69-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bdf69-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bdf69-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bdf69-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bdf69-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bdf69-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bdf69-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bdf69-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bdf69-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bdf69-130">Windows 2000 Server</span></span>



| <span data-ttu-id="bdf69-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-131">Entry</span></span> | <span data-ttu-id="bdf69-132">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-135">System-Only</span></span>            | <span data-ttu-id="bdf69-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-136">False</span></span>                           |
| <span data-ttu-id="bdf69-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-137">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-138">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-138">True</span></span>                            |
| <span data-ttu-id="bdf69-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-139">Is Indexed</span></span>             | <span data-ttu-id="bdf69-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-140">False</span></span>                           |
| <span data-ttu-id="bdf69-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-141">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-142">False</span></span>                           |
| <span data-ttu-id="bdf69-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-147">Search-Flags</span></span>           | <span data-ttu-id="bdf69-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-148">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-149">System-Flags</span></span>           | <span data-ttu-id="bdf69-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-150">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-151">Classes used in</span></span>        | [<span data-ttu-id="bdf69-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bdf69-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdf69-153">Windows Server 2003</span></span>



| <span data-ttu-id="bdf69-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-154">Entry</span></span> | <span data-ttu-id="bdf69-155">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-158">System-Only</span></span>            | <span data-ttu-id="bdf69-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-159">False</span></span>                           |
| <span data-ttu-id="bdf69-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-160">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-161">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-161">True</span></span>                            |
| <span data-ttu-id="bdf69-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-162">Is Indexed</span></span>             | <span data-ttu-id="bdf69-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-163">False</span></span>                           |
| <span data-ttu-id="bdf69-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-164">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-165">False</span></span>                           |
| <span data-ttu-id="bdf69-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-170">Search-Flags</span></span>           | <span data-ttu-id="bdf69-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-171">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-172">System-Flags</span></span>           | <span data-ttu-id="bdf69-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-173">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-174">Classes used in</span></span>        | [<span data-ttu-id="bdf69-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bdf69-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="bdf69-176">ADAM</span></span>



| <span data-ttu-id="bdf69-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-177">Entry</span></span> | <span data-ttu-id="bdf69-178">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-181">System-Only</span></span>            | <span data-ttu-id="bdf69-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-182">False</span></span>                           |
| <span data-ttu-id="bdf69-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-183">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-184">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-184">True</span></span>                            |
| <span data-ttu-id="bdf69-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-185">Is Indexed</span></span>             | <span data-ttu-id="bdf69-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-186">False</span></span>                           |
| <span data-ttu-id="bdf69-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-187">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-188">False</span></span>                           |
| <span data-ttu-id="bdf69-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-193">Search-Flags</span></span>           | <span data-ttu-id="bdf69-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-194">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-195">System-Flags</span></span>           | <span data-ttu-id="bdf69-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-196">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-197">Classes used in</span></span>        | [<span data-ttu-id="bdf69-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bdf69-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bdf69-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bdf69-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-200">Entry</span></span> | <span data-ttu-id="bdf69-201">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-204">System-Only</span></span>            | <span data-ttu-id="bdf69-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-205">False</span></span>                           |
| <span data-ttu-id="bdf69-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-206">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-207">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-207">True</span></span>                            |
| <span data-ttu-id="bdf69-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-208">Is Indexed</span></span>             | <span data-ttu-id="bdf69-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-209">False</span></span>                           |
| <span data-ttu-id="bdf69-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-210">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-211">False</span></span>                           |
| <span data-ttu-id="bdf69-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-216">Search-Flags</span></span>           | <span data-ttu-id="bdf69-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-217">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-218">System-Flags</span></span>           | <span data-ttu-id="bdf69-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-219">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-220">Classes used in</span></span>        | [<span data-ttu-id="bdf69-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bdf69-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdf69-222">Windows Server 2008</span></span>



| <span data-ttu-id="bdf69-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-223">Entry</span></span> | <span data-ttu-id="bdf69-224">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-227">System-Only</span></span>            | <span data-ttu-id="bdf69-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-228">False</span></span>                           |
| <span data-ttu-id="bdf69-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-229">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-230">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-230">True</span></span>                            |
| <span data-ttu-id="bdf69-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-231">Is Indexed</span></span>             | <span data-ttu-id="bdf69-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-232">False</span></span>                           |
| <span data-ttu-id="bdf69-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-233">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-234">False</span></span>                           |
| <span data-ttu-id="bdf69-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-239">Search-Flags</span></span>           | <span data-ttu-id="bdf69-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-240">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-241">System-Flags</span></span>           | <span data-ttu-id="bdf69-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-242">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-243">Classes used in</span></span>        | [<span data-ttu-id="bdf69-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bdf69-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bdf69-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bdf69-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-246">Entry</span></span> | <span data-ttu-id="bdf69-247">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-250">System-Only</span></span>            | <span data-ttu-id="bdf69-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-251">False</span></span>                           |
| <span data-ttu-id="bdf69-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-252">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-253">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-253">True</span></span>                            |
| <span data-ttu-id="bdf69-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-254">Is Indexed</span></span>             | <span data-ttu-id="bdf69-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-255">False</span></span>                           |
| <span data-ttu-id="bdf69-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-256">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-257">False</span></span>                           |
| <span data-ttu-id="bdf69-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-262">Search-Flags</span></span>           | <span data-ttu-id="bdf69-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-263">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-264">System-Flags</span></span>           | <span data-ttu-id="bdf69-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-265">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-266">Classes used in</span></span>        | [<span data-ttu-id="bdf69-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bdf69-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bdf69-268">Windows Server 2012</span></span>



| <span data-ttu-id="bdf69-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="bdf69-269">Entry</span></span> | <span data-ttu-id="bdf69-270">Значение</span><span class="sxs-lookup"><span data-stu-id="bdf69-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bdf69-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bdf69-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bdf69-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="bdf69-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="bdf69-273">System-Only</span></span>            | <span data-ttu-id="bdf69-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-274">False</span></span>                           |
| <span data-ttu-id="bdf69-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bdf69-275">Is-Single-Valued</span></span>       | <span data-ttu-id="bdf69-276">True</span><span class="sxs-lookup"><span data-stu-id="bdf69-276">True</span></span>                            |
| <span data-ttu-id="bdf69-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bdf69-277">Is Indexed</span></span>             | <span data-ttu-id="bdf69-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-278">False</span></span>                           |
| <span data-ttu-id="bdf69-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bdf69-279">In Global Catalog</span></span>      | <span data-ttu-id="bdf69-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="bdf69-280">False</span></span>                           |
| <span data-ttu-id="bdf69-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bdf69-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="bdf69-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bdf69-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bdf69-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bdf69-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="bdf69-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bdf69-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="bdf69-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-285">Search-Flags</span></span>           | <span data-ttu-id="bdf69-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bdf69-286">0x00000000</span></span>                      |
| <span data-ttu-id="bdf69-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bdf69-287">System-Flags</span></span>           | <span data-ttu-id="bdf69-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bdf69-288">0x00000010</span></span>                      |
| <span data-ttu-id="bdf69-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bdf69-289">Classes used in</span></span>        | [<span data-ttu-id="bdf69-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bdf69-290">**Top**</span></span>](c-top.md)<br/> |



 

 





