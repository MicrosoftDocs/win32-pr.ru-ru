---
title: MS-DS-Quota-действующий атрибут
description: Эффективная квота субъекта безопасности, вычисленная на основе назначенных квот для раздела каталога.
ms.assetid: 22422499-9b56-4d74-a30e-63917abacdd1
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Quota-экономично
- Схема AD атрибута msDS-Куотаеффективе
topic_type:
- apiref
api_name:
- ms-DS-Quota-Effective
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe610c87c356431883cecded5eda3e0a9c42297
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494022"
---
# <a name="ms-ds-quota-effective-attribute"></a><span data-ttu-id="958e1-105">MS-DS-Quota-действующий атрибут</span><span class="sxs-lookup"><span data-stu-id="958e1-105">ms-DS-Quota-Effective attribute</span></span>

<span data-ttu-id="958e1-106">Эффективная квота субъекта безопасности, вычисленная на основе назначенных квот для раздела каталога.</span><span class="sxs-lookup"><span data-stu-id="958e1-106">The effective quota for a security principal computed from the assigned quotas for a directory partition.</span></span>



| <span data-ttu-id="958e1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-107">Entry</span></span> | <span data-ttu-id="958e1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="958e1-109">CN</span><span class="sxs-lookup"><span data-stu-id="958e1-109">CN</span></span>                | <span data-ttu-id="958e1-110">MS-DS-Quota-эффективная</span><span class="sxs-lookup"><span data-stu-id="958e1-110">ms-DS-Quota-Effective</span></span>                |
| <span data-ttu-id="958e1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="958e1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="958e1-112">msDS-Куотаеффективе</span><span class="sxs-lookup"><span data-stu-id="958e1-112">msDS-QuotaEffective</span></span>                  |
| <span data-ttu-id="958e1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="958e1-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="958e1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="958e1-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="958e1-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="958e1-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="958e1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-116">Attribute-Id</span></span>      | <span data-ttu-id="958e1-117">1.2.840.113556.1.4.1848</span><span class="sxs-lookup"><span data-stu-id="958e1-117">1.2.840.113556.1.4.1848</span></span>              |
| <span data-ttu-id="958e1-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="958e1-118">System-Id-Guid</span></span>    | <span data-ttu-id="958e1-119">6655b152-101c-48b4-b347-e1fcebc60157</span><span class="sxs-lookup"><span data-stu-id="958e1-119">6655b152-101c-48b4-b347-e1fcebc60157</span></span> |
| <span data-ttu-id="958e1-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="958e1-120">Syntax</span></span>            | [<span data-ttu-id="958e1-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="958e1-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="958e1-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="958e1-122">Implementations</span></span>

