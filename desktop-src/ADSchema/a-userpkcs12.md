---
title: атрибут userPKCS12
description: PDU PKCS \ 12 PFX для обмена личной идентификационной информацией.
ms.assetid: dbc35a0f-c42d-4d1d-8ac6-5eca997af0fe
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута userPKCS12
topic_type:
- apiref
api_name:
- userPKCS12
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8493bf46bc41d062f254f6e7d50331ed22dec25
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072093"
---
# <a name="userpkcs12-attribute"></a><span data-ttu-id="09658-104">атрибут userPKCS12</span><span class="sxs-lookup"><span data-stu-id="09658-104">userPKCS12 attribute</span></span>

<span data-ttu-id="09658-105">\#PDU PKCS 12 PFX для обмена идентификационными данными личного удостоверения.</span><span class="sxs-lookup"><span data-stu-id="09658-105">PKCS \#12 PFX PDU for exchange of personal identity information.</span></span>



| <span data-ttu-id="09658-106">Ввод</span><span class="sxs-lookup"><span data-stu-id="09658-106">Entry</span></span> | <span data-ttu-id="09658-107">Значение</span><span class="sxs-lookup"><span data-stu-id="09658-107">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="09658-108">CN</span><span class="sxs-lookup"><span data-stu-id="09658-108">CN</span></span>                | <span data-ttu-id="09658-109">userPKCS12</span><span class="sxs-lookup"><span data-stu-id="09658-109">userPKCS12</span></span>                                            |
| <span data-ttu-id="09658-110">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="09658-110">Ldap-Display-Name</span></span> | <span data-ttu-id="09658-111">userPKCS12</span><span class="sxs-lookup"><span data-stu-id="09658-111">userPKCS12</span></span>                                            |
| <span data-ttu-id="09658-112">Размер</span><span class="sxs-lookup"><span data-stu-id="09658-112">Size</span></span>              | \-                                                    |
| <span data-ttu-id="09658-113">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="09658-113">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="09658-114">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="09658-114">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="09658-115">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09658-115">Attribute-Id</span></span>      | <span data-ttu-id="09658-116">2.16.840.1.113730.3.1.216</span><span class="sxs-lookup"><span data-stu-id="09658-116">2.16.840.1.113730.3.1.216</span></span>                             |
| <span data-ttu-id="09658-117">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="09658-117">System-Id-Guid</span></span>    | <span data-ttu-id="09658-118">23998ab5-70f8-4007-a4c1-a84a38311f9a</span><span class="sxs-lookup"><span data-stu-id="09658-118">23998ab5-70f8-4007-a4c1-a84a38311f9a</span></span>                  |
| <span data-ttu-id="09658-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09658-119">Syntax</span></span>            | [<span data-ttu-id="09658-120">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="09658-120">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="09658-121">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="09658-121">Implementations</span></span>

-   [<span data-ttu-id="09658-122">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09658-122">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09658-123">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09658-123">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09658-124">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09658-124">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09658-125">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09658-125">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09658-126">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09658-126">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="09658-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09658-127">Windows Server 2003</span></span>



| <span data-ttu-id="09658-128">Ввод</span><span class="sxs-lookup"><span data-stu-id="09658-128">Entry</span></span> | <span data-ttu-id="09658-129">Значение</span><span class="sxs-lookup"><span data-stu-id="09658-129">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09658-130">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09658-130">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09658-131">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="09658-132">System-Only</span></span>            | <span data-ttu-id="09658-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-133">False</span></span>                                                                                 |
| <span data-ttu-id="09658-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09658-134">Is-Single-Valued</span></span>       | <span data-ttu-id="09658-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-135">False</span></span>                                                                                 |
| <span data-ttu-id="09658-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09658-136">Is Indexed</span></span>             | <span data-ttu-id="09658-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-137">False</span></span>                                                                                 |
| <span data-ttu-id="09658-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09658-138">In Global Catalog</span></span>      | <span data-ttu-id="09658-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-139">False</span></span>                                                                                 |
| <span data-ttu-id="09658-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09658-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="09658-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09658-141">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="09658-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09658-142">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09658-143">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-144">Search-Flags</span></span>           | <span data-ttu-id="09658-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-145">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-146">System-Flags</span></span>           | <span data-ttu-id="09658-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-147">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09658-148">Classes used in</span></span>        | [<span data-ttu-id="09658-149">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="09658-149">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="09658-150">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="09658-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09658-151">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09658-151">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09658-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="09658-152">Entry</span></span> | <span data-ttu-id="09658-153">Значение</span><span class="sxs-lookup"><span data-stu-id="09658-153">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09658-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09658-154">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09658-155">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="09658-156">System-Only</span></span>            | <span data-ttu-id="09658-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-157">False</span></span>                                                                                 |
| <span data-ttu-id="09658-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09658-158">Is-Single-Valued</span></span>       | <span data-ttu-id="09658-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-159">False</span></span>                                                                                 |
| <span data-ttu-id="09658-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09658-160">Is Indexed</span></span>             | <span data-ttu-id="09658-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-161">False</span></span>                                                                                 |
| <span data-ttu-id="09658-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09658-162">In Global Catalog</span></span>      | <span data-ttu-id="09658-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-163">False</span></span>                                                                                 |
| <span data-ttu-id="09658-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09658-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="09658-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09658-165">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="09658-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09658-166">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09658-167">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-168">Search-Flags</span></span>           | <span data-ttu-id="09658-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-169">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-170">System-Flags</span></span>           | <span data-ttu-id="09658-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-171">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09658-172">Classes used in</span></span>        | [<span data-ttu-id="09658-173">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="09658-173">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="09658-174">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="09658-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09658-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09658-175">Windows Server 2008</span></span>



| <span data-ttu-id="09658-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="09658-176">Entry</span></span> | <span data-ttu-id="09658-177">Значение</span><span class="sxs-lookup"><span data-stu-id="09658-177">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09658-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09658-178">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09658-179">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="09658-180">System-Only</span></span>            | <span data-ttu-id="09658-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-181">False</span></span>                                                                                 |
| <span data-ttu-id="09658-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09658-182">Is-Single-Valued</span></span>       | <span data-ttu-id="09658-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-183">False</span></span>                                                                                 |
| <span data-ttu-id="09658-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09658-184">Is Indexed</span></span>             | <span data-ttu-id="09658-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-185">False</span></span>                                                                                 |
| <span data-ttu-id="09658-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09658-186">In Global Catalog</span></span>      | <span data-ttu-id="09658-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-187">False</span></span>                                                                                 |
| <span data-ttu-id="09658-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09658-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="09658-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09658-189">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="09658-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09658-190">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09658-191">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-192">Search-Flags</span></span>           | <span data-ttu-id="09658-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-193">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-194">System-Flags</span></span>           | <span data-ttu-id="09658-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-195">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09658-196">Classes used in</span></span>        | [<span data-ttu-id="09658-197">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="09658-197">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="09658-198">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="09658-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09658-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09658-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09658-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="09658-200">Entry</span></span> | <span data-ttu-id="09658-201">Значение</span><span class="sxs-lookup"><span data-stu-id="09658-201">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09658-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09658-202">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09658-203">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="09658-204">System-Only</span></span>            | <span data-ttu-id="09658-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-205">False</span></span>                                                                                 |
| <span data-ttu-id="09658-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09658-206">Is-Single-Valued</span></span>       | <span data-ttu-id="09658-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-207">False</span></span>                                                                                 |
| <span data-ttu-id="09658-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09658-208">Is Indexed</span></span>             | <span data-ttu-id="09658-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-209">False</span></span>                                                                                 |
| <span data-ttu-id="09658-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09658-210">In Global Catalog</span></span>      | <span data-ttu-id="09658-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-211">False</span></span>                                                                                 |
| <span data-ttu-id="09658-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09658-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="09658-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09658-213">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="09658-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09658-214">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09658-215">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-216">Search-Flags</span></span>           | <span data-ttu-id="09658-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-217">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-218">System-Flags</span></span>           | <span data-ttu-id="09658-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-219">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09658-220">Classes used in</span></span>        | [<span data-ttu-id="09658-221">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="09658-221">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="09658-222">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="09658-222">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09658-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09658-223">Windows Server 2012</span></span>



| <span data-ttu-id="09658-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="09658-224">Entry</span></span> | <span data-ttu-id="09658-225">Значение</span><span class="sxs-lookup"><span data-stu-id="09658-225">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09658-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09658-226">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09658-227">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="09658-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="09658-228">System-Only</span></span>            | <span data-ttu-id="09658-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-229">False</span></span>                                                                                 |
| <span data-ttu-id="09658-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09658-230">Is-Single-Valued</span></span>       | <span data-ttu-id="09658-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-231">False</span></span>                                                                                 |
| <span data-ttu-id="09658-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09658-232">Is Indexed</span></span>             | <span data-ttu-id="09658-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-233">False</span></span>                                                                                 |
| <span data-ttu-id="09658-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09658-234">In Global Catalog</span></span>      | <span data-ttu-id="09658-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="09658-235">False</span></span>                                                                                 |
| <span data-ttu-id="09658-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09658-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="09658-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09658-237">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="09658-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09658-238">Range-Lower</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09658-239">Range-Upper</span></span>            | \-                                                                                    |
| <span data-ttu-id="09658-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-240">Search-Flags</span></span>           | <span data-ttu-id="09658-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-241">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09658-242">System-Flags</span></span>           | <span data-ttu-id="09658-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="09658-243">0x00000000</span></span>                                                                            |
| <span data-ttu-id="09658-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09658-244">Classes used in</span></span>        | [<span data-ttu-id="09658-245">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="09658-245">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="09658-246">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="09658-246">**User**</span></span>](c-user.md)<br/> |



 

 





