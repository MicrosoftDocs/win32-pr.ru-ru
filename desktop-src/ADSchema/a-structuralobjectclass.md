---
title: Атрибут "структурный объект — класс"
description: Этот сконструированный атрибут хранит список классов, содержащихся в иерархии классов, включая абстрактные классы. Этот список содержит динамически связанные вспомогательные классы.
ms.assetid: f7311cb9-4816-4caa-9cae-cbcd61b93d27
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута класса структурного объекта
- Схема AD атрибута Структуралобжекткласс
topic_type:
- apiref
api_name:
- Structural-Object-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdcc236c0c65aa365400894dd6ccfb845af04b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655286"
---
# <a name="structural-object-class-attribute"></a><span data-ttu-id="27241-106">Атрибут "структурный объект — класс"</span><span class="sxs-lookup"><span data-stu-id="27241-106">Structural-Object-Class attribute</span></span>

<span data-ttu-id="27241-107">Этот сконструированный атрибут хранит список классов, содержащихся в иерархии классов, включая абстрактные классы.</span><span class="sxs-lookup"><span data-stu-id="27241-107">This constructed attribute stores a list of classes contained in a class hierarchy, including abstract classes.</span></span> <span data-ttu-id="27241-108">Этот список содержит динамически связанные вспомогательные классы.</span><span class="sxs-lookup"><span data-stu-id="27241-108">This list does contain dynamically linked auxiliary classes.</span></span>



| <span data-ttu-id="27241-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-109">Entry</span></span> | <span data-ttu-id="27241-110">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="27241-111">CN</span><span class="sxs-lookup"><span data-stu-id="27241-111">CN</span></span>                | <span data-ttu-id="27241-112">Структурный объектный класс</span><span class="sxs-lookup"><span data-stu-id="27241-112">Structural-Object-Class</span></span>                                         |
| <span data-ttu-id="27241-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="27241-113">Ldap-Display-Name</span></span> | <span data-ttu-id="27241-114">структуралобжекткласс</span><span class="sxs-lookup"><span data-stu-id="27241-114">structuralObjectClass</span></span>                                           |
| <span data-ttu-id="27241-115">Размер</span><span class="sxs-lookup"><span data-stu-id="27241-115">Size</span></span>              | \-                                                              |
| <span data-ttu-id="27241-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="27241-116">Update Privilege</span></span>  | <span data-ttu-id="27241-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="27241-117">This value is set by the system.</span></span>                                |
| <span data-ttu-id="27241-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="27241-118">Update Frequency</span></span>  | <span data-ttu-id="27241-119">При создании класса.</span><span class="sxs-lookup"><span data-stu-id="27241-119">At class creation.</span></span>                                              |
| <span data-ttu-id="27241-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27241-120">Attribute-Id</span></span>      | <span data-ttu-id="27241-121">2.5.21.9</span><span class="sxs-lookup"><span data-stu-id="27241-121">2.5.21.9</span></span>                                                        |
| <span data-ttu-id="27241-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="27241-122">System-Id-Guid</span></span>    | <span data-ttu-id="27241-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span><span class="sxs-lookup"><span data-stu-id="27241-123">3860949f-f6a8-4b38-9950-81ecb6bc2982</span></span>                            |
| <span data-ttu-id="27241-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27241-124">Syntax</span></span>            | [<span data-ttu-id="27241-125">**String(идентификатор_объекта)**</span><span class="sxs-lookup"><span data-stu-id="27241-125">**String(Object-Identifier)**</span></span>](s-string-object-identifier.md) |



## <a name="implementations"></a><span data-ttu-id="27241-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="27241-126">Implementations</span></span>

