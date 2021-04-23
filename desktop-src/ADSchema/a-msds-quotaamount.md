---
title: Атрибут ms-DS-Quota-Amount
description: Назначенная квота в терминах количества объектов, принадлежащих базе данных.
ms.assetid: 6ae57661-e384-493b-82a9-c002eab277a1
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута суммы MS-DS-Quota
- Схема AD атрибута msDS-Куотаамаунт
topic_type:
- apiref
api_name:
- ms-DS-Quota-Amount
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1629f93d077cabcfaf7f812a72ca7fb0c417320
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893486"
---
# <a name="ms-ds-quota-amount-attribute"></a><span data-ttu-id="f655b-105">Атрибут ms-DS-Quota-Amount</span><span class="sxs-lookup"><span data-stu-id="f655b-105">ms-DS-Quota-Amount attribute</span></span>

<span data-ttu-id="f655b-106">Назначенная квота в терминах количества объектов, принадлежащих базе данных.</span><span class="sxs-lookup"><span data-stu-id="f655b-106">The assigned quota in terms of number of objects owned in the database.</span></span>



| <span data-ttu-id="f655b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-107">Entry</span></span> | <span data-ttu-id="f655b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f655b-109">CN</span><span class="sxs-lookup"><span data-stu-id="f655b-109">CN</span></span>                | <span data-ttu-id="f655b-110">MS-DS-Quota-сумма</span><span class="sxs-lookup"><span data-stu-id="f655b-110">ms-DS-Quota-Amount</span></span>                   |
| <span data-ttu-id="f655b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f655b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f655b-112">msDS-Куотаамаунт</span><span class="sxs-lookup"><span data-stu-id="f655b-112">msDS-QuotaAmount</span></span>                     |
| <span data-ttu-id="f655b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f655b-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="f655b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f655b-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f655b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f655b-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f655b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-116">Attribute-Id</span></span>      | <span data-ttu-id="f655b-117">1.2.840.113556.1.4.1845</span><span class="sxs-lookup"><span data-stu-id="f655b-117">1.2.840.113556.1.4.1845</span></span>              |
| <span data-ttu-id="f655b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f655b-118">System-Id-Guid</span></span>    | <span data-ttu-id="f655b-119">fbb9a00d-3a8c-4233-9cf9-7189264903a1</span><span class="sxs-lookup"><span data-stu-id="f655b-119">fbb9a00d-3a8c-4233-9cf9-7189264903a1</span></span> |
| <span data-ttu-id="f655b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f655b-120">Syntax</span></span>            | [<span data-ttu-id="f655b-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="f655b-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="f655b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f655b-122">Implementations</span></span>

-   [<span data-ttu-id="f655b-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f655b-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f655b-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="f655b-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="f655b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f655b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f655b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f655b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f655b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f655b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f655b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f655b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f655b-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f655b-129">Windows Server 2003</span></span>



| <span data-ttu-id="f655b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-130">Entry</span></span> | <span data-ttu-id="f655b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-131">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f655b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f655b-132">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-133">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f655b-134">System-Only</span></span>            | <span data-ttu-id="f655b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-135">False</span></span>                                                         |
| <span data-ttu-id="f655b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f655b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f655b-137">True</span><span class="sxs-lookup"><span data-stu-id="f655b-137">True</span></span>                                                          |
| <span data-ttu-id="f655b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f655b-138">Is Indexed</span></span>             | <span data-ttu-id="f655b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-139">False</span></span>                                                         |
| <span data-ttu-id="f655b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f655b-140">In Global Catalog</span></span>      | <span data-ttu-id="f655b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-141">False</span></span>                                                         |
| <span data-ttu-id="f655b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f655b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f655b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f655b-143">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f655b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f655b-144">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f655b-145">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-146">Search-Flags</span></span>           | <span data-ttu-id="f655b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f655b-147">0x00000000</span></span>                                                    |
| <span data-ttu-id="f655b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-148">System-Flags</span></span>           | <span data-ttu-id="f655b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f655b-149">0x00000010</span></span>                                                    |
| <span data-ttu-id="f655b-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f655b-150">Classes used in</span></span>        | [<span data-ttu-id="f655b-151">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="f655b-151">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="adam"></a><span data-ttu-id="f655b-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="f655b-152">ADAM</span></span>



| <span data-ttu-id="f655b-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-153">Entry</span></span> | <span data-ttu-id="f655b-154">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-154">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f655b-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f655b-155">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-156">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f655b-157">System-Only</span></span>            | <span data-ttu-id="f655b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-158">False</span></span>                                                         |
| <span data-ttu-id="f655b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f655b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f655b-160">True</span><span class="sxs-lookup"><span data-stu-id="f655b-160">True</span></span>                                                          |
| <span data-ttu-id="f655b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f655b-161">Is Indexed</span></span>             | <span data-ttu-id="f655b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-162">False</span></span>                                                         |
| <span data-ttu-id="f655b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f655b-163">In Global Catalog</span></span>      | <span data-ttu-id="f655b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-164">False</span></span>                                                         |
| <span data-ttu-id="f655b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f655b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f655b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f655b-166">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f655b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f655b-167">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f655b-168">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-169">Search-Flags</span></span>           | <span data-ttu-id="f655b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f655b-170">0x00000000</span></span>                                                    |
| <span data-ttu-id="f655b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-171">System-Flags</span></span>           | <span data-ttu-id="f655b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f655b-172">0x00000010</span></span>                                                    |
| <span data-ttu-id="f655b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f655b-173">Classes used in</span></span>        | [<span data-ttu-id="f655b-174">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="f655b-174">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f655b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f655b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f655b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-176">Entry</span></span> | <span data-ttu-id="f655b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-177">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f655b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f655b-178">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-179">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f655b-180">System-Only</span></span>            | <span data-ttu-id="f655b-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-181">False</span></span>                                                         |
| <span data-ttu-id="f655b-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f655b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f655b-183">True</span><span class="sxs-lookup"><span data-stu-id="f655b-183">True</span></span>                                                          |
| <span data-ttu-id="f655b-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f655b-184">Is Indexed</span></span>             | <span data-ttu-id="f655b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-185">False</span></span>                                                         |
| <span data-ttu-id="f655b-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f655b-186">In Global Catalog</span></span>      | <span data-ttu-id="f655b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-187">False</span></span>                                                         |
| <span data-ttu-id="f655b-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f655b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f655b-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f655b-189">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f655b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f655b-190">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f655b-191">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-192">Search-Flags</span></span>           | <span data-ttu-id="f655b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f655b-193">0x00000000</span></span>                                                    |
| <span data-ttu-id="f655b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-194">System-Flags</span></span>           | <span data-ttu-id="f655b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f655b-195">0x00000010</span></span>                                                    |
| <span data-ttu-id="f655b-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f655b-196">Classes used in</span></span>        | [<span data-ttu-id="f655b-197">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="f655b-197">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f655b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f655b-198">Windows Server 2008</span></span>



| <span data-ttu-id="f655b-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-199">Entry</span></span> | <span data-ttu-id="f655b-200">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-200">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f655b-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f655b-201">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-202">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f655b-203">System-Only</span></span>            | <span data-ttu-id="f655b-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-204">False</span></span>                                                         |
| <span data-ttu-id="f655b-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f655b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f655b-206">True</span><span class="sxs-lookup"><span data-stu-id="f655b-206">True</span></span>                                                          |
| <span data-ttu-id="f655b-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f655b-207">Is Indexed</span></span>             | <span data-ttu-id="f655b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-208">False</span></span>                                                         |
| <span data-ttu-id="f655b-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f655b-209">In Global Catalog</span></span>      | <span data-ttu-id="f655b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-210">False</span></span>                                                         |
| <span data-ttu-id="f655b-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f655b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f655b-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f655b-212">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f655b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f655b-213">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f655b-214">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-215">Search-Flags</span></span>           | <span data-ttu-id="f655b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f655b-216">0x00000000</span></span>                                                    |
| <span data-ttu-id="f655b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-217">System-Flags</span></span>           | <span data-ttu-id="f655b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f655b-218">0x00000010</span></span>                                                    |
| <span data-ttu-id="f655b-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f655b-219">Classes used in</span></span>        | [<span data-ttu-id="f655b-220">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="f655b-220">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f655b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f655b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f655b-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-222">Entry</span></span> | <span data-ttu-id="f655b-223">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-223">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f655b-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f655b-224">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-225">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f655b-226">System-Only</span></span>            | <span data-ttu-id="f655b-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-227">False</span></span>                                                         |
| <span data-ttu-id="f655b-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f655b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f655b-229">True</span><span class="sxs-lookup"><span data-stu-id="f655b-229">True</span></span>                                                          |
| <span data-ttu-id="f655b-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f655b-230">Is Indexed</span></span>             | <span data-ttu-id="f655b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-231">False</span></span>                                                         |
| <span data-ttu-id="f655b-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f655b-232">In Global Catalog</span></span>      | <span data-ttu-id="f655b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-233">False</span></span>                                                         |
| <span data-ttu-id="f655b-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f655b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f655b-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f655b-235">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f655b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f655b-236">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f655b-237">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-238">Search-Flags</span></span>           | <span data-ttu-id="f655b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f655b-239">0x00000000</span></span>                                                    |
| <span data-ttu-id="f655b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-240">System-Flags</span></span>           | <span data-ttu-id="f655b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f655b-241">0x00000010</span></span>                                                    |
| <span data-ttu-id="f655b-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f655b-242">Classes used in</span></span>        | [<span data-ttu-id="f655b-243">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="f655b-243">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f655b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f655b-244">Windows Server 2012</span></span>



| <span data-ttu-id="f655b-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="f655b-245">Entry</span></span> | <span data-ttu-id="f655b-246">Значение</span><span class="sxs-lookup"><span data-stu-id="f655b-246">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f655b-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f655b-247">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f655b-248">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="f655b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f655b-249">System-Only</span></span>            | <span data-ttu-id="f655b-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-250">False</span></span>                                                         |
| <span data-ttu-id="f655b-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f655b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f655b-252">True</span><span class="sxs-lookup"><span data-stu-id="f655b-252">True</span></span>                                                          |
| <span data-ttu-id="f655b-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f655b-253">Is Indexed</span></span>             | <span data-ttu-id="f655b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-254">False</span></span>                                                         |
| <span data-ttu-id="f655b-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f655b-255">In Global Catalog</span></span>      | <span data-ttu-id="f655b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="f655b-256">False</span></span>                                                         |
| <span data-ttu-id="f655b-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f655b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f655b-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f655b-258">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="f655b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f655b-259">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f655b-260">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="f655b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-261">Search-Flags</span></span>           | <span data-ttu-id="f655b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f655b-262">0x00000000</span></span>                                                    |
| <span data-ttu-id="f655b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f655b-263">System-Flags</span></span>           | <span data-ttu-id="f655b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f655b-264">0x00000010</span></span>                                                    |
| <span data-ttu-id="f655b-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f655b-265">Classes used in</span></span>        | [<span data-ttu-id="f655b-266">**MS-DS-Quota-Control**</span><span class="sxs-lookup"><span data-stu-id="f655b-266">**ms-DS-Quota-Control**</span></span>](c-msds-quotacontrol.md)<br/> |



 

 





