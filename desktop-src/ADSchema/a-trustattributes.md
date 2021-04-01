---
title: Атрибут Trust-Attributes
description: Этот атрибут хранит атрибуты доверия для доверенного домена.
ms.assetid: c85b98a6-4d09-4eb2-821b-58ef558b3460
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Attributes
- Схема AD атрибута Трустаттрибутес
topic_type:
- apiref
api_name:
- Trust-Attributes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81dc06f73fbda5dab7ce8d2a07bfc90323d2b29
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804811"
---
# <a name="trust-attributes-attribute"></a><span data-ttu-id="c3314-105">Атрибут Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="c3314-105">Trust-Attributes attribute</span></span>

<span data-ttu-id="c3314-106">Этот атрибут хранит атрибуты доверия для доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="c3314-106">This attribute stores the trust attributes for a trusted domain.</span></span> <span data-ttu-id="c3314-107">Возможны следующие значения атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c3314-107">Possible attribute values are as follows:</span></span>

-   <span data-ttu-id="c3314-108">\_Атрибут доверия \_ , не являющийся \_ транзитивным, отключает транзитивность.</span><span class="sxs-lookup"><span data-stu-id="c3314-108">TRUST\_ATTRIBUTE\_NON\_TRANSITIVE Disable transitivity.</span></span>
-   <span data-ttu-id="c3314-109">\_ \_ \_ Родительское доверие дерева атрибута доверия установлено в родительский элемент дерева Организации.</span><span class="sxs-lookup"><span data-stu-id="c3314-109">TRUST\_ATTRIBUTE\_TREE\_PARENT Trust is set to the organization tree parent.</span></span>
-   <span data-ttu-id="c3314-110">ДОВЕРИЕ \_ \_ \_ корневым доверием дерева атрибута доверия с другим корнем дерева в лесу.</span><span class="sxs-lookup"><span data-stu-id="c3314-110">TRUST\_ATTRIBUTE\_TREE\_ROOT Trust set to another tree root in the forest.</span></span>
-   <span data-ttu-id="c3314-111">\_Атрибут доверия \_ \_ только надежная ссылка допустима только для клиентов верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="c3314-111">TRUST\_ATTRIBUTE\_UPLEVEL\_ONLY Trusted link valid only for uplevel client.</span></span>



