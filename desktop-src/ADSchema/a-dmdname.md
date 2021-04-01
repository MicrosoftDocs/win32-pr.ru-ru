---
title: Атрибут DMD-Name
description: Имя, используемое для задания секции схемы. Не используется AD.
ms.assetid: 0ee35c32-add7-4b20-8d83-59b4b91df6ad
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DMD-Name
- Схема AD атрибута Дмднаме
topic_type:
- apiref
api_name:
- DMD-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25684af133748ca73c8ace31b0471a5d1e0a787
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989535"
---
# <a name="dmd-name-attribute"></a><span data-ttu-id="6c080-106">Атрибут DMD-Name</span><span class="sxs-lookup"><span data-stu-id="6c080-106">DMD-Name attribute</span></span>

<span data-ttu-id="6c080-107">Имя, используемое для задания секции схемы.</span><span class="sxs-lookup"><span data-stu-id="6c080-107">A name used to identify the schema partition.</span></span> <span data-ttu-id="6c080-108">Не используется AD.</span><span class="sxs-lookup"><span data-stu-id="6c080-108">Not used by AD.</span></span>



| <span data-ttu-id="6c080-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-109">Entry</span></span> | <span data-ttu-id="6c080-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6c080-111">CN</span><span class="sxs-lookup"><span data-stu-id="6c080-111">CN</span></span>                | <span data-ttu-id="6c080-112">DMD-Name</span><span class="sxs-lookup"><span data-stu-id="6c080-112">DMD-Name</span></span>                                    |
| <span data-ttu-id="6c080-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6c080-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6c080-114">дмднаме</span><span class="sxs-lookup"><span data-stu-id="6c080-114">dmdName</span></span>                                     |
| <span data-ttu-id="6c080-115">Размер</span><span class="sxs-lookup"><span data-stu-id="6c080-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="6c080-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6c080-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="6c080-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6c080-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="6c080-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-118">Attribute-Id</span></span>      | <span data-ttu-id="6c080-119">1.2.840.113556.1.2.598</span><span class="sxs-lookup"><span data-stu-id="6c080-119">1.2.840.113556.1.2.598</span></span>                      |
| <span data-ttu-id="6c080-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6c080-120">System-Id-Guid</span></span>    | <span data-ttu-id="6c080-121">167757b9-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6c080-121">167757b9-47f3-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="6c080-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c080-122">Syntax</span></span>            | [<span data-ttu-id="6c080-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6c080-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6c080-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6c080-124">Implementations</span></span>

