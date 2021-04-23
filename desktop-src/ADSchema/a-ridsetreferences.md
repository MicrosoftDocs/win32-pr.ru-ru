---
title: Атрибут RID-Set-References
description: Список ссылок на RID-Set объекты, которые управляют выделением относительных идентификаторов (RID).
ms.assetid: 9bd02a20-97a3-455f-ab77-f84add844974
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута RID-Set-References
- Схема AD атрибута Ридсетреференцес
topic_type:
- apiref
api_name:
- RID-Set-References
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4115d013a19e7dc8f100f35b57ee3658855e3b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655299"
---
# <a name="rid-set-references-attribute"></a><span data-ttu-id="8cff0-105">Атрибут RID-Set-References</span><span class="sxs-lookup"><span data-stu-id="8cff0-105">RID-Set-References attribute</span></span>

<span data-ttu-id="8cff0-106">Список ссылок на RID-Set объекты, которые управляют выделением относительных идентификаторов (RID).</span><span class="sxs-lookup"><span data-stu-id="8cff0-106">List of references to RID-Set objects that manage Relative Identifier (RID) allocation.</span></span>



| <span data-ttu-id="8cff0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-107">Entry</span></span> | <span data-ttu-id="8cff0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8cff0-109">CN</span><span class="sxs-lookup"><span data-stu-id="8cff0-109">CN</span></span>                | <span data-ttu-id="8cff0-110">RID-Set-References</span><span class="sxs-lookup"><span data-stu-id="8cff0-110">RID-Set-References</span></span>                      |
| <span data-ttu-id="8cff0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8cff0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8cff0-112">ридсетреференцес</span><span class="sxs-lookup"><span data-stu-id="8cff0-112">rIDSetReferences</span></span>                        |
| <span data-ttu-id="8cff0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8cff0-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="8cff0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8cff0-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="8cff0-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8cff0-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="8cff0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-116">Attribute-Id</span></span>      | <span data-ttu-id="8cff0-117">1.2.840.113556.1.4.669</span><span class="sxs-lookup"><span data-stu-id="8cff0-117">1.2.840.113556.1.4.669</span></span>                  |
| <span data-ttu-id="8cff0-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8cff0-118">System-Id-Guid</span></span>    | <span data-ttu-id="8cff0-119">7bfdcb7b-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8cff0-119">7bfdcb7b-4807-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="8cff0-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cff0-120">Syntax</span></span>            | [<span data-ttu-id="8cff0-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8cff0-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="8cff0-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8cff0-122">Implementations</span></span>

