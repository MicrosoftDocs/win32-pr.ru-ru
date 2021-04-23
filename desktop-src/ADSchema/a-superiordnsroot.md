---
title: Атрибут «старший-DNS-Root»
description: Это системный атрибут, используемый для создания ссылок.
ms.assetid: 421f8315-26e2-457d-ae76-868b7fc6551a
ms.tgt_platform: multiple
keywords:
- Схема AD корневого атрибута DNS
- Схема AD атрибута Супериорднсрут
topic_type:
- apiref
api_name:
- Superior-DNS-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6561839cf5137968adbac628ad6046b8b86dab85
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655285"
---
# <a name="superior-dns-root-attribute"></a><span data-ttu-id="4fafc-105">Атрибут «старший-DNS-Root»</span><span class="sxs-lookup"><span data-stu-id="4fafc-105">Superior-DNS-Root attribute</span></span>

<span data-ttu-id="4fafc-106">Это системный атрибут, используемый для создания ссылок.</span><span class="sxs-lookup"><span data-stu-id="4fafc-106">This is a system attribute that is used for referrals generation.</span></span>



| <span data-ttu-id="4fafc-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-107">Entry</span></span> | <span data-ttu-id="4fafc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="4fafc-109">CN</span><span class="sxs-lookup"><span data-stu-id="4fafc-109">CN</span></span>                | <span data-ttu-id="4fafc-110">Старший DNS-корневой узел</span><span class="sxs-lookup"><span data-stu-id="4fafc-110">Superior-DNS-Root</span></span>                           |
| <span data-ttu-id="4fafc-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4fafc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4fafc-112">супериорднсрут</span><span class="sxs-lookup"><span data-stu-id="4fafc-112">superiorDNSRoot</span></span>                             |
| <span data-ttu-id="4fafc-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4fafc-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="4fafc-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4fafc-114">Update Privilege</span></span>  | <span data-ttu-id="4fafc-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="4fafc-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="4fafc-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4fafc-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="4fafc-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-117">Attribute-Id</span></span>      | <span data-ttu-id="4fafc-118">1.2.840.113556.1.4.532</span><span class="sxs-lookup"><span data-stu-id="4fafc-118">1.2.840.113556.1.4.532</span></span>                      |
| <span data-ttu-id="4fafc-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4fafc-119">System-Id-Guid</span></span>    | <span data-ttu-id="4fafc-120">5245801d-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4fafc-120">5245801d-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="4fafc-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fafc-121">Syntax</span></span>            | [<span data-ttu-id="4fafc-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="4fafc-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="4fafc-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4fafc-123">Implementations</span></span>

