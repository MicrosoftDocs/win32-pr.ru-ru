---
title: Атрибут ms-DS-Allowed-to-Delegate
description: Это атрибут для объектов учетной записи службы (компьютера или учетной записи пользователя).
ms.assetid: a370174e-fd00-4f47-b23c-b0cc2657cee7
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Active-DS-Allow-to-Delegate
- Схема AD атрибута msDS-Алловедтоделегатето
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Delegate-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9562442d20053848e48cd2b1d501e65611f7d2a9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655215"
---
# <a name="ms-ds-allowed-to-delegate-to-attribute"></a><span data-ttu-id="824d8-105">Атрибут ms-DS-Allowed-to-Delegate</span><span class="sxs-lookup"><span data-stu-id="824d8-105">ms-DS-Allowed-To-Delegate-To attribute</span></span>

<span data-ttu-id="824d8-106">Это атрибут для объектов учетной записи службы (компьютера или учетной записи пользователя).</span><span class="sxs-lookup"><span data-stu-id="824d8-106">This is an attribute on service account (computer or user account) objects.</span></span> <span data-ttu-id="824d8-107">Он содержит список имен субъектов-служб (SPN).</span><span class="sxs-lookup"><span data-stu-id="824d8-107">It contains a list of Service Principal Names (SPNs).</span></span> <span data-ttu-id="824d8-108">Этот атрибут используется для настройки службы таким образом, чтобы она могла получать билеты службы, которые можно использовать для ограниченного делегирования.</span><span class="sxs-lookup"><span data-stu-id="824d8-108">This attribute is used to configure a service so that it can obtain service tickets that can be used for Constrained Delegation.</span></span>



| <span data-ttu-id="824d8-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="824d8-109">Entry</span></span> | <span data-ttu-id="824d8-110">Значение</span><span class="sxs-lookup"><span data-stu-id="824d8-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="824d8-111">CN</span><span class="sxs-lookup"><span data-stu-id="824d8-111">CN</span></span>                | <span data-ttu-id="824d8-112">MS-DS-Allowed-to-Delegate-to</span><span class="sxs-lookup"><span data-stu-id="824d8-112">ms-DS-Allowed-To-Delegate-To</span></span>                |
| <span data-ttu-id="824d8-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="824d8-113">Ldap-Display-Name</span></span> | <span data-ttu-id="824d8-114">msDS-Алловедтоделегатето</span><span class="sxs-lookup"><span data-stu-id="824d8-114">msDS-AllowedToDelegateTo</span></span>                    |
| <span data-ttu-id="824d8-115">Размер</span><span class="sxs-lookup"><span data-stu-id="824d8-115">Size</span></span>              | <span data-ttu-id="824d8-116">от 0 до 64 КБ</span><span class="sxs-lookup"><span data-stu-id="824d8-116">0 to 64K</span></span>                                    |
| <span data-ttu-id="824d8-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="824d8-117">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="824d8-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="824d8-118">Update Frequency</span></span>  | <span data-ttu-id="824d8-119">Редко</span><span class="sxs-lookup"><span data-stu-id="824d8-119">Infrequently</span></span>                                |
| <span data-ttu-id="824d8-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="824d8-120">Attribute-Id</span></span>      | <span data-ttu-id="824d8-121">1.2.840.113556.1.4.1787</span><span class="sxs-lookup"><span data-stu-id="824d8-121">1.2.840.113556.1.4.1787</span></span>                     |
| <span data-ttu-id="824d8-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="824d8-122">System-Id-Guid</span></span>    | <span data-ttu-id="824d8-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span><span class="sxs-lookup"><span data-stu-id="824d8-123">800d94d7-b7a1-42a1-b14d-7cae1423d07f</span></span>        |
| <span data-ttu-id="824d8-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="824d8-124">Syntax</span></span>            | [<span data-ttu-id="824d8-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="824d8-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="824d8-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="824d8-126">Implementations</span></span>