-   [<span data-ttu-id="8cff0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8cff0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8cff0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cff0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cff0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cff0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cff0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cff0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cff0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cff0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cff0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cff0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8cff0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cff0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8cff0-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-130">Entry</span></span> | <span data-ttu-id="8cff0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-131">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8cff0-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cff0-132">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-133">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cff0-134">System-Only</span></span>            | <span data-ttu-id="8cff0-135">True</span><span class="sxs-lookup"><span data-stu-id="8cff0-135">True</span></span>                                      |
| <span data-ttu-id="8cff0-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cff0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8cff0-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-137">False</span></span>                                     |
| <span data-ttu-id="8cff0-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cff0-138">Is Indexed</span></span>             | <span data-ttu-id="8cff0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-139">False</span></span>                                     |
| <span data-ttu-id="8cff0-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cff0-140">In Global Catalog</span></span>      | <span data-ttu-id="8cff0-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-141">False</span></span>                                     |
| <span data-ttu-id="8cff0-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cff0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cff0-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cff0-143">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="8cff0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cff0-144">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cff0-145">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-146">Search-Flags</span></span>           | <span data-ttu-id="8cff0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cff0-147">0x00000000</span></span>                                |
| <span data-ttu-id="8cff0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-148">System-Flags</span></span>           | <span data-ttu-id="8cff0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cff0-149">0x00000010</span></span>                                |
| <span data-ttu-id="8cff0-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cff0-150">Classes used in</span></span>        | [<span data-ttu-id="8cff0-151">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="8cff0-151">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8cff0-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cff0-152">Windows Server 2003</span></span>



| <span data-ttu-id="8cff0-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-153">Entry</span></span> | <span data-ttu-id="8cff0-154">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-154">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8cff0-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cff0-155">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-156">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cff0-157">System-Only</span></span>            | <span data-ttu-id="8cff0-158">True</span><span class="sxs-lookup"><span data-stu-id="8cff0-158">True</span></span>                                      |
| <span data-ttu-id="8cff0-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cff0-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8cff0-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-160">False</span></span>                                     |
| <span data-ttu-id="8cff0-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cff0-161">Is Indexed</span></span>             | <span data-ttu-id="8cff0-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-162">False</span></span>                                     |
| <span data-ttu-id="8cff0-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cff0-163">In Global Catalog</span></span>      | <span data-ttu-id="8cff0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-164">False</span></span>                                     |
| <span data-ttu-id="8cff0-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cff0-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cff0-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cff0-166">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="8cff0-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cff0-167">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cff0-168">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-169">Search-Flags</span></span>           | <span data-ttu-id="8cff0-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cff0-170">0x00000000</span></span>                                |
| <span data-ttu-id="8cff0-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-171">System-Flags</span></span>           | <span data-ttu-id="8cff0-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cff0-172">0x00000010</span></span>                                |
| <span data-ttu-id="8cff0-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cff0-173">Classes used in</span></span>        | [<span data-ttu-id="8cff0-174">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="8cff0-174">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cff0-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cff0-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cff0-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-176">Entry</span></span> | <span data-ttu-id="8cff0-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-177">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8cff0-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cff0-178">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-179">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cff0-180">System-Only</span></span>            | <span data-ttu-id="8cff0-181">True</span><span class="sxs-lookup"><span data-stu-id="8cff0-181">True</span></span>                                      |
| <span data-ttu-id="8cff0-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cff0-182">Is-Single-Valued</span></span>       | <span data-ttu-id="8cff0-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-183">False</span></span>                                     |
| <span data-ttu-id="8cff0-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cff0-184">Is Indexed</span></span>             | <span data-ttu-id="8cff0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-185">False</span></span>                                     |
| <span data-ttu-id="8cff0-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cff0-186">In Global Catalog</span></span>      | <span data-ttu-id="8cff0-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-187">False</span></span>                                     |
| <span data-ttu-id="8cff0-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cff0-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cff0-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cff0-189">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="8cff0-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cff0-190">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cff0-191">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-192">Search-Flags</span></span>           | <span data-ttu-id="8cff0-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cff0-193">0x00000000</span></span>                                |
| <span data-ttu-id="8cff0-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-194">System-Flags</span></span>           | <span data-ttu-id="8cff0-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cff0-195">0x00000010</span></span>                                |
| <span data-ttu-id="8cff0-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cff0-196">Classes used in</span></span>        | [<span data-ttu-id="8cff0-197">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="8cff0-197">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cff0-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cff0-198">Windows Server 2008</span></span>



| <span data-ttu-id="8cff0-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-199">Entry</span></span> | <span data-ttu-id="8cff0-200">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-200">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8cff0-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cff0-201">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-202">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cff0-203">System-Only</span></span>            | <span data-ttu-id="8cff0-204">True</span><span class="sxs-lookup"><span data-stu-id="8cff0-204">True</span></span>                                      |
| <span data-ttu-id="8cff0-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cff0-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8cff0-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-206">False</span></span>                                     |
| <span data-ttu-id="8cff0-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cff0-207">Is Indexed</span></span>             | <span data-ttu-id="8cff0-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-208">False</span></span>                                     |
| <span data-ttu-id="8cff0-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cff0-209">In Global Catalog</span></span>      | <span data-ttu-id="8cff0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-210">False</span></span>                                     |
| <span data-ttu-id="8cff0-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cff0-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cff0-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cff0-212">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="8cff0-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cff0-213">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cff0-214">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-215">Search-Flags</span></span>           | <span data-ttu-id="8cff0-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cff0-216">0x00000000</span></span>                                |
| <span data-ttu-id="8cff0-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-217">System-Flags</span></span>           | <span data-ttu-id="8cff0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cff0-218">0x00000010</span></span>                                |
| <span data-ttu-id="8cff0-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cff0-219">Classes used in</span></span>        | [<span data-ttu-id="8cff0-220">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="8cff0-220">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cff0-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cff0-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cff0-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-222">Entry</span></span> | <span data-ttu-id="8cff0-223">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-223">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8cff0-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cff0-224">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-225">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cff0-226">System-Only</span></span>            | <span data-ttu-id="8cff0-227">True</span><span class="sxs-lookup"><span data-stu-id="8cff0-227">True</span></span>                                      |
| <span data-ttu-id="8cff0-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cff0-228">Is-Single-Valued</span></span>       | <span data-ttu-id="8cff0-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-229">False</span></span>                                     |
| <span data-ttu-id="8cff0-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cff0-230">Is Indexed</span></span>             | <span data-ttu-id="8cff0-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-231">False</span></span>                                     |
| <span data-ttu-id="8cff0-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cff0-232">In Global Catalog</span></span>      | <span data-ttu-id="8cff0-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-233">False</span></span>                                     |
| <span data-ttu-id="8cff0-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cff0-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cff0-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cff0-235">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="8cff0-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cff0-236">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cff0-237">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-238">Search-Flags</span></span>           | <span data-ttu-id="8cff0-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cff0-239">0x00000000</span></span>                                |
| <span data-ttu-id="8cff0-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-240">System-Flags</span></span>           | <span data-ttu-id="8cff0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cff0-241">0x00000010</span></span>                                |
| <span data-ttu-id="8cff0-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cff0-242">Classes used in</span></span>        | [<span data-ttu-id="8cff0-243">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="8cff0-243">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cff0-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cff0-244">Windows Server 2012</span></span>



| <span data-ttu-id="8cff0-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cff0-245">Entry</span></span> | <span data-ttu-id="8cff0-246">Значение</span><span class="sxs-lookup"><span data-stu-id="8cff0-246">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="8cff0-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cff0-247">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cff0-248">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="8cff0-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cff0-249">System-Only</span></span>            | <span data-ttu-id="8cff0-250">True</span><span class="sxs-lookup"><span data-stu-id="8cff0-250">True</span></span>                                      |
| <span data-ttu-id="8cff0-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cff0-251">Is-Single-Valued</span></span>       | <span data-ttu-id="8cff0-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-252">False</span></span>                                     |
| <span data-ttu-id="8cff0-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cff0-253">Is Indexed</span></span>             | <span data-ttu-id="8cff0-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-254">False</span></span>                                     |
| <span data-ttu-id="8cff0-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cff0-255">In Global Catalog</span></span>      | <span data-ttu-id="8cff0-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cff0-256">False</span></span>                                     |
| <span data-ttu-id="8cff0-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cff0-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cff0-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cff0-258">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="8cff0-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cff0-259">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cff0-260">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="8cff0-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-261">Search-Flags</span></span>           | <span data-ttu-id="8cff0-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cff0-262">0x00000000</span></span>                                |
| <span data-ttu-id="8cff0-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cff0-263">System-Flags</span></span>           | <span data-ttu-id="8cff0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8cff0-264">0x00000010</span></span>                                |
| <span data-ttu-id="8cff0-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cff0-265">Classes used in</span></span>        | [<span data-ttu-id="8cff0-266">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="8cff0-266">**Computer**</span></span>](c-computer.md)<br/> |



 

 





