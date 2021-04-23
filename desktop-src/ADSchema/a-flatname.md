---
title: Атрибут Flat-Name
description: Для доменов Windows NT неструктурированное имя является NetBIOS-именем. Для ссылок, не имеющих \ 8211; Домены Windows NT, неструктурированное имя — это идентифицирующее имя этого домена или значение NULL.
ms.assetid: ec368657-a0e7-4416-ab80-1d18d98bbcfa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Flat-Name
- Схема AD атрибута Флатнаме
topic_type:
- apiref
api_name:
- Flat-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373ee0736c051932fdb6dd20701f0c5ec353ad3b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493593"
---
# <a name="flat-name-attribute"></a><span data-ttu-id="9cf76-106">Атрибут Flat-Name</span><span class="sxs-lookup"><span data-stu-id="9cf76-106">Flat-Name attribute</span></span>

<span data-ttu-id="9cf76-107">Для доменов Windows NT неструктурированное имя является NetBIOS-именем.</span><span class="sxs-lookup"><span data-stu-id="9cf76-107">For Windows NT domains, the flat name is the NetBIOS name.</span></span> <span data-ttu-id="9cf76-108">Для ссылок, не являющихся доменами Windows NT, неструктурированным именем является идентифицирующее имя этого домена или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9cf76-108">For links with non Windows NT domains, the flat name is the identifying name of that domain, or it is **NULL**.</span></span>



