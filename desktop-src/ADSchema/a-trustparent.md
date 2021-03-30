---
title: Атрибут Trust-Parent
description: Родительский элемент в иерархии доверия KERBEROS.
ms.assetid: 738cf509-42a2-40b6-a525-6df34c02d0f0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Parent
- Схема AD атрибута Трустпарент
topic_type:
- apiref
api_name:
- Trust-Parent
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8be971c7597b14daf7a694e41c9d67714e5f0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804805"
---
# <a name="trust-parent-attribute"></a><span data-ttu-id="996f8-105">Атрибут Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="996f8-105">Trust-Parent attribute</span></span>

<span data-ttu-id="996f8-106">Родительский элемент в иерархии доверия KERBEROS.</span><span class="sxs-lookup"><span data-stu-id="996f8-106">The parent in KERBEROS trust hierarchy.</span></span>



| <span data-ttu-id="996f8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-107">Entry</span></span> | <span data-ttu-id="996f8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="996f8-109">CN</span><span class="sxs-lookup"><span data-stu-id="996f8-109">CN</span></span>                | <span data-ttu-id="996f8-110">Trust-Parent</span><span class="sxs-lookup"><span data-stu-id="996f8-110">Trust-Parent</span></span>                            |
| <span data-ttu-id="996f8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="996f8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="996f8-112">трустпарент</span><span class="sxs-lookup"><span data-stu-id="996f8-112">trustParent</span></span>                             |
| <span data-ttu-id="996f8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="996f8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="996f8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="996f8-114">Update Privilege</span></span>  | <span data-ttu-id="996f8-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="996f8-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="996f8-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="996f8-116">Update Frequency</span></span>  | <span data-ttu-id="996f8-117">При создании дочернего домена.</span><span class="sxs-lookup"><span data-stu-id="996f8-117">When a child domain is created.</span></span>         |
| <span data-ttu-id="996f8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-118">Attribute-Id</span></span>      | <span data-ttu-id="996f8-119">1.2.840.113556.1.4.471</span><span class="sxs-lookup"><span data-stu-id="996f8-119">1.2.840.113556.1.4.471</span></span>                  |
| <span data-ttu-id="996f8-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="996f8-120">System-Id-Guid</span></span>    | <span data-ttu-id="996f8-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="996f8-121">b000ea7a-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="996f8-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="996f8-122">Syntax</span></span>            | [<span data-ttu-id="996f8-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="996f8-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="996f8-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="996f8-124">Implementations</span></span>

