---
title: Атрибут Dns-Root
description: Самое верхнему доменному имени DNS, назначенному разделу домена или каталога.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Dns-Root
- Схема AD атрибута Днсрут
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654967"
---
# <a name="dns-root-attribute"></a><span data-ttu-id="19c62-105">Атрибут Dns-Root</span><span class="sxs-lookup"><span data-stu-id="19c62-105">Dns-Root attribute</span></span>

<span data-ttu-id="19c62-106">Самое верхнему доменному имени DNS, назначенному разделу домена или каталога.</span><span class="sxs-lookup"><span data-stu-id="19c62-106">The uppermost DNS domain name assigned to a domain/directory partition.</span></span> <span data-ttu-id="19c62-107">Это значение задается для объекта crossRef и используется, помимо прочего, для создания ссылок.</span><span class="sxs-lookup"><span data-stu-id="19c62-107">This is set on a crossRef object and is used, among other things, for referral generation.</span></span> <span data-ttu-id="19c62-108">При поиске по всему доменному дереву поиск должен быть инициирован в объекте Dns-Root.</span><span class="sxs-lookup"><span data-stu-id="19c62-108">When searching through an entire domain tree, the search must be initiated at the Dns-Root object.</span></span> <span data-ttu-id="19c62-109">Этот атрибут может быть многозначным, в этом случае создается несколько ссылок.</span><span class="sxs-lookup"><span data-stu-id="19c62-109">This attribute can be multi-valued, in which case multiple referrals are generated.</span></span>



| <span data-ttu-id="19c62-110">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-110">Entry</span></span> | <span data-ttu-id="19c62-111">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="19c62-112">CN</span><span class="sxs-lookup"><span data-stu-id="19c62-112">CN</span></span>                | <span data-ttu-id="19c62-113">Dns-Root</span><span class="sxs-lookup"><span data-stu-id="19c62-113">Dns-Root</span></span>                                    |
| <span data-ttu-id="19c62-114">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="19c62-114">Ldap-Display-Name</span></span> | <span data-ttu-id="19c62-115">днсрут</span><span class="sxs-lookup"><span data-stu-id="19c62-115">dnsRoot</span></span>                                     |
| <span data-ttu-id="19c62-116">Размер</span><span class="sxs-lookup"><span data-stu-id="19c62-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="19c62-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="19c62-117">Update Privilege</span></span>  | <span data-ttu-id="19c62-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="19c62-118">This value is set by the system.</span></span>            |
| <span data-ttu-id="19c62-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="19c62-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="19c62-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-120">Attribute-Id</span></span>      | <span data-ttu-id="19c62-121">1.2.840.113556.1.4.28</span><span class="sxs-lookup"><span data-stu-id="19c62-121">1.2.840.113556.1.4.28</span></span>                       |
| <span data-ttu-id="19c62-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="19c62-122">System-Id-Guid</span></span>    | <span data-ttu-id="19c62-123">bf967959-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="19c62-123">bf967959-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="19c62-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19c62-124">Syntax</span></span>            | [<span data-ttu-id="19c62-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="19c62-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="19c62-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="19c62-126">Implementations</span></span>