| <span data-ttu-id="c3314-112">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-112">Entry</span></span> | <span data-ttu-id="c3314-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-113">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c3314-114">CN</span><span class="sxs-lookup"><span data-stu-id="c3314-114">CN</span></span>                | <span data-ttu-id="c3314-115">Trust-Attributes</span><span class="sxs-lookup"><span data-stu-id="c3314-115">Trust-Attributes</span></span>                     |
| <span data-ttu-id="c3314-116">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c3314-116">Ldap-Display-Name</span></span> | <span data-ttu-id="c3314-117">трустаттрибутес</span><span class="sxs-lookup"><span data-stu-id="c3314-117">trustAttributes</span></span>                      |
| <span data-ttu-id="c3314-118">Размер</span><span class="sxs-lookup"><span data-stu-id="c3314-118">Size</span></span>              | \-                                   |
| <span data-ttu-id="c3314-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c3314-119">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c3314-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c3314-120">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c3314-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-121">Attribute-Id</span></span>      | <span data-ttu-id="c3314-122">1.2.840.113556.1.4.470</span><span class="sxs-lookup"><span data-stu-id="c3314-122">1.2.840.113556.1.4.470</span></span>               |
| <span data-ttu-id="c3314-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c3314-123">System-Id-Guid</span></span>    | <span data-ttu-id="c3314-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="c3314-124">80a67e5a-9f22-11d0-afdd-00c04fd930c9</span></span> |
| <span data-ttu-id="c3314-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3314-125">Syntax</span></span>            | [<span data-ttu-id="c3314-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="c3314-126">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c3314-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c3314-127">Implementations</span></span>

-   [<span data-ttu-id="c3314-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c3314-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c3314-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c3314-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c3314-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c3314-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c3314-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c3314-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c3314-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c3314-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c3314-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c3314-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c3314-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c3314-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c3314-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-135">Entry</span></span> | <span data-ttu-id="c3314-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-136">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c3314-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c3314-137">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-138">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3314-139">System-Only</span></span>            | <span data-ttu-id="c3314-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-140">False</span></span>                                                |
| <span data-ttu-id="c3314-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c3314-141">Is-Single-Valued</span></span>       | <span data-ttu-id="c3314-142">True</span><span class="sxs-lookup"><span data-stu-id="c3314-142">True</span></span>                                                 |
| <span data-ttu-id="c3314-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c3314-143">Is Indexed</span></span>             | <span data-ttu-id="c3314-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-144">False</span></span>                                                |
| <span data-ttu-id="c3314-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c3314-145">In Global Catalog</span></span>      | <span data-ttu-id="c3314-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-146">False</span></span>                                                |
| <span data-ttu-id="c3314-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c3314-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3314-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3314-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c3314-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3314-149">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3314-150">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-151">Search-Flags</span></span>           | <span data-ttu-id="c3314-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3314-152">0x00000000</span></span>                                           |
| <span data-ttu-id="c3314-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-153">System-Flags</span></span>           | <span data-ttu-id="c3314-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3314-154">0x00000010</span></span>                                           |
| <span data-ttu-id="c3314-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c3314-155">Classes used in</span></span>        | [<span data-ttu-id="c3314-156">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="c3314-156">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c3314-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c3314-157">Windows Server 2003</span></span>



| <span data-ttu-id="c3314-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-158">Entry</span></span> | <span data-ttu-id="c3314-159">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-159">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c3314-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c3314-160">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-161">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3314-162">System-Only</span></span>            | <span data-ttu-id="c3314-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-163">False</span></span>                                                |
| <span data-ttu-id="c3314-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c3314-164">Is-Single-Valued</span></span>       | <span data-ttu-id="c3314-165">True</span><span class="sxs-lookup"><span data-stu-id="c3314-165">True</span></span>                                                 |
| <span data-ttu-id="c3314-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c3314-166">Is Indexed</span></span>             | <span data-ttu-id="c3314-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-167">False</span></span>                                                |
| <span data-ttu-id="c3314-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c3314-168">In Global Catalog</span></span>      | <span data-ttu-id="c3314-169">True</span><span class="sxs-lookup"><span data-stu-id="c3314-169">True</span></span>                                                 |
| <span data-ttu-id="c3314-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c3314-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3314-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3314-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c3314-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3314-172">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3314-173">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-174">Search-Flags</span></span>           | <span data-ttu-id="c3314-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3314-175">0x00000000</span></span>                                           |
| <span data-ttu-id="c3314-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-176">System-Flags</span></span>           | <span data-ttu-id="c3314-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3314-177">0x00000010</span></span>                                           |
| <span data-ttu-id="c3314-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c3314-178">Classes used in</span></span>        | [<span data-ttu-id="c3314-179">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="c3314-179">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c3314-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c3314-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c3314-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-181">Entry</span></span> | <span data-ttu-id="c3314-182">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-182">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c3314-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c3314-183">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-184">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3314-185">System-Only</span></span>            | <span data-ttu-id="c3314-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-186">False</span></span>                                                |
| <span data-ttu-id="c3314-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c3314-187">Is-Single-Valued</span></span>       | <span data-ttu-id="c3314-188">True</span><span class="sxs-lookup"><span data-stu-id="c3314-188">True</span></span>                                                 |
| <span data-ttu-id="c3314-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c3314-189">Is Indexed</span></span>             | <span data-ttu-id="c3314-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-190">False</span></span>                                                |
| <span data-ttu-id="c3314-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c3314-191">In Global Catalog</span></span>      | <span data-ttu-id="c3314-192">True</span><span class="sxs-lookup"><span data-stu-id="c3314-192">True</span></span>                                                 |
| <span data-ttu-id="c3314-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c3314-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3314-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3314-194">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c3314-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3314-195">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3314-196">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-197">Search-Flags</span></span>           | <span data-ttu-id="c3314-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3314-198">0x00000000</span></span>                                           |
| <span data-ttu-id="c3314-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-199">System-Flags</span></span>           | <span data-ttu-id="c3314-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3314-200">0x00000010</span></span>                                           |
| <span data-ttu-id="c3314-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c3314-201">Classes used in</span></span>        | [<span data-ttu-id="c3314-202">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="c3314-202">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c3314-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3314-203">Windows Server 2008</span></span>



| <span data-ttu-id="c3314-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-204">Entry</span></span> | <span data-ttu-id="c3314-205">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-205">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c3314-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c3314-206">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-207">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3314-208">System-Only</span></span>            | <span data-ttu-id="c3314-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-209">False</span></span>                                                |
| <span data-ttu-id="c3314-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c3314-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c3314-211">True</span><span class="sxs-lookup"><span data-stu-id="c3314-211">True</span></span>                                                 |
| <span data-ttu-id="c3314-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c3314-212">Is Indexed</span></span>             | <span data-ttu-id="c3314-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-213">False</span></span>                                                |
| <span data-ttu-id="c3314-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c3314-214">In Global Catalog</span></span>      | <span data-ttu-id="c3314-215">True</span><span class="sxs-lookup"><span data-stu-id="c3314-215">True</span></span>                                                 |
| <span data-ttu-id="c3314-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c3314-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3314-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3314-217">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c3314-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3314-218">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3314-219">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-220">Search-Flags</span></span>           | <span data-ttu-id="c3314-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3314-221">0x00000000</span></span>                                           |
| <span data-ttu-id="c3314-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-222">System-Flags</span></span>           | <span data-ttu-id="c3314-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3314-223">0x00000010</span></span>                                           |
| <span data-ttu-id="c3314-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c3314-224">Classes used in</span></span>        | [<span data-ttu-id="c3314-225">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="c3314-225">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c3314-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c3314-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c3314-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-227">Entry</span></span> | <span data-ttu-id="c3314-228">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-228">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c3314-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c3314-229">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-230">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3314-231">System-Only</span></span>            | <span data-ttu-id="c3314-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-232">False</span></span>                                                |
| <span data-ttu-id="c3314-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c3314-233">Is-Single-Valued</span></span>       | <span data-ttu-id="c3314-234">True</span><span class="sxs-lookup"><span data-stu-id="c3314-234">True</span></span>                                                 |
| <span data-ttu-id="c3314-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c3314-235">Is Indexed</span></span>             | <span data-ttu-id="c3314-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-236">False</span></span>                                                |
| <span data-ttu-id="c3314-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c3314-237">In Global Catalog</span></span>      | <span data-ttu-id="c3314-238">True</span><span class="sxs-lookup"><span data-stu-id="c3314-238">True</span></span>                                                 |
| <span data-ttu-id="c3314-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c3314-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3314-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3314-240">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c3314-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3314-241">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3314-242">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-243">Search-Flags</span></span>           | <span data-ttu-id="c3314-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3314-244">0x00000000</span></span>                                           |
| <span data-ttu-id="c3314-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-245">System-Flags</span></span>           | <span data-ttu-id="c3314-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3314-246">0x00000010</span></span>                                           |
| <span data-ttu-id="c3314-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c3314-247">Classes used in</span></span>        | [<span data-ttu-id="c3314-248">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="c3314-248">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c3314-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3314-249">Windows Server 2012</span></span>



| <span data-ttu-id="c3314-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="c3314-250">Entry</span></span> | <span data-ttu-id="c3314-251">Значение</span><span class="sxs-lookup"><span data-stu-id="c3314-251">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c3314-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c3314-252">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c3314-253">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c3314-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="c3314-254">System-Only</span></span>            | <span data-ttu-id="c3314-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-255">False</span></span>                                                |
| <span data-ttu-id="c3314-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c3314-256">Is-Single-Valued</span></span>       | <span data-ttu-id="c3314-257">True</span><span class="sxs-lookup"><span data-stu-id="c3314-257">True</span></span>                                                 |
| <span data-ttu-id="c3314-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c3314-258">Is Indexed</span></span>             | <span data-ttu-id="c3314-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c3314-259">False</span></span>                                                |
| <span data-ttu-id="c3314-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c3314-260">In Global Catalog</span></span>      | <span data-ttu-id="c3314-261">True</span><span class="sxs-lookup"><span data-stu-id="c3314-261">True</span></span>                                                 |
| <span data-ttu-id="c3314-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c3314-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="c3314-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c3314-263">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c3314-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c3314-264">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c3314-265">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="c3314-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-266">Search-Flags</span></span>           | <span data-ttu-id="c3314-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3314-267">0x00000000</span></span>                                           |
| <span data-ttu-id="c3314-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c3314-268">System-Flags</span></span>           | <span data-ttu-id="c3314-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c3314-269">0x00000010</span></span>                                           |
| <span data-ttu-id="c3314-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c3314-270">Classes used in</span></span>        | [<span data-ttu-id="c3314-271">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="c3314-271">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





