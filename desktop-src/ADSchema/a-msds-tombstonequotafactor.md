---
title: Атрибут ms-DS-захоронение — Quota
description: Процентный коэффициент, на который следует уменьшить число объектов-захоронений в целях учета квот.
ms.assetid: 602c2fe0-d3b7-45e8-8ce8-35a7163f7b25
ms.tgt_platform: multiple
keywords:
- Схема Active-DS-захоронения-атрибут-фактор для атрибута Quota
- Схема AD атрибута msDS-Томбстонекуотафактор
topic_type:
- apiref
api_name:
- ms-DS-Tombstone-Quota-Factor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a44dd7f648754c2ded7334c9b221022d936ebfb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535999"
---
# <a name="ms-ds-tombstone-quota-factor-attribute"></a><span data-ttu-id="e63e5-105">Атрибут ms-DS-захоронение — Quota</span><span class="sxs-lookup"><span data-stu-id="e63e5-105">ms-DS-Tombstone-Quota-Factor attribute</span></span>

<span data-ttu-id="e63e5-106">Процентный коэффициент, на который следует уменьшить число объектов-захоронений в целях учета квот.</span><span class="sxs-lookup"><span data-stu-id="e63e5-106">The percentage factor by which the tombstone object count should be reduced for the purpose of quota accounting.</span></span>