-   [<span data-ttu-id="824d8-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="824d8-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="824d8-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="824d8-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="824d8-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="824d8-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="824d8-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="824d8-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="824d8-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="824d8-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="824d8-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="824d8-132">Windows Server 2003</span></span>



| <span data-ttu-id="824d8-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="824d8-133">Entry</span></span> | <span data-ttu-id="824d8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="824d8-134">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="824d8-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="824d8-135">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d8-136">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d8-137">System-Only</span></span>            | <span data-ttu-id="824d8-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-138">False</span></span>                                                              |
| <span data-ttu-id="824d8-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="824d8-139">Is-Single-Valued</span></span>       | <span data-ttu-id="824d8-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-140">False</span></span>                                                              |
| <span data-ttu-id="824d8-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="824d8-141">Is Indexed</span></span>             | <span data-ttu-id="824d8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-142">False</span></span>                                                              |
| <span data-ttu-id="824d8-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="824d8-143">In Global Catalog</span></span>      | <span data-ttu-id="824d8-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-144">False</span></span>                                                              |
| <span data-ttu-id="824d8-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="824d8-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d8-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="824d8-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="824d8-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d8-147">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d8-148">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-149">Search-Flags</span></span>           | <span data-ttu-id="824d8-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d8-150">0x00000000</span></span>                                                         |
| <span data-ttu-id="824d8-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-151">System-Flags</span></span>           | <span data-ttu-id="824d8-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d8-152">0x00000010</span></span>                                                         |
| <span data-ttu-id="824d8-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="824d8-153">Classes used in</span></span>        | [<span data-ttu-id="824d8-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="824d8-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="824d8-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="824d8-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="824d8-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="824d8-156">Entry</span></span> | <span data-ttu-id="824d8-157">Значение</span><span class="sxs-lookup"><span data-stu-id="824d8-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="824d8-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="824d8-158">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d8-159">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d8-160">System-Only</span></span>            | <span data-ttu-id="824d8-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-161">False</span></span>                                                              |
| <span data-ttu-id="824d8-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="824d8-162">Is-Single-Valued</span></span>       | <span data-ttu-id="824d8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-163">False</span></span>                                                              |
| <span data-ttu-id="824d8-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="824d8-164">Is Indexed</span></span>             | <span data-ttu-id="824d8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-165">False</span></span>                                                              |
| <span data-ttu-id="824d8-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="824d8-166">In Global Catalog</span></span>      | <span data-ttu-id="824d8-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-167">False</span></span>                                                              |
| <span data-ttu-id="824d8-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="824d8-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d8-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="824d8-169">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="824d8-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d8-170">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d8-171">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-172">Search-Flags</span></span>           | <span data-ttu-id="824d8-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d8-173">0x00000000</span></span>                                                         |
| <span data-ttu-id="824d8-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-174">System-Flags</span></span>           | <span data-ttu-id="824d8-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d8-175">0x00000010</span></span>                                                         |
| <span data-ttu-id="824d8-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="824d8-176">Classes used in</span></span>        | [<span data-ttu-id="824d8-177">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="824d8-177">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="824d8-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="824d8-178">Windows Server 2008</span></span>



| <span data-ttu-id="824d8-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="824d8-179">Entry</span></span> | <span data-ttu-id="824d8-180">Значение</span><span class="sxs-lookup"><span data-stu-id="824d8-180">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="824d8-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="824d8-181">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d8-182">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d8-183">System-Only</span></span>            | <span data-ttu-id="824d8-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-184">False</span></span>                                                              |
| <span data-ttu-id="824d8-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="824d8-185">Is-Single-Valued</span></span>       | <span data-ttu-id="824d8-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-186">False</span></span>                                                              |
| <span data-ttu-id="824d8-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="824d8-187">Is Indexed</span></span>             | <span data-ttu-id="824d8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-188">False</span></span>                                                              |
| <span data-ttu-id="824d8-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="824d8-189">In Global Catalog</span></span>      | <span data-ttu-id="824d8-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-190">False</span></span>                                                              |
| <span data-ttu-id="824d8-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="824d8-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d8-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="824d8-192">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="824d8-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d8-193">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d8-194">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-195">Search-Flags</span></span>           | <span data-ttu-id="824d8-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d8-196">0x00000000</span></span>                                                         |
| <span data-ttu-id="824d8-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-197">System-Flags</span></span>           | <span data-ttu-id="824d8-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d8-198">0x00000010</span></span>                                                         |
| <span data-ttu-id="824d8-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="824d8-199">Classes used in</span></span>        | [<span data-ttu-id="824d8-200">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="824d8-200">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="824d8-201">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="824d8-201">Windows Server 2008 R2</span></span>



| <span data-ttu-id="824d8-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="824d8-202">Entry</span></span> | <span data-ttu-id="824d8-203">Значение</span><span class="sxs-lookup"><span data-stu-id="824d8-203">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="824d8-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="824d8-204">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d8-205">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d8-206">System-Only</span></span>            | <span data-ttu-id="824d8-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-207">False</span></span>                                                              |
| <span data-ttu-id="824d8-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="824d8-208">Is-Single-Valued</span></span>       | <span data-ttu-id="824d8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-209">False</span></span>                                                              |
| <span data-ttu-id="824d8-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="824d8-210">Is Indexed</span></span>             | <span data-ttu-id="824d8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-211">False</span></span>                                                              |
| <span data-ttu-id="824d8-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="824d8-212">In Global Catalog</span></span>      | <span data-ttu-id="824d8-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-213">False</span></span>                                                              |
| <span data-ttu-id="824d8-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="824d8-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d8-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="824d8-215">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="824d8-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d8-216">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d8-217">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-218">Search-Flags</span></span>           | <span data-ttu-id="824d8-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d8-219">0x00000000</span></span>                                                         |
| <span data-ttu-id="824d8-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-220">System-Flags</span></span>           | <span data-ttu-id="824d8-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d8-221">0x00000010</span></span>                                                         |
| <span data-ttu-id="824d8-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="824d8-222">Classes used in</span></span>        | [<span data-ttu-id="824d8-223">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="824d8-223">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="824d8-224">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="824d8-224">Windows Server 2012</span></span>



| <span data-ttu-id="824d8-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="824d8-225">Entry</span></span> | <span data-ttu-id="824d8-226">Значение</span><span class="sxs-lookup"><span data-stu-id="824d8-226">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="824d8-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="824d8-227">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="824d8-228">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="824d8-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="824d8-229">System-Only</span></span>            | <span data-ttu-id="824d8-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-230">False</span></span>                                                              |
| <span data-ttu-id="824d8-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="824d8-231">Is-Single-Valued</span></span>       | <span data-ttu-id="824d8-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-232">False</span></span>                                                              |
| <span data-ttu-id="824d8-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="824d8-233">Is Indexed</span></span>             | <span data-ttu-id="824d8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-234">False</span></span>                                                              |
| <span data-ttu-id="824d8-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="824d8-235">In Global Catalog</span></span>      | <span data-ttu-id="824d8-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="824d8-236">False</span></span>                                                              |
| <span data-ttu-id="824d8-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="824d8-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="824d8-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="824d8-238">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="824d8-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="824d8-239">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="824d8-240">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="824d8-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-241">Search-Flags</span></span>           | <span data-ttu-id="824d8-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="824d8-242">0x00000000</span></span>                                                         |
| <span data-ttu-id="824d8-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="824d8-243">System-Flags</span></span>           | <span data-ttu-id="824d8-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="824d8-244">0x00000010</span></span>                                                         |
| <span data-ttu-id="824d8-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="824d8-245">Classes used in</span></span>        | [<span data-ttu-id="824d8-246">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="824d8-246">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





