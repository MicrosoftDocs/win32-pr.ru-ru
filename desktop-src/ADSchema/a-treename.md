---
title: Атрибут Tree-Name
description: DNS-имя домена в корне дерева.
ms.assetid: 3b509e77-a66e-4d80-b74e-33a4276ce1e2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Tree-Name
- Схема AD атрибута Тринаме
topic_type:
- apiref
api_name:
- Tree-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105687a5adb56198ba0908d549a7bb85fe9c1ee3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893250"
---
# <a name="tree-name-attribute"></a><span data-ttu-id="e9189-105">Атрибут Tree-Name</span><span class="sxs-lookup"><span data-stu-id="e9189-105">Tree-Name attribute</span></span>

<span data-ttu-id="e9189-106">DNS-имя домена в корне дерева.</span><span class="sxs-lookup"><span data-stu-id="e9189-106">DNS name of the domain at the root of a tree.</span></span>



| <span data-ttu-id="e9189-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-107">Entry</span></span> | <span data-ttu-id="e9189-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e9189-109">CN</span><span class="sxs-lookup"><span data-stu-id="e9189-109">CN</span></span>                | <span data-ttu-id="e9189-110">Tree-Name</span><span class="sxs-lookup"><span data-stu-id="e9189-110">Tree-Name</span></span>                                   |
| <span data-ttu-id="e9189-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e9189-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e9189-112">тринаме</span><span class="sxs-lookup"><span data-stu-id="e9189-112">treeName</span></span>                                    |
| <span data-ttu-id="e9189-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e9189-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="e9189-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e9189-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e9189-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e9189-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e9189-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-116">Attribute-Id</span></span>      | <span data-ttu-id="e9189-117">1.2.840.113556.1.4.660</span><span class="sxs-lookup"><span data-stu-id="e9189-117">1.2.840.113556.1.4.660</span></span>                      |
| <span data-ttu-id="e9189-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e9189-118">System-Id-Guid</span></span>    | <span data-ttu-id="e9189-119">28630ebd-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e9189-119">28630ebd-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="e9189-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9189-120">Syntax</span></span>            | [<span data-ttu-id="e9189-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e9189-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e9189-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e9189-122">Implementations</span></span>