| <span data-ttu-id="e63e5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-107">Entry</span></span> | <span data-ttu-id="e63e5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e63e5-109">CN</span><span class="sxs-lookup"><span data-stu-id="e63e5-109">CN</span></span>                | <span data-ttu-id="e63e5-110">MS-DS-захоронение-фактор квоты</span><span class="sxs-lookup"><span data-stu-id="e63e5-110">ms-DS-Tombstone-Quota-Factor</span></span>         |
| <span data-ttu-id="e63e5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e63e5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e63e5-112">msDS-Томбстонекуотафактор</span><span class="sxs-lookup"><span data-stu-id="e63e5-112">msDS-TombstoneQuotaFactor</span></span>            |
| <span data-ttu-id="e63e5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e63e5-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="e63e5-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e63e5-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e63e5-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e63e5-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e63e5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-116">Attribute-Id</span></span>      | <span data-ttu-id="e63e5-117">1.2.840.113556.1.4.1847</span><span class="sxs-lookup"><span data-stu-id="e63e5-117">1.2.840.113556.1.4.1847</span></span>              |
| <span data-ttu-id="e63e5-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e63e5-118">System-Id-Guid</span></span>    | <span data-ttu-id="e63e5-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span><span class="sxs-lookup"><span data-stu-id="e63e5-119">461744d7-f3b6-45ba-8753-fb9552a5df32</span></span> |
| <span data-ttu-id="e63e5-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e63e5-120">Syntax</span></span>            | [<span data-ttu-id="e63e5-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="e63e5-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e63e5-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e63e5-122">Implementations</span></span>

-   [<span data-ttu-id="e63e5-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e63e5-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e63e5-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="e63e5-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="e63e5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e63e5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e63e5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e63e5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e63e5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e63e5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e63e5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e63e5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="e63e5-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e63e5-129">Windows Server 2003</span></span>



| <span data-ttu-id="e63e5-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-130">Entry</span></span> | <span data-ttu-id="e63e5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e63e5-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e63e5-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="e63e5-134">System-Only</span></span>            | <span data-ttu-id="e63e5-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-135">False</span></span>                                                             |
| <span data-ttu-id="e63e5-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e63e5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="e63e5-137">True</span><span class="sxs-lookup"><span data-stu-id="e63e5-137">True</span></span>                                                              |
| <span data-ttu-id="e63e5-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e63e5-138">Is Indexed</span></span>             | <span data-ttu-id="e63e5-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-139">False</span></span>                                                             |
| <span data-ttu-id="e63e5-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e63e5-140">In Global Catalog</span></span>      | <span data-ttu-id="e63e5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-141">False</span></span>                                                             |
| <span data-ttu-id="e63e5-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e63e5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="e63e5-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e63e5-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e63e5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e63e5-144">Range-Lower</span></span>            | <span data-ttu-id="e63e5-145">0</span><span class="sxs-lookup"><span data-stu-id="e63e5-145">0</span></span>                                                                 |
| <span data-ttu-id="e63e5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e63e5-146">Range-Upper</span></span>            | <span data-ttu-id="e63e5-147">100</span><span class="sxs-lookup"><span data-stu-id="e63e5-147">100</span></span>                                                               |
| <span data-ttu-id="e63e5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-148">Search-Flags</span></span>           | <span data-ttu-id="e63e5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e63e5-149">0x00000000</span></span>                                                        |
| <span data-ttu-id="e63e5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-150">System-Flags</span></span>           | <span data-ttu-id="e63e5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e63e5-151">0x00000010</span></span>                                                        |
| <span data-ttu-id="e63e5-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e63e5-152">Classes used in</span></span>        | [<span data-ttu-id="e63e5-153">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="e63e5-153">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="e63e5-154">ADAM</span><span class="sxs-lookup"><span data-stu-id="e63e5-154">ADAM</span></span>



| <span data-ttu-id="e63e5-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-155">Entry</span></span> | <span data-ttu-id="e63e5-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e63e5-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e63e5-157">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-158">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e63e5-159">System-Only</span></span>            | <span data-ttu-id="e63e5-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-160">False</span></span>                                                             |
| <span data-ttu-id="e63e5-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e63e5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e63e5-162">True</span><span class="sxs-lookup"><span data-stu-id="e63e5-162">True</span></span>                                                              |
| <span data-ttu-id="e63e5-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e63e5-163">Is Indexed</span></span>             | <span data-ttu-id="e63e5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-164">False</span></span>                                                             |
| <span data-ttu-id="e63e5-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e63e5-165">In Global Catalog</span></span>      | <span data-ttu-id="e63e5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-166">False</span></span>                                                             |
| <span data-ttu-id="e63e5-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e63e5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e63e5-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e63e5-168">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e63e5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e63e5-169">Range-Lower</span></span>            | <span data-ttu-id="e63e5-170">0</span><span class="sxs-lookup"><span data-stu-id="e63e5-170">0</span></span>                                                                 |
| <span data-ttu-id="e63e5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e63e5-171">Range-Upper</span></span>            | <span data-ttu-id="e63e5-172">100</span><span class="sxs-lookup"><span data-stu-id="e63e5-172">100</span></span>                                                               |
| <span data-ttu-id="e63e5-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-173">Search-Flags</span></span>           | <span data-ttu-id="e63e5-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e63e5-174">0x00000000</span></span>                                                        |
| <span data-ttu-id="e63e5-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-175">System-Flags</span></span>           | <span data-ttu-id="e63e5-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e63e5-176">0x00000010</span></span>                                                        |
| <span data-ttu-id="e63e5-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e63e5-177">Classes used in</span></span>        | [<span data-ttu-id="e63e5-178">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="e63e5-178">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e63e5-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e63e5-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e63e5-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-180">Entry</span></span> | <span data-ttu-id="e63e5-181">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e63e5-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e63e5-182">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-183">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="e63e5-184">System-Only</span></span>            | <span data-ttu-id="e63e5-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-185">False</span></span>                                                             |
| <span data-ttu-id="e63e5-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e63e5-186">Is-Single-Valued</span></span>       | <span data-ttu-id="e63e5-187">True</span><span class="sxs-lookup"><span data-stu-id="e63e5-187">True</span></span>                                                              |
| <span data-ttu-id="e63e5-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e63e5-188">Is Indexed</span></span>             | <span data-ttu-id="e63e5-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-189">False</span></span>                                                             |
| <span data-ttu-id="e63e5-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e63e5-190">In Global Catalog</span></span>      | <span data-ttu-id="e63e5-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-191">False</span></span>                                                             |
| <span data-ttu-id="e63e5-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e63e5-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="e63e5-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e63e5-193">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e63e5-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e63e5-194">Range-Lower</span></span>            | <span data-ttu-id="e63e5-195">0</span><span class="sxs-lookup"><span data-stu-id="e63e5-195">0</span></span>                                                                 |
| <span data-ttu-id="e63e5-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e63e5-196">Range-Upper</span></span>            | <span data-ttu-id="e63e5-197">100</span><span class="sxs-lookup"><span data-stu-id="e63e5-197">100</span></span>                                                               |
| <span data-ttu-id="e63e5-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-198">Search-Flags</span></span>           | <span data-ttu-id="e63e5-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e63e5-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="e63e5-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-200">System-Flags</span></span>           | <span data-ttu-id="e63e5-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e63e5-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="e63e5-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e63e5-202">Classes used in</span></span>        | [<span data-ttu-id="e63e5-203">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="e63e5-203">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e63e5-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e63e5-204">Windows Server 2008</span></span>



| <span data-ttu-id="e63e5-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-205">Entry</span></span> | <span data-ttu-id="e63e5-206">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e63e5-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e63e5-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="e63e5-209">System-Only</span></span>            | <span data-ttu-id="e63e5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-210">False</span></span>                                                             |
| <span data-ttu-id="e63e5-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e63e5-211">Is-Single-Valued</span></span>       | <span data-ttu-id="e63e5-212">True</span><span class="sxs-lookup"><span data-stu-id="e63e5-212">True</span></span>                                                              |
| <span data-ttu-id="e63e5-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e63e5-213">Is Indexed</span></span>             | <span data-ttu-id="e63e5-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-214">False</span></span>                                                             |
| <span data-ttu-id="e63e5-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e63e5-215">In Global Catalog</span></span>      | <span data-ttu-id="e63e5-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-216">False</span></span>                                                             |
| <span data-ttu-id="e63e5-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e63e5-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="e63e5-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e63e5-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e63e5-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e63e5-219">Range-Lower</span></span>            | <span data-ttu-id="e63e5-220">0</span><span class="sxs-lookup"><span data-stu-id="e63e5-220">0</span></span>                                                                 |
| <span data-ttu-id="e63e5-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e63e5-221">Range-Upper</span></span>            | <span data-ttu-id="e63e5-222">100</span><span class="sxs-lookup"><span data-stu-id="e63e5-222">100</span></span>                                                               |
| <span data-ttu-id="e63e5-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-223">Search-Flags</span></span>           | <span data-ttu-id="e63e5-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e63e5-224">0x00000000</span></span>                                                        |
| <span data-ttu-id="e63e5-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-225">System-Flags</span></span>           | <span data-ttu-id="e63e5-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e63e5-226">0x00000010</span></span>                                                        |
| <span data-ttu-id="e63e5-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e63e5-227">Classes used in</span></span>        | [<span data-ttu-id="e63e5-228">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="e63e5-228">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e63e5-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e63e5-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e63e5-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-230">Entry</span></span> | <span data-ttu-id="e63e5-231">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e63e5-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e63e5-232">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-233">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="e63e5-234">System-Only</span></span>            | <span data-ttu-id="e63e5-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-235">False</span></span>                                                             |
| <span data-ttu-id="e63e5-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e63e5-236">Is-Single-Valued</span></span>       | <span data-ttu-id="e63e5-237">True</span><span class="sxs-lookup"><span data-stu-id="e63e5-237">True</span></span>                                                              |
| <span data-ttu-id="e63e5-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e63e5-238">Is Indexed</span></span>             | <span data-ttu-id="e63e5-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-239">False</span></span>                                                             |
| <span data-ttu-id="e63e5-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e63e5-240">In Global Catalog</span></span>      | <span data-ttu-id="e63e5-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-241">False</span></span>                                                             |
| <span data-ttu-id="e63e5-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e63e5-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="e63e5-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e63e5-243">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e63e5-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e63e5-244">Range-Lower</span></span>            | <span data-ttu-id="e63e5-245">0</span><span class="sxs-lookup"><span data-stu-id="e63e5-245">0</span></span>                                                                 |
| <span data-ttu-id="e63e5-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e63e5-246">Range-Upper</span></span>            | <span data-ttu-id="e63e5-247">100</span><span class="sxs-lookup"><span data-stu-id="e63e5-247">100</span></span>                                                               |
| <span data-ttu-id="e63e5-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-248">Search-Flags</span></span>           | <span data-ttu-id="e63e5-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e63e5-249">0x00000000</span></span>                                                        |
| <span data-ttu-id="e63e5-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-250">System-Flags</span></span>           | <span data-ttu-id="e63e5-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e63e5-251">0x00000010</span></span>                                                        |
| <span data-ttu-id="e63e5-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e63e5-252">Classes used in</span></span>        | [<span data-ttu-id="e63e5-253">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="e63e5-253">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e63e5-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e63e5-254">Windows Server 2012</span></span>



| <span data-ttu-id="e63e5-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="e63e5-255">Entry</span></span> | <span data-ttu-id="e63e5-256">Значение</span><span class="sxs-lookup"><span data-stu-id="e63e5-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="e63e5-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e63e5-257">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e63e5-258">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="e63e5-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e63e5-259">System-Only</span></span>            | <span data-ttu-id="e63e5-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-260">False</span></span>                                                             |
| <span data-ttu-id="e63e5-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e63e5-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e63e5-262">True</span><span class="sxs-lookup"><span data-stu-id="e63e5-262">True</span></span>                                                              |
| <span data-ttu-id="e63e5-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e63e5-263">Is Indexed</span></span>             | <span data-ttu-id="e63e5-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-264">False</span></span>                                                             |
| <span data-ttu-id="e63e5-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e63e5-265">In Global Catalog</span></span>      | <span data-ttu-id="e63e5-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="e63e5-266">False</span></span>                                                             |
| <span data-ttu-id="e63e5-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e63e5-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e63e5-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e63e5-268">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="e63e5-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e63e5-269">Range-Lower</span></span>            | <span data-ttu-id="e63e5-270">0</span><span class="sxs-lookup"><span data-stu-id="e63e5-270">0</span></span>                                                                 |
| <span data-ttu-id="e63e5-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e63e5-271">Range-Upper</span></span>            | <span data-ttu-id="e63e5-272">100</span><span class="sxs-lookup"><span data-stu-id="e63e5-272">100</span></span>                                                               |
| <span data-ttu-id="e63e5-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-273">Search-Flags</span></span>           | <span data-ttu-id="e63e5-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e63e5-274">0x00000000</span></span>                                                        |
| <span data-ttu-id="e63e5-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e63e5-275">System-Flags</span></span>           | <span data-ttu-id="e63e5-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e63e5-276">0x00000010</span></span>                                                        |
| <span data-ttu-id="e63e5-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e63e5-277">Classes used in</span></span>        | [<span data-ttu-id="e63e5-278">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="e63e5-278">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





