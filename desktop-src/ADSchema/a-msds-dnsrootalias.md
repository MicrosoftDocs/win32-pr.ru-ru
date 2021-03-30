---
title: Атрибут ms-DS-Днсруталиас
description: Используется для хранения псевдонима домена.
ms.assetid: 36b64363-947f-4af9-947f-eefead55bb02
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-Днсруталиас
- Схема AD атрибута msDS-Днсруталиас
topic_type:
- apiref
api_name:
- ms-DS-DnsRootAlias
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f0b20b9316aaa9e68ab1ed907135c5640c1480f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805027"
---
# <a name="ms-ds-dnsrootalias-attribute"></a><span data-ttu-id="6bd07-105">Атрибут ms-DS-Днсруталиас</span><span class="sxs-lookup"><span data-stu-id="6bd07-105">ms-DS-DnsRootAlias attribute</span></span>

<span data-ttu-id="6bd07-106">Используется для хранения псевдонима домена.</span><span class="sxs-lookup"><span data-stu-id="6bd07-106">Used to store the domain alias.</span></span>



| <span data-ttu-id="6bd07-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-107">Entry</span></span> | <span data-ttu-id="6bd07-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="6bd07-109">CN</span><span class="sxs-lookup"><span data-stu-id="6bd07-109">CN</span></span>                | <span data-ttu-id="6bd07-110">MS-DS-Днсруталиас</span><span class="sxs-lookup"><span data-stu-id="6bd07-110">ms-DS-DnsRootAlias</span></span>                          |
| <span data-ttu-id="6bd07-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6bd07-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6bd07-112">msDS-Днсруталиас</span><span class="sxs-lookup"><span data-stu-id="6bd07-112">msDS-DnsRootAlias</span></span>                           |
| <span data-ttu-id="6bd07-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6bd07-113">Size</span></span>              | <span data-ttu-id="6bd07-114">Максимальный размер 255 байт.</span><span class="sxs-lookup"><span data-stu-id="6bd07-114">Maximum size 255 bytes.</span></span>                     |
| <span data-ttu-id="6bd07-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6bd07-115">Update Privilege</span></span>  | <span data-ttu-id="6bd07-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="6bd07-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="6bd07-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6bd07-117">Update Frequency</span></span>  | <span data-ttu-id="6bd07-118">Только во время реструктуризации домена.</span><span class="sxs-lookup"><span data-stu-id="6bd07-118">Only during domain restructure.</span></span>             |
| <span data-ttu-id="6bd07-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-119">Attribute-Id</span></span>      | <span data-ttu-id="6bd07-120">1.2.840.113556.1.4.1719</span><span class="sxs-lookup"><span data-stu-id="6bd07-120">1.2.840.113556.1.4.1719</span></span>                     |
| <span data-ttu-id="6bd07-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6bd07-121">System-Id-Guid</span></span>    | <span data-ttu-id="6bd07-122">2143acca-eead-4d29-b591-85fa49ce9173</span><span class="sxs-lookup"><span data-stu-id="6bd07-122">2143acca-eead-4d29-b591-85fa49ce9173</span></span>        |
| <span data-ttu-id="6bd07-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bd07-123">Syntax</span></span>            | [<span data-ttu-id="6bd07-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6bd07-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="6bd07-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6bd07-125">Implementations</span></span>

-   [<span data-ttu-id="6bd07-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6bd07-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6bd07-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6bd07-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="6bd07-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6bd07-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6bd07-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6bd07-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6bd07-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6bd07-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6bd07-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6bd07-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="6bd07-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6bd07-132">Windows Server 2003</span></span>



| <span data-ttu-id="6bd07-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-133">Entry</span></span> | <span data-ttu-id="6bd07-134">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-134">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="6bd07-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6bd07-135">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-136">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="6bd07-137">System-Only</span></span>            | <span data-ttu-id="6bd07-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-138">False</span></span>                                      |
| <span data-ttu-id="6bd07-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6bd07-139">Is-Single-Valued</span></span>       | <span data-ttu-id="6bd07-140">True</span><span class="sxs-lookup"><span data-stu-id="6bd07-140">True</span></span>                                       |
| <span data-ttu-id="6bd07-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6bd07-141">Is Indexed</span></span>             | <span data-ttu-id="6bd07-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-142">False</span></span>                                      |
| <span data-ttu-id="6bd07-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6bd07-143">In Global Catalog</span></span>      | <span data-ttu-id="6bd07-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-144">False</span></span>                                      |
| <span data-ttu-id="6bd07-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6bd07-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="6bd07-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6bd07-146">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="6bd07-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6bd07-147">Range-Lower</span></span>            | <span data-ttu-id="6bd07-148">0</span><span class="sxs-lookup"><span data-stu-id="6bd07-148">0</span></span>                                          |
| <span data-ttu-id="6bd07-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6bd07-149">Range-Upper</span></span>            | <span data-ttu-id="6bd07-150">255</span><span class="sxs-lookup"><span data-stu-id="6bd07-150">255</span></span>                                        |
| <span data-ttu-id="6bd07-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-151">Search-Flags</span></span>           | <span data-ttu-id="6bd07-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6bd07-152">0x00000000</span></span>                                 |
| <span data-ttu-id="6bd07-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-153">System-Flags</span></span>           | <span data-ttu-id="6bd07-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6bd07-154">0x00000010</span></span>                                 |
| <span data-ttu-id="6bd07-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6bd07-155">Classes used in</span></span>        | [<span data-ttu-id="6bd07-156">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="6bd07-156">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="6bd07-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="6bd07-157">ADAM</span></span>



| <span data-ttu-id="6bd07-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-158">Entry</span></span> | <span data-ttu-id="6bd07-159">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-159">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="6bd07-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6bd07-160">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-161">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="6bd07-162">System-Only</span></span>            | <span data-ttu-id="6bd07-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-163">False</span></span>                                      |
| <span data-ttu-id="6bd07-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6bd07-164">Is-Single-Valued</span></span>       | <span data-ttu-id="6bd07-165">True</span><span class="sxs-lookup"><span data-stu-id="6bd07-165">True</span></span>                                       |
| <span data-ttu-id="6bd07-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6bd07-166">Is Indexed</span></span>             | <span data-ttu-id="6bd07-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-167">False</span></span>                                      |
| <span data-ttu-id="6bd07-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6bd07-168">In Global Catalog</span></span>      | <span data-ttu-id="6bd07-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-169">False</span></span>                                      |
| <span data-ttu-id="6bd07-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6bd07-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="6bd07-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6bd07-171">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="6bd07-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6bd07-172">Range-Lower</span></span>            | <span data-ttu-id="6bd07-173">0</span><span class="sxs-lookup"><span data-stu-id="6bd07-173">0</span></span>                                          |
| <span data-ttu-id="6bd07-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6bd07-174">Range-Upper</span></span>            | <span data-ttu-id="6bd07-175">255</span><span class="sxs-lookup"><span data-stu-id="6bd07-175">255</span></span>                                        |
| <span data-ttu-id="6bd07-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-176">Search-Flags</span></span>           | <span data-ttu-id="6bd07-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6bd07-177">0x00000000</span></span>                                 |
| <span data-ttu-id="6bd07-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-178">System-Flags</span></span>           | <span data-ttu-id="6bd07-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6bd07-179">0x00000010</span></span>                                 |
| <span data-ttu-id="6bd07-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6bd07-180">Classes used in</span></span>        | [<span data-ttu-id="6bd07-181">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="6bd07-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6bd07-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6bd07-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6bd07-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-183">Entry</span></span> | <span data-ttu-id="6bd07-184">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-184">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="6bd07-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6bd07-185">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-186">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="6bd07-187">System-Only</span></span>            | <span data-ttu-id="6bd07-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-188">False</span></span>                                      |
| <span data-ttu-id="6bd07-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6bd07-189">Is-Single-Valued</span></span>       | <span data-ttu-id="6bd07-190">True</span><span class="sxs-lookup"><span data-stu-id="6bd07-190">True</span></span>                                       |
| <span data-ttu-id="6bd07-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6bd07-191">Is Indexed</span></span>             | <span data-ttu-id="6bd07-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-192">False</span></span>                                      |
| <span data-ttu-id="6bd07-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6bd07-193">In Global Catalog</span></span>      | <span data-ttu-id="6bd07-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-194">False</span></span>                                      |
| <span data-ttu-id="6bd07-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6bd07-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="6bd07-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6bd07-196">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="6bd07-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6bd07-197">Range-Lower</span></span>            | <span data-ttu-id="6bd07-198">0</span><span class="sxs-lookup"><span data-stu-id="6bd07-198">0</span></span>                                          |
| <span data-ttu-id="6bd07-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6bd07-199">Range-Upper</span></span>            | <span data-ttu-id="6bd07-200">255</span><span class="sxs-lookup"><span data-stu-id="6bd07-200">255</span></span>                                        |
| <span data-ttu-id="6bd07-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-201">Search-Flags</span></span>           | <span data-ttu-id="6bd07-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6bd07-202">0x00000000</span></span>                                 |
| <span data-ttu-id="6bd07-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-203">System-Flags</span></span>           | <span data-ttu-id="6bd07-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6bd07-204">0x00000010</span></span>                                 |
| <span data-ttu-id="6bd07-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6bd07-205">Classes used in</span></span>        | [<span data-ttu-id="6bd07-206">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="6bd07-206">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6bd07-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bd07-207">Windows Server 2008</span></span>



| <span data-ttu-id="6bd07-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-208">Entry</span></span> | <span data-ttu-id="6bd07-209">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-209">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="6bd07-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6bd07-210">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-211">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="6bd07-212">System-Only</span></span>            | <span data-ttu-id="6bd07-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-213">False</span></span>                                      |
| <span data-ttu-id="6bd07-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6bd07-214">Is-Single-Valued</span></span>       | <span data-ttu-id="6bd07-215">True</span><span class="sxs-lookup"><span data-stu-id="6bd07-215">True</span></span>                                       |
| <span data-ttu-id="6bd07-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6bd07-216">Is Indexed</span></span>             | <span data-ttu-id="6bd07-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-217">False</span></span>                                      |
| <span data-ttu-id="6bd07-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6bd07-218">In Global Catalog</span></span>      | <span data-ttu-id="6bd07-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-219">False</span></span>                                      |
| <span data-ttu-id="6bd07-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6bd07-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="6bd07-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6bd07-221">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="6bd07-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6bd07-222">Range-Lower</span></span>            | <span data-ttu-id="6bd07-223">0</span><span class="sxs-lookup"><span data-stu-id="6bd07-223">0</span></span>                                          |
| <span data-ttu-id="6bd07-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6bd07-224">Range-Upper</span></span>            | <span data-ttu-id="6bd07-225">255</span><span class="sxs-lookup"><span data-stu-id="6bd07-225">255</span></span>                                        |
| <span data-ttu-id="6bd07-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-226">Search-Flags</span></span>           | <span data-ttu-id="6bd07-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6bd07-227">0x00000000</span></span>                                 |
| <span data-ttu-id="6bd07-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-228">System-Flags</span></span>           | <span data-ttu-id="6bd07-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6bd07-229">0x00000010</span></span>                                 |
| <span data-ttu-id="6bd07-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6bd07-230">Classes used in</span></span>        | [<span data-ttu-id="6bd07-231">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="6bd07-231">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6bd07-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6bd07-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6bd07-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-233">Entry</span></span> | <span data-ttu-id="6bd07-234">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-234">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="6bd07-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6bd07-235">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-236">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="6bd07-237">System-Only</span></span>            | <span data-ttu-id="6bd07-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-238">False</span></span>                                      |
| <span data-ttu-id="6bd07-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6bd07-239">Is-Single-Valued</span></span>       | <span data-ttu-id="6bd07-240">True</span><span class="sxs-lookup"><span data-stu-id="6bd07-240">True</span></span>                                       |
| <span data-ttu-id="6bd07-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6bd07-241">Is Indexed</span></span>             | <span data-ttu-id="6bd07-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-242">False</span></span>                                      |
| <span data-ttu-id="6bd07-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6bd07-243">In Global Catalog</span></span>      | <span data-ttu-id="6bd07-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-244">False</span></span>                                      |
| <span data-ttu-id="6bd07-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6bd07-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="6bd07-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6bd07-246">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="6bd07-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6bd07-247">Range-Lower</span></span>            | <span data-ttu-id="6bd07-248">0</span><span class="sxs-lookup"><span data-stu-id="6bd07-248">0</span></span>                                          |
| <span data-ttu-id="6bd07-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6bd07-249">Range-Upper</span></span>            | <span data-ttu-id="6bd07-250">255</span><span class="sxs-lookup"><span data-stu-id="6bd07-250">255</span></span>                                        |
| <span data-ttu-id="6bd07-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-251">Search-Flags</span></span>           | <span data-ttu-id="6bd07-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6bd07-252">0x00000000</span></span>                                 |
| <span data-ttu-id="6bd07-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-253">System-Flags</span></span>           | <span data-ttu-id="6bd07-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6bd07-254">0x00000010</span></span>                                 |
| <span data-ttu-id="6bd07-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6bd07-255">Classes used in</span></span>        | [<span data-ttu-id="6bd07-256">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="6bd07-256">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6bd07-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6bd07-257">Windows Server 2012</span></span>



| <span data-ttu-id="6bd07-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="6bd07-258">Entry</span></span> | <span data-ttu-id="6bd07-259">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd07-259">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="6bd07-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6bd07-260">Link-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6bd07-261">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="6bd07-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="6bd07-262">System-Only</span></span>            | <span data-ttu-id="6bd07-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-263">False</span></span>                                      |
| <span data-ttu-id="6bd07-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6bd07-264">Is-Single-Valued</span></span>       | <span data-ttu-id="6bd07-265">True</span><span class="sxs-lookup"><span data-stu-id="6bd07-265">True</span></span>                                       |
| <span data-ttu-id="6bd07-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6bd07-266">Is Indexed</span></span>             | <span data-ttu-id="6bd07-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-267">False</span></span>                                      |
| <span data-ttu-id="6bd07-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6bd07-268">In Global Catalog</span></span>      | <span data-ttu-id="6bd07-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="6bd07-269">False</span></span>                                      |
| <span data-ttu-id="6bd07-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6bd07-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="6bd07-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6bd07-271">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="6bd07-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6bd07-272">Range-Lower</span></span>            | <span data-ttu-id="6bd07-273">0</span><span class="sxs-lookup"><span data-stu-id="6bd07-273">0</span></span>                                          |
| <span data-ttu-id="6bd07-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6bd07-274">Range-Upper</span></span>            | <span data-ttu-id="6bd07-275">255</span><span class="sxs-lookup"><span data-stu-id="6bd07-275">255</span></span>                                        |
| <span data-ttu-id="6bd07-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-276">Search-Flags</span></span>           | <span data-ttu-id="6bd07-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6bd07-277">0x00000000</span></span>                                 |
| <span data-ttu-id="6bd07-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6bd07-278">System-Flags</span></span>           | <span data-ttu-id="6bd07-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6bd07-279">0x00000010</span></span>                                 |
| <span data-ttu-id="6bd07-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6bd07-280">Classes used in</span></span>        | [<span data-ttu-id="6bd07-281">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="6bd07-281">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