-   [<span data-ttu-id="e9189-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9189-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9189-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9189-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9189-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9189-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9189-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9189-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9189-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9189-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9189-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9189-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9189-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9189-129">Windows 2000 Server</span></span>



| <span data-ttu-id="e9189-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-130">Entry</span></span> | <span data-ttu-id="e9189-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-131">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e9189-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9189-132">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-133">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9189-134">System-Only</span></span>            | <span data-ttu-id="e9189-135">True</span><span class="sxs-lookup"><span data-stu-id="e9189-135">True</span></span>                                         |
| <span data-ttu-id="e9189-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9189-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e9189-137">True</span><span class="sxs-lookup"><span data-stu-id="e9189-137">True</span></span>                                         |
| <span data-ttu-id="e9189-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9189-138">Is Indexed</span></span>             | <span data-ttu-id="e9189-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-139">False</span></span>                                        |
| <span data-ttu-id="e9189-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9189-140">In Global Catalog</span></span>      | <span data-ttu-id="e9189-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-141">False</span></span>                                        |
| <span data-ttu-id="e9189-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9189-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9189-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9189-143">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e9189-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9189-144">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e9189-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9189-145">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e9189-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-146">Search-Flags</span></span>           | <span data-ttu-id="e9189-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9189-147">0x00000000</span></span>                                   |
| <span data-ttu-id="e9189-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-148">System-Flags</span></span>           | <span data-ttu-id="e9189-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9189-149">0x00000010</span></span>                                   |
| <span data-ttu-id="e9189-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9189-150">Classes used in</span></span>        | [<span data-ttu-id="e9189-151">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e9189-151">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9189-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9189-152">Windows Server 2003</span></span>



| <span data-ttu-id="e9189-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-153">Entry</span></span> | <span data-ttu-id="e9189-154">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-154">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e9189-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9189-155">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-156">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9189-157">System-Only</span></span>            | <span data-ttu-id="e9189-158">True</span><span class="sxs-lookup"><span data-stu-id="e9189-158">True</span></span>                                         |
| <span data-ttu-id="e9189-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9189-159">Is-Single-Valued</span></span>       | <span data-ttu-id="e9189-160">True</span><span class="sxs-lookup"><span data-stu-id="e9189-160">True</span></span>                                         |
| <span data-ttu-id="e9189-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9189-161">Is Indexed</span></span>             | <span data-ttu-id="e9189-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-162">False</span></span>                                        |
| <span data-ttu-id="e9189-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9189-163">In Global Catalog</span></span>      | <span data-ttu-id="e9189-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-164">False</span></span>                                        |
| <span data-ttu-id="e9189-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9189-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9189-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9189-166">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e9189-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9189-167">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e9189-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9189-168">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e9189-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-169">Search-Flags</span></span>           | <span data-ttu-id="e9189-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9189-170">0x00000000</span></span>                                   |
| <span data-ttu-id="e9189-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-171">System-Flags</span></span>           | <span data-ttu-id="e9189-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9189-172">0x00000010</span></span>                                   |
| <span data-ttu-id="e9189-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9189-173">Classes used in</span></span>        | [<span data-ttu-id="e9189-174">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e9189-174">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9189-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9189-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9189-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-176">Entry</span></span> | <span data-ttu-id="e9189-177">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-177">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e9189-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9189-178">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-179">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9189-180">System-Only</span></span>            | <span data-ttu-id="e9189-181">True</span><span class="sxs-lookup"><span data-stu-id="e9189-181">True</span></span>                                         |
| <span data-ttu-id="e9189-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9189-182">Is-Single-Valued</span></span>       | <span data-ttu-id="e9189-183">True</span><span class="sxs-lookup"><span data-stu-id="e9189-183">True</span></span>                                         |
| <span data-ttu-id="e9189-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9189-184">Is Indexed</span></span>             | <span data-ttu-id="e9189-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-185">False</span></span>                                        |
| <span data-ttu-id="e9189-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9189-186">In Global Catalog</span></span>      | <span data-ttu-id="e9189-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-187">False</span></span>                                        |
| <span data-ttu-id="e9189-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9189-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9189-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9189-189">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e9189-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9189-190">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e9189-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9189-191">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e9189-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-192">Search-Flags</span></span>           | <span data-ttu-id="e9189-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9189-193">0x00000000</span></span>                                   |
| <span data-ttu-id="e9189-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-194">System-Flags</span></span>           | <span data-ttu-id="e9189-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9189-195">0x00000010</span></span>                                   |
| <span data-ttu-id="e9189-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9189-196">Classes used in</span></span>        | [<span data-ttu-id="e9189-197">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e9189-197">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9189-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9189-198">Windows Server 2008</span></span>



| <span data-ttu-id="e9189-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-199">Entry</span></span> | <span data-ttu-id="e9189-200">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-200">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e9189-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9189-201">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-202">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9189-203">System-Only</span></span>            | <span data-ttu-id="e9189-204">True</span><span class="sxs-lookup"><span data-stu-id="e9189-204">True</span></span>                                         |
| <span data-ttu-id="e9189-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9189-205">Is-Single-Valued</span></span>       | <span data-ttu-id="e9189-206">True</span><span class="sxs-lookup"><span data-stu-id="e9189-206">True</span></span>                                         |
| <span data-ttu-id="e9189-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9189-207">Is Indexed</span></span>             | <span data-ttu-id="e9189-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-208">False</span></span>                                        |
| <span data-ttu-id="e9189-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9189-209">In Global Catalog</span></span>      | <span data-ttu-id="e9189-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-210">False</span></span>                                        |
| <span data-ttu-id="e9189-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9189-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9189-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9189-212">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e9189-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9189-213">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e9189-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9189-214">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e9189-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-215">Search-Flags</span></span>           | <span data-ttu-id="e9189-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9189-216">0x00000000</span></span>                                   |
| <span data-ttu-id="e9189-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-217">System-Flags</span></span>           | <span data-ttu-id="e9189-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9189-218">0x00000010</span></span>                                   |
| <span data-ttu-id="e9189-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9189-219">Classes used in</span></span>        | [<span data-ttu-id="e9189-220">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e9189-220">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9189-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9189-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9189-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-222">Entry</span></span> | <span data-ttu-id="e9189-223">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-223">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e9189-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9189-224">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-225">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9189-226">System-Only</span></span>            | <span data-ttu-id="e9189-227">True</span><span class="sxs-lookup"><span data-stu-id="e9189-227">True</span></span>                                         |
| <span data-ttu-id="e9189-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9189-228">Is-Single-Valued</span></span>       | <span data-ttu-id="e9189-229">True</span><span class="sxs-lookup"><span data-stu-id="e9189-229">True</span></span>                                         |
| <span data-ttu-id="e9189-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9189-230">Is Indexed</span></span>             | <span data-ttu-id="e9189-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-231">False</span></span>                                        |
| <span data-ttu-id="e9189-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9189-232">In Global Catalog</span></span>      | <span data-ttu-id="e9189-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-233">False</span></span>                                        |
| <span data-ttu-id="e9189-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9189-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9189-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9189-235">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e9189-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9189-236">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e9189-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9189-237">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e9189-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-238">Search-Flags</span></span>           | <span data-ttu-id="e9189-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9189-239">0x00000000</span></span>                                   |
| <span data-ttu-id="e9189-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-240">System-Flags</span></span>           | <span data-ttu-id="e9189-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9189-241">0x00000010</span></span>                                   |
| <span data-ttu-id="e9189-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9189-242">Classes used in</span></span>        | [<span data-ttu-id="e9189-243">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e9189-243">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9189-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9189-244">Windows Server 2012</span></span>



| <span data-ttu-id="e9189-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9189-245">Entry</span></span> | <span data-ttu-id="e9189-246">Значение</span><span class="sxs-lookup"><span data-stu-id="e9189-246">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="e9189-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9189-247">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9189-248">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="e9189-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9189-249">System-Only</span></span>            | <span data-ttu-id="e9189-250">True</span><span class="sxs-lookup"><span data-stu-id="e9189-250">True</span></span>                                         |
| <span data-ttu-id="e9189-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9189-251">Is-Single-Valued</span></span>       | <span data-ttu-id="e9189-252">True</span><span class="sxs-lookup"><span data-stu-id="e9189-252">True</span></span>                                         |
| <span data-ttu-id="e9189-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9189-253">Is Indexed</span></span>             | <span data-ttu-id="e9189-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-254">False</span></span>                                        |
| <span data-ttu-id="e9189-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9189-255">In Global Catalog</span></span>      | <span data-ttu-id="e9189-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9189-256">False</span></span>                                        |
| <span data-ttu-id="e9189-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9189-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9189-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9189-258">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="e9189-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9189-259">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="e9189-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9189-260">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="e9189-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-261">Search-Flags</span></span>           | <span data-ttu-id="e9189-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9189-262">0x00000000</span></span>                                   |
| <span data-ttu-id="e9189-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9189-263">System-Flags</span></span>           | <span data-ttu-id="e9189-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9189-264">0x00000010</span></span>                                   |
| <span data-ttu-id="e9189-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9189-265">Classes used in</span></span>        | [<span data-ttu-id="e9189-266">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="e9189-266">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