-   [<span data-ttu-id="996f8-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="996f8-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="996f8-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="996f8-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="996f8-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="996f8-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="996f8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="996f8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="996f8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="996f8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="996f8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="996f8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="996f8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="996f8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="996f8-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="996f8-132">Windows 2000 Server</span></span>



| <span data-ttu-id="996f8-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-133">Entry</span></span> | <span data-ttu-id="996f8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-137">System-Only</span></span>            | <span data-ttu-id="996f8-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-138">False</span></span>                                      |
| <span data-ttu-id="996f8-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-140">True</span><span class="sxs-lookup"><span data-stu-id="996f8-140">True</span></span>                                       |
| <span data-ttu-id="996f8-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-141">Is Indexed</span></span>             | <span data-ttu-id="996f8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-142">False</span></span>                                      |
| <span data-ttu-id="996f8-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-143">In Global Catalog</span></span>      | <span data-ttu-id="996f8-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-144">False</span></span>                                      |
| <span data-ttu-id="996f8-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-147">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-148">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-149">Search-Flags</span></span>           | <span data-ttu-id="996f8-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-150">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-151">System-Flags</span></span>           | <span data-ttu-id="996f8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-152">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-153">Classes used in</span></span>        | [<span data-ttu-id="996f8-154">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-154">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="996f8-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="996f8-155">Windows Server 2003</span></span>



| <span data-ttu-id="996f8-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-156">Entry</span></span> | <span data-ttu-id="996f8-157">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-157">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-158">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-159">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-160">System-Only</span></span>            | <span data-ttu-id="996f8-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-161">False</span></span>                                      |
| <span data-ttu-id="996f8-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-163">True</span><span class="sxs-lookup"><span data-stu-id="996f8-163">True</span></span>                                       |
| <span data-ttu-id="996f8-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-164">Is Indexed</span></span>             | <span data-ttu-id="996f8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-165">False</span></span>                                      |
| <span data-ttu-id="996f8-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-166">In Global Catalog</span></span>      | <span data-ttu-id="996f8-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-167">False</span></span>                                      |
| <span data-ttu-id="996f8-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-169">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-170">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-171">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-172">Search-Flags</span></span>           | <span data-ttu-id="996f8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-173">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-174">System-Flags</span></span>           | <span data-ttu-id="996f8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-175">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-176">Classes used in</span></span>        | [<span data-ttu-id="996f8-177">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-177">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="996f8-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="996f8-178">ADAM</span></span>



| <span data-ttu-id="996f8-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-179">Entry</span></span> | <span data-ttu-id="996f8-180">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-180">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-181">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-183">System-Only</span></span>            | <span data-ttu-id="996f8-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-184">False</span></span>                                      |
| <span data-ttu-id="996f8-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-185">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-186">True</span><span class="sxs-lookup"><span data-stu-id="996f8-186">True</span></span>                                       |
| <span data-ttu-id="996f8-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-187">Is Indexed</span></span>             | <span data-ttu-id="996f8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-188">False</span></span>                                      |
| <span data-ttu-id="996f8-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-189">In Global Catalog</span></span>      | <span data-ttu-id="996f8-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-190">False</span></span>                                      |
| <span data-ttu-id="996f8-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-195">Search-Flags</span></span>           | <span data-ttu-id="996f8-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-196">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-197">System-Flags</span></span>           | <span data-ttu-id="996f8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-198">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-199">Classes used in</span></span>        | [<span data-ttu-id="996f8-200">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="996f8-201">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="996f8-201">Windows Server 2003 R2</span></span>



| <span data-ttu-id="996f8-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-202">Entry</span></span> | <span data-ttu-id="996f8-203">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-204">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-205">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-206">System-Only</span></span>            | <span data-ttu-id="996f8-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-207">False</span></span>                                      |
| <span data-ttu-id="996f8-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-208">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-209">True</span><span class="sxs-lookup"><span data-stu-id="996f8-209">True</span></span>                                       |
| <span data-ttu-id="996f8-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-210">Is Indexed</span></span>             | <span data-ttu-id="996f8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-211">False</span></span>                                      |
| <span data-ttu-id="996f8-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-212">In Global Catalog</span></span>      | <span data-ttu-id="996f8-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-213">False</span></span>                                      |
| <span data-ttu-id="996f8-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-215">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-216">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-217">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-218">Search-Flags</span></span>           | <span data-ttu-id="996f8-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-219">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-220">System-Flags</span></span>           | <span data-ttu-id="996f8-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-221">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-222">Classes used in</span></span>        | [<span data-ttu-id="996f8-223">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-223">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="996f8-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="996f8-224">Windows Server 2008</span></span>



| <span data-ttu-id="996f8-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-225">Entry</span></span> | <span data-ttu-id="996f8-226">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-226">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-227">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-228">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-229">System-Only</span></span>            | <span data-ttu-id="996f8-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-230">False</span></span>                                      |
| <span data-ttu-id="996f8-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-231">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-232">True</span><span class="sxs-lookup"><span data-stu-id="996f8-232">True</span></span>                                       |
| <span data-ttu-id="996f8-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-233">Is Indexed</span></span>             | <span data-ttu-id="996f8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-234">False</span></span>                                      |
| <span data-ttu-id="996f8-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-235">In Global Catalog</span></span>      | <span data-ttu-id="996f8-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-236">False</span></span>                                      |
| <span data-ttu-id="996f8-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-238">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-239">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-240">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-241">Search-Flags</span></span>           | <span data-ttu-id="996f8-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-242">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-243">System-Flags</span></span>           | <span data-ttu-id="996f8-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-244">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-245">Classes used in</span></span>        | [<span data-ttu-id="996f8-246">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-246">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="996f8-247">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="996f8-247">Windows Server 2008 R2</span></span>



| <span data-ttu-id="996f8-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-248">Entry</span></span> | <span data-ttu-id="996f8-249">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-249">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-250">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-251">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-252">System-Only</span></span>            | <span data-ttu-id="996f8-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-253">False</span></span>                                      |
| <span data-ttu-id="996f8-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-254">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-255">True</span><span class="sxs-lookup"><span data-stu-id="996f8-255">True</span></span>                                       |
| <span data-ttu-id="996f8-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-256">Is Indexed</span></span>             | <span data-ttu-id="996f8-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-257">False</span></span>                                      |
| <span data-ttu-id="996f8-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-258">In Global Catalog</span></span>      | <span data-ttu-id="996f8-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-259">False</span></span>                                      |
| <span data-ttu-id="996f8-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-261">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-262">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-263">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-264">Search-Flags</span></span>           | <span data-ttu-id="996f8-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-265">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-266">System-Flags</span></span>           | <span data-ttu-id="996f8-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-267">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-268">Classes used in</span></span>        | [<span data-ttu-id="996f8-269">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-269">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="996f8-270">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="996f8-270">Windows Server 2012</span></span>



| <span data-ttu-id="996f8-271">Ввод</span><span class="sxs-lookup"><span data-stu-id="996f8-271">Entry</span></span> | <span data-ttu-id="996f8-272">Значение</span><span class="sxs-lookup"><span data-stu-id="996f8-272">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="996f8-273">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="996f8-273">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="996f8-274">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="996f8-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="996f8-275">System-Only</span></span>            | <span data-ttu-id="996f8-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-276">False</span></span>                                      |
| <span data-ttu-id="996f8-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="996f8-277">Is-Single-Valued</span></span>       | <span data-ttu-id="996f8-278">True</span><span class="sxs-lookup"><span data-stu-id="996f8-278">True</span></span>                                       |
| <span data-ttu-id="996f8-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="996f8-279">Is Indexed</span></span>             | <span data-ttu-id="996f8-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-280">False</span></span>                                      |
| <span data-ttu-id="996f8-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="996f8-281">In Global Catalog</span></span>      | <span data-ttu-id="996f8-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="996f8-282">False</span></span>                                      |
| <span data-ttu-id="996f8-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="996f8-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="996f8-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="996f8-284">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="996f8-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="996f8-285">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="996f8-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="996f8-286">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="996f8-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-287">Search-Flags</span></span>           | <span data-ttu-id="996f8-288">0x00000000</span><span class="sxs-lookup"><span data-stu-id="996f8-288">0x00000000</span></span>                                 |
| <span data-ttu-id="996f8-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="996f8-289">System-Flags</span></span>           | <span data-ttu-id="996f8-290">0x00000010</span><span class="sxs-lookup"><span data-stu-id="996f8-290">0x00000010</span></span>                                 |
| <span data-ttu-id="996f8-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="996f8-291">Classes used in</span></span>        | [<span data-ttu-id="996f8-292">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="996f8-292">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





