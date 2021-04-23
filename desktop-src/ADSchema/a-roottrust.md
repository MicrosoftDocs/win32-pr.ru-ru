---
title: Атрибут Root-Trust
description: Различающееся имя другой перекрестной ссылки.
ms.assetid: ae886a08-e6ba-4346-815f-8fbf38a347d7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Root-Trust
- Схема AD атрибута Руттруст
topic_type:
- apiref
api_name:
- Root-Trust
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 748785f4c00900fb3183b53f8e801ea32b6a1657
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138487"
---
# <a name="root-trust-attribute"></a><span data-ttu-id="461b8-105">Атрибут Root-Trust</span><span class="sxs-lookup"><span data-stu-id="461b8-105">Root-Trust attribute</span></span>

<span data-ttu-id="461b8-106">Различающееся имя другой перекрестной ссылки.</span><span class="sxs-lookup"><span data-stu-id="461b8-106">The Distinguished Name of another Cross-Ref.</span></span>



| <span data-ttu-id="461b8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-107">Entry</span></span> | <span data-ttu-id="461b8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="461b8-109">CN</span><span class="sxs-lookup"><span data-stu-id="461b8-109">CN</span></span>                | <span data-ttu-id="461b8-110">Root-Trust</span><span class="sxs-lookup"><span data-stu-id="461b8-110">Root-Trust</span></span>                              |
| <span data-ttu-id="461b8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="461b8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="461b8-112">руттруст</span><span class="sxs-lookup"><span data-stu-id="461b8-112">rootTrust</span></span>                               |
| <span data-ttu-id="461b8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="461b8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="461b8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="461b8-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="461b8-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="461b8-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="461b8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-116">Attribute-Id</span></span>      | <span data-ttu-id="461b8-117">1.2.840.113556.1.4.674</span><span class="sxs-lookup"><span data-stu-id="461b8-117">1.2.840.113556.1.4.674</span></span>                  |
| <span data-ttu-id="461b8-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="461b8-118">System-Id-Guid</span></span>    | <span data-ttu-id="461b8-119">7bfdcb80-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="461b8-119">7bfdcb80-4807-11d1-a9c3-0000f80367c1</span></span>    |
| <span data-ttu-id="461b8-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="461b8-120">Syntax</span></span>            | [<span data-ttu-id="461b8-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="461b8-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="461b8-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="461b8-122">Implementations</span></span>

