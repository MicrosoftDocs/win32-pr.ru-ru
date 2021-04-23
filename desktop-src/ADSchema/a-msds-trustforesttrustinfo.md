---
title: Атрибут ms-DS-Trust-лесом-Trust-info
description: Содержит сведения о доверии лесов (двоичный BLOB-объект), используемый системой для объекта Trusted-Domain.
ms.assetid: 60944ff6-d2b1-4f53-8557-7d79a7d9df51
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Trust-лесом-Trust-info
- Схема AD атрибута msDS-Трустфоресттрустинфо
topic_type:
- apiref
api_name:
- ms-DS-Trust-Forest-Trust-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e259abaeae4d99b80b8ff6a390901f1c9f51e6a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804660"
---
# <a name="ms-ds-trust-forest-trust-info-attribute"></a><span data-ttu-id="90921-105">Атрибут ms-DS-Trust-лесом-Trust-info</span><span class="sxs-lookup"><span data-stu-id="90921-105">ms-DS-Trust-Forest-Trust-Info attribute</span></span>

<span data-ttu-id="90921-106">Содержит сведения о доверии лесов (двоичный BLOB-объект), используемый системой для объекта Trusted-Domain.</span><span class="sxs-lookup"><span data-stu-id="90921-106">Contains forest trust information (a binary BLOB) that is used by the system for a Trusted-Domain object.</span></span>



