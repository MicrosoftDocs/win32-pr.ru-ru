---
title: Атрибут "домен-политика-ссылка"
description: Различающееся имя объекта политики домена, из которого копируется объект политики.
ms.assetid: 914920de-6dc2-4dda-bf10-a34f5315eb74
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута, ссылающаяся на политику домена
- Схема AD атрибута Домаинполициреференце
topic_type:
- apiref
api_name:
- Domain-Policy-Reference
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9723abde3bd04dc9c50f6b4c00f1ed80c4da0c2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989533"
---
# <a name="domain-policy-reference-attribute"></a><span data-ttu-id="4cd3d-105">Атрибут "домен-политика-ссылка"</span><span class="sxs-lookup"><span data-stu-id="4cd3d-105">Domain-Policy-Reference attribute</span></span>

<span data-ttu-id="4cd3d-106">Различающееся имя объекта политики домена, из которого копируется объект политики.</span><span class="sxs-lookup"><span data-stu-id="4cd3d-106">The Distinguished Name of a domain policy object that a policy object copies from.</span></span>



| <span data-ttu-id="4cd3d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-107">Entry</span></span> | <span data-ttu-id="4cd3d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="4cd3d-109">CN</span><span class="sxs-lookup"><span data-stu-id="4cd3d-109">CN</span></span>                | <span data-ttu-id="4cd3d-110">Справочник по политикам домена</span><span class="sxs-lookup"><span data-stu-id="4cd3d-110">Domain-Policy-Reference</span></span>                 |
| <span data-ttu-id="4cd3d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4cd3d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4cd3d-112">домаинполициреференце</span><span class="sxs-lookup"><span data-stu-id="4cd3d-112">domainPolicyReference</span></span>                   |
| <span data-ttu-id="4cd3d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4cd3d-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="4cd3d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4cd3d-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="4cd3d-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4cd3d-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="4cd3d-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-116">Attribute-Id</span></span>      | <span data-ttu-id="4cd3d-117">1.2.840.113556.1.4.422</span><span class="sxs-lookup"><span data-stu-id="4cd3d-117">1.2.840.113556.1.4.422</span></span>                  |
| <span data-ttu-id="4cd3d-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4cd3d-118">System-Id-Guid</span></span>    | <span data-ttu-id="4cd3d-119">80a67e2a-9f22-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="4cd3d-119">80a67e2a-9f22-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="4cd3d-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cd3d-120">Syntax</span></span>            | [<span data-ttu-id="4cd3d-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="4cd3d-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4cd3d-122">Implementations</span></span>

-   [<span data-ttu-id="4cd3d-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4cd3d-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4cd3d-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4cd3d-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4cd3d-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4cd3d-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4cd3d-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4cd3d-129">Windows 2000 Server</span></span>



| <span data-ttu-id="4cd3d-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-130">Entry</span></span> | <span data-ttu-id="4cd3d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-131">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="4cd3d-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd3d-132">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-133">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cd3d-134">System-Only</span></span>            | <span data-ttu-id="4cd3d-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-135">False</span></span>                                              |
| <span data-ttu-id="4cd3d-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4cd3d-136">Is-Single-Valued</span></span>       | <span data-ttu-id="4cd3d-137">True</span><span class="sxs-lookup"><span data-stu-id="4cd3d-137">True</span></span>                                               |
| <span data-ttu-id="4cd3d-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4cd3d-138">Is Indexed</span></span>             | <span data-ttu-id="4cd3d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-139">False</span></span>                                              |
| <span data-ttu-id="4cd3d-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4cd3d-140">In Global Catalog</span></span>      | <span data-ttu-id="4cd3d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-141">False</span></span>                                              |
| <span data-ttu-id="4cd3d-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4cd3d-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cd3d-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4cd3d-143">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="4cd3d-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cd3d-144">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cd3d-145">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-146">Search-Flags</span></span>           | <span data-ttu-id="4cd3d-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cd3d-147">0x00000000</span></span>                                         |
| <span data-ttu-id="4cd3d-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-148">System-Flags</span></span>           | <span data-ttu-id="4cd3d-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cd3d-149">0x00000010</span></span>                                         |
| <span data-ttu-id="4cd3d-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4cd3d-150">Classes used in</span></span>        | [<span data-ttu-id="4cd3d-151">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-151">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4cd3d-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4cd3d-152">Windows Server 2003</span></span>



| <span data-ttu-id="4cd3d-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-153">Entry</span></span> | <span data-ttu-id="4cd3d-154">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-154">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="4cd3d-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd3d-155">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-156">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cd3d-157">System-Only</span></span>            | <span data-ttu-id="4cd3d-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-158">False</span></span>                                              |
| <span data-ttu-id="4cd3d-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4cd3d-159">Is-Single-Valued</span></span>       | <span data-ttu-id="4cd3d-160">True</span><span class="sxs-lookup"><span data-stu-id="4cd3d-160">True</span></span>                                               |
| <span data-ttu-id="4cd3d-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4cd3d-161">Is Indexed</span></span>             | <span data-ttu-id="4cd3d-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-162">False</span></span>                                              |
| <span data-ttu-id="4cd3d-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4cd3d-163">In Global Catalog</span></span>      | <span data-ttu-id="4cd3d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-164">False</span></span>                                              |
| <span data-ttu-id="4cd3d-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4cd3d-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cd3d-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4cd3d-166">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="4cd3d-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cd3d-167">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cd3d-168">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-169">Search-Flags</span></span>           | <span data-ttu-id="4cd3d-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cd3d-170">0x00000000</span></span>                                         |
| <span data-ttu-id="4cd3d-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-171">System-Flags</span></span>           | <span data-ttu-id="4cd3d-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cd3d-172">0x00000010</span></span>                                         |
| <span data-ttu-id="4cd3d-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4cd3d-173">Classes used in</span></span>        | [<span data-ttu-id="4cd3d-174">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-174">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4cd3d-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4cd3d-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4cd3d-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-176">Entry</span></span> | <span data-ttu-id="4cd3d-177">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-177">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="4cd3d-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd3d-178">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-179">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cd3d-180">System-Only</span></span>            | <span data-ttu-id="4cd3d-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-181">False</span></span>                                              |
| <span data-ttu-id="4cd3d-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4cd3d-182">Is-Single-Valued</span></span>       | <span data-ttu-id="4cd3d-183">True</span><span class="sxs-lookup"><span data-stu-id="4cd3d-183">True</span></span>                                               |
| <span data-ttu-id="4cd3d-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4cd3d-184">Is Indexed</span></span>             | <span data-ttu-id="4cd3d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-185">False</span></span>                                              |
| <span data-ttu-id="4cd3d-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4cd3d-186">In Global Catalog</span></span>      | <span data-ttu-id="4cd3d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-187">False</span></span>                                              |
| <span data-ttu-id="4cd3d-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4cd3d-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cd3d-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4cd3d-189">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="4cd3d-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cd3d-190">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cd3d-191">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-192">Search-Flags</span></span>           | <span data-ttu-id="4cd3d-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cd3d-193">0x00000000</span></span>                                         |
| <span data-ttu-id="4cd3d-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-194">System-Flags</span></span>           | <span data-ttu-id="4cd3d-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cd3d-195">0x00000010</span></span>                                         |
| <span data-ttu-id="4cd3d-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4cd3d-196">Classes used in</span></span>        | [<span data-ttu-id="4cd3d-197">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-197">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4cd3d-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cd3d-198">Windows Server 2008</span></span>



| <span data-ttu-id="4cd3d-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-199">Entry</span></span> | <span data-ttu-id="4cd3d-200">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-200">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="4cd3d-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd3d-201">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-202">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cd3d-203">System-Only</span></span>            | <span data-ttu-id="4cd3d-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-204">False</span></span>                                              |
| <span data-ttu-id="4cd3d-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4cd3d-205">Is-Single-Valued</span></span>       | <span data-ttu-id="4cd3d-206">True</span><span class="sxs-lookup"><span data-stu-id="4cd3d-206">True</span></span>                                               |
| <span data-ttu-id="4cd3d-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4cd3d-207">Is Indexed</span></span>             | <span data-ttu-id="4cd3d-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-208">False</span></span>                                              |
| <span data-ttu-id="4cd3d-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4cd3d-209">In Global Catalog</span></span>      | <span data-ttu-id="4cd3d-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-210">False</span></span>                                              |
| <span data-ttu-id="4cd3d-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4cd3d-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cd3d-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4cd3d-212">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="4cd3d-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cd3d-213">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cd3d-214">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-215">Search-Flags</span></span>           | <span data-ttu-id="4cd3d-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cd3d-216">0x00000000</span></span>                                         |
| <span data-ttu-id="4cd3d-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-217">System-Flags</span></span>           | <span data-ttu-id="4cd3d-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cd3d-218">0x00000010</span></span>                                         |
| <span data-ttu-id="4cd3d-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4cd3d-219">Classes used in</span></span>        | [<span data-ttu-id="4cd3d-220">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-220">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4cd3d-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4cd3d-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4cd3d-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-222">Entry</span></span> | <span data-ttu-id="4cd3d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-223">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="4cd3d-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd3d-224">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-225">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cd3d-226">System-Only</span></span>            | <span data-ttu-id="4cd3d-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-227">False</span></span>                                              |
| <span data-ttu-id="4cd3d-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4cd3d-228">Is-Single-Valued</span></span>       | <span data-ttu-id="4cd3d-229">True</span><span class="sxs-lookup"><span data-stu-id="4cd3d-229">True</span></span>                                               |
| <span data-ttu-id="4cd3d-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4cd3d-230">Is Indexed</span></span>             | <span data-ttu-id="4cd3d-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-231">False</span></span>                                              |
| <span data-ttu-id="4cd3d-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4cd3d-232">In Global Catalog</span></span>      | <span data-ttu-id="4cd3d-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-233">False</span></span>                                              |
| <span data-ttu-id="4cd3d-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4cd3d-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cd3d-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4cd3d-235">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="4cd3d-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cd3d-236">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cd3d-237">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-238">Search-Flags</span></span>           | <span data-ttu-id="4cd3d-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cd3d-239">0x00000000</span></span>                                         |
| <span data-ttu-id="4cd3d-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-240">System-Flags</span></span>           | <span data-ttu-id="4cd3d-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cd3d-241">0x00000010</span></span>                                         |
| <span data-ttu-id="4cd3d-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4cd3d-242">Classes used in</span></span>        | [<span data-ttu-id="4cd3d-243">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-243">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4cd3d-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cd3d-244">Windows Server 2012</span></span>



| <span data-ttu-id="4cd3d-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="4cd3d-245">Entry</span></span> | <span data-ttu-id="4cd3d-246">Значение</span><span class="sxs-lookup"><span data-stu-id="4cd3d-246">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="4cd3d-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4cd3d-247">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4cd3d-248">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="4cd3d-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="4cd3d-249">System-Only</span></span>            | <span data-ttu-id="4cd3d-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-250">False</span></span>                                              |
| <span data-ttu-id="4cd3d-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4cd3d-251">Is-Single-Valued</span></span>       | <span data-ttu-id="4cd3d-252">True</span><span class="sxs-lookup"><span data-stu-id="4cd3d-252">True</span></span>                                               |
| <span data-ttu-id="4cd3d-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4cd3d-253">Is Indexed</span></span>             | <span data-ttu-id="4cd3d-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-254">False</span></span>                                              |
| <span data-ttu-id="4cd3d-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4cd3d-255">In Global Catalog</span></span>      | <span data-ttu-id="4cd3d-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="4cd3d-256">False</span></span>                                              |
| <span data-ttu-id="4cd3d-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4cd3d-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="4cd3d-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4cd3d-258">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="4cd3d-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4cd3d-259">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4cd3d-260">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="4cd3d-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-261">Search-Flags</span></span>           | <span data-ttu-id="4cd3d-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4cd3d-262">0x00000000</span></span>                                         |
| <span data-ttu-id="4cd3d-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4cd3d-263">System-Flags</span></span>           | <span data-ttu-id="4cd3d-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4cd3d-264">0x00000010</span></span>                                         |
| <span data-ttu-id="4cd3d-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4cd3d-265">Classes used in</span></span>        | [<span data-ttu-id="4cd3d-266">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="4cd3d-266">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