-   [<span data-ttu-id="461b8-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="461b8-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="461b8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="461b8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="461b8-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="461b8-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="461b8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="461b8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="461b8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="461b8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="461b8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="461b8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="461b8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="461b8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="461b8-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="461b8-130">Windows 2000 Server</span></span>



| <span data-ttu-id="461b8-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-131">Entry</span></span> | <span data-ttu-id="461b8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-132">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-133">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-135">System-Only</span></span>            | <span data-ttu-id="461b8-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-136">False</span></span>                                      |
| <span data-ttu-id="461b8-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-138">False</span></span>                                      |
| <span data-ttu-id="461b8-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-139">Is Indexed</span></span>             | <span data-ttu-id="461b8-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-140">False</span></span>                                      |
| <span data-ttu-id="461b8-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-141">In Global Catalog</span></span>      | <span data-ttu-id="461b8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-142">False</span></span>                                      |
| <span data-ttu-id="461b8-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-147">Search-Flags</span></span>           | <span data-ttu-id="461b8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-148">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-149">System-Flags</span></span>           | <span data-ttu-id="461b8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-150">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-151">Classes used in</span></span>        | [<span data-ttu-id="461b8-152">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="461b8-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="461b8-153">Windows Server 2003</span></span>



| <span data-ttu-id="461b8-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-154">Entry</span></span> | <span data-ttu-id="461b8-155">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-156">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-158">System-Only</span></span>            | <span data-ttu-id="461b8-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-159">False</span></span>                                      |
| <span data-ttu-id="461b8-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-161">False</span></span>                                      |
| <span data-ttu-id="461b8-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-162">Is Indexed</span></span>             | <span data-ttu-id="461b8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-163">False</span></span>                                      |
| <span data-ttu-id="461b8-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-164">In Global Catalog</span></span>      | <span data-ttu-id="461b8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-165">False</span></span>                                      |
| <span data-ttu-id="461b8-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-170">Search-Flags</span></span>           | <span data-ttu-id="461b8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-171">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-172">System-Flags</span></span>           | <span data-ttu-id="461b8-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-173">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-174">Classes used in</span></span>        | [<span data-ttu-id="461b8-175">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="461b8-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="461b8-176">ADAM</span></span>



| <span data-ttu-id="461b8-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-177">Entry</span></span> | <span data-ttu-id="461b8-178">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-179">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-180">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-181">System-Only</span></span>            | <span data-ttu-id="461b8-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-182">False</span></span>                                      |
| <span data-ttu-id="461b8-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-184">False</span></span>                                      |
| <span data-ttu-id="461b8-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-185">Is Indexed</span></span>             | <span data-ttu-id="461b8-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-186">False</span></span>                                      |
| <span data-ttu-id="461b8-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-187">In Global Catalog</span></span>      | <span data-ttu-id="461b8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-188">False</span></span>                                      |
| <span data-ttu-id="461b8-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-190">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-191">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-192">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-193">Search-Flags</span></span>           | <span data-ttu-id="461b8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-194">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-195">System-Flags</span></span>           | <span data-ttu-id="461b8-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-196">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-197">Classes used in</span></span>        | [<span data-ttu-id="461b8-198">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-198">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="461b8-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="461b8-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="461b8-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-200">Entry</span></span> | <span data-ttu-id="461b8-201">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-201">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-202">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-203">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-204">System-Only</span></span>            | <span data-ttu-id="461b8-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-205">False</span></span>                                      |
| <span data-ttu-id="461b8-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-207">False</span></span>                                      |
| <span data-ttu-id="461b8-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-208">Is Indexed</span></span>             | <span data-ttu-id="461b8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-209">False</span></span>                                      |
| <span data-ttu-id="461b8-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-210">In Global Catalog</span></span>      | <span data-ttu-id="461b8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-211">False</span></span>                                      |
| <span data-ttu-id="461b8-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-213">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-214">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-215">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-216">Search-Flags</span></span>           | <span data-ttu-id="461b8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-217">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-218">System-Flags</span></span>           | <span data-ttu-id="461b8-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-219">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-220">Classes used in</span></span>        | [<span data-ttu-id="461b8-221">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-221">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="461b8-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="461b8-222">Windows Server 2008</span></span>



| <span data-ttu-id="461b8-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-223">Entry</span></span> | <span data-ttu-id="461b8-224">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-224">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-225">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-226">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-227">System-Only</span></span>            | <span data-ttu-id="461b8-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-228">False</span></span>                                      |
| <span data-ttu-id="461b8-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-230">False</span></span>                                      |
| <span data-ttu-id="461b8-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-231">Is Indexed</span></span>             | <span data-ttu-id="461b8-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-232">False</span></span>                                      |
| <span data-ttu-id="461b8-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-233">In Global Catalog</span></span>      | <span data-ttu-id="461b8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-234">False</span></span>                                      |
| <span data-ttu-id="461b8-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-236">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-237">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-238">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-239">Search-Flags</span></span>           | <span data-ttu-id="461b8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-240">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-241">System-Flags</span></span>           | <span data-ttu-id="461b8-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-242">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-243">Classes used in</span></span>        | [<span data-ttu-id="461b8-244">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-244">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="461b8-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="461b8-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="461b8-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-246">Entry</span></span> | <span data-ttu-id="461b8-247">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-247">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-248">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-249">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-250">System-Only</span></span>            | <span data-ttu-id="461b8-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-251">False</span></span>                                      |
| <span data-ttu-id="461b8-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-252">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-253">False</span></span>                                      |
| <span data-ttu-id="461b8-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-254">Is Indexed</span></span>             | <span data-ttu-id="461b8-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-255">False</span></span>                                      |
| <span data-ttu-id="461b8-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-256">In Global Catalog</span></span>      | <span data-ttu-id="461b8-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-257">False</span></span>                                      |
| <span data-ttu-id="461b8-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-259">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-260">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-261">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-262">Search-Flags</span></span>           | <span data-ttu-id="461b8-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-263">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-264">System-Flags</span></span>           | <span data-ttu-id="461b8-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-265">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-266">Classes used in</span></span>        | [<span data-ttu-id="461b8-267">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-267">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="461b8-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="461b8-268">Windows Server 2012</span></span>



| <span data-ttu-id="461b8-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="461b8-269">Entry</span></span> | <span data-ttu-id="461b8-270">Значение</span><span class="sxs-lookup"><span data-stu-id="461b8-270">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="461b8-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="461b8-271">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="461b8-272">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="461b8-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="461b8-273">System-Only</span></span>            | <span data-ttu-id="461b8-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-274">False</span></span>                                      |
| <span data-ttu-id="461b8-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="461b8-275">Is-Single-Valued</span></span>       | <span data-ttu-id="461b8-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-276">False</span></span>                                      |
| <span data-ttu-id="461b8-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="461b8-277">Is Indexed</span></span>             | <span data-ttu-id="461b8-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-278">False</span></span>                                      |
| <span data-ttu-id="461b8-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="461b8-279">In Global Catalog</span></span>      | <span data-ttu-id="461b8-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="461b8-280">False</span></span>                                      |
| <span data-ttu-id="461b8-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="461b8-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="461b8-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="461b8-282">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="461b8-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="461b8-283">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="461b8-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="461b8-284">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="461b8-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-285">Search-Flags</span></span>           | <span data-ttu-id="461b8-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="461b8-286">0x00000000</span></span>                                 |
| <span data-ttu-id="461b8-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="461b8-287">System-Flags</span></span>           | <span data-ttu-id="461b8-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="461b8-288">0x00000010</span></span>                                 |
| <span data-ttu-id="461b8-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="461b8-289">Classes used in</span></span>        | [<span data-ttu-id="461b8-290">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="461b8-290">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





