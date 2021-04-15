---
title: Атрибут "рассматривать как конечный лист"
description: Описатели отображения. Этот флаг имеет значение TRUE, чтобы связанный класс отображался как конечный класс, даже если он имеет дочерние элементы.
ms.assetid: 7b19fc04-69ac-4e4b-8b9b-bd1ec74fcea7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "рассматривать как конечный лист"
- Схема AD атрибута Треатаслеаф
topic_type:
- apiref
api_name:
- Treat-As-Leaf
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d357fa368818a9b216fe18a394b806e390b46b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655280"
---
# <a name="treat-as-leaf-attribute"></a><span data-ttu-id="8924b-105">Атрибут "рассматривать как конечный лист"</span><span class="sxs-lookup"><span data-stu-id="8924b-105">Treat-As-Leaf attribute</span></span>

<span data-ttu-id="8924b-106">Описатели отображения. Этот флаг имеет значение **true** , чтобы связанный класс отображался как конечный класс, даже если он имеет дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="8924b-106">Display-specifiers with this flag set to **TRUE** force the related class to be displayed as a leaf class even if it has children.</span></span>



| <span data-ttu-id="8924b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-107">Entry</span></span> | <span data-ttu-id="8924b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8924b-109">CN</span><span class="sxs-lookup"><span data-stu-id="8924b-109">CN</span></span>                | <span data-ttu-id="8924b-110">Обрабатывать как конечный</span><span class="sxs-lookup"><span data-stu-id="8924b-110">Treat-As-Leaf</span></span>                        |
| <span data-ttu-id="8924b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8924b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8924b-112">треатаслеаф</span><span class="sxs-lookup"><span data-stu-id="8924b-112">treatAsLeaf</span></span>                          |
| <span data-ttu-id="8924b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8924b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="8924b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8924b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8924b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8924b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8924b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-116">Attribute-Id</span></span>      | <span data-ttu-id="8924b-117">1.2.840.113556.1.4.806</span><span class="sxs-lookup"><span data-stu-id="8924b-117">1.2.840.113556.1.4.806</span></span>               |
| <span data-ttu-id="8924b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8924b-118">System-Id-Guid</span></span>    | <span data-ttu-id="8924b-119">8fd044e3-771f-11d1-aeae-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8924b-119">8fd044e3-771f-11d1-aeae-0000f80367c1</span></span> |
| <span data-ttu-id="8924b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8924b-120">Syntax</span></span>            | [<span data-ttu-id="8924b-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="8924b-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="8924b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8924b-122">Implementations</span></span>

-   [<span data-ttu-id="8924b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8924b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8924b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8924b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8924b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8924b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8924b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8924b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8924b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8924b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8924b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8924b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8924b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8924b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8924b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-130">Entry</span></span> | <span data-ttu-id="8924b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-131">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8924b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8924b-132">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-133">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8924b-134">System-Only</span></span>            | <span data-ttu-id="8924b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-135">False</span></span>                                                      |
| <span data-ttu-id="8924b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8924b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8924b-137">True</span><span class="sxs-lookup"><span data-stu-id="8924b-137">True</span></span>                                                       |
| <span data-ttu-id="8924b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8924b-138">Is Indexed</span></span>             | <span data-ttu-id="8924b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-139">False</span></span>                                                      |
| <span data-ttu-id="8924b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8924b-140">In Global Catalog</span></span>      | <span data-ttu-id="8924b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-141">False</span></span>                                                      |
| <span data-ttu-id="8924b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8924b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8924b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8924b-143">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8924b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8924b-144">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8924b-145">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-146">Search-Flags</span></span>           | <span data-ttu-id="8924b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8924b-147">0x00000000</span></span>                                                 |
| <span data-ttu-id="8924b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-148">System-Flags</span></span>           | <span data-ttu-id="8924b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8924b-149">0x00000010</span></span>                                                 |
| <span data-ttu-id="8924b-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8924b-150">Classes used in</span></span>        | [<span data-ttu-id="8924b-151">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="8924b-151">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8924b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8924b-152">Windows Server 2003</span></span>



| <span data-ttu-id="8924b-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-153">Entry</span></span> | <span data-ttu-id="8924b-154">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-154">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8924b-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8924b-155">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-156">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8924b-157">System-Only</span></span>            | <span data-ttu-id="8924b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-158">False</span></span>                                                      |
| <span data-ttu-id="8924b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8924b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8924b-160">True</span><span class="sxs-lookup"><span data-stu-id="8924b-160">True</span></span>                                                       |
| <span data-ttu-id="8924b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8924b-161">Is Indexed</span></span>             | <span data-ttu-id="8924b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-162">False</span></span>                                                      |
| <span data-ttu-id="8924b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8924b-163">In Global Catalog</span></span>      | <span data-ttu-id="8924b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-164">False</span></span>                                                      |
| <span data-ttu-id="8924b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8924b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8924b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8924b-166">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8924b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8924b-167">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8924b-168">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-169">Search-Flags</span></span>           | <span data-ttu-id="8924b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8924b-170">0x00000000</span></span>                                                 |
| <span data-ttu-id="8924b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-171">System-Flags</span></span>           | <span data-ttu-id="8924b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8924b-172">0x00000010</span></span>                                                 |
| <span data-ttu-id="8924b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8924b-173">Classes used in</span></span>        | [<span data-ttu-id="8924b-174">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="8924b-174">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8924b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8924b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8924b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-176">Entry</span></span> | <span data-ttu-id="8924b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-177">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8924b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8924b-178">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-179">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="8924b-180">System-Only</span></span>            | <span data-ttu-id="8924b-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-181">False</span></span>                                                      |
| <span data-ttu-id="8924b-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8924b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="8924b-183">True</span><span class="sxs-lookup"><span data-stu-id="8924b-183">True</span></span>                                                       |
| <span data-ttu-id="8924b-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8924b-184">Is Indexed</span></span>             | <span data-ttu-id="8924b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-185">False</span></span>                                                      |
| <span data-ttu-id="8924b-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8924b-186">In Global Catalog</span></span>      | <span data-ttu-id="8924b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-187">False</span></span>                                                      |
| <span data-ttu-id="8924b-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8924b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="8924b-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8924b-189">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8924b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8924b-190">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8924b-191">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-192">Search-Flags</span></span>           | <span data-ttu-id="8924b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8924b-193">0x00000000</span></span>                                                 |
| <span data-ttu-id="8924b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-194">System-Flags</span></span>           | <span data-ttu-id="8924b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8924b-195">0x00000010</span></span>                                                 |
| <span data-ttu-id="8924b-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8924b-196">Classes used in</span></span>        | [<span data-ttu-id="8924b-197">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="8924b-197">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8924b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8924b-198">Windows Server 2008</span></span>



| <span data-ttu-id="8924b-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-199">Entry</span></span> | <span data-ttu-id="8924b-200">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-200">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8924b-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8924b-201">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-202">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8924b-203">System-Only</span></span>            | <span data-ttu-id="8924b-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-204">False</span></span>                                                      |
| <span data-ttu-id="8924b-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8924b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8924b-206">True</span><span class="sxs-lookup"><span data-stu-id="8924b-206">True</span></span>                                                       |
| <span data-ttu-id="8924b-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8924b-207">Is Indexed</span></span>             | <span data-ttu-id="8924b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-208">False</span></span>                                                      |
| <span data-ttu-id="8924b-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8924b-209">In Global Catalog</span></span>      | <span data-ttu-id="8924b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-210">False</span></span>                                                      |
| <span data-ttu-id="8924b-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8924b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8924b-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8924b-212">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8924b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8924b-213">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8924b-214">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-215">Search-Flags</span></span>           | <span data-ttu-id="8924b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8924b-216">0x00000000</span></span>                                                 |
| <span data-ttu-id="8924b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-217">System-Flags</span></span>           | <span data-ttu-id="8924b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8924b-218">0x00000010</span></span>                                                 |
| <span data-ttu-id="8924b-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8924b-219">Classes used in</span></span>        | [<span data-ttu-id="8924b-220">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="8924b-220">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8924b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8924b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8924b-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-222">Entry</span></span> | <span data-ttu-id="8924b-223">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-223">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8924b-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8924b-224">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-225">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="8924b-226">System-Only</span></span>            | <span data-ttu-id="8924b-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-227">False</span></span>                                                      |
| <span data-ttu-id="8924b-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8924b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="8924b-229">True</span><span class="sxs-lookup"><span data-stu-id="8924b-229">True</span></span>                                                       |
| <span data-ttu-id="8924b-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8924b-230">Is Indexed</span></span>             | <span data-ttu-id="8924b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-231">False</span></span>                                                      |
| <span data-ttu-id="8924b-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8924b-232">In Global Catalog</span></span>      | <span data-ttu-id="8924b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-233">False</span></span>                                                      |
| <span data-ttu-id="8924b-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8924b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="8924b-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8924b-235">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8924b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8924b-236">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8924b-237">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-238">Search-Flags</span></span>           | <span data-ttu-id="8924b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8924b-239">0x00000000</span></span>                                                 |
| <span data-ttu-id="8924b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-240">System-Flags</span></span>           | <span data-ttu-id="8924b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8924b-241">0x00000010</span></span>                                                 |
| <span data-ttu-id="8924b-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8924b-242">Classes used in</span></span>        | [<span data-ttu-id="8924b-243">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="8924b-243">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8924b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8924b-244">Windows Server 2012</span></span>



| <span data-ttu-id="8924b-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="8924b-245">Entry</span></span> | <span data-ttu-id="8924b-246">Значение</span><span class="sxs-lookup"><span data-stu-id="8924b-246">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="8924b-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8924b-247">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8924b-248">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="8924b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="8924b-249">System-Only</span></span>            | <span data-ttu-id="8924b-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-250">False</span></span>                                                      |
| <span data-ttu-id="8924b-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8924b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="8924b-252">True</span><span class="sxs-lookup"><span data-stu-id="8924b-252">True</span></span>                                                       |
| <span data-ttu-id="8924b-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8924b-253">Is Indexed</span></span>             | <span data-ttu-id="8924b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-254">False</span></span>                                                      |
| <span data-ttu-id="8924b-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8924b-255">In Global Catalog</span></span>      | <span data-ttu-id="8924b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8924b-256">False</span></span>                                                      |
| <span data-ttu-id="8924b-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8924b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="8924b-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8924b-258">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="8924b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8924b-259">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8924b-260">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="8924b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-261">Search-Flags</span></span>           | <span data-ttu-id="8924b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8924b-262">0x00000000</span></span>                                                 |
| <span data-ttu-id="8924b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8924b-263">System-Flags</span></span>           | <span data-ttu-id="8924b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8924b-264">0x00000010</span></span>                                                 |
| <span data-ttu-id="8924b-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8924b-265">Classes used in</span></span>        | [<span data-ttu-id="8924b-266">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="8924b-266">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