-   [<span data-ttu-id="958e1-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="958e1-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="958e1-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="958e1-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="958e1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="958e1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="958e1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="958e1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="958e1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="958e1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="958e1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="958e1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="958e1-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="958e1-129">Windows Server 2003</span></span>



| <span data-ttu-id="958e1-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-130">Entry</span></span> | <span data-ttu-id="958e1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="958e1-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="958e1-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="958e1-134">System-Only</span></span>            | <span data-ttu-id="958e1-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-135">False</span></span>                                                             |
| <span data-ttu-id="958e1-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="958e1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="958e1-137">True</span><span class="sxs-lookup"><span data-stu-id="958e1-137">True</span></span>                                                              |
| <span data-ttu-id="958e1-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="958e1-138">Is Indexed</span></span>             | <span data-ttu-id="958e1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-139">False</span></span>                                                             |
| <span data-ttu-id="958e1-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="958e1-140">In Global Catalog</span></span>      | <span data-ttu-id="958e1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-141">False</span></span>                                                             |
| <span data-ttu-id="958e1-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="958e1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="958e1-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="958e1-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="958e1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="958e1-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="958e1-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-146">Search-Flags</span></span>           | <span data-ttu-id="958e1-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="958e1-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="958e1-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-148">System-Flags</span></span>           | <span data-ttu-id="958e1-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="958e1-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="958e1-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="958e1-150">Classes used in</span></span>        | [<span data-ttu-id="958e1-151">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="958e1-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="958e1-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="958e1-152">ADAM</span></span>



| <span data-ttu-id="958e1-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-153">Entry</span></span> | <span data-ttu-id="958e1-154">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="958e1-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="958e1-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="958e1-157">System-Only</span></span>            | <span data-ttu-id="958e1-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-158">False</span></span>                                                             |
| <span data-ttu-id="958e1-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="958e1-159">Is-Single-Valued</span></span>       | <span data-ttu-id="958e1-160">True</span><span class="sxs-lookup"><span data-stu-id="958e1-160">True</span></span>                                                              |
| <span data-ttu-id="958e1-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="958e1-161">Is Indexed</span></span>             | <span data-ttu-id="958e1-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-162">False</span></span>                                                             |
| <span data-ttu-id="958e1-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="958e1-163">In Global Catalog</span></span>      | <span data-ttu-id="958e1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-164">False</span></span>                                                             |
| <span data-ttu-id="958e1-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="958e1-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="958e1-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="958e1-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="958e1-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="958e1-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="958e1-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-169">Search-Flags</span></span>           | <span data-ttu-id="958e1-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="958e1-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="958e1-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-171">System-Flags</span></span>           | <span data-ttu-id="958e1-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="958e1-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="958e1-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="958e1-173">Classes used in</span></span>        | [<span data-ttu-id="958e1-174">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="958e1-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="958e1-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="958e1-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="958e1-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-176">Entry</span></span> | <span data-ttu-id="958e1-177">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="958e1-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="958e1-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="958e1-180">System-Only</span></span>            | <span data-ttu-id="958e1-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-181">False</span></span>                                                             |
| <span data-ttu-id="958e1-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="958e1-182">Is-Single-Valued</span></span>       | <span data-ttu-id="958e1-183">True</span><span class="sxs-lookup"><span data-stu-id="958e1-183">True</span></span>                                                              |
| <span data-ttu-id="958e1-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="958e1-184">Is Indexed</span></span>             | <span data-ttu-id="958e1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-185">False</span></span>                                                             |
| <span data-ttu-id="958e1-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="958e1-186">In Global Catalog</span></span>      | <span data-ttu-id="958e1-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-187">False</span></span>                                                             |
| <span data-ttu-id="958e1-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="958e1-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="958e1-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="958e1-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="958e1-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="958e1-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="958e1-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-192">Search-Flags</span></span>           | <span data-ttu-id="958e1-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="958e1-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="958e1-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-194">System-Flags</span></span>           | <span data-ttu-id="958e1-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="958e1-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="958e1-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="958e1-196">Classes used in</span></span>        | [<span data-ttu-id="958e1-197">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="958e1-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="958e1-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="958e1-198">Windows Server 2008</span></span>



| <span data-ttu-id="958e1-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-199">Entry</span></span> | <span data-ttu-id="958e1-200">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="958e1-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="958e1-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="958e1-203">System-Only</span></span>            | <span data-ttu-id="958e1-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-204">False</span></span>                                                             |
| <span data-ttu-id="958e1-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="958e1-205">Is-Single-Valued</span></span>       | <span data-ttu-id="958e1-206">True</span><span class="sxs-lookup"><span data-stu-id="958e1-206">True</span></span>                                                              |
| <span data-ttu-id="958e1-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="958e1-207">Is Indexed</span></span>             | <span data-ttu-id="958e1-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-208">False</span></span>                                                             |
| <span data-ttu-id="958e1-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="958e1-209">In Global Catalog</span></span>      | <span data-ttu-id="958e1-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-210">False</span></span>                                                             |
| <span data-ttu-id="958e1-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="958e1-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="958e1-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="958e1-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="958e1-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="958e1-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="958e1-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-215">Search-Flags</span></span>           | <span data-ttu-id="958e1-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="958e1-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="958e1-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-217">System-Flags</span></span>           | <span data-ttu-id="958e1-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="958e1-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="958e1-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="958e1-219">Classes used in</span></span>        | [<span data-ttu-id="958e1-220">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="958e1-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="958e1-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="958e1-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="958e1-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-222">Entry</span></span> | <span data-ttu-id="958e1-223">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="958e1-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="958e1-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="958e1-226">System-Only</span></span>            | <span data-ttu-id="958e1-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-227">False</span></span>                                                             |
| <span data-ttu-id="958e1-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="958e1-228">Is-Single-Valued</span></span>       | <span data-ttu-id="958e1-229">True</span><span class="sxs-lookup"><span data-stu-id="958e1-229">True</span></span>                                                              |
| <span data-ttu-id="958e1-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="958e1-230">Is Indexed</span></span>             | <span data-ttu-id="958e1-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-231">False</span></span>                                                             |
| <span data-ttu-id="958e1-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="958e1-232">In Global Catalog</span></span>      | <span data-ttu-id="958e1-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-233">False</span></span>                                                             |
| <span data-ttu-id="958e1-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="958e1-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="958e1-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="958e1-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="958e1-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="958e1-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="958e1-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-238">Search-Flags</span></span>           | <span data-ttu-id="958e1-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="958e1-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="958e1-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-240">System-Flags</span></span>           | <span data-ttu-id="958e1-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="958e1-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="958e1-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="958e1-242">Classes used in</span></span>        | [<span data-ttu-id="958e1-243">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="958e1-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="958e1-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="958e1-244">Windows Server 2012</span></span>



| <span data-ttu-id="958e1-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="958e1-245">Entry</span></span> | <span data-ttu-id="958e1-246">Значение</span><span class="sxs-lookup"><span data-stu-id="958e1-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="958e1-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="958e1-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="958e1-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="958e1-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="958e1-249">System-Only</span></span>            | <span data-ttu-id="958e1-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-250">False</span></span>                                                             |
| <span data-ttu-id="958e1-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="958e1-251">Is-Single-Valued</span></span>       | <span data-ttu-id="958e1-252">True</span><span class="sxs-lookup"><span data-stu-id="958e1-252">True</span></span>                                                              |
| <span data-ttu-id="958e1-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="958e1-253">Is Indexed</span></span>             | <span data-ttu-id="958e1-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-254">False</span></span>                                                             |
| <span data-ttu-id="958e1-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="958e1-255">In Global Catalog</span></span>      | <span data-ttu-id="958e1-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="958e1-256">False</span></span>                                                             |
| <span data-ttu-id="958e1-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="958e1-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="958e1-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="958e1-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="958e1-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="958e1-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="958e1-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="958e1-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-261">Search-Flags</span></span>           | <span data-ttu-id="958e1-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="958e1-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="958e1-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="958e1-263">System-Flags</span></span>           | <span data-ttu-id="958e1-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="958e1-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="958e1-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="958e1-265">Classes used in</span></span>        | [<span data-ttu-id="958e1-266">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="958e1-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





