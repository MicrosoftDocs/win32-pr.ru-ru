---
title: атрибут, используемый MS-DS-Quota
description: Текущая квота, используемая субъектом безопасности в базе данных каталогов.
ms.assetid: 3a31c0c7-9791-4e00-81e5-ee596f94e3c9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута, используемая MS-DS-Quota
- Схема AD атрибута msDS-Куотаусед
topic_type:
- apiref
api_name:
- ms-DS-Quota-Used
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59cc425c83fd7f1a85f41cd9d23e234115e0b55
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655427"
---
# <a name="ms-ds-quota-used-attribute"></a><span data-ttu-id="cc6f6-105">атрибут, используемый MS-DS-Quota</span><span class="sxs-lookup"><span data-stu-id="cc6f6-105">ms-DS-Quota-Used attribute</span></span>

<span data-ttu-id="cc6f6-106">Текущая квота, используемая субъектом безопасности в базе данных каталогов.</span><span class="sxs-lookup"><span data-stu-id="cc6f6-106">The current quota consumed by a security principal in the directory database.</span></span>



| <span data-ttu-id="cc6f6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-107">Entry</span></span> | <span data-ttu-id="cc6f6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="cc6f6-109">CN</span><span class="sxs-lookup"><span data-stu-id="cc6f6-109">CN</span></span>                | <span data-ttu-id="cc6f6-110">Используется MS-DS-Quota</span><span class="sxs-lookup"><span data-stu-id="cc6f6-110">ms-DS-Quota-Used</span></span>                     |
| <span data-ttu-id="cc6f6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cc6f6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cc6f6-112">msDS-Куотаусед</span><span class="sxs-lookup"><span data-stu-id="cc6f6-112">msDS-QuotaUsed</span></span>                       |
| <span data-ttu-id="cc6f6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cc6f6-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="cc6f6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cc6f6-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="cc6f6-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cc6f6-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="cc6f6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-116">Attribute-Id</span></span>      | <span data-ttu-id="cc6f6-117">1.2.840.113556.1.4.1849</span><span class="sxs-lookup"><span data-stu-id="cc6f6-117">1.2.840.113556.1.4.1849</span></span>              |
| <span data-ttu-id="cc6f6-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cc6f6-118">System-Id-Guid</span></span>    | <span data-ttu-id="cc6f6-119">b5a84308-615d-4bb7-b05f-2f1746aa439f</span><span class="sxs-lookup"><span data-stu-id="cc6f6-119">b5a84308-615d-4bb7-b05f-2f1746aa439f</span></span> |
| <span data-ttu-id="cc6f6-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc6f6-120">Syntax</span></span>            | [<span data-ttu-id="cc6f6-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="cc6f6-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cc6f6-122">Implementations</span></span>

-   [<span data-ttu-id="cc6f6-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cc6f6-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="cc6f6-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cc6f6-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cc6f6-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cc6f6-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="cc6f6-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cc6f6-129">Windows Server 2003</span></span>



| <span data-ttu-id="cc6f6-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-130">Entry</span></span> | <span data-ttu-id="cc6f6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc6f6-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc6f6-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc6f6-134">System-Only</span></span>            | <span data-ttu-id="cc6f6-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-135">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc6f6-136">Is-Single-Valued</span></span>       | <span data-ttu-id="cc6f6-137">True</span><span class="sxs-lookup"><span data-stu-id="cc6f6-137">True</span></span>                                                              |
| <span data-ttu-id="cc6f6-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc6f6-138">Is Indexed</span></span>             | <span data-ttu-id="cc6f6-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-139">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc6f6-140">In Global Catalog</span></span>      | <span data-ttu-id="cc6f6-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-141">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc6f6-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc6f6-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc6f6-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cc6f6-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc6f6-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc6f6-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-146">Search-Flags</span></span>           | <span data-ttu-id="cc6f6-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc6f6-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="cc6f6-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-148">System-Flags</span></span>           | <span data-ttu-id="cc6f6-149">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc6f6-149">0x00000014</span></span>                                                        |
| <span data-ttu-id="cc6f6-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc6f6-150">Classes used in</span></span>        | [<span data-ttu-id="cc6f6-151">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="cc6f6-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="cc6f6-152">ADAM</span></span>



| <span data-ttu-id="cc6f6-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-153">Entry</span></span> | <span data-ttu-id="cc6f6-154">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc6f6-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc6f6-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc6f6-157">System-Only</span></span>            | <span data-ttu-id="cc6f6-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-158">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc6f6-159">Is-Single-Valued</span></span>       | <span data-ttu-id="cc6f6-160">True</span><span class="sxs-lookup"><span data-stu-id="cc6f6-160">True</span></span>                                                              |
| <span data-ttu-id="cc6f6-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc6f6-161">Is Indexed</span></span>             | <span data-ttu-id="cc6f6-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-162">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc6f6-163">In Global Catalog</span></span>      | <span data-ttu-id="cc6f6-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-164">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc6f6-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc6f6-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc6f6-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cc6f6-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc6f6-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc6f6-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-169">Search-Flags</span></span>           | <span data-ttu-id="cc6f6-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc6f6-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="cc6f6-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-171">System-Flags</span></span>           | <span data-ttu-id="cc6f6-172">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc6f6-172">0x00000014</span></span>                                                        |
| <span data-ttu-id="cc6f6-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc6f6-173">Classes used in</span></span>        | [<span data-ttu-id="cc6f6-174">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cc6f6-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cc6f6-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cc6f6-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-176">Entry</span></span> | <span data-ttu-id="cc6f6-177">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc6f6-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc6f6-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc6f6-180">System-Only</span></span>            | <span data-ttu-id="cc6f6-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-181">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc6f6-182">Is-Single-Valued</span></span>       | <span data-ttu-id="cc6f6-183">True</span><span class="sxs-lookup"><span data-stu-id="cc6f6-183">True</span></span>                                                              |
| <span data-ttu-id="cc6f6-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc6f6-184">Is Indexed</span></span>             | <span data-ttu-id="cc6f6-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-185">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc6f6-186">In Global Catalog</span></span>      | <span data-ttu-id="cc6f6-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-187">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc6f6-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc6f6-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc6f6-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cc6f6-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc6f6-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc6f6-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-192">Search-Flags</span></span>           | <span data-ttu-id="cc6f6-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc6f6-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="cc6f6-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-194">System-Flags</span></span>           | <span data-ttu-id="cc6f6-195">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc6f6-195">0x00000014</span></span>                                                        |
| <span data-ttu-id="cc6f6-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc6f6-196">Classes used in</span></span>        | [<span data-ttu-id="cc6f6-197">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cc6f6-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc6f6-198">Windows Server 2008</span></span>



| <span data-ttu-id="cc6f6-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-199">Entry</span></span> | <span data-ttu-id="cc6f6-200">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc6f6-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc6f6-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc6f6-203">System-Only</span></span>            | <span data-ttu-id="cc6f6-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-204">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc6f6-205">Is-Single-Valued</span></span>       | <span data-ttu-id="cc6f6-206">True</span><span class="sxs-lookup"><span data-stu-id="cc6f6-206">True</span></span>                                                              |
| <span data-ttu-id="cc6f6-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc6f6-207">Is Indexed</span></span>             | <span data-ttu-id="cc6f6-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-208">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc6f6-209">In Global Catalog</span></span>      | <span data-ttu-id="cc6f6-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-210">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc6f6-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc6f6-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc6f6-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cc6f6-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc6f6-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc6f6-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-215">Search-Flags</span></span>           | <span data-ttu-id="cc6f6-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc6f6-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="cc6f6-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-217">System-Flags</span></span>           | <span data-ttu-id="cc6f6-218">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc6f6-218">0x00000014</span></span>                                                        |
| <span data-ttu-id="cc6f6-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc6f6-219">Classes used in</span></span>        | [<span data-ttu-id="cc6f6-220">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cc6f6-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cc6f6-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cc6f6-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-222">Entry</span></span> | <span data-ttu-id="cc6f6-223">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc6f6-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc6f6-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc6f6-226">System-Only</span></span>            | <span data-ttu-id="cc6f6-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-227">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc6f6-228">Is-Single-Valued</span></span>       | <span data-ttu-id="cc6f6-229">True</span><span class="sxs-lookup"><span data-stu-id="cc6f6-229">True</span></span>                                                              |
| <span data-ttu-id="cc6f6-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc6f6-230">Is Indexed</span></span>             | <span data-ttu-id="cc6f6-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-231">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc6f6-232">In Global Catalog</span></span>      | <span data-ttu-id="cc6f6-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-233">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc6f6-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc6f6-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc6f6-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cc6f6-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc6f6-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc6f6-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-238">Search-Flags</span></span>           | <span data-ttu-id="cc6f6-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc6f6-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="cc6f6-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-240">System-Flags</span></span>           | <span data-ttu-id="cc6f6-241">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc6f6-241">0x00000014</span></span>                                                        |
| <span data-ttu-id="cc6f6-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc6f6-242">Classes used in</span></span>        | [<span data-ttu-id="cc6f6-243">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cc6f6-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc6f6-244">Windows Server 2012</span></span>



| <span data-ttu-id="cc6f6-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="cc6f6-245">Entry</span></span> | <span data-ttu-id="cc6f6-246">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6f6-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="cc6f6-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cc6f6-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cc6f6-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="cc6f6-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="cc6f6-249">System-Only</span></span>            | <span data-ttu-id="cc6f6-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-250">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cc6f6-251">Is-Single-Valued</span></span>       | <span data-ttu-id="cc6f6-252">True</span><span class="sxs-lookup"><span data-stu-id="cc6f6-252">True</span></span>                                                              |
| <span data-ttu-id="cc6f6-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cc6f6-253">Is Indexed</span></span>             | <span data-ttu-id="cc6f6-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-254">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cc6f6-255">In Global Catalog</span></span>      | <span data-ttu-id="cc6f6-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="cc6f6-256">False</span></span>                                                             |
| <span data-ttu-id="cc6f6-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cc6f6-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="cc6f6-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cc6f6-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="cc6f6-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cc6f6-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cc6f6-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="cc6f6-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-261">Search-Flags</span></span>           | <span data-ttu-id="cc6f6-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cc6f6-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="cc6f6-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cc6f6-263">System-Flags</span></span>           | <span data-ttu-id="cc6f6-264">0x00000014</span><span class="sxs-lookup"><span data-stu-id="cc6f6-264">0x00000014</span></span>                                                        |
| <span data-ttu-id="cc6f6-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cc6f6-265">Classes used in</span></span>        | [<span data-ttu-id="cc6f6-266">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="cc6f6-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





