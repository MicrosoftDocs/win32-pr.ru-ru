---
title: Атрибут имеет права владельца
description: Обратная ссылка на привилегии, удерживаемые данным участником.
ms.assetid: 94355fbc-f7d8-460b-a516-1576629ca63e
ms.tgt_platform: multiple
keywords:
- — Это схема AD атрибута-права владельца
- Схема AD атрибута Испривилежехолдер
topic_type:
- apiref
api_name:
- Is-Privilege-Holder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895a0202f6ca51ffe7982f33c1fc9f02d021d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655250"
---
# <a name="is-privilege-holder-attribute"></a><span data-ttu-id="76cc5-105">Атрибут имеет права владельца</span><span class="sxs-lookup"><span data-stu-id="76cc5-105">Is-Privilege-Holder attribute</span></span>

<span data-ttu-id="76cc5-106">Обратная ссылка на привилегии, удерживаемые данным участником.</span><span class="sxs-lookup"><span data-stu-id="76cc5-106">Backward link to privileges held by a given principal.</span></span>



| <span data-ttu-id="76cc5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-107">Entry</span></span> | <span data-ttu-id="76cc5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="76cc5-109">CN</span><span class="sxs-lookup"><span data-stu-id="76cc5-109">CN</span></span>                | <span data-ttu-id="76cc5-110">Имеет права владельца</span><span class="sxs-lookup"><span data-stu-id="76cc5-110">Is-Privilege-Holder</span></span>                     |
| <span data-ttu-id="76cc5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="76cc5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="76cc5-112">испривилежехолдер</span><span class="sxs-lookup"><span data-stu-id="76cc5-112">isPrivilegeHolder</span></span>                       |
| <span data-ttu-id="76cc5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="76cc5-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="76cc5-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="76cc5-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="76cc5-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="76cc5-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="76cc5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-116">Attribute-Id</span></span>      | <span data-ttu-id="76cc5-117">1.2.840.113556.1.4.638</span><span class="sxs-lookup"><span data-stu-id="76cc5-117">1.2.840.113556.1.4.638</span></span>                  |
| <span data-ttu-id="76cc5-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="76cc5-118">System-Id-Guid</span></span>    | <span data-ttu-id="76cc5-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="76cc5-119">19405b9c-3cfa-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="76cc5-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76cc5-120">Syntax</span></span>            | [<span data-ttu-id="76cc5-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="76cc5-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="76cc5-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="76cc5-122">Implementations</span></span>

-   [<span data-ttu-id="76cc5-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="76cc5-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="76cc5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="76cc5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="76cc5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="76cc5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="76cc5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="76cc5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="76cc5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="76cc5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="76cc5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="76cc5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="76cc5-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76cc5-129">Windows 2000 Server</span></span>



| <span data-ttu-id="76cc5-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-130">Entry</span></span> | <span data-ttu-id="76cc5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-131">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76cc5-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76cc5-132">Link-Id</span></span>                | <span data-ttu-id="76cc5-133">71</span><span class="sxs-lookup"><span data-stu-id="76cc5-133">71</span></span>                              |
| <span data-ttu-id="76cc5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76cc5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="76cc5-135">System-Only</span></span>            | <span data-ttu-id="76cc5-136">True</span><span class="sxs-lookup"><span data-stu-id="76cc5-136">True</span></span>                            |
| <span data-ttu-id="76cc5-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76cc5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="76cc5-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-138">False</span></span>                           |
| <span data-ttu-id="76cc5-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76cc5-139">Is Indexed</span></span>             | <span data-ttu-id="76cc5-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-140">False</span></span>                           |
| <span data-ttu-id="76cc5-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76cc5-141">In Global Catalog</span></span>      | <span data-ttu-id="76cc5-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-142">False</span></span>                           |
| <span data-ttu-id="76cc5-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76cc5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="76cc5-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76cc5-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76cc5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76cc5-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76cc5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76cc5-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76cc5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-147">Search-Flags</span></span>           | <span data-ttu-id="76cc5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76cc5-148">0x00000000</span></span>                      |
| <span data-ttu-id="76cc5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-149">System-Flags</span></span>           | <span data-ttu-id="76cc5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76cc5-150">0x00000010</span></span>                      |
| <span data-ttu-id="76cc5-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76cc5-151">Classes used in</span></span>        | [<span data-ttu-id="76cc5-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76cc5-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="76cc5-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76cc5-153">Windows Server 2003</span></span>



| <span data-ttu-id="76cc5-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-154">Entry</span></span> | <span data-ttu-id="76cc5-155">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76cc5-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76cc5-156">Link-Id</span></span>                | <span data-ttu-id="76cc5-157">71</span><span class="sxs-lookup"><span data-stu-id="76cc5-157">71</span></span>                              |
| <span data-ttu-id="76cc5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-158">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76cc5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="76cc5-159">System-Only</span></span>            | <span data-ttu-id="76cc5-160">True</span><span class="sxs-lookup"><span data-stu-id="76cc5-160">True</span></span>                            |
| <span data-ttu-id="76cc5-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76cc5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="76cc5-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-162">False</span></span>                           |
| <span data-ttu-id="76cc5-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76cc5-163">Is Indexed</span></span>             | <span data-ttu-id="76cc5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-164">False</span></span>                           |
| <span data-ttu-id="76cc5-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76cc5-165">In Global Catalog</span></span>      | <span data-ttu-id="76cc5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-166">False</span></span>                           |
| <span data-ttu-id="76cc5-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76cc5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="76cc5-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76cc5-168">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76cc5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76cc5-169">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76cc5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76cc5-170">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76cc5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-171">Search-Flags</span></span>           | <span data-ttu-id="76cc5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76cc5-172">0x00000000</span></span>                      |
| <span data-ttu-id="76cc5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-173">System-Flags</span></span>           | <span data-ttu-id="76cc5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76cc5-174">0x00000010</span></span>                      |
| <span data-ttu-id="76cc5-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76cc5-175">Classes used in</span></span>        | [<span data-ttu-id="76cc5-176">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76cc5-176">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="76cc5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="76cc5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="76cc5-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-178">Entry</span></span> | <span data-ttu-id="76cc5-179">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-179">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76cc5-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76cc5-180">Link-Id</span></span>                | <span data-ttu-id="76cc5-181">71</span><span class="sxs-lookup"><span data-stu-id="76cc5-181">71</span></span>                              |
| <span data-ttu-id="76cc5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-182">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76cc5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="76cc5-183">System-Only</span></span>            | <span data-ttu-id="76cc5-184">True</span><span class="sxs-lookup"><span data-stu-id="76cc5-184">True</span></span>                            |
| <span data-ttu-id="76cc5-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76cc5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="76cc5-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-186">False</span></span>                           |
| <span data-ttu-id="76cc5-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76cc5-187">Is Indexed</span></span>             | <span data-ttu-id="76cc5-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-188">False</span></span>                           |
| <span data-ttu-id="76cc5-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76cc5-189">In Global Catalog</span></span>      | <span data-ttu-id="76cc5-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-190">False</span></span>                           |
| <span data-ttu-id="76cc5-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76cc5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="76cc5-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76cc5-192">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76cc5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76cc5-193">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76cc5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76cc5-194">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76cc5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-195">Search-Flags</span></span>           | <span data-ttu-id="76cc5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76cc5-196">0x00000000</span></span>                      |
| <span data-ttu-id="76cc5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-197">System-Flags</span></span>           | <span data-ttu-id="76cc5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76cc5-198">0x00000010</span></span>                      |
| <span data-ttu-id="76cc5-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76cc5-199">Classes used in</span></span>        | [<span data-ttu-id="76cc5-200">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76cc5-200">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="76cc5-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76cc5-201">Windows Server 2008</span></span>



| <span data-ttu-id="76cc5-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-202">Entry</span></span> | <span data-ttu-id="76cc5-203">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-203">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76cc5-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76cc5-204">Link-Id</span></span>                | <span data-ttu-id="76cc5-205">71</span><span class="sxs-lookup"><span data-stu-id="76cc5-205">71</span></span>                              |
| <span data-ttu-id="76cc5-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76cc5-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="76cc5-207">System-Only</span></span>            | <span data-ttu-id="76cc5-208">True</span><span class="sxs-lookup"><span data-stu-id="76cc5-208">True</span></span>                            |
| <span data-ttu-id="76cc5-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76cc5-209">Is-Single-Valued</span></span>       | <span data-ttu-id="76cc5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-210">False</span></span>                           |
| <span data-ttu-id="76cc5-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76cc5-211">Is Indexed</span></span>             | <span data-ttu-id="76cc5-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-212">False</span></span>                           |
| <span data-ttu-id="76cc5-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76cc5-213">In Global Catalog</span></span>      | <span data-ttu-id="76cc5-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-214">False</span></span>                           |
| <span data-ttu-id="76cc5-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76cc5-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="76cc5-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76cc5-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76cc5-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76cc5-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76cc5-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76cc5-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76cc5-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-219">Search-Flags</span></span>           | <span data-ttu-id="76cc5-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76cc5-220">0x00000000</span></span>                      |
| <span data-ttu-id="76cc5-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-221">System-Flags</span></span>           | <span data-ttu-id="76cc5-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76cc5-222">0x00000010</span></span>                      |
| <span data-ttu-id="76cc5-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76cc5-223">Classes used in</span></span>        | [<span data-ttu-id="76cc5-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76cc5-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="76cc5-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76cc5-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="76cc5-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-226">Entry</span></span> | <span data-ttu-id="76cc5-227">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76cc5-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76cc5-228">Link-Id</span></span>                | <span data-ttu-id="76cc5-229">71</span><span class="sxs-lookup"><span data-stu-id="76cc5-229">71</span></span>                              |
| <span data-ttu-id="76cc5-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-230">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76cc5-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="76cc5-231">System-Only</span></span>            | <span data-ttu-id="76cc5-232">True</span><span class="sxs-lookup"><span data-stu-id="76cc5-232">True</span></span>                            |
| <span data-ttu-id="76cc5-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76cc5-233">Is-Single-Valued</span></span>       | <span data-ttu-id="76cc5-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-234">False</span></span>                           |
| <span data-ttu-id="76cc5-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76cc5-235">Is Indexed</span></span>             | <span data-ttu-id="76cc5-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-236">False</span></span>                           |
| <span data-ttu-id="76cc5-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76cc5-237">In Global Catalog</span></span>      | <span data-ttu-id="76cc5-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-238">False</span></span>                           |
| <span data-ttu-id="76cc5-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76cc5-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="76cc5-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76cc5-240">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76cc5-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76cc5-241">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76cc5-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76cc5-242">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76cc5-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-243">Search-Flags</span></span>           | <span data-ttu-id="76cc5-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76cc5-244">0x00000000</span></span>                      |
| <span data-ttu-id="76cc5-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-245">System-Flags</span></span>           | <span data-ttu-id="76cc5-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76cc5-246">0x00000010</span></span>                      |
| <span data-ttu-id="76cc5-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76cc5-247">Classes used in</span></span>        | [<span data-ttu-id="76cc5-248">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76cc5-248">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="76cc5-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="76cc5-249">Windows Server 2012</span></span>



| <span data-ttu-id="76cc5-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="76cc5-250">Entry</span></span> | <span data-ttu-id="76cc5-251">Значение</span><span class="sxs-lookup"><span data-stu-id="76cc5-251">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="76cc5-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="76cc5-252">Link-Id</span></span>                | <span data-ttu-id="76cc5-253">71</span><span class="sxs-lookup"><span data-stu-id="76cc5-253">71</span></span>                              |
| <span data-ttu-id="76cc5-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="76cc5-254">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="76cc5-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="76cc5-255">System-Only</span></span>            | <span data-ttu-id="76cc5-256">True</span><span class="sxs-lookup"><span data-stu-id="76cc5-256">True</span></span>                            |
| <span data-ttu-id="76cc5-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="76cc5-257">Is-Single-Valued</span></span>       | <span data-ttu-id="76cc5-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-258">False</span></span>                           |
| <span data-ttu-id="76cc5-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="76cc5-259">Is Indexed</span></span>             | <span data-ttu-id="76cc5-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-260">False</span></span>                           |
| <span data-ttu-id="76cc5-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="76cc5-261">In Global Catalog</span></span>      | <span data-ttu-id="76cc5-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="76cc5-262">False</span></span>                           |
| <span data-ttu-id="76cc5-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="76cc5-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="76cc5-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="76cc5-264">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="76cc5-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="76cc5-265">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="76cc5-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="76cc5-266">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="76cc5-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-267">Search-Flags</span></span>           | <span data-ttu-id="76cc5-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="76cc5-268">0x00000000</span></span>                      |
| <span data-ttu-id="76cc5-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="76cc5-269">System-Flags</span></span>           | <span data-ttu-id="76cc5-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="76cc5-270">0x00000010</span></span>                      |
| <span data-ttu-id="76cc5-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="76cc5-271">Classes used in</span></span>        | [<span data-ttu-id="76cc5-272">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="76cc5-272">**Top**</span></span>](c-top.md)<br/> |



 

 