| <span data-ttu-id="90921-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="90921-107">Entry</span></span> | <span data-ttu-id="90921-108">Значение</span><span class="sxs-lookup"><span data-stu-id="90921-108">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90921-109">CN</span><span class="sxs-lookup"><span data-stu-id="90921-109">CN</span></span>                | <span data-ttu-id="90921-110">MS-DS-Trust-лес-Trust-сведения</span><span class="sxs-lookup"><span data-stu-id="90921-110">ms-DS-Trust-Forest-Trust-Info</span></span>                                                                                      |
| <span data-ttu-id="90921-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="90921-111">Ldap-Display-Name</span></span> | <span data-ttu-id="90921-112">msDS-Трустфоресттрустинфо</span><span class="sxs-lookup"><span data-stu-id="90921-112">msDS-TrustForestTrustInfo</span></span>                                                                                          |
| <span data-ttu-id="90921-113">Размер</span><span class="sxs-lookup"><span data-stu-id="90921-113">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="90921-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="90921-114">Update Privilege</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="90921-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="90921-115">Update Frequency</span></span>  | <span data-ttu-id="90921-116">Только при изменении отношения доверия между лесами.</span><span class="sxs-lookup"><span data-stu-id="90921-116">Only when trust relationship between forests changes.</span></span> <span data-ttu-id="90921-117">Это может произойти при изменении топологии доверенного леса.</span><span class="sxs-lookup"><span data-stu-id="90921-117">This can happen if the topology of a trusted forest changes.</span></span> |
| <span data-ttu-id="90921-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90921-118">Attribute-Id</span></span>      | <span data-ttu-id="90921-119">1.2.840.113556.1.4.1702</span><span class="sxs-lookup"><span data-stu-id="90921-119">1.2.840.113556.1.4.1702</span></span>                                                                                            |
| <span data-ttu-id="90921-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="90921-120">System-Id-Guid</span></span>    | <span data-ttu-id="90921-121">29cc866e-49d3-4969-942e-1dbc0925d183</span><span class="sxs-lookup"><span data-stu-id="90921-121">29cc866e-49d3-4969-942e-1dbc0925d183</span></span>                                                                               |
| <span data-ttu-id="90921-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90921-122">Syntax</span></span>            | [<span data-ttu-id="90921-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="90921-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="90921-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="90921-124">Implementations</span></span>

-   [<span data-ttu-id="90921-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90921-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90921-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90921-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90921-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90921-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90921-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90921-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90921-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90921-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="90921-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90921-130">Windows Server 2003</span></span>



| <span data-ttu-id="90921-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="90921-131">Entry</span></span> | <span data-ttu-id="90921-132">Значение</span><span class="sxs-lookup"><span data-stu-id="90921-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90921-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90921-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90921-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="90921-135">System-Only</span></span>            | <span data-ttu-id="90921-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-136">False</span></span>                                                |
| <span data-ttu-id="90921-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90921-137">Is-Single-Valued</span></span>       | <span data-ttu-id="90921-138">True</span><span class="sxs-lookup"><span data-stu-id="90921-138">True</span></span>                                                 |
| <span data-ttu-id="90921-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90921-139">Is Indexed</span></span>             | <span data-ttu-id="90921-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-140">False</span></span>                                                |
| <span data-ttu-id="90921-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90921-141">In Global Catalog</span></span>      | <span data-ttu-id="90921-142">True</span><span class="sxs-lookup"><span data-stu-id="90921-142">True</span></span>                                                 |
| <span data-ttu-id="90921-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90921-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="90921-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90921-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90921-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90921-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90921-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90921-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90921-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-147">Search-Flags</span></span>           | <span data-ttu-id="90921-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90921-148">0x00000000</span></span>                                           |
| <span data-ttu-id="90921-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-149">System-Flags</span></span>           | <span data-ttu-id="90921-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90921-150">0x00000010</span></span>                                           |
| <span data-ttu-id="90921-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90921-151">Classes used in</span></span>        | [<span data-ttu-id="90921-152">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="90921-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90921-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90921-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90921-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="90921-154">Entry</span></span> | <span data-ttu-id="90921-155">Значение</span><span class="sxs-lookup"><span data-stu-id="90921-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90921-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90921-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90921-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="90921-158">System-Only</span></span>            | <span data-ttu-id="90921-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-159">False</span></span>                                                |
| <span data-ttu-id="90921-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90921-160">Is-Single-Valued</span></span>       | <span data-ttu-id="90921-161">True</span><span class="sxs-lookup"><span data-stu-id="90921-161">True</span></span>                                                 |
| <span data-ttu-id="90921-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90921-162">Is Indexed</span></span>             | <span data-ttu-id="90921-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-163">False</span></span>                                                |
| <span data-ttu-id="90921-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90921-164">In Global Catalog</span></span>      | <span data-ttu-id="90921-165">True</span><span class="sxs-lookup"><span data-stu-id="90921-165">True</span></span>                                                 |
| <span data-ttu-id="90921-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90921-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="90921-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90921-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90921-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90921-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90921-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90921-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90921-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-170">Search-Flags</span></span>           | <span data-ttu-id="90921-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90921-171">0x00000000</span></span>                                           |
| <span data-ttu-id="90921-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-172">System-Flags</span></span>           | <span data-ttu-id="90921-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90921-173">0x00000010</span></span>                                           |
| <span data-ttu-id="90921-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90921-174">Classes used in</span></span>        | [<span data-ttu-id="90921-175">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="90921-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90921-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90921-176">Windows Server 2008</span></span>



| <span data-ttu-id="90921-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="90921-177">Entry</span></span> | <span data-ttu-id="90921-178">Значение</span><span class="sxs-lookup"><span data-stu-id="90921-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90921-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90921-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90921-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="90921-181">System-Only</span></span>            | <span data-ttu-id="90921-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-182">False</span></span>                                                |
| <span data-ttu-id="90921-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90921-183">Is-Single-Valued</span></span>       | <span data-ttu-id="90921-184">True</span><span class="sxs-lookup"><span data-stu-id="90921-184">True</span></span>                                                 |
| <span data-ttu-id="90921-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90921-185">Is Indexed</span></span>             | <span data-ttu-id="90921-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-186">False</span></span>                                                |
| <span data-ttu-id="90921-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90921-187">In Global Catalog</span></span>      | <span data-ttu-id="90921-188">True</span><span class="sxs-lookup"><span data-stu-id="90921-188">True</span></span>                                                 |
| <span data-ttu-id="90921-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90921-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="90921-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90921-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90921-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90921-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90921-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90921-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90921-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-193">Search-Flags</span></span>           | <span data-ttu-id="90921-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90921-194">0x00000000</span></span>                                           |
| <span data-ttu-id="90921-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-195">System-Flags</span></span>           | <span data-ttu-id="90921-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90921-196">0x00000010</span></span>                                           |
| <span data-ttu-id="90921-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90921-197">Classes used in</span></span>        | [<span data-ttu-id="90921-198">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="90921-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90921-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90921-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90921-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="90921-200">Entry</span></span> | <span data-ttu-id="90921-201">Значение</span><span class="sxs-lookup"><span data-stu-id="90921-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90921-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90921-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90921-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="90921-204">System-Only</span></span>            | <span data-ttu-id="90921-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-205">False</span></span>                                                |
| <span data-ttu-id="90921-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90921-206">Is-Single-Valued</span></span>       | <span data-ttu-id="90921-207">True</span><span class="sxs-lookup"><span data-stu-id="90921-207">True</span></span>                                                 |
| <span data-ttu-id="90921-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90921-208">Is Indexed</span></span>             | <span data-ttu-id="90921-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-209">False</span></span>                                                |
| <span data-ttu-id="90921-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90921-210">In Global Catalog</span></span>      | <span data-ttu-id="90921-211">True</span><span class="sxs-lookup"><span data-stu-id="90921-211">True</span></span>                                                 |
| <span data-ttu-id="90921-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90921-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="90921-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90921-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90921-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90921-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90921-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90921-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90921-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-216">Search-Flags</span></span>           | <span data-ttu-id="90921-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90921-217">0x00000000</span></span>                                           |
| <span data-ttu-id="90921-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-218">System-Flags</span></span>           | <span data-ttu-id="90921-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90921-219">0x00000010</span></span>                                           |
| <span data-ttu-id="90921-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90921-220">Classes used in</span></span>        | [<span data-ttu-id="90921-221">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="90921-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90921-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90921-222">Windows Server 2012</span></span>



| <span data-ttu-id="90921-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="90921-223">Entry</span></span> | <span data-ttu-id="90921-224">Значение</span><span class="sxs-lookup"><span data-stu-id="90921-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="90921-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90921-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90921-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="90921-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="90921-227">System-Only</span></span>            | <span data-ttu-id="90921-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-228">False</span></span>                                                |
| <span data-ttu-id="90921-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90921-229">Is-Single-Valued</span></span>       | <span data-ttu-id="90921-230">True</span><span class="sxs-lookup"><span data-stu-id="90921-230">True</span></span>                                                 |
| <span data-ttu-id="90921-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90921-231">Is Indexed</span></span>             | <span data-ttu-id="90921-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="90921-232">False</span></span>                                                |
| <span data-ttu-id="90921-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90921-233">In Global Catalog</span></span>      | <span data-ttu-id="90921-234">True</span><span class="sxs-lookup"><span data-stu-id="90921-234">True</span></span>                                                 |
| <span data-ttu-id="90921-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90921-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="90921-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90921-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="90921-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90921-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="90921-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90921-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="90921-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-239">Search-Flags</span></span>           | <span data-ttu-id="90921-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="90921-240">0x00000000</span></span>                                           |
| <span data-ttu-id="90921-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90921-241">System-Flags</span></span>           | <span data-ttu-id="90921-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="90921-242">0x00000010</span></span>                                           |
| <span data-ttu-id="90921-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90921-243">Classes used in</span></span>        | [<span data-ttu-id="90921-244">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="90921-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