-   [<span data-ttu-id="4fafc-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4fafc-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4fafc-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4fafc-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4fafc-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4fafc-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4fafc-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4fafc-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4fafc-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4fafc-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4fafc-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4fafc-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4fafc-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4fafc-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4fafc-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4fafc-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4fafc-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-132">Entry</span></span> | <span data-ttu-id="4fafc-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-133">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-134">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-135">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-136">System-Only</span></span>            | <span data-ttu-id="4fafc-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-137">False</span></span>                                      |
| <span data-ttu-id="4fafc-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-139">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-139">True</span></span>                                       |
| <span data-ttu-id="4fafc-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-140">Is Indexed</span></span>             | <span data-ttu-id="4fafc-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-141">False</span></span>                                      |
| <span data-ttu-id="4fafc-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-142">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-143">False</span></span>                                      |
| <span data-ttu-id="4fafc-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-145">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-146">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-147">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-148">Search-Flags</span></span>           | <span data-ttu-id="4fafc-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-149">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-150">System-Flags</span></span>           | <span data-ttu-id="4fafc-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-151">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-152">Classes used in</span></span>        | [<span data-ttu-id="4fafc-153">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-153">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4fafc-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4fafc-154">Windows Server 2003</span></span>



| <span data-ttu-id="4fafc-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-155">Entry</span></span> | <span data-ttu-id="4fafc-156">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-156">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-157">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-159">System-Only</span></span>            | <span data-ttu-id="4fafc-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-160">False</span></span>                                      |
| <span data-ttu-id="4fafc-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-162">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-162">True</span></span>                                       |
| <span data-ttu-id="4fafc-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-163">Is Indexed</span></span>             | <span data-ttu-id="4fafc-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-164">False</span></span>                                      |
| <span data-ttu-id="4fafc-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-165">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-166">False</span></span>                                      |
| <span data-ttu-id="4fafc-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-171">Search-Flags</span></span>           | <span data-ttu-id="4fafc-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-172">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-173">System-Flags</span></span>           | <span data-ttu-id="4fafc-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-174">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-175">Classes used in</span></span>        | [<span data-ttu-id="4fafc-176">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4fafc-177">ADAM</span><span class="sxs-lookup"><span data-stu-id="4fafc-177">ADAM</span></span>



| <span data-ttu-id="4fafc-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-178">Entry</span></span> | <span data-ttu-id="4fafc-179">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-180">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-182">System-Only</span></span>            | <span data-ttu-id="4fafc-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-183">False</span></span>                                      |
| <span data-ttu-id="4fafc-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-185">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-185">True</span></span>                                       |
| <span data-ttu-id="4fafc-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-186">Is Indexed</span></span>             | <span data-ttu-id="4fafc-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-187">False</span></span>                                      |
| <span data-ttu-id="4fafc-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-188">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-189">False</span></span>                                      |
| <span data-ttu-id="4fafc-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-194">Search-Flags</span></span>           | <span data-ttu-id="4fafc-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-195">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-196">System-Flags</span></span>           | <span data-ttu-id="4fafc-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-197">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-198">Classes used in</span></span>        | [<span data-ttu-id="4fafc-199">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4fafc-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4fafc-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4fafc-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-201">Entry</span></span> | <span data-ttu-id="4fafc-202">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-202">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-203">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-204">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-205">System-Only</span></span>            | <span data-ttu-id="4fafc-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-206">False</span></span>                                      |
| <span data-ttu-id="4fafc-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-208">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-208">True</span></span>                                       |
| <span data-ttu-id="4fafc-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-209">Is Indexed</span></span>             | <span data-ttu-id="4fafc-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-210">False</span></span>                                      |
| <span data-ttu-id="4fafc-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-211">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-212">False</span></span>                                      |
| <span data-ttu-id="4fafc-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-214">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-215">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-216">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-217">Search-Flags</span></span>           | <span data-ttu-id="4fafc-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-218">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-219">System-Flags</span></span>           | <span data-ttu-id="4fafc-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-220">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-221">Classes used in</span></span>        | [<span data-ttu-id="4fafc-222">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-222">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4fafc-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4fafc-223">Windows Server 2008</span></span>



| <span data-ttu-id="4fafc-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-224">Entry</span></span> | <span data-ttu-id="4fafc-225">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-225">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-226">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-227">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-228">System-Only</span></span>            | <span data-ttu-id="4fafc-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-229">False</span></span>                                      |
| <span data-ttu-id="4fafc-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-231">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-231">True</span></span>                                       |
| <span data-ttu-id="4fafc-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-232">Is Indexed</span></span>             | <span data-ttu-id="4fafc-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-233">False</span></span>                                      |
| <span data-ttu-id="4fafc-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-234">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-235">False</span></span>                                      |
| <span data-ttu-id="4fafc-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-237">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-238">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-239">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-240">Search-Flags</span></span>           | <span data-ttu-id="4fafc-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-241">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-242">System-Flags</span></span>           | <span data-ttu-id="4fafc-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-243">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-244">Classes used in</span></span>        | [<span data-ttu-id="4fafc-245">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-245">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4fafc-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4fafc-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4fafc-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-247">Entry</span></span> | <span data-ttu-id="4fafc-248">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-248">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-249">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-250">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-251">System-Only</span></span>            | <span data-ttu-id="4fafc-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-252">False</span></span>                                      |
| <span data-ttu-id="4fafc-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-254">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-254">True</span></span>                                       |
| <span data-ttu-id="4fafc-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-255">Is Indexed</span></span>             | <span data-ttu-id="4fafc-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-256">False</span></span>                                      |
| <span data-ttu-id="4fafc-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-257">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-258">False</span></span>                                      |
| <span data-ttu-id="4fafc-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-260">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-261">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-262">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-263">Search-Flags</span></span>           | <span data-ttu-id="4fafc-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-264">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-265">System-Flags</span></span>           | <span data-ttu-id="4fafc-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-266">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-267">Classes used in</span></span>        | [<span data-ttu-id="4fafc-268">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-268">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4fafc-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4fafc-269">Windows Server 2012</span></span>



| <span data-ttu-id="4fafc-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="4fafc-270">Entry</span></span> | <span data-ttu-id="4fafc-271">Значение</span><span class="sxs-lookup"><span data-stu-id="4fafc-271">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="4fafc-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4fafc-272">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4fafc-273">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="4fafc-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="4fafc-274">System-Only</span></span>            | <span data-ttu-id="4fafc-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-275">False</span></span>                                      |
| <span data-ttu-id="4fafc-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4fafc-276">Is-Single-Valued</span></span>       | <span data-ttu-id="4fafc-277">True</span><span class="sxs-lookup"><span data-stu-id="4fafc-277">True</span></span>                                       |
| <span data-ttu-id="4fafc-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4fafc-278">Is Indexed</span></span>             | <span data-ttu-id="4fafc-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-279">False</span></span>                                      |
| <span data-ttu-id="4fafc-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4fafc-280">In Global Catalog</span></span>      | <span data-ttu-id="4fafc-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="4fafc-281">False</span></span>                                      |
| <span data-ttu-id="4fafc-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4fafc-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="4fafc-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4fafc-283">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="4fafc-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4fafc-284">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4fafc-285">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="4fafc-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-286">Search-Flags</span></span>           | <span data-ttu-id="4fafc-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4fafc-287">0x00000000</span></span>                                 |
| <span data-ttu-id="4fafc-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4fafc-288">System-Flags</span></span>           | <span data-ttu-id="4fafc-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4fafc-289">0x00000010</span></span>                                 |
| <span data-ttu-id="4fafc-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4fafc-290">Classes used in</span></span>        | [<span data-ttu-id="4fafc-291">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="4fafc-291">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