-   [<span data-ttu-id="6c080-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c080-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c080-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c080-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c080-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6c080-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6c080-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c080-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c080-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c080-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c080-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c080-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c080-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c080-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c080-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c080-132">Windows 2000 Server</span></span>



| <span data-ttu-id="6c080-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-133">Entry</span></span> | <span data-ttu-id="6c080-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-136">MAPI-Id</span></span>                | <span data-ttu-id="6c080-137">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-137">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-138">System-Only</span></span>            | <span data-ttu-id="6c080-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-139">False</span></span>                           |
| <span data-ttu-id="6c080-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-140">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-141">True</span><span class="sxs-lookup"><span data-stu-id="6c080-141">True</span></span>                            |
| <span data-ttu-id="6c080-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-142">Is Indexed</span></span>             | <span data-ttu-id="6c080-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-143">False</span></span>                           |
| <span data-ttu-id="6c080-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-144">In Global Catalog</span></span>      | <span data-ttu-id="6c080-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-145">False</span></span>                           |
| <span data-ttu-id="6c080-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-148">Range-Lower</span></span>            | <span data-ttu-id="6c080-149">1</span><span class="sxs-lookup"><span data-stu-id="6c080-149">1</span></span>                               |
| <span data-ttu-id="6c080-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-150">Range-Upper</span></span>            | <span data-ttu-id="6c080-151">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-151">1024</span></span>                            |
| <span data-ttu-id="6c080-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-152">Search-Flags</span></span>           | <span data-ttu-id="6c080-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-153">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-154">System-Flags</span></span>           | <span data-ttu-id="6c080-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-155">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-156">Classes used in</span></span>        | [<span data-ttu-id="6c080-157">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-157">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c080-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c080-158">Windows Server 2003</span></span>



| <span data-ttu-id="6c080-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-159">Entry</span></span> | <span data-ttu-id="6c080-160">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-162">MAPI-Id</span></span>                | <span data-ttu-id="6c080-163">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-163">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-164">System-Only</span></span>            | <span data-ttu-id="6c080-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-165">False</span></span>                           |
| <span data-ttu-id="6c080-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-166">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-167">True</span><span class="sxs-lookup"><span data-stu-id="6c080-167">True</span></span>                            |
| <span data-ttu-id="6c080-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-168">Is Indexed</span></span>             | <span data-ttu-id="6c080-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-169">False</span></span>                           |
| <span data-ttu-id="6c080-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-170">In Global Catalog</span></span>      | <span data-ttu-id="6c080-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-171">False</span></span>                           |
| <span data-ttu-id="6c080-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-174">Range-Lower</span></span>            | <span data-ttu-id="6c080-175">1</span><span class="sxs-lookup"><span data-stu-id="6c080-175">1</span></span>                               |
| <span data-ttu-id="6c080-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-176">Range-Upper</span></span>            | <span data-ttu-id="6c080-177">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-177">1024</span></span>                            |
| <span data-ttu-id="6c080-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-178">Search-Flags</span></span>           | <span data-ttu-id="6c080-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-179">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-180">System-Flags</span></span>           | <span data-ttu-id="6c080-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-181">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-182">Classes used in</span></span>        | [<span data-ttu-id="6c080-183">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-183">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6c080-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="6c080-184">ADAM</span></span>



| <span data-ttu-id="6c080-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-185">Entry</span></span> | <span data-ttu-id="6c080-186">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-186">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-187">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-188">MAPI-Id</span></span>                | <span data-ttu-id="6c080-189">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-189">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-190">System-Only</span></span>            | <span data-ttu-id="6c080-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-191">False</span></span>                           |
| <span data-ttu-id="6c080-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-192">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-193">True</span><span class="sxs-lookup"><span data-stu-id="6c080-193">True</span></span>                            |
| <span data-ttu-id="6c080-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-194">Is Indexed</span></span>             | <span data-ttu-id="6c080-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-195">False</span></span>                           |
| <span data-ttu-id="6c080-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-196">In Global Catalog</span></span>      | <span data-ttu-id="6c080-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-197">False</span></span>                           |
| <span data-ttu-id="6c080-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-199">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-200">Range-Lower</span></span>            | <span data-ttu-id="6c080-201">1</span><span class="sxs-lookup"><span data-stu-id="6c080-201">1</span></span>                               |
| <span data-ttu-id="6c080-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-202">Range-Upper</span></span>            | <span data-ttu-id="6c080-203">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-203">1024</span></span>                            |
| <span data-ttu-id="6c080-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-204">Search-Flags</span></span>           | <span data-ttu-id="6c080-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-205">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-206">System-Flags</span></span>           | <span data-ttu-id="6c080-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-207">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-208">Classes used in</span></span>        | [<span data-ttu-id="6c080-209">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-209">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c080-210">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c080-210">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c080-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-211">Entry</span></span> | <span data-ttu-id="6c080-212">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-212">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-213">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-214">MAPI-Id</span></span>                | <span data-ttu-id="6c080-215">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-215">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-216">System-Only</span></span>            | <span data-ttu-id="6c080-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-217">False</span></span>                           |
| <span data-ttu-id="6c080-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-218">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-219">True</span><span class="sxs-lookup"><span data-stu-id="6c080-219">True</span></span>                            |
| <span data-ttu-id="6c080-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-220">Is Indexed</span></span>             | <span data-ttu-id="6c080-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-221">False</span></span>                           |
| <span data-ttu-id="6c080-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-222">In Global Catalog</span></span>      | <span data-ttu-id="6c080-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-223">False</span></span>                           |
| <span data-ttu-id="6c080-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-225">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-226">Range-Lower</span></span>            | <span data-ttu-id="6c080-227">1</span><span class="sxs-lookup"><span data-stu-id="6c080-227">1</span></span>                               |
| <span data-ttu-id="6c080-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-228">Range-Upper</span></span>            | <span data-ttu-id="6c080-229">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-229">1024</span></span>                            |
| <span data-ttu-id="6c080-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-230">Search-Flags</span></span>           | <span data-ttu-id="6c080-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-231">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-232">System-Flags</span></span>           | <span data-ttu-id="6c080-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-233">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-234">Classes used in</span></span>        | [<span data-ttu-id="6c080-235">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-235">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c080-236">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c080-236">Windows Server 2008</span></span>



| <span data-ttu-id="6c080-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-237">Entry</span></span> | <span data-ttu-id="6c080-238">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-238">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-239">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-240">MAPI-Id</span></span>                | <span data-ttu-id="6c080-241">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-241">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-242">System-Only</span></span>            | <span data-ttu-id="6c080-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-243">False</span></span>                           |
| <span data-ttu-id="6c080-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-244">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-245">True</span><span class="sxs-lookup"><span data-stu-id="6c080-245">True</span></span>                            |
| <span data-ttu-id="6c080-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-246">Is Indexed</span></span>             | <span data-ttu-id="6c080-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-247">False</span></span>                           |
| <span data-ttu-id="6c080-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-248">In Global Catalog</span></span>      | <span data-ttu-id="6c080-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-249">False</span></span>                           |
| <span data-ttu-id="6c080-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-251">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-252">Range-Lower</span></span>            | <span data-ttu-id="6c080-253">1</span><span class="sxs-lookup"><span data-stu-id="6c080-253">1</span></span>                               |
| <span data-ttu-id="6c080-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-254">Range-Upper</span></span>            | <span data-ttu-id="6c080-255">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-255">1024</span></span>                            |
| <span data-ttu-id="6c080-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-256">Search-Flags</span></span>           | <span data-ttu-id="6c080-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-257">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-258">System-Flags</span></span>           | <span data-ttu-id="6c080-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-259">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-260">Classes used in</span></span>        | [<span data-ttu-id="6c080-261">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-261">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c080-262">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c080-262">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c080-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-263">Entry</span></span> | <span data-ttu-id="6c080-264">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-264">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-265">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-266">MAPI-Id</span></span>                | <span data-ttu-id="6c080-267">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-267">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-268">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-268">System-Only</span></span>            | <span data-ttu-id="6c080-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-269">False</span></span>                           |
| <span data-ttu-id="6c080-270">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-270">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-271">True</span><span class="sxs-lookup"><span data-stu-id="6c080-271">True</span></span>                            |
| <span data-ttu-id="6c080-272">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-272">Is Indexed</span></span>             | <span data-ttu-id="6c080-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-273">False</span></span>                           |
| <span data-ttu-id="6c080-274">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-274">In Global Catalog</span></span>      | <span data-ttu-id="6c080-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-275">False</span></span>                           |
| <span data-ttu-id="6c080-276">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-276">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-277">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-277">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-278">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-278">Range-Lower</span></span>            | <span data-ttu-id="6c080-279">1</span><span class="sxs-lookup"><span data-stu-id="6c080-279">1</span></span>                               |
| <span data-ttu-id="6c080-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-280">Range-Upper</span></span>            | <span data-ttu-id="6c080-281">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-281">1024</span></span>                            |
| <span data-ttu-id="6c080-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-282">Search-Flags</span></span>           | <span data-ttu-id="6c080-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-283">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-284">System-Flags</span></span>           | <span data-ttu-id="6c080-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-285">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-286">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-286">Classes used in</span></span>        | [<span data-ttu-id="6c080-287">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-287">**DMD**</span></span>](c-dmd.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c080-288">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c080-288">Windows Server 2012</span></span>



| <span data-ttu-id="6c080-289">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c080-289">Entry</span></span> | <span data-ttu-id="6c080-290">Значение</span><span class="sxs-lookup"><span data-stu-id="6c080-290">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="6c080-291">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c080-291">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="6c080-292">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c080-292">MAPI-Id</span></span>                | <span data-ttu-id="6c080-293">0x8C56</span><span class="sxs-lookup"><span data-stu-id="6c080-293">0x8C56</span></span>                          |
| <span data-ttu-id="6c080-294">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c080-294">System-Only</span></span>            | <span data-ttu-id="6c080-295">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-295">False</span></span>                           |
| <span data-ttu-id="6c080-296">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c080-296">Is-Single-Valued</span></span>       | <span data-ttu-id="6c080-297">True</span><span class="sxs-lookup"><span data-stu-id="6c080-297">True</span></span>                            |
| <span data-ttu-id="6c080-298">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c080-298">Is Indexed</span></span>             | <span data-ttu-id="6c080-299">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-299">False</span></span>                           |
| <span data-ttu-id="6c080-300">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c080-300">In Global Catalog</span></span>      | <span data-ttu-id="6c080-301">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c080-301">False</span></span>                           |
| <span data-ttu-id="6c080-302">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c080-302">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c080-303">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c080-303">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="6c080-304">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c080-304">Range-Lower</span></span>            | <span data-ttu-id="6c080-305">1</span><span class="sxs-lookup"><span data-stu-id="6c080-305">1</span></span>                               |
| <span data-ttu-id="6c080-306">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c080-306">Range-Upper</span></span>            | <span data-ttu-id="6c080-307">1024</span><span class="sxs-lookup"><span data-stu-id="6c080-307">1024</span></span>                            |
| <span data-ttu-id="6c080-308">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-308">Search-Flags</span></span>           | <span data-ttu-id="6c080-309">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c080-309">0x00000000</span></span>                      |
| <span data-ttu-id="6c080-310">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c080-310">System-Flags</span></span>           | <span data-ttu-id="6c080-311">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c080-311">0x00000010</span></span>                      |
| <span data-ttu-id="6c080-312">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c080-312">Classes used in</span></span>        | [<span data-ttu-id="6c080-313">**дмд**</span><span class="sxs-lookup"><span data-stu-id="6c080-313">**DMD**</span></span>](c-dmd.md)<br/> |



 

 





