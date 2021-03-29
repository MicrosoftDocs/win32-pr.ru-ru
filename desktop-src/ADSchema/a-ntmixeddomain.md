---
title: NT-смешанный атрибут домена
description: Указывает, что домен работает в собственном режиме или в смешанном режиме. Этот атрибут находится в объекте Домаинднс (Head) для домена.
ms.assetid: 49872cbc-844f-4d60-89b6-0150b9116740
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов в смешанных доменах NT
- Схема AD атрибута Нтмикседдомаин
topic_type:
- apiref
api_name:
- NT-Mixed-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d73291f392141b80ca8916b86fffa0055226c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655103"
---
# <a name="nt-mixed-domain-attribute"></a><span data-ttu-id="147c0-106">NT-смешанный атрибут домена</span><span class="sxs-lookup"><span data-stu-id="147c0-106">NT-Mixed-Domain attribute</span></span>

<span data-ttu-id="147c0-107">Указывает, что домен работает в собственном режиме или в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="147c0-107">Indicates that the domain is in native mode or mixed mode.</span></span> <span data-ttu-id="147c0-108">Этот атрибут находится в объекте Домаинднс (Head) для домена.</span><span class="sxs-lookup"><span data-stu-id="147c0-108">This attribute is found in the domainDNS (head) object for the domain.</span></span>



| <span data-ttu-id="147c0-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-109">Entry</span></span> | <span data-ttu-id="147c0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-110">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="147c0-111">CN</span><span class="sxs-lookup"><span data-stu-id="147c0-111">CN</span></span>                | <span data-ttu-id="147c0-112">NT — смешанный домен</span><span class="sxs-lookup"><span data-stu-id="147c0-112">NT-Mixed-Domain</span></span>                       |
| <span data-ttu-id="147c0-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="147c0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="147c0-114">нтмикседдомаин</span><span class="sxs-lookup"><span data-stu-id="147c0-114">nTMixedDomain</span></span>                         |
| <span data-ttu-id="147c0-115">Размер</span><span class="sxs-lookup"><span data-stu-id="147c0-115">Size</span></span>              | <span data-ttu-id="147c0-116">4 байта.</span><span class="sxs-lookup"><span data-stu-id="147c0-116">4 bytes.</span></span> <span data-ttu-id="147c0-117">Смешанный режим 1, собственный режим 0.</span><span class="sxs-lookup"><span data-stu-id="147c0-117">Mixed mode 1, native mode 0.</span></span> |
| <span data-ttu-id="147c0-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="147c0-118">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="147c0-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="147c0-119">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="147c0-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-120">Attribute-Id</span></span>      | <span data-ttu-id="147c0-121">1.2.840.113556.1.4.357</span><span class="sxs-lookup"><span data-stu-id="147c0-121">1.2.840.113556.1.4.357</span></span>                |
| <span data-ttu-id="147c0-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="147c0-122">System-Id-Guid</span></span>    | <span data-ttu-id="147c0-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="147c0-123">3e97891f-8c01-11d0-afda-00c04fd930c9</span></span>  |
| <span data-ttu-id="147c0-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="147c0-124">Syntax</span></span>            | [<span data-ttu-id="147c0-125">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="147c0-125">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="147c0-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="147c0-126">Implementations</span></span>

