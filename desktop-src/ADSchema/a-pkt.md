---
title: Атрибут PKT
description: Таблица знаний раздела DFS. Описывает структуру распределенная файловая система иерархии.
ms.assetid: a7b2e9ee-04c0-40e8-8670-8261575a45ab
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута PKT
- Схема AD атрибута pKT
topic_type:
- apiref
api_name:
- PKT
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1647e2730b254121763b6598a8ec365b376dd52d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138118"
---
# <a name="pkt-attribute"></a><span data-ttu-id="ec2d5-106">Атрибут PKT</span><span class="sxs-lookup"><span data-stu-id="ec2d5-106">PKT attribute</span></span>

<span data-ttu-id="ec2d5-107">Таблица знаний раздела DFS.</span><span class="sxs-lookup"><span data-stu-id="ec2d5-107">DFS Partition Knowledge Table.</span></span> <span data-ttu-id="ec2d5-108">Описывает структуру распределенная файловая система иерархии.</span><span class="sxs-lookup"><span data-stu-id="ec2d5-108">Describes the structure of a Distributed File System hierarchy.</span></span>



| <span data-ttu-id="ec2d5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-109">Entry</span></span> | <span data-ttu-id="ec2d5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ec2d5-111">CN</span><span class="sxs-lookup"><span data-stu-id="ec2d5-111">CN</span></span>                | <span data-ttu-id="ec2d5-112">PKT</span><span class="sxs-lookup"><span data-stu-id="ec2d5-112">PKT</span></span>                                                   |
| <span data-ttu-id="ec2d5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ec2d5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ec2d5-114">pKT</span><span class="sxs-lookup"><span data-stu-id="ec2d5-114">pKT</span></span>                                                   |
| <span data-ttu-id="ec2d5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="ec2d5-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ec2d5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ec2d5-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ec2d5-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ec2d5-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ec2d5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-118">Attribute-Id</span></span>      | <span data-ttu-id="ec2d5-119">1.2.840.113556.1.4.206</span><span class="sxs-lookup"><span data-stu-id="ec2d5-119">1.2.840.113556.1.4.206</span></span>                                |
| <span data-ttu-id="ec2d5-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ec2d5-120">System-Id-Guid</span></span>    | <span data-ttu-id="ec2d5-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="ec2d5-121">8447f9f1-1027-11d0-a05f-00aa006c33ed</span></span>                  |
| <span data-ttu-id="ec2d5-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec2d5-122">Syntax</span></span>            | [<span data-ttu-id="ec2d5-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ec2d5-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ec2d5-124">Implementations</span></span>

-   [<span data-ttu-id="ec2d5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ec2d5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ec2d5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ec2d5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ec2d5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ec2d5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ec2d5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec2d5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ec2d5-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-132">Entry</span></span> | <span data-ttu-id="ec2d5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-133">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="ec2d5-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec2d5-134">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-135">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2d5-136">System-Only</span></span>            | <span data-ttu-id="ec2d5-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-137">False</span></span>                                |
| <span data-ttu-id="ec2d5-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec2d5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2d5-139">True</span><span class="sxs-lookup"><span data-stu-id="ec2d5-139">True</span></span>                                 |
| <span data-ttu-id="ec2d5-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec2d5-140">Is Indexed</span></span>             | <span data-ttu-id="ec2d5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-141">False</span></span>                                |
| <span data-ttu-id="ec2d5-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec2d5-142">In Global Catalog</span></span>      | <span data-ttu-id="ec2d5-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-143">False</span></span>                                |
| <span data-ttu-id="ec2d5-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec2d5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2d5-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec2d5-145">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="ec2d5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2d5-146">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2d5-147">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-148">Search-Flags</span></span>           | <span data-ttu-id="ec2d5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2d5-149">0x00000000</span></span>                           |
| <span data-ttu-id="ec2d5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-150">System-Flags</span></span>           | <span data-ttu-id="ec2d5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec2d5-151">0x00000010</span></span>                           |
| <span data-ttu-id="ec2d5-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec2d5-152">Classes used in</span></span>        | [<span data-ttu-id="ec2d5-153">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-153">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ec2d5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ec2d5-154">Windows Server 2003</span></span>



| <span data-ttu-id="ec2d5-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-155">Entry</span></span> | <span data-ttu-id="ec2d5-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-156">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="ec2d5-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec2d5-157">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-158">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2d5-159">System-Only</span></span>            | <span data-ttu-id="ec2d5-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-160">False</span></span>                                |
| <span data-ttu-id="ec2d5-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec2d5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2d5-162">True</span><span class="sxs-lookup"><span data-stu-id="ec2d5-162">True</span></span>                                 |
| <span data-ttu-id="ec2d5-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec2d5-163">Is Indexed</span></span>             | <span data-ttu-id="ec2d5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-164">False</span></span>                                |
| <span data-ttu-id="ec2d5-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec2d5-165">In Global Catalog</span></span>      | <span data-ttu-id="ec2d5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-166">False</span></span>                                |
| <span data-ttu-id="ec2d5-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec2d5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2d5-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec2d5-168">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="ec2d5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2d5-169">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2d5-170">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-171">Search-Flags</span></span>           | <span data-ttu-id="ec2d5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2d5-172">0x00000000</span></span>                           |
| <span data-ttu-id="ec2d5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-173">System-Flags</span></span>           | <span data-ttu-id="ec2d5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec2d5-174">0x00000010</span></span>                           |
| <span data-ttu-id="ec2d5-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec2d5-175">Classes used in</span></span>        | [<span data-ttu-id="ec2d5-176">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-176">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ec2d5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ec2d5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ec2d5-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-178">Entry</span></span> | <span data-ttu-id="ec2d5-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-179">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="ec2d5-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec2d5-180">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-181">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2d5-182">System-Only</span></span>            | <span data-ttu-id="ec2d5-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-183">False</span></span>                                |
| <span data-ttu-id="ec2d5-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec2d5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2d5-185">True</span><span class="sxs-lookup"><span data-stu-id="ec2d5-185">True</span></span>                                 |
| <span data-ttu-id="ec2d5-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec2d5-186">Is Indexed</span></span>             | <span data-ttu-id="ec2d5-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-187">False</span></span>                                |
| <span data-ttu-id="ec2d5-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec2d5-188">In Global Catalog</span></span>      | <span data-ttu-id="ec2d5-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-189">False</span></span>                                |
| <span data-ttu-id="ec2d5-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec2d5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2d5-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec2d5-191">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="ec2d5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2d5-192">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2d5-193">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-194">Search-Flags</span></span>           | <span data-ttu-id="ec2d5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2d5-195">0x00000000</span></span>                           |
| <span data-ttu-id="ec2d5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-196">System-Flags</span></span>           | <span data-ttu-id="ec2d5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec2d5-197">0x00000010</span></span>                           |
| <span data-ttu-id="ec2d5-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec2d5-198">Classes used in</span></span>        | [<span data-ttu-id="ec2d5-199">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-199">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ec2d5-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec2d5-200">Windows Server 2008</span></span>



| <span data-ttu-id="ec2d5-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-201">Entry</span></span> | <span data-ttu-id="ec2d5-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-202">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="ec2d5-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec2d5-203">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-204">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2d5-205">System-Only</span></span>            | <span data-ttu-id="ec2d5-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-206">False</span></span>                                |
| <span data-ttu-id="ec2d5-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec2d5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2d5-208">True</span><span class="sxs-lookup"><span data-stu-id="ec2d5-208">True</span></span>                                 |
| <span data-ttu-id="ec2d5-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec2d5-209">Is Indexed</span></span>             | <span data-ttu-id="ec2d5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-210">False</span></span>                                |
| <span data-ttu-id="ec2d5-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec2d5-211">In Global Catalog</span></span>      | <span data-ttu-id="ec2d5-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-212">False</span></span>                                |
| <span data-ttu-id="ec2d5-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec2d5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2d5-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec2d5-214">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="ec2d5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2d5-215">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2d5-216">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-217">Search-Flags</span></span>           | <span data-ttu-id="ec2d5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2d5-218">0x00000000</span></span>                           |
| <span data-ttu-id="ec2d5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-219">System-Flags</span></span>           | <span data-ttu-id="ec2d5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec2d5-220">0x00000010</span></span>                           |
| <span data-ttu-id="ec2d5-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec2d5-221">Classes used in</span></span>        | [<span data-ttu-id="ec2d5-222">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-222">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ec2d5-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec2d5-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ec2d5-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-224">Entry</span></span> | <span data-ttu-id="ec2d5-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-225">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="ec2d5-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec2d5-226">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-227">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2d5-228">System-Only</span></span>            | <span data-ttu-id="ec2d5-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-229">False</span></span>                                |
| <span data-ttu-id="ec2d5-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec2d5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2d5-231">True</span><span class="sxs-lookup"><span data-stu-id="ec2d5-231">True</span></span>                                 |
| <span data-ttu-id="ec2d5-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec2d5-232">Is Indexed</span></span>             | <span data-ttu-id="ec2d5-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-233">False</span></span>                                |
| <span data-ttu-id="ec2d5-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec2d5-234">In Global Catalog</span></span>      | <span data-ttu-id="ec2d5-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-235">False</span></span>                                |
| <span data-ttu-id="ec2d5-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec2d5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2d5-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec2d5-237">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="ec2d5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2d5-238">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2d5-239">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-240">Search-Flags</span></span>           | <span data-ttu-id="ec2d5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2d5-241">0x00000000</span></span>                           |
| <span data-ttu-id="ec2d5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-242">System-Flags</span></span>           | <span data-ttu-id="ec2d5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec2d5-243">0x00000010</span></span>                           |
| <span data-ttu-id="ec2d5-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec2d5-244">Classes used in</span></span>        | [<span data-ttu-id="ec2d5-245">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-245">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ec2d5-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec2d5-246">Windows Server 2012</span></span>



| <span data-ttu-id="ec2d5-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="ec2d5-247">Entry</span></span> | <span data-ttu-id="ec2d5-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ec2d5-248">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="ec2d5-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ec2d5-249">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ec2d5-250">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="ec2d5-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ec2d5-251">System-Only</span></span>            | <span data-ttu-id="ec2d5-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-252">False</span></span>                                |
| <span data-ttu-id="ec2d5-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ec2d5-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ec2d5-254">True</span><span class="sxs-lookup"><span data-stu-id="ec2d5-254">True</span></span>                                 |
| <span data-ttu-id="ec2d5-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ec2d5-255">Is Indexed</span></span>             | <span data-ttu-id="ec2d5-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-256">False</span></span>                                |
| <span data-ttu-id="ec2d5-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ec2d5-257">In Global Catalog</span></span>      | <span data-ttu-id="ec2d5-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="ec2d5-258">False</span></span>                                |
| <span data-ttu-id="ec2d5-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ec2d5-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ec2d5-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ec2d5-260">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="ec2d5-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ec2d5-261">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ec2d5-262">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="ec2d5-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-263">Search-Flags</span></span>           | <span data-ttu-id="ec2d5-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ec2d5-264">0x00000000</span></span>                           |
| <span data-ttu-id="ec2d5-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ec2d5-265">System-Flags</span></span>           | <span data-ttu-id="ec2d5-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ec2d5-266">0x00000010</span></span>                           |
| <span data-ttu-id="ec2d5-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ec2d5-267">Classes used in</span></span>        | [<span data-ttu-id="ec2d5-268">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="ec2d5-268">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