-   [<span data-ttu-id="27241-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27241-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27241-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="27241-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="27241-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27241-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27241-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27241-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27241-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27241-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27241-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27241-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="27241-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27241-133">Windows Server 2003</span></span>



| <span data-ttu-id="27241-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-134">Entry</span></span> | <span data-ttu-id="27241-135">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="27241-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27241-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27241-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="27241-138">System-Only</span></span>            | <span data-ttu-id="27241-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-139">False</span></span>                           |
| <span data-ttu-id="27241-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27241-140">Is-Single-Valued</span></span>       | <span data-ttu-id="27241-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-141">False</span></span>                           |
| <span data-ttu-id="27241-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27241-142">Is Indexed</span></span>             | <span data-ttu-id="27241-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-143">False</span></span>                           |
| <span data-ttu-id="27241-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27241-144">In Global Catalog</span></span>      | <span data-ttu-id="27241-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-145">False</span></span>                           |
| <span data-ttu-id="27241-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27241-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="27241-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27241-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="27241-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27241-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="27241-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27241-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="27241-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-150">Search-Flags</span></span>           | <span data-ttu-id="27241-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27241-151">0x00000000</span></span>                      |
| <span data-ttu-id="27241-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-152">System-Flags</span></span>           | <span data-ttu-id="27241-153">0x00000014</span><span class="sxs-lookup"><span data-stu-id="27241-153">0x00000014</span></span>                      |
| <span data-ttu-id="27241-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27241-154">Classes used in</span></span>        | [<span data-ttu-id="27241-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="27241-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="27241-156">ADAM</span><span class="sxs-lookup"><span data-stu-id="27241-156">ADAM</span></span>



| <span data-ttu-id="27241-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-157">Entry</span></span> | <span data-ttu-id="27241-158">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="27241-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27241-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27241-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="27241-161">System-Only</span></span>            | <span data-ttu-id="27241-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-162">False</span></span>                           |
| <span data-ttu-id="27241-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27241-163">Is-Single-Valued</span></span>       | <span data-ttu-id="27241-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-164">False</span></span>                           |
| <span data-ttu-id="27241-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27241-165">Is Indexed</span></span>             | <span data-ttu-id="27241-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-166">False</span></span>                           |
| <span data-ttu-id="27241-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27241-167">In Global Catalog</span></span>      | <span data-ttu-id="27241-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-168">False</span></span>                           |
| <span data-ttu-id="27241-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27241-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="27241-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27241-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="27241-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27241-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="27241-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27241-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="27241-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-173">Search-Flags</span></span>           | <span data-ttu-id="27241-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27241-174">0x00000000</span></span>                      |
| <span data-ttu-id="27241-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-175">System-Flags</span></span>           | <span data-ttu-id="27241-176">0x00000014</span><span class="sxs-lookup"><span data-stu-id="27241-176">0x00000014</span></span>                      |
| <span data-ttu-id="27241-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27241-177">Classes used in</span></span>        | [<span data-ttu-id="27241-178">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="27241-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27241-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27241-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27241-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-180">Entry</span></span> | <span data-ttu-id="27241-181">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="27241-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27241-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27241-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="27241-184">System-Only</span></span>            | <span data-ttu-id="27241-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-185">False</span></span>                           |
| <span data-ttu-id="27241-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27241-186">Is-Single-Valued</span></span>       | <span data-ttu-id="27241-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-187">False</span></span>                           |
| <span data-ttu-id="27241-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27241-188">Is Indexed</span></span>             | <span data-ttu-id="27241-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-189">False</span></span>                           |
| <span data-ttu-id="27241-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27241-190">In Global Catalog</span></span>      | <span data-ttu-id="27241-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-191">False</span></span>                           |
| <span data-ttu-id="27241-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27241-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="27241-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27241-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="27241-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27241-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="27241-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27241-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="27241-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-196">Search-Flags</span></span>           | <span data-ttu-id="27241-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27241-197">0x00000000</span></span>                      |
| <span data-ttu-id="27241-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-198">System-Flags</span></span>           | <span data-ttu-id="27241-199">0x00000014</span><span class="sxs-lookup"><span data-stu-id="27241-199">0x00000014</span></span>                      |
| <span data-ttu-id="27241-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27241-200">Classes used in</span></span>        | [<span data-ttu-id="27241-201">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="27241-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27241-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27241-202">Windows Server 2008</span></span>



| <span data-ttu-id="27241-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-203">Entry</span></span> | <span data-ttu-id="27241-204">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="27241-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27241-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27241-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="27241-207">System-Only</span></span>            | <span data-ttu-id="27241-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-208">False</span></span>                           |
| <span data-ttu-id="27241-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27241-209">Is-Single-Valued</span></span>       | <span data-ttu-id="27241-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-210">False</span></span>                           |
| <span data-ttu-id="27241-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27241-211">Is Indexed</span></span>             | <span data-ttu-id="27241-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-212">False</span></span>                           |
| <span data-ttu-id="27241-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27241-213">In Global Catalog</span></span>      | <span data-ttu-id="27241-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-214">False</span></span>                           |
| <span data-ttu-id="27241-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27241-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="27241-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27241-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="27241-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27241-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="27241-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27241-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="27241-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-219">Search-Flags</span></span>           | <span data-ttu-id="27241-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27241-220">0x00000000</span></span>                      |
| <span data-ttu-id="27241-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-221">System-Flags</span></span>           | <span data-ttu-id="27241-222">0x00000014</span><span class="sxs-lookup"><span data-stu-id="27241-222">0x00000014</span></span>                      |
| <span data-ttu-id="27241-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27241-223">Classes used in</span></span>        | [<span data-ttu-id="27241-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="27241-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27241-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27241-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27241-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-226">Entry</span></span> | <span data-ttu-id="27241-227">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="27241-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27241-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27241-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="27241-230">System-Only</span></span>            | <span data-ttu-id="27241-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-231">False</span></span>                           |
| <span data-ttu-id="27241-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27241-232">Is-Single-Valued</span></span>       | <span data-ttu-id="27241-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-233">False</span></span>                           |
| <span data-ttu-id="27241-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27241-234">Is Indexed</span></span>             | <span data-ttu-id="27241-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-235">False</span></span>                           |
| <span data-ttu-id="27241-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27241-236">In Global Catalog</span></span>      | <span data-ttu-id="27241-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-237">False</span></span>                           |
| <span data-ttu-id="27241-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27241-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="27241-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27241-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="27241-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27241-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="27241-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27241-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="27241-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-242">Search-Flags</span></span>           | <span data-ttu-id="27241-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27241-243">0x00000000</span></span>                      |
| <span data-ttu-id="27241-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-244">System-Flags</span></span>           | <span data-ttu-id="27241-245">0x00000014</span><span class="sxs-lookup"><span data-stu-id="27241-245">0x00000014</span></span>                      |
| <span data-ttu-id="27241-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27241-246">Classes used in</span></span>        | [<span data-ttu-id="27241-247">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="27241-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27241-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27241-248">Windows Server 2012</span></span>



| <span data-ttu-id="27241-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="27241-249">Entry</span></span> | <span data-ttu-id="27241-250">Значение</span><span class="sxs-lookup"><span data-stu-id="27241-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="27241-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27241-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27241-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="27241-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="27241-253">System-Only</span></span>            | <span data-ttu-id="27241-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-254">False</span></span>                           |
| <span data-ttu-id="27241-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27241-255">Is-Single-Valued</span></span>       | <span data-ttu-id="27241-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-256">False</span></span>                           |
| <span data-ttu-id="27241-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27241-257">Is Indexed</span></span>             | <span data-ttu-id="27241-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-258">False</span></span>                           |
| <span data-ttu-id="27241-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27241-259">In Global Catalog</span></span>      | <span data-ttu-id="27241-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="27241-260">False</span></span>                           |
| <span data-ttu-id="27241-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27241-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="27241-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27241-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="27241-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27241-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="27241-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27241-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="27241-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-265">Search-Flags</span></span>           | <span data-ttu-id="27241-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27241-266">0x00000000</span></span>                      |
| <span data-ttu-id="27241-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27241-267">System-Flags</span></span>           | <span data-ttu-id="27241-268">0x00000014</span><span class="sxs-lookup"><span data-stu-id="27241-268">0x00000014</span></span>                      |
| <span data-ttu-id="27241-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27241-269">Classes used in</span></span>        | [<span data-ttu-id="27241-270">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="27241-270">**Top**</span></span>](c-top.md)<br/> |



 

 