-   [<span data-ttu-id="19c62-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="19c62-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="19c62-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="19c62-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="19c62-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="19c62-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="19c62-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="19c62-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="19c62-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="19c62-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="19c62-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="19c62-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="19c62-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="19c62-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="19c62-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="19c62-134">Windows 2000 Server</span></span>



| <span data-ttu-id="19c62-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-135">Entry</span></span> | <span data-ttu-id="19c62-136">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-136">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-137">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-138">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-139">System-Only</span></span>            | <span data-ttu-id="19c62-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-140">False</span></span>                                      |
| <span data-ttu-id="19c62-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-141">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-142">False</span></span>                                      |
| <span data-ttu-id="19c62-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-143">Is Indexed</span></span>             | <span data-ttu-id="19c62-144">True</span><span class="sxs-lookup"><span data-stu-id="19c62-144">True</span></span>                                       |
| <span data-ttu-id="19c62-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-145">In Global Catalog</span></span>      | <span data-ttu-id="19c62-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-146">False</span></span>                                      |
| <span data-ttu-id="19c62-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-148">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-149">Range-Lower</span></span>            | <span data-ttu-id="19c62-150">1</span><span class="sxs-lookup"><span data-stu-id="19c62-150">1</span></span>                                          |
| <span data-ttu-id="19c62-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-151">Range-Upper</span></span>            | <span data-ttu-id="19c62-152">255</span><span class="sxs-lookup"><span data-stu-id="19c62-152">255</span></span>                                        |
| <span data-ttu-id="19c62-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-153">Search-Flags</span></span>           | <span data-ttu-id="19c62-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-154">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-155">System-Flags</span></span>           | <span data-ttu-id="19c62-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-156">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-157">Classes used in</span></span>        | [<span data-ttu-id="19c62-158">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-158">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="19c62-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19c62-159">Windows Server 2003</span></span>



| <span data-ttu-id="19c62-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-160">Entry</span></span> | <span data-ttu-id="19c62-161">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-161">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-162">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-163">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-164">System-Only</span></span>            | <span data-ttu-id="19c62-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-165">False</span></span>                                      |
| <span data-ttu-id="19c62-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-166">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-167">False</span></span>                                      |
| <span data-ttu-id="19c62-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-168">Is Indexed</span></span>             | <span data-ttu-id="19c62-169">True</span><span class="sxs-lookup"><span data-stu-id="19c62-169">True</span></span>                                       |
| <span data-ttu-id="19c62-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-170">In Global Catalog</span></span>      | <span data-ttu-id="19c62-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-171">False</span></span>                                      |
| <span data-ttu-id="19c62-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-173">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-174">Range-Lower</span></span>            | <span data-ttu-id="19c62-175">1</span><span class="sxs-lookup"><span data-stu-id="19c62-175">1</span></span>                                          |
| <span data-ttu-id="19c62-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-176">Range-Upper</span></span>            | <span data-ttu-id="19c62-177">255</span><span class="sxs-lookup"><span data-stu-id="19c62-177">255</span></span>                                        |
| <span data-ttu-id="19c62-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-178">Search-Flags</span></span>           | <span data-ttu-id="19c62-179">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-179">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-180">System-Flags</span></span>           | <span data-ttu-id="19c62-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-181">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-182">Classes used in</span></span>        | [<span data-ttu-id="19c62-183">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-183">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="19c62-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="19c62-184">ADAM</span></span>



| <span data-ttu-id="19c62-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-185">Entry</span></span> | <span data-ttu-id="19c62-186">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-186">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-187">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-188">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-189">System-Only</span></span>            | <span data-ttu-id="19c62-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-190">False</span></span>                                      |
| <span data-ttu-id="19c62-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-191">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-192">False</span></span>                                      |
| <span data-ttu-id="19c62-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-193">Is Indexed</span></span>             | <span data-ttu-id="19c62-194">True</span><span class="sxs-lookup"><span data-stu-id="19c62-194">True</span></span>                                       |
| <span data-ttu-id="19c62-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-195">In Global Catalog</span></span>      | <span data-ttu-id="19c62-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-196">False</span></span>                                      |
| <span data-ttu-id="19c62-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-198">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-199">Range-Lower</span></span>            | <span data-ttu-id="19c62-200">1</span><span class="sxs-lookup"><span data-stu-id="19c62-200">1</span></span>                                          |
| <span data-ttu-id="19c62-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-201">Range-Upper</span></span>            | <span data-ttu-id="19c62-202">255</span><span class="sxs-lookup"><span data-stu-id="19c62-202">255</span></span>                                        |
| <span data-ttu-id="19c62-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-203">Search-Flags</span></span>           | <span data-ttu-id="19c62-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-204">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-205">System-Flags</span></span>           | <span data-ttu-id="19c62-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-206">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-207">Classes used in</span></span>        | [<span data-ttu-id="19c62-208">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-208">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="19c62-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="19c62-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="19c62-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-210">Entry</span></span> | <span data-ttu-id="19c62-211">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-211">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-212">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-213">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-214">System-Only</span></span>            | <span data-ttu-id="19c62-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-215">False</span></span>                                      |
| <span data-ttu-id="19c62-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-216">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-217">False</span></span>                                      |
| <span data-ttu-id="19c62-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-218">Is Indexed</span></span>             | <span data-ttu-id="19c62-219">True</span><span class="sxs-lookup"><span data-stu-id="19c62-219">True</span></span>                                       |
| <span data-ttu-id="19c62-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-220">In Global Catalog</span></span>      | <span data-ttu-id="19c62-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-221">False</span></span>                                      |
| <span data-ttu-id="19c62-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-223">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-224">Range-Lower</span></span>            | <span data-ttu-id="19c62-225">1</span><span class="sxs-lookup"><span data-stu-id="19c62-225">1</span></span>                                          |
| <span data-ttu-id="19c62-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-226">Range-Upper</span></span>            | <span data-ttu-id="19c62-227">255</span><span class="sxs-lookup"><span data-stu-id="19c62-227">255</span></span>                                        |
| <span data-ttu-id="19c62-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-228">Search-Flags</span></span>           | <span data-ttu-id="19c62-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-229">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-230">System-Flags</span></span>           | <span data-ttu-id="19c62-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-231">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-232">Classes used in</span></span>        | [<span data-ttu-id="19c62-233">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="19c62-234">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19c62-234">Windows Server 2008</span></span>



| <span data-ttu-id="19c62-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-235">Entry</span></span> | <span data-ttu-id="19c62-236">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-236">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-237">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-238">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-239">System-Only</span></span>            | <span data-ttu-id="19c62-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-240">False</span></span>                                      |
| <span data-ttu-id="19c62-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-241">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-242">False</span></span>                                      |
| <span data-ttu-id="19c62-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-243">Is Indexed</span></span>             | <span data-ttu-id="19c62-244">True</span><span class="sxs-lookup"><span data-stu-id="19c62-244">True</span></span>                                       |
| <span data-ttu-id="19c62-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-245">In Global Catalog</span></span>      | <span data-ttu-id="19c62-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-246">False</span></span>                                      |
| <span data-ttu-id="19c62-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-248">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-249">Range-Lower</span></span>            | <span data-ttu-id="19c62-250">1</span><span class="sxs-lookup"><span data-stu-id="19c62-250">1</span></span>                                          |
| <span data-ttu-id="19c62-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-251">Range-Upper</span></span>            | <span data-ttu-id="19c62-252">255</span><span class="sxs-lookup"><span data-stu-id="19c62-252">255</span></span>                                        |
| <span data-ttu-id="19c62-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-253">Search-Flags</span></span>           | <span data-ttu-id="19c62-254">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-254">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-255">System-Flags</span></span>           | <span data-ttu-id="19c62-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-256">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-257">Classes used in</span></span>        | [<span data-ttu-id="19c62-258">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-258">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="19c62-259">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="19c62-259">Windows Server 2008 R2</span></span>



| <span data-ttu-id="19c62-260">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-260">Entry</span></span> | <span data-ttu-id="19c62-261">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-261">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-262">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-262">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-263">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-264">System-Only</span></span>            | <span data-ttu-id="19c62-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-265">False</span></span>                                      |
| <span data-ttu-id="19c62-266">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-266">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-267">False</span></span>                                      |
| <span data-ttu-id="19c62-268">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-268">Is Indexed</span></span>             | <span data-ttu-id="19c62-269">True</span><span class="sxs-lookup"><span data-stu-id="19c62-269">True</span></span>                                       |
| <span data-ttu-id="19c62-270">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-270">In Global Catalog</span></span>      | <span data-ttu-id="19c62-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-271">False</span></span>                                      |
| <span data-ttu-id="19c62-272">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-273">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-273">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-274">Range-Lower</span></span>            | <span data-ttu-id="19c62-275">1</span><span class="sxs-lookup"><span data-stu-id="19c62-275">1</span></span>                                          |
| <span data-ttu-id="19c62-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-276">Range-Upper</span></span>            | <span data-ttu-id="19c62-277">255</span><span class="sxs-lookup"><span data-stu-id="19c62-277">255</span></span>                                        |
| <span data-ttu-id="19c62-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-278">Search-Flags</span></span>           | <span data-ttu-id="19c62-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-279">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-280">System-Flags</span></span>           | <span data-ttu-id="19c62-281">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-281">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-282">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-282">Classes used in</span></span>        | [<span data-ttu-id="19c62-283">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-283">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="19c62-284">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19c62-284">Windows Server 2012</span></span>



| <span data-ttu-id="19c62-285">Ввод</span><span class="sxs-lookup"><span data-stu-id="19c62-285">Entry</span></span> | <span data-ttu-id="19c62-286">Значение</span><span class="sxs-lookup"><span data-stu-id="19c62-286">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="19c62-287">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="19c62-287">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-288">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="19c62-288">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="19c62-289">System-Only</span><span class="sxs-lookup"><span data-stu-id="19c62-289">System-Only</span></span>            | <span data-ttu-id="19c62-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-290">False</span></span>                                      |
| <span data-ttu-id="19c62-291">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="19c62-291">Is-Single-Valued</span></span>       | <span data-ttu-id="19c62-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-292">False</span></span>                                      |
| <span data-ttu-id="19c62-293">Индексируется</span><span class="sxs-lookup"><span data-stu-id="19c62-293">Is Indexed</span></span>             | <span data-ttu-id="19c62-294">True</span><span class="sxs-lookup"><span data-stu-id="19c62-294">True</span></span>                                       |
| <span data-ttu-id="19c62-295">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="19c62-295">In Global Catalog</span></span>      | <span data-ttu-id="19c62-296">Неверно</span><span class="sxs-lookup"><span data-stu-id="19c62-296">False</span></span>                                      |
| <span data-ttu-id="19c62-297">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="19c62-297">NT-Security-Descriptor</span></span> | <span data-ttu-id="19c62-298">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="19c62-298">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="19c62-299">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="19c62-299">Range-Lower</span></span>            | <span data-ttu-id="19c62-300">1</span><span class="sxs-lookup"><span data-stu-id="19c62-300">1</span></span>                                          |
| <span data-ttu-id="19c62-301">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="19c62-301">Range-Upper</span></span>            | <span data-ttu-id="19c62-302">255</span><span class="sxs-lookup"><span data-stu-id="19c62-302">255</span></span>                                        |
| <span data-ttu-id="19c62-303">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-303">Search-Flags</span></span>           | <span data-ttu-id="19c62-304">0x00000001</span><span class="sxs-lookup"><span data-stu-id="19c62-304">0x00000001</span></span>                                 |
| <span data-ttu-id="19c62-305">System-Flags</span><span class="sxs-lookup"><span data-stu-id="19c62-305">System-Flags</span></span>           | <span data-ttu-id="19c62-306">0x00000010</span><span class="sxs-lookup"><span data-stu-id="19c62-306">0x00000010</span></span>                                 |
| <span data-ttu-id="19c62-307">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="19c62-307">Classes used in</span></span>        | [<span data-ttu-id="19c62-308">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="19c62-308">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