-   [<span data-ttu-id="147c0-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="147c0-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="147c0-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="147c0-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="147c0-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="147c0-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="147c0-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="147c0-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="147c0-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="147c0-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="147c0-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="147c0-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="147c0-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="147c0-133">Windows 2000 Server</span></span>



| <span data-ttu-id="147c0-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-134">Entry</span></span> | <span data-ttu-id="147c0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-135">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="147c0-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="147c0-136">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="147c0-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-137">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="147c0-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="147c0-138">System-Only</span></span>            | <span data-ttu-id="147c0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-139">False</span></span>                                        |
| <span data-ttu-id="147c0-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="147c0-140">Is-Single-Valued</span></span>       | <span data-ttu-id="147c0-141">True</span><span class="sxs-lookup"><span data-stu-id="147c0-141">True</span></span>                                         |
| <span data-ttu-id="147c0-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="147c0-142">Is Indexed</span></span>             | <span data-ttu-id="147c0-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-143">False</span></span>                                        |
| <span data-ttu-id="147c0-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="147c0-144">In Global Catalog</span></span>      | <span data-ttu-id="147c0-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-145">False</span></span>                                        |
| <span data-ttu-id="147c0-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="147c0-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="147c0-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="147c0-147">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="147c0-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="147c0-148">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="147c0-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="147c0-149">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="147c0-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-150">Search-Flags</span></span>           | <span data-ttu-id="147c0-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="147c0-151">0x00000000</span></span>                                   |
| <span data-ttu-id="147c0-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-152">System-Flags</span></span>           | <span data-ttu-id="147c0-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="147c0-153">0x00000010</span></span>                                   |
| <span data-ttu-id="147c0-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="147c0-154">Classes used in</span></span>        | [<span data-ttu-id="147c0-155">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="147c0-155">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="147c0-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="147c0-156">Windows Server 2003</span></span>



| <span data-ttu-id="147c0-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-157">Entry</span></span> | <span data-ttu-id="147c0-158">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147c0-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="147c0-159">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-160">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="147c0-161">System-Only</span></span>            | <span data-ttu-id="147c0-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-162">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="147c0-163">Is-Single-Valued</span></span>       | <span data-ttu-id="147c0-164">True</span><span class="sxs-lookup"><span data-stu-id="147c0-164">True</span></span>                                                                                    |
| <span data-ttu-id="147c0-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="147c0-165">Is Indexed</span></span>             | <span data-ttu-id="147c0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-166">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="147c0-167">In Global Catalog</span></span>      | <span data-ttu-id="147c0-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-168">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="147c0-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="147c0-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="147c0-170">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="147c0-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="147c0-171">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="147c0-172">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-173">Search-Flags</span></span>           | <span data-ttu-id="147c0-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="147c0-174">0x00000000</span></span>                                                                              |
| <span data-ttu-id="147c0-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-175">System-Flags</span></span>           | <span data-ttu-id="147c0-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="147c0-176">0x00000010</span></span>                                                                              |
| <span data-ttu-id="147c0-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="147c0-177">Classes used in</span></span>        | [<span data-ttu-id="147c0-178">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="147c0-178">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="147c0-179">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="147c0-179">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="147c0-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="147c0-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="147c0-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-181">Entry</span></span> | <span data-ttu-id="147c0-182">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-182">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147c0-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="147c0-183">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-184">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="147c0-185">System-Only</span></span>            | <span data-ttu-id="147c0-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-186">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="147c0-187">Is-Single-Valued</span></span>       | <span data-ttu-id="147c0-188">True</span><span class="sxs-lookup"><span data-stu-id="147c0-188">True</span></span>                                                                                    |
| <span data-ttu-id="147c0-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="147c0-189">Is Indexed</span></span>             | <span data-ttu-id="147c0-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-190">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="147c0-191">In Global Catalog</span></span>      | <span data-ttu-id="147c0-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-192">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="147c0-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="147c0-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="147c0-194">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="147c0-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="147c0-195">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="147c0-196">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-197">Search-Flags</span></span>           | <span data-ttu-id="147c0-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="147c0-198">0x00000000</span></span>                                                                              |
| <span data-ttu-id="147c0-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-199">System-Flags</span></span>           | <span data-ttu-id="147c0-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="147c0-200">0x00000010</span></span>                                                                              |
| <span data-ttu-id="147c0-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="147c0-201">Classes used in</span></span>        | [<span data-ttu-id="147c0-202">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="147c0-202">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="147c0-203">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="147c0-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="147c0-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="147c0-204">Windows Server 2008</span></span>



| <span data-ttu-id="147c0-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-205">Entry</span></span> | <span data-ttu-id="147c0-206">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-206">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147c0-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="147c0-207">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-208">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="147c0-209">System-Only</span></span>            | <span data-ttu-id="147c0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-210">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="147c0-211">Is-Single-Valued</span></span>       | <span data-ttu-id="147c0-212">True</span><span class="sxs-lookup"><span data-stu-id="147c0-212">True</span></span>                                                                                    |
| <span data-ttu-id="147c0-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="147c0-213">Is Indexed</span></span>             | <span data-ttu-id="147c0-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-214">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="147c0-215">In Global Catalog</span></span>      | <span data-ttu-id="147c0-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-216">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="147c0-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="147c0-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="147c0-218">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="147c0-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="147c0-219">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="147c0-220">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-221">Search-Flags</span></span>           | <span data-ttu-id="147c0-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="147c0-222">0x00000000</span></span>                                                                              |
| <span data-ttu-id="147c0-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-223">System-Flags</span></span>           | <span data-ttu-id="147c0-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="147c0-224">0x00000010</span></span>                                                                              |
| <span data-ttu-id="147c0-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="147c0-225">Classes used in</span></span>        | [<span data-ttu-id="147c0-226">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="147c0-226">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="147c0-227">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="147c0-227">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="147c0-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="147c0-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="147c0-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-229">Entry</span></span> | <span data-ttu-id="147c0-230">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-230">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147c0-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="147c0-231">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-232">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="147c0-233">System-Only</span></span>            | <span data-ttu-id="147c0-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-234">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="147c0-235">Is-Single-Valued</span></span>       | <span data-ttu-id="147c0-236">True</span><span class="sxs-lookup"><span data-stu-id="147c0-236">True</span></span>                                                                                    |
| <span data-ttu-id="147c0-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="147c0-237">Is Indexed</span></span>             | <span data-ttu-id="147c0-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-238">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="147c0-239">In Global Catalog</span></span>      | <span data-ttu-id="147c0-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-240">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="147c0-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="147c0-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="147c0-242">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="147c0-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="147c0-243">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="147c0-244">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-245">Search-Flags</span></span>           | <span data-ttu-id="147c0-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="147c0-246">0x00000000</span></span>                                                                              |
| <span data-ttu-id="147c0-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-247">System-Flags</span></span>           | <span data-ttu-id="147c0-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="147c0-248">0x00000010</span></span>                                                                              |
| <span data-ttu-id="147c0-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="147c0-249">Classes used in</span></span>        | [<span data-ttu-id="147c0-250">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="147c0-250">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="147c0-251">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="147c0-251">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="147c0-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="147c0-252">Windows Server 2012</span></span>



| <span data-ttu-id="147c0-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="147c0-253">Entry</span></span> | <span data-ttu-id="147c0-254">Значение</span><span class="sxs-lookup"><span data-stu-id="147c0-254">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="147c0-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="147c0-255">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="147c0-256">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="147c0-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="147c0-257">System-Only</span></span>            | <span data-ttu-id="147c0-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-258">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="147c0-259">Is-Single-Valued</span></span>       | <span data-ttu-id="147c0-260">True</span><span class="sxs-lookup"><span data-stu-id="147c0-260">True</span></span>                                                                                    |
| <span data-ttu-id="147c0-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="147c0-261">Is Indexed</span></span>             | <span data-ttu-id="147c0-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-262">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="147c0-263">In Global Catalog</span></span>      | <span data-ttu-id="147c0-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="147c0-264">False</span></span>                                                                                   |
| <span data-ttu-id="147c0-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="147c0-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="147c0-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="147c0-266">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="147c0-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="147c0-267">Range-Lower</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="147c0-268">Range-Upper</span></span>            | \-                                                                                      |
| <span data-ttu-id="147c0-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-269">Search-Flags</span></span>           | <span data-ttu-id="147c0-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="147c0-270">0x00000000</span></span>                                                                              |
| <span data-ttu-id="147c0-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="147c0-271">System-Flags</span></span>           | <span data-ttu-id="147c0-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="147c0-272">0x00000010</span></span>                                                                              |
| <span data-ttu-id="147c0-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="147c0-273">Classes used in</span></span>        | [<span data-ttu-id="147c0-274">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="147c0-274">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="147c0-275">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="147c0-275">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





