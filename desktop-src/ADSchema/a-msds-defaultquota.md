---
title: атрибут квоты MS-DS-Default-
description: Квота по умолчанию, которая будет применяться к субъекту безопасности, который создает объект в NC, если не существует спецификации квоты, охватывающей субъект безопасности.
ms.assetid: 48074aaa-3997-40ac-92fe-b3112408ab45
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута квоты MS-DS-Default
- Схема AD атрибута msDS-Дефаулткуота
topic_type:
- apiref
api_name:
- ms-DS-Default-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96f1429be72c623843608856da88729b1240c38
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989827"
---
# <a name="ms-ds-default-quota-attribute"></a><span data-ttu-id="a34fc-105">атрибут квоты MS-DS-Default-</span><span class="sxs-lookup"><span data-stu-id="a34fc-105">ms-DS-Default-Quota attribute</span></span>

<span data-ttu-id="a34fc-106">Квота по умолчанию, которая будет применяться к субъекту безопасности, который создает объект в NC, если не существует спецификации квоты, охватывающей субъект безопасности.</span><span class="sxs-lookup"><span data-stu-id="a34fc-106">The default quota that will apply to a security principal that creates an object in the NC if no quota specification exists that covers the security principal.</span></span>



| <span data-ttu-id="a34fc-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-107">Entry</span></span> | <span data-ttu-id="a34fc-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a34fc-109">CN</span><span class="sxs-lookup"><span data-stu-id="a34fc-109">CN</span></span>                | <span data-ttu-id="a34fc-110">MS-DS-Default-квота</span><span class="sxs-lookup"><span data-stu-id="a34fc-110">ms-DS-Default-Quota</span></span>                  |
| <span data-ttu-id="a34fc-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a34fc-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a34fc-112">msDS-Дефаулткуота</span><span class="sxs-lookup"><span data-stu-id="a34fc-112">msDS-DefaultQuota</span></span>                    |
| <span data-ttu-id="a34fc-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a34fc-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="a34fc-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a34fc-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a34fc-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a34fc-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a34fc-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-116">Attribute-Id</span></span>      | <span data-ttu-id="a34fc-117">1.2.840.113556.1.4.1846</span><span class="sxs-lookup"><span data-stu-id="a34fc-117">1.2.840.113556.1.4.1846</span></span>              |
| <span data-ttu-id="a34fc-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a34fc-118">System-Id-Guid</span></span>    | <span data-ttu-id="a34fc-119">6818f726-674b-441b-8a3a-f40596374cea</span><span class="sxs-lookup"><span data-stu-id="a34fc-119">6818f726-674b-441b-8a3a-f40596374cea</span></span> |
| <span data-ttu-id="a34fc-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a34fc-120">Syntax</span></span>            | [<span data-ttu-id="a34fc-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a34fc-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a34fc-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a34fc-122">Implementations</span></span>

-   [<span data-ttu-id="a34fc-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a34fc-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a34fc-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a34fc-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a34fc-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a34fc-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a34fc-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a34fc-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a34fc-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a34fc-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a34fc-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a34fc-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a34fc-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a34fc-129">Windows Server 2003</span></span>



| <span data-ttu-id="a34fc-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-130">Entry</span></span> | <span data-ttu-id="a34fc-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a34fc-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a34fc-132">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-133">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a34fc-134">System-Only</span></span>            | <span data-ttu-id="a34fc-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-135">False</span></span>                                                             |
| <span data-ttu-id="a34fc-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a34fc-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a34fc-137">True</span><span class="sxs-lookup"><span data-stu-id="a34fc-137">True</span></span>                                                              |
| <span data-ttu-id="a34fc-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a34fc-138">Is Indexed</span></span>             | <span data-ttu-id="a34fc-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-139">False</span></span>                                                             |
| <span data-ttu-id="a34fc-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a34fc-140">In Global Catalog</span></span>      | <span data-ttu-id="a34fc-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-141">False</span></span>                                                             |
| <span data-ttu-id="a34fc-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a34fc-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a34fc-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a34fc-143">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a34fc-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a34fc-144">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a34fc-145">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-146">Search-Flags</span></span>           | <span data-ttu-id="a34fc-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a34fc-147">0x00000000</span></span>                                                        |
| <span data-ttu-id="a34fc-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-148">System-Flags</span></span>           | <span data-ttu-id="a34fc-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a34fc-149">0x00000010</span></span>                                                        |
| <span data-ttu-id="a34fc-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a34fc-150">Classes used in</span></span>        | [<span data-ttu-id="a34fc-151">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="a34fc-151">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a34fc-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="a34fc-152">ADAM</span></span>



| <span data-ttu-id="a34fc-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-153">Entry</span></span> | <span data-ttu-id="a34fc-154">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a34fc-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a34fc-155">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-156">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a34fc-157">System-Only</span></span>            | <span data-ttu-id="a34fc-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-158">False</span></span>                                                             |
| <span data-ttu-id="a34fc-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a34fc-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a34fc-160">True</span><span class="sxs-lookup"><span data-stu-id="a34fc-160">True</span></span>                                                              |
| <span data-ttu-id="a34fc-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a34fc-161">Is Indexed</span></span>             | <span data-ttu-id="a34fc-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-162">False</span></span>                                                             |
| <span data-ttu-id="a34fc-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a34fc-163">In Global Catalog</span></span>      | <span data-ttu-id="a34fc-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-164">False</span></span>                                                             |
| <span data-ttu-id="a34fc-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a34fc-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a34fc-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a34fc-166">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a34fc-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a34fc-167">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a34fc-168">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-169">Search-Flags</span></span>           | <span data-ttu-id="a34fc-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a34fc-170">0x00000000</span></span>                                                        |
| <span data-ttu-id="a34fc-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-171">System-Flags</span></span>           | <span data-ttu-id="a34fc-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a34fc-172">0x00000010</span></span>                                                        |
| <span data-ttu-id="a34fc-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a34fc-173">Classes used in</span></span>        | [<span data-ttu-id="a34fc-174">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="a34fc-174">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a34fc-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a34fc-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a34fc-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-176">Entry</span></span> | <span data-ttu-id="a34fc-177">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a34fc-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a34fc-178">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-179">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a34fc-180">System-Only</span></span>            | <span data-ttu-id="a34fc-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-181">False</span></span>                                                             |
| <span data-ttu-id="a34fc-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a34fc-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a34fc-183">True</span><span class="sxs-lookup"><span data-stu-id="a34fc-183">True</span></span>                                                              |
| <span data-ttu-id="a34fc-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a34fc-184">Is Indexed</span></span>             | <span data-ttu-id="a34fc-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-185">False</span></span>                                                             |
| <span data-ttu-id="a34fc-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a34fc-186">In Global Catalog</span></span>      | <span data-ttu-id="a34fc-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-187">False</span></span>                                                             |
| <span data-ttu-id="a34fc-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a34fc-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a34fc-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a34fc-189">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a34fc-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a34fc-190">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a34fc-191">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-192">Search-Flags</span></span>           | <span data-ttu-id="a34fc-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a34fc-193">0x00000000</span></span>                                                        |
| <span data-ttu-id="a34fc-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-194">System-Flags</span></span>           | <span data-ttu-id="a34fc-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a34fc-195">0x00000010</span></span>                                                        |
| <span data-ttu-id="a34fc-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a34fc-196">Classes used in</span></span>        | [<span data-ttu-id="a34fc-197">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="a34fc-197">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a34fc-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a34fc-198">Windows Server 2008</span></span>



| <span data-ttu-id="a34fc-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-199">Entry</span></span> | <span data-ttu-id="a34fc-200">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a34fc-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a34fc-201">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-202">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a34fc-203">System-Only</span></span>            | <span data-ttu-id="a34fc-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-204">False</span></span>                                                             |
| <span data-ttu-id="a34fc-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a34fc-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a34fc-206">True</span><span class="sxs-lookup"><span data-stu-id="a34fc-206">True</span></span>                                                              |
| <span data-ttu-id="a34fc-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a34fc-207">Is Indexed</span></span>             | <span data-ttu-id="a34fc-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-208">False</span></span>                                                             |
| <span data-ttu-id="a34fc-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a34fc-209">In Global Catalog</span></span>      | <span data-ttu-id="a34fc-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-210">False</span></span>                                                             |
| <span data-ttu-id="a34fc-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a34fc-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a34fc-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a34fc-212">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a34fc-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a34fc-213">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a34fc-214">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-215">Search-Flags</span></span>           | <span data-ttu-id="a34fc-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a34fc-216">0x00000000</span></span>                                                        |
| <span data-ttu-id="a34fc-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-217">System-Flags</span></span>           | <span data-ttu-id="a34fc-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a34fc-218">0x00000010</span></span>                                                        |
| <span data-ttu-id="a34fc-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a34fc-219">Classes used in</span></span>        | [<span data-ttu-id="a34fc-220">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="a34fc-220">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a34fc-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a34fc-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a34fc-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-222">Entry</span></span> | <span data-ttu-id="a34fc-223">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a34fc-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a34fc-224">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-225">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a34fc-226">System-Only</span></span>            | <span data-ttu-id="a34fc-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-227">False</span></span>                                                             |
| <span data-ttu-id="a34fc-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a34fc-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a34fc-229">True</span><span class="sxs-lookup"><span data-stu-id="a34fc-229">True</span></span>                                                              |
| <span data-ttu-id="a34fc-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a34fc-230">Is Indexed</span></span>             | <span data-ttu-id="a34fc-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-231">False</span></span>                                                             |
| <span data-ttu-id="a34fc-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a34fc-232">In Global Catalog</span></span>      | <span data-ttu-id="a34fc-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-233">False</span></span>                                                             |
| <span data-ttu-id="a34fc-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a34fc-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a34fc-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a34fc-235">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a34fc-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a34fc-236">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a34fc-237">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-238">Search-Flags</span></span>           | <span data-ttu-id="a34fc-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a34fc-239">0x00000000</span></span>                                                        |
| <span data-ttu-id="a34fc-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-240">System-Flags</span></span>           | <span data-ttu-id="a34fc-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a34fc-241">0x00000010</span></span>                                                        |
| <span data-ttu-id="a34fc-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a34fc-242">Classes used in</span></span>        | [<span data-ttu-id="a34fc-243">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="a34fc-243">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a34fc-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a34fc-244">Windows Server 2012</span></span>



| <span data-ttu-id="a34fc-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="a34fc-245">Entry</span></span> | <span data-ttu-id="a34fc-246">Значение</span><span class="sxs-lookup"><span data-stu-id="a34fc-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a34fc-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a34fc-247">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a34fc-248">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="a34fc-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="a34fc-249">System-Only</span></span>            | <span data-ttu-id="a34fc-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-250">False</span></span>                                                             |
| <span data-ttu-id="a34fc-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a34fc-251">Is-Single-Valued</span></span>       | <span data-ttu-id="a34fc-252">True</span><span class="sxs-lookup"><span data-stu-id="a34fc-252">True</span></span>                                                              |
| <span data-ttu-id="a34fc-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a34fc-253">Is Indexed</span></span>             | <span data-ttu-id="a34fc-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-254">False</span></span>                                                             |
| <span data-ttu-id="a34fc-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a34fc-255">In Global Catalog</span></span>      | <span data-ttu-id="a34fc-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="a34fc-256">False</span></span>                                                             |
| <span data-ttu-id="a34fc-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a34fc-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="a34fc-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a34fc-258">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="a34fc-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a34fc-259">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a34fc-260">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="a34fc-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-261">Search-Flags</span></span>           | <span data-ttu-id="a34fc-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a34fc-262">0x00000000</span></span>                                                        |
| <span data-ttu-id="a34fc-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a34fc-263">System-Flags</span></span>           | <span data-ttu-id="a34fc-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a34fc-264">0x00000010</span></span>                                                        |
| <span data-ttu-id="a34fc-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a34fc-265">Classes used in</span></span>        | [<span data-ttu-id="a34fc-266">**Контейнер MS-DS-Quota-**</span><span class="sxs-lookup"><span data-stu-id="a34fc-266">**ms-DS-Quota-Container**</span></span>](c-msds-quotacontainer.md)<br/> |



 

 





