---
title: Атрибут ms-DS-Top-Quota-Usage
description: Список пользователей с наибольшей квотой, в настоящее время находящихся в базе данных каталога, упорядоченный по снижению использования квоты.
ms.assetid: c52db8c8-233c-495f-b3fe-edbe1d723677
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута использования MS-DS-Top-Quota
- Схема AD атрибута msDS-Топкуотаусаже
topic_type:
- apiref
api_name:
- ms-DS-Top-Quota-Usage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db787c0360eff64c726ec680c9fd2a18da1e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655416"
---
# <a name="ms-ds-top-quota-usage-attribute"></a><span data-ttu-id="eb52b-105">Атрибут ms-DS-Top-Quota-Usage</span><span class="sxs-lookup"><span data-stu-id="eb52b-105">ms-DS-Top-Quota-Usage attribute</span></span>

<span data-ttu-id="eb52b-106">Список пользователей с наибольшей квотой, в настоящее время находящихся в базе данных каталога, упорядоченный по снижению использования квоты.</span><span class="sxs-lookup"><span data-stu-id="eb52b-106">The list of top quota users currently in the directory database, ordered by decreasing quota usage.</span></span>



| <span data-ttu-id="eb52b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-107">Entry</span></span> | <span data-ttu-id="eb52b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="eb52b-109">CN</span><span class="sxs-lookup"><span data-stu-id="eb52b-109">CN</span></span>                | <span data-ttu-id="eb52b-110">MS-DS-верхняя квота — использование</span><span class="sxs-lookup"><span data-stu-id="eb52b-110">ms-DS-Top-Quota-Usage</span></span>                       |
| <span data-ttu-id="eb52b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="eb52b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eb52b-112">msDS-Топкуотаусаже</span><span class="sxs-lookup"><span data-stu-id="eb52b-112">msDS-TopQuotaUsage</span></span>                          |
| <span data-ttu-id="eb52b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="eb52b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="eb52b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="eb52b-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="eb52b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="eb52b-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="eb52b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-116">Attribute-Id</span></span>      | <span data-ttu-id="eb52b-117">1.2.840.113556.1.4.1850</span><span class="sxs-lookup"><span data-stu-id="eb52b-117">1.2.840.113556.1.4.1850</span></span>                     |
| <span data-ttu-id="eb52b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="eb52b-118">System-Id-Guid</span></span>    | <span data-ttu-id="eb52b-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span><span class="sxs-lookup"><span data-stu-id="eb52b-119">7b7cce4f-f1f5-4bb6-b7eb-23504af19e75</span></span>        |
| <span data-ttu-id="eb52b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb52b-120">Syntax</span></span>            | [<span data-ttu-id="eb52b-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="eb52b-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="eb52b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="eb52b-122">Implementations</span></span>

-   [<span data-ttu-id="eb52b-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eb52b-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eb52b-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="eb52b-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="eb52b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eb52b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eb52b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eb52b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eb52b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eb52b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eb52b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eb52b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="eb52b-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eb52b-129">Windows Server 2003</span></span>



| <span data-ttu-id="eb52b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-130">Entry</span></span> | <span data-ttu-id="eb52b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eb52b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb52b-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb52b-134">System-Only</span></span>            | <span data-ttu-id="eb52b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-135">False</span></span>                                                             |
| <span data-ttu-id="eb52b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb52b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="eb52b-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-137">False</span></span>                                                             |
| <span data-ttu-id="eb52b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb52b-138">Is Indexed</span></span>             | <span data-ttu-id="eb52b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-139">False</span></span>                                                             |
| <span data-ttu-id="eb52b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb52b-140">In Global Catalog</span></span>      | <span data-ttu-id="eb52b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-141">False</span></span>                                                             |
| <span data-ttu-id="eb52b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb52b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb52b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb52b-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="eb52b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb52b-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb52b-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-146">Search-Flags</span></span>           | <span data-ttu-id="eb52b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb52b-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="eb52b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-148">System-Flags</span></span>           | <span data-ttu-id="eb52b-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="eb52b-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="eb52b-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb52b-150">Classes used in</span></span>        | [<span data-ttu-id="eb52b-151">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="eb52b-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="eb52b-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="eb52b-152">ADAM</span></span>



| <span data-ttu-id="eb52b-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-153">Entry</span></span> | <span data-ttu-id="eb52b-154">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eb52b-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb52b-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb52b-157">System-Only</span></span>            | <span data-ttu-id="eb52b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-158">False</span></span>                                                             |
| <span data-ttu-id="eb52b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb52b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="eb52b-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-160">False</span></span>                                                             |
| <span data-ttu-id="eb52b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb52b-161">Is Indexed</span></span>             | <span data-ttu-id="eb52b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-162">False</span></span>                                                             |
| <span data-ttu-id="eb52b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb52b-163">In Global Catalog</span></span>      | <span data-ttu-id="eb52b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-164">False</span></span>                                                             |
| <span data-ttu-id="eb52b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb52b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb52b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb52b-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="eb52b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb52b-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb52b-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-169">Search-Flags</span></span>           | <span data-ttu-id="eb52b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb52b-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="eb52b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-171">System-Flags</span></span>           | <span data-ttu-id="eb52b-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="eb52b-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="eb52b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb52b-173">Classes used in</span></span>        | [<span data-ttu-id="eb52b-174">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="eb52b-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eb52b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eb52b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eb52b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-176">Entry</span></span> | <span data-ttu-id="eb52b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eb52b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb52b-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb52b-180">System-Only</span></span>            | <span data-ttu-id="eb52b-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-181">False</span></span>                                                             |
| <span data-ttu-id="eb52b-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb52b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="eb52b-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-183">False</span></span>                                                             |
| <span data-ttu-id="eb52b-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb52b-184">Is Indexed</span></span>             | <span data-ttu-id="eb52b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-185">False</span></span>                                                             |
| <span data-ttu-id="eb52b-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb52b-186">In Global Catalog</span></span>      | <span data-ttu-id="eb52b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-187">False</span></span>                                                             |
| <span data-ttu-id="eb52b-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb52b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb52b-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb52b-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="eb52b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb52b-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb52b-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-192">Search-Flags</span></span>           | <span data-ttu-id="eb52b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb52b-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="eb52b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-194">System-Flags</span></span>           | <span data-ttu-id="eb52b-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="eb52b-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="eb52b-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb52b-196">Classes used in</span></span>        | [<span data-ttu-id="eb52b-197">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="eb52b-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eb52b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb52b-198">Windows Server 2008</span></span>



| <span data-ttu-id="eb52b-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-199">Entry</span></span> | <span data-ttu-id="eb52b-200">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eb52b-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb52b-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb52b-203">System-Only</span></span>            | <span data-ttu-id="eb52b-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-204">False</span></span>                                                             |
| <span data-ttu-id="eb52b-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb52b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="eb52b-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-206">False</span></span>                                                             |
| <span data-ttu-id="eb52b-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb52b-207">Is Indexed</span></span>             | <span data-ttu-id="eb52b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-208">False</span></span>                                                             |
| <span data-ttu-id="eb52b-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb52b-209">In Global Catalog</span></span>      | <span data-ttu-id="eb52b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-210">False</span></span>                                                             |
| <span data-ttu-id="eb52b-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb52b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb52b-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb52b-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="eb52b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb52b-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb52b-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-215">Search-Flags</span></span>           | <span data-ttu-id="eb52b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb52b-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="eb52b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-217">System-Flags</span></span>           | <span data-ttu-id="eb52b-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="eb52b-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="eb52b-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb52b-219">Classes used in</span></span>        | [<span data-ttu-id="eb52b-220">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="eb52b-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eb52b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eb52b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eb52b-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-222">Entry</span></span> | <span data-ttu-id="eb52b-223">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eb52b-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb52b-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb52b-226">System-Only</span></span>            | <span data-ttu-id="eb52b-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-227">False</span></span>                                                             |
| <span data-ttu-id="eb52b-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb52b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="eb52b-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-229">False</span></span>                                                             |
| <span data-ttu-id="eb52b-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb52b-230">Is Indexed</span></span>             | <span data-ttu-id="eb52b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-231">False</span></span>                                                             |
| <span data-ttu-id="eb52b-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb52b-232">In Global Catalog</span></span>      | <span data-ttu-id="eb52b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-233">False</span></span>                                                             |
| <span data-ttu-id="eb52b-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb52b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb52b-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb52b-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="eb52b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb52b-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb52b-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-238">Search-Flags</span></span>           | <span data-ttu-id="eb52b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb52b-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="eb52b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-240">System-Flags</span></span>           | <span data-ttu-id="eb52b-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="eb52b-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="eb52b-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb52b-242">Classes used in</span></span>        | [<span data-ttu-id="eb52b-243">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="eb52b-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eb52b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb52b-244">Windows Server 2012</span></span>



| <span data-ttu-id="eb52b-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="eb52b-245">Entry</span></span> | <span data-ttu-id="eb52b-246">Значение</span><span class="sxs-lookup"><span data-stu-id="eb52b-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="eb52b-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eb52b-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eb52b-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="eb52b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="eb52b-249">System-Only</span></span>            | <span data-ttu-id="eb52b-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-250">False</span></span>                                                             |
| <span data-ttu-id="eb52b-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eb52b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="eb52b-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-252">False</span></span>                                                             |
| <span data-ttu-id="eb52b-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eb52b-253">Is Indexed</span></span>             | <span data-ttu-id="eb52b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-254">False</span></span>                                                             |
| <span data-ttu-id="eb52b-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eb52b-255">In Global Catalog</span></span>      | <span data-ttu-id="eb52b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="eb52b-256">False</span></span>                                                             |
| <span data-ttu-id="eb52b-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eb52b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="eb52b-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eb52b-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="eb52b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eb52b-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eb52b-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="eb52b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-261">Search-Flags</span></span>           | <span data-ttu-id="eb52b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eb52b-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="eb52b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eb52b-263">System-Flags</span></span>           | <span data-ttu-id="eb52b-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="eb52b-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="eb52b-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eb52b-265">Classes used in</span></span>        | [<span data-ttu-id="eb52b-266">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="eb52b-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