| <span data-ttu-id="9cf76-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-109">Entry</span></span> | <span data-ttu-id="9cf76-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9cf76-111">CN</span><span class="sxs-lookup"><span data-stu-id="9cf76-111">CN</span></span>                | <span data-ttu-id="9cf76-112">Flat-Name</span><span class="sxs-lookup"><span data-stu-id="9cf76-112">Flat-Name</span></span>                                   |
| <span data-ttu-id="9cf76-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9cf76-113">Ldap-Display-Name</span></span> | <span data-ttu-id="9cf76-114">флатнаме</span><span class="sxs-lookup"><span data-stu-id="9cf76-114">flatName</span></span>                                    |
| <span data-ttu-id="9cf76-115">Размер</span><span class="sxs-lookup"><span data-stu-id="9cf76-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="9cf76-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9cf76-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9cf76-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9cf76-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9cf76-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-118">Attribute-Id</span></span>      | <span data-ttu-id="9cf76-119">1.2.840.113556.1.4.511</span><span class="sxs-lookup"><span data-stu-id="9cf76-119">1.2.840.113556.1.4.511</span></span>                      |
| <span data-ttu-id="9cf76-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9cf76-120">System-Id-Guid</span></span>    | <span data-ttu-id="9cf76-121">b7b13117-b82e-11d0-afee-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="9cf76-121">b7b13117-b82e-11d0-afee-0000f80367c1</span></span>        |
| <span data-ttu-id="9cf76-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cf76-122">Syntax</span></span>            | [<span data-ttu-id="9cf76-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="9cf76-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9cf76-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9cf76-124">Implementations</span></span>

-   [<span data-ttu-id="9cf76-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9cf76-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9cf76-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9cf76-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9cf76-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9cf76-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9cf76-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9cf76-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9cf76-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9cf76-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9cf76-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9cf76-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9cf76-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9cf76-131">Windows 2000 Server</span></span>



| <span data-ttu-id="9cf76-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-132">Entry</span></span> | <span data-ttu-id="9cf76-133">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf76-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9cf76-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cf76-136">System-Only</span></span>            | <span data-ttu-id="9cf76-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-137">False</span></span>                                                |
| <span data-ttu-id="9cf76-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9cf76-138">Is-Single-Valued</span></span>       | <span data-ttu-id="9cf76-139">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-139">True</span></span>                                                 |
| <span data-ttu-id="9cf76-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9cf76-140">Is Indexed</span></span>             | <span data-ttu-id="9cf76-141">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-141">True</span></span>                                                 |
| <span data-ttu-id="9cf76-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9cf76-142">In Global Catalog</span></span>      | <span data-ttu-id="9cf76-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-143">False</span></span>                                                |
| <span data-ttu-id="9cf76-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9cf76-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cf76-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9cf76-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9cf76-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cf76-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cf76-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-148">Search-Flags</span></span>           | <span data-ttu-id="9cf76-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf76-149">0x00000001</span></span>                                           |
| <span data-ttu-id="9cf76-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-150">System-Flags</span></span>           | <span data-ttu-id="9cf76-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf76-151">0x00000010</span></span>                                           |
| <span data-ttu-id="9cf76-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9cf76-152">Classes used in</span></span>        | [<span data-ttu-id="9cf76-153">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="9cf76-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9cf76-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9cf76-154">Windows Server 2003</span></span>



| <span data-ttu-id="9cf76-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-155">Entry</span></span> | <span data-ttu-id="9cf76-156">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf76-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9cf76-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cf76-159">System-Only</span></span>            | <span data-ttu-id="9cf76-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-160">False</span></span>                                                |
| <span data-ttu-id="9cf76-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9cf76-161">Is-Single-Valued</span></span>       | <span data-ttu-id="9cf76-162">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-162">True</span></span>                                                 |
| <span data-ttu-id="9cf76-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9cf76-163">Is Indexed</span></span>             | <span data-ttu-id="9cf76-164">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-164">True</span></span>                                                 |
| <span data-ttu-id="9cf76-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9cf76-165">In Global Catalog</span></span>      | <span data-ttu-id="9cf76-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-166">False</span></span>                                                |
| <span data-ttu-id="9cf76-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9cf76-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cf76-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9cf76-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9cf76-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cf76-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cf76-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-171">Search-Flags</span></span>           | <span data-ttu-id="9cf76-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf76-172">0x00000001</span></span>                                           |
| <span data-ttu-id="9cf76-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-173">System-Flags</span></span>           | <span data-ttu-id="9cf76-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf76-174">0x00000010</span></span>                                           |
| <span data-ttu-id="9cf76-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9cf76-175">Classes used in</span></span>        | [<span data-ttu-id="9cf76-176">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="9cf76-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9cf76-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9cf76-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9cf76-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-178">Entry</span></span> | <span data-ttu-id="9cf76-179">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf76-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9cf76-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cf76-182">System-Only</span></span>            | <span data-ttu-id="9cf76-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-183">False</span></span>                                                |
| <span data-ttu-id="9cf76-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9cf76-184">Is-Single-Valued</span></span>       | <span data-ttu-id="9cf76-185">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-185">True</span></span>                                                 |
| <span data-ttu-id="9cf76-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9cf76-186">Is Indexed</span></span>             | <span data-ttu-id="9cf76-187">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-187">True</span></span>                                                 |
| <span data-ttu-id="9cf76-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9cf76-188">In Global Catalog</span></span>      | <span data-ttu-id="9cf76-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-189">False</span></span>                                                |
| <span data-ttu-id="9cf76-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9cf76-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cf76-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9cf76-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9cf76-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cf76-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cf76-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-194">Search-Flags</span></span>           | <span data-ttu-id="9cf76-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf76-195">0x00000001</span></span>                                           |
| <span data-ttu-id="9cf76-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-196">System-Flags</span></span>           | <span data-ttu-id="9cf76-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf76-197">0x00000010</span></span>                                           |
| <span data-ttu-id="9cf76-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9cf76-198">Classes used in</span></span>        | [<span data-ttu-id="9cf76-199">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="9cf76-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9cf76-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cf76-200">Windows Server 2008</span></span>



| <span data-ttu-id="9cf76-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-201">Entry</span></span> | <span data-ttu-id="9cf76-202">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf76-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9cf76-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cf76-205">System-Only</span></span>            | <span data-ttu-id="9cf76-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-206">False</span></span>                                                |
| <span data-ttu-id="9cf76-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9cf76-207">Is-Single-Valued</span></span>       | <span data-ttu-id="9cf76-208">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-208">True</span></span>                                                 |
| <span data-ttu-id="9cf76-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9cf76-209">Is Indexed</span></span>             | <span data-ttu-id="9cf76-210">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-210">True</span></span>                                                 |
| <span data-ttu-id="9cf76-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9cf76-211">In Global Catalog</span></span>      | <span data-ttu-id="9cf76-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-212">False</span></span>                                                |
| <span data-ttu-id="9cf76-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9cf76-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cf76-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9cf76-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9cf76-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cf76-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cf76-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-217">Search-Flags</span></span>           | <span data-ttu-id="9cf76-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf76-218">0x00000001</span></span>                                           |
| <span data-ttu-id="9cf76-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-219">System-Flags</span></span>           | <span data-ttu-id="9cf76-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf76-220">0x00000010</span></span>                                           |
| <span data-ttu-id="9cf76-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9cf76-221">Classes used in</span></span>        | [<span data-ttu-id="9cf76-222">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="9cf76-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9cf76-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9cf76-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9cf76-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-224">Entry</span></span> | <span data-ttu-id="9cf76-225">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf76-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9cf76-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cf76-228">System-Only</span></span>            | <span data-ttu-id="9cf76-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-229">False</span></span>                                                |
| <span data-ttu-id="9cf76-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9cf76-230">Is-Single-Valued</span></span>       | <span data-ttu-id="9cf76-231">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-231">True</span></span>                                                 |
| <span data-ttu-id="9cf76-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9cf76-232">Is Indexed</span></span>             | <span data-ttu-id="9cf76-233">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-233">True</span></span>                                                 |
| <span data-ttu-id="9cf76-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9cf76-234">In Global Catalog</span></span>      | <span data-ttu-id="9cf76-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-235">False</span></span>                                                |
| <span data-ttu-id="9cf76-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9cf76-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cf76-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9cf76-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9cf76-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cf76-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cf76-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-240">Search-Flags</span></span>           | <span data-ttu-id="9cf76-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf76-241">0x00000001</span></span>                                           |
| <span data-ttu-id="9cf76-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-242">System-Flags</span></span>           | <span data-ttu-id="9cf76-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf76-243">0x00000010</span></span>                                           |
| <span data-ttu-id="9cf76-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9cf76-244">Classes used in</span></span>        | [<span data-ttu-id="9cf76-245">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="9cf76-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9cf76-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9cf76-246">Windows Server 2012</span></span>



| <span data-ttu-id="9cf76-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="9cf76-247">Entry</span></span> | <span data-ttu-id="9cf76-248">Значение</span><span class="sxs-lookup"><span data-stu-id="9cf76-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="9cf76-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9cf76-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9cf76-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="9cf76-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9cf76-251">System-Only</span></span>            | <span data-ttu-id="9cf76-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-252">False</span></span>                                                |
| <span data-ttu-id="9cf76-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9cf76-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9cf76-254">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-254">True</span></span>                                                 |
| <span data-ttu-id="9cf76-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9cf76-255">Is Indexed</span></span>             | <span data-ttu-id="9cf76-256">True</span><span class="sxs-lookup"><span data-stu-id="9cf76-256">True</span></span>                                                 |
| <span data-ttu-id="9cf76-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9cf76-257">In Global Catalog</span></span>      | <span data-ttu-id="9cf76-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="9cf76-258">False</span></span>                                                |
| <span data-ttu-id="9cf76-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9cf76-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9cf76-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9cf76-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="9cf76-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9cf76-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9cf76-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="9cf76-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-263">Search-Flags</span></span>           | <span data-ttu-id="9cf76-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9cf76-264">0x00000001</span></span>                                           |
| <span data-ttu-id="9cf76-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9cf76-265">System-Flags</span></span>           | <span data-ttu-id="9cf76-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9cf76-266">0x00000010</span></span>                                           |
| <span data-ttu-id="9cf76-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9cf76-267">Classes used in</span></span>        | [<span data-ttu-id="9cf76-268">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="9cf76-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





