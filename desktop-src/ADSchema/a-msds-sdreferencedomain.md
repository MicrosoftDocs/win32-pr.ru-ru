---
title: Атрибут ms-DS-SD-Reference-domain
description: Имя домена, используемого для преобразования дескрипторов безопасности для контекста, не являющегося доменом.
ms.assetid: 5e0591e8-bf2a-4788-867e-c15c35b35a14
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута домена MS-DS-SD-Reference
- Схема AD атрибута msDS-Сдреференцедомаин
topic_type:
- apiref
api_name:
- ms-DS-SD-Reference-Domain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df717205937bc50c394835f2e3c00f182b8ab91
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138942"
---
# <a name="ms-ds-sd-reference-domain-attribute"></a><span data-ttu-id="18c73-105">Атрибут ms-DS-SD-Reference-domain</span><span class="sxs-lookup"><span data-stu-id="18c73-105">ms-DS-SD-Reference-Domain attribute</span></span>

<span data-ttu-id="18c73-106">Имя домена, используемого для преобразования дескрипторов безопасности для контекста, не являющегося доменом.</span><span class="sxs-lookup"><span data-stu-id="18c73-106">The name of the domain to be used for security descriptor translation for a non-domain-naming context.</span></span>



| <span data-ttu-id="18c73-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-107">Entry</span></span> | <span data-ttu-id="18c73-108">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="18c73-109">CN</span><span class="sxs-lookup"><span data-stu-id="18c73-109">CN</span></span>                | <span data-ttu-id="18c73-110">MS-DS-SD-Reference-domain</span><span class="sxs-lookup"><span data-stu-id="18c73-110">ms-DS-SD-Reference-Domain</span></span>               |
| <span data-ttu-id="18c73-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="18c73-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18c73-112">msDS-Сдреференцедомаин</span><span class="sxs-lookup"><span data-stu-id="18c73-112">msDS-SDReferenceDomain</span></span>                  |
| <span data-ttu-id="18c73-113">Размер</span><span class="sxs-lookup"><span data-stu-id="18c73-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="18c73-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="18c73-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="18c73-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="18c73-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="18c73-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-116">Attribute-Id</span></span>      | <span data-ttu-id="18c73-117">1.2.840.113556.1.4.1711</span><span class="sxs-lookup"><span data-stu-id="18c73-117">1.2.840.113556.1.4.1711</span></span>                 |
| <span data-ttu-id="18c73-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="18c73-118">System-Id-Guid</span></span>    | <span data-ttu-id="18c73-119">4c51e316-f628-43a5-b06b-ffb695fcb4f3</span><span class="sxs-lookup"><span data-stu-id="18c73-119">4c51e316-f628-43a5-b06b-ffb695fcb4f3</span></span>    |
| <span data-ttu-id="18c73-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18c73-120">Syntax</span></span>            | [<span data-ttu-id="18c73-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="18c73-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="18c73-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="18c73-122">Implementations</span></span>

-   [<span data-ttu-id="18c73-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18c73-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18c73-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="18c73-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="18c73-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18c73-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18c73-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18c73-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18c73-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18c73-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18c73-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18c73-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="18c73-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18c73-129">Windows Server 2003</span></span>



| <span data-ttu-id="18c73-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-130">Entry</span></span> | <span data-ttu-id="18c73-131">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-131">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="18c73-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18c73-132">Link-Id</span></span>                | <span data-ttu-id="18c73-133">2000</span><span class="sxs-lookup"><span data-stu-id="18c73-133">2000</span></span>                                       |
| <span data-ttu-id="18c73-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-134">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="18c73-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="18c73-135">System-Only</span></span>            | <span data-ttu-id="18c73-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-136">False</span></span>                                      |
| <span data-ttu-id="18c73-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18c73-137">Is-Single-Valued</span></span>       | <span data-ttu-id="18c73-138">True</span><span class="sxs-lookup"><span data-stu-id="18c73-138">True</span></span>                                       |
| <span data-ttu-id="18c73-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18c73-139">Is Indexed</span></span>             | <span data-ttu-id="18c73-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-140">False</span></span>                                      |
| <span data-ttu-id="18c73-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18c73-141">In Global Catalog</span></span>      | <span data-ttu-id="18c73-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-142">False</span></span>                                      |
| <span data-ttu-id="18c73-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18c73-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="18c73-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18c73-144">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="18c73-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18c73-145">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="18c73-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18c73-146">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="18c73-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-147">Search-Flags</span></span>           | <span data-ttu-id="18c73-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18c73-148">0x00000000</span></span>                                 |
| <span data-ttu-id="18c73-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-149">System-Flags</span></span>           | <span data-ttu-id="18c73-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18c73-150">0x00000010</span></span>                                 |
| <span data-ttu-id="18c73-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18c73-151">Classes used in</span></span>        | [<span data-ttu-id="18c73-152">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="18c73-152">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="adam"></a><span data-ttu-id="18c73-153">ADAM</span><span class="sxs-lookup"><span data-stu-id="18c73-153">ADAM</span></span>



| <span data-ttu-id="18c73-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-154">Entry</span></span> | <span data-ttu-id="18c73-155">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-155">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="18c73-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18c73-156">Link-Id</span></span>                | <span data-ttu-id="18c73-157">2000</span><span class="sxs-lookup"><span data-stu-id="18c73-157">2000</span></span>                                       |
| <span data-ttu-id="18c73-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-158">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="18c73-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="18c73-159">System-Only</span></span>            | <span data-ttu-id="18c73-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-160">False</span></span>                                      |
| <span data-ttu-id="18c73-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18c73-161">Is-Single-Valued</span></span>       | <span data-ttu-id="18c73-162">True</span><span class="sxs-lookup"><span data-stu-id="18c73-162">True</span></span>                                       |
| <span data-ttu-id="18c73-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18c73-163">Is Indexed</span></span>             | <span data-ttu-id="18c73-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-164">False</span></span>                                      |
| <span data-ttu-id="18c73-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18c73-165">In Global Catalog</span></span>      | <span data-ttu-id="18c73-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-166">False</span></span>                                      |
| <span data-ttu-id="18c73-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18c73-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="18c73-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18c73-168">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="18c73-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18c73-169">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="18c73-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18c73-170">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="18c73-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-171">Search-Flags</span></span>           | <span data-ttu-id="18c73-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18c73-172">0x00000000</span></span>                                 |
| <span data-ttu-id="18c73-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-173">System-Flags</span></span>           | <span data-ttu-id="18c73-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18c73-174">0x00000010</span></span>                                 |
| <span data-ttu-id="18c73-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18c73-175">Classes used in</span></span>        | [<span data-ttu-id="18c73-176">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="18c73-176">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18c73-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18c73-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18c73-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-178">Entry</span></span> | <span data-ttu-id="18c73-179">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-179">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="18c73-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18c73-180">Link-Id</span></span>                | <span data-ttu-id="18c73-181">2000</span><span class="sxs-lookup"><span data-stu-id="18c73-181">2000</span></span>                                       |
| <span data-ttu-id="18c73-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-182">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="18c73-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="18c73-183">System-Only</span></span>            | <span data-ttu-id="18c73-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-184">False</span></span>                                      |
| <span data-ttu-id="18c73-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18c73-185">Is-Single-Valued</span></span>       | <span data-ttu-id="18c73-186">True</span><span class="sxs-lookup"><span data-stu-id="18c73-186">True</span></span>                                       |
| <span data-ttu-id="18c73-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18c73-187">Is Indexed</span></span>             | <span data-ttu-id="18c73-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-188">False</span></span>                                      |
| <span data-ttu-id="18c73-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18c73-189">In Global Catalog</span></span>      | <span data-ttu-id="18c73-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-190">False</span></span>                                      |
| <span data-ttu-id="18c73-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18c73-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="18c73-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18c73-192">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="18c73-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18c73-193">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="18c73-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18c73-194">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="18c73-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-195">Search-Flags</span></span>           | <span data-ttu-id="18c73-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18c73-196">0x00000000</span></span>                                 |
| <span data-ttu-id="18c73-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-197">System-Flags</span></span>           | <span data-ttu-id="18c73-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18c73-198">0x00000010</span></span>                                 |
| <span data-ttu-id="18c73-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18c73-199">Classes used in</span></span>        | [<span data-ttu-id="18c73-200">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="18c73-200">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18c73-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18c73-201">Windows Server 2008</span></span>



| <span data-ttu-id="18c73-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-202">Entry</span></span> | <span data-ttu-id="18c73-203">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-203">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="18c73-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18c73-204">Link-Id</span></span>                | <span data-ttu-id="18c73-205">2000</span><span class="sxs-lookup"><span data-stu-id="18c73-205">2000</span></span>                                       |
| <span data-ttu-id="18c73-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-206">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="18c73-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="18c73-207">System-Only</span></span>            | <span data-ttu-id="18c73-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-208">False</span></span>                                      |
| <span data-ttu-id="18c73-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18c73-209">Is-Single-Valued</span></span>       | <span data-ttu-id="18c73-210">True</span><span class="sxs-lookup"><span data-stu-id="18c73-210">True</span></span>                                       |
| <span data-ttu-id="18c73-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18c73-211">Is Indexed</span></span>             | <span data-ttu-id="18c73-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-212">False</span></span>                                      |
| <span data-ttu-id="18c73-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18c73-213">In Global Catalog</span></span>      | <span data-ttu-id="18c73-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-214">False</span></span>                                      |
| <span data-ttu-id="18c73-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18c73-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="18c73-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18c73-216">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="18c73-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18c73-217">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="18c73-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18c73-218">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="18c73-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-219">Search-Flags</span></span>           | <span data-ttu-id="18c73-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18c73-220">0x00000000</span></span>                                 |
| <span data-ttu-id="18c73-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-221">System-Flags</span></span>           | <span data-ttu-id="18c73-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18c73-222">0x00000010</span></span>                                 |
| <span data-ttu-id="18c73-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18c73-223">Classes used in</span></span>        | [<span data-ttu-id="18c73-224">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="18c73-224">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18c73-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18c73-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18c73-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-226">Entry</span></span> | <span data-ttu-id="18c73-227">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-227">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="18c73-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18c73-228">Link-Id</span></span>                | <span data-ttu-id="18c73-229">2000</span><span class="sxs-lookup"><span data-stu-id="18c73-229">2000</span></span>                                       |
| <span data-ttu-id="18c73-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-230">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="18c73-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="18c73-231">System-Only</span></span>            | <span data-ttu-id="18c73-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-232">False</span></span>                                      |
| <span data-ttu-id="18c73-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18c73-233">Is-Single-Valued</span></span>       | <span data-ttu-id="18c73-234">True</span><span class="sxs-lookup"><span data-stu-id="18c73-234">True</span></span>                                       |
| <span data-ttu-id="18c73-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18c73-235">Is Indexed</span></span>             | <span data-ttu-id="18c73-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-236">False</span></span>                                      |
| <span data-ttu-id="18c73-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18c73-237">In Global Catalog</span></span>      | <span data-ttu-id="18c73-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-238">False</span></span>                                      |
| <span data-ttu-id="18c73-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18c73-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="18c73-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18c73-240">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="18c73-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18c73-241">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="18c73-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18c73-242">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="18c73-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-243">Search-Flags</span></span>           | <span data-ttu-id="18c73-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18c73-244">0x00000000</span></span>                                 |
| <span data-ttu-id="18c73-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-245">System-Flags</span></span>           | <span data-ttu-id="18c73-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18c73-246">0x00000010</span></span>                                 |
| <span data-ttu-id="18c73-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18c73-247">Classes used in</span></span>        | [<span data-ttu-id="18c73-248">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="18c73-248">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18c73-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18c73-249">Windows Server 2012</span></span>



| <span data-ttu-id="18c73-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="18c73-250">Entry</span></span> | <span data-ttu-id="18c73-251">Значение</span><span class="sxs-lookup"><span data-stu-id="18c73-251">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="18c73-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18c73-252">Link-Id</span></span>                | <span data-ttu-id="18c73-253">2000</span><span class="sxs-lookup"><span data-stu-id="18c73-253">2000</span></span>                                       |
| <span data-ttu-id="18c73-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18c73-254">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="18c73-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="18c73-255">System-Only</span></span>            | <span data-ttu-id="18c73-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-256">False</span></span>                                      |
| <span data-ttu-id="18c73-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18c73-257">Is-Single-Valued</span></span>       | <span data-ttu-id="18c73-258">True</span><span class="sxs-lookup"><span data-stu-id="18c73-258">True</span></span>                                       |
| <span data-ttu-id="18c73-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18c73-259">Is Indexed</span></span>             | <span data-ttu-id="18c73-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-260">False</span></span>                                      |
| <span data-ttu-id="18c73-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18c73-261">In Global Catalog</span></span>      | <span data-ttu-id="18c73-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="18c73-262">False</span></span>                                      |
| <span data-ttu-id="18c73-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18c73-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="18c73-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18c73-264">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="18c73-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18c73-265">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="18c73-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18c73-266">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="18c73-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-267">Search-Flags</span></span>           | <span data-ttu-id="18c73-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18c73-268">0x00000000</span></span>                                 |
| <span data-ttu-id="18c73-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18c73-269">System-Flags</span></span>           | <span data-ttu-id="18c73-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18c73-270">0x00000010</span></span>                                 |
| <span data-ttu-id="18c73-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18c73-271">Classes used in</span></span>        | [<span data-ttu-id="18c73-272">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="18c73-272">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





