---
title: Атрибут Dns-Record
description: Используется для хранения двоичных записей DNS-ресурсов в объектах DNS.
ms.assetid: 2d5a17da-0efc-450e-b247-3ab6d2de3a5d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Dns-Record
- Схема AD атрибута Днсрекорд
topic_type:
- apiref
api_name:
- Dns-Record
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 013fa5ef4a9fcec151f996c347cdfd525438aa7d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139031"
---
# <a name="dns-record-attribute"></a><span data-ttu-id="7e3bb-105">Атрибут Dns-Record</span><span class="sxs-lookup"><span data-stu-id="7e3bb-105">Dns-Record attribute</span></span>

<span data-ttu-id="7e3bb-106">Используется для хранения двоичных записей DNS-ресурсов в объектах DNS.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-106">Used to store binary DNS resource records on DNS objects.</span></span>



| <span data-ttu-id="7e3bb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-107">Entry</span></span> | <span data-ttu-id="7e3bb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="7e3bb-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e3bb-109">CN</span></span>                | <span data-ttu-id="7e3bb-110">Dns-Record</span><span class="sxs-lookup"><span data-stu-id="7e3bb-110">Dns-Record</span></span>                                            |
| <span data-ttu-id="7e3bb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7e3bb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e3bb-112">днсрекорд</span><span class="sxs-lookup"><span data-stu-id="7e3bb-112">dnsRecord</span></span>                                             |
| <span data-ttu-id="7e3bb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7e3bb-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="7e3bb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7e3bb-114">Update Privilege</span></span>  | <span data-ttu-id="7e3bb-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="7e3bb-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7e3bb-116">Update Frequency</span></span>  | <span data-ttu-id="7e3bb-117">При изменении записей ресурсов DNS.</span><span class="sxs-lookup"><span data-stu-id="7e3bb-117">Whenever DNS resource records change.</span></span>                 |
| <span data-ttu-id="7e3bb-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-118">Attribute-Id</span></span>      | <span data-ttu-id="7e3bb-119">1.2.840.113556.1.4.382</span><span class="sxs-lookup"><span data-stu-id="7e3bb-119">1.2.840.113556.1.4.382</span></span>                                |
| <span data-ttu-id="7e3bb-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7e3bb-120">System-Id-Guid</span></span>    | <span data-ttu-id="7e3bb-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="7e3bb-121">e0fa1e69-9b45-11d0-afdd-00c04fd930c9</span></span>                  |
| <span data-ttu-id="7e3bb-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e3bb-122">Syntax</span></span>            | [<span data-ttu-id="7e3bb-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="7e3bb-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7e3bb-124">Implementations</span></span>

-   [<span data-ttu-id="7e3bb-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e3bb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e3bb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e3bb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e3bb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e3bb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e3bb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e3bb-131">Windows 2000 Server</span></span>



| <span data-ttu-id="7e3bb-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-132">Entry</span></span> | <span data-ttu-id="7e3bb-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e3bb-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e3bb-134">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-135">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3bb-136">System-Only</span></span>            | <span data-ttu-id="7e3bb-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-137">False</span></span>                                    |
| <span data-ttu-id="7e3bb-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e3bb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3bb-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-139">False</span></span>                                    |
| <span data-ttu-id="7e3bb-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e3bb-140">Is Indexed</span></span>             | <span data-ttu-id="7e3bb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-141">False</span></span>                                    |
| <span data-ttu-id="7e3bb-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e3bb-142">In Global Catalog</span></span>      | <span data-ttu-id="7e3bb-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-143">False</span></span>                                    |
| <span data-ttu-id="7e3bb-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e3bb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3bb-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-145">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e3bb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3bb-146">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3bb-147">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-148">Search-Flags</span></span>           | <span data-ttu-id="7e3bb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bb-149">0x00000000</span></span>                               |
| <span data-ttu-id="7e3bb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-150">System-Flags</span></span>           | <span data-ttu-id="7e3bb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3bb-151">0x00000010</span></span>                               |
| <span data-ttu-id="7e3bb-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e3bb-152">Classes used in</span></span>        | [<span data-ttu-id="7e3bb-153">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e3bb-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e3bb-154">Windows Server 2003</span></span>



| <span data-ttu-id="7e3bb-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-155">Entry</span></span> | <span data-ttu-id="7e3bb-156">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-156">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e3bb-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e3bb-157">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-158">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3bb-159">System-Only</span></span>            | <span data-ttu-id="7e3bb-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-160">False</span></span>                                    |
| <span data-ttu-id="7e3bb-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e3bb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3bb-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-162">False</span></span>                                    |
| <span data-ttu-id="7e3bb-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e3bb-163">Is Indexed</span></span>             | <span data-ttu-id="7e3bb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-164">False</span></span>                                    |
| <span data-ttu-id="7e3bb-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e3bb-165">In Global Catalog</span></span>      | <span data-ttu-id="7e3bb-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-166">False</span></span>                                    |
| <span data-ttu-id="7e3bb-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e3bb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3bb-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-168">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e3bb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3bb-169">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3bb-170">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-171">Search-Flags</span></span>           | <span data-ttu-id="7e3bb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bb-172">0x00000000</span></span>                               |
| <span data-ttu-id="7e3bb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-173">System-Flags</span></span>           | <span data-ttu-id="7e3bb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3bb-174">0x00000010</span></span>                               |
| <span data-ttu-id="7e3bb-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e3bb-175">Classes used in</span></span>        | [<span data-ttu-id="7e3bb-176">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-176">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e3bb-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e3bb-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e3bb-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-178">Entry</span></span> | <span data-ttu-id="7e3bb-179">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-179">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e3bb-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e3bb-180">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-181">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3bb-182">System-Only</span></span>            | <span data-ttu-id="7e3bb-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-183">False</span></span>                                    |
| <span data-ttu-id="7e3bb-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e3bb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3bb-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-185">False</span></span>                                    |
| <span data-ttu-id="7e3bb-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e3bb-186">Is Indexed</span></span>             | <span data-ttu-id="7e3bb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-187">False</span></span>                                    |
| <span data-ttu-id="7e3bb-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e3bb-188">In Global Catalog</span></span>      | <span data-ttu-id="7e3bb-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-189">False</span></span>                                    |
| <span data-ttu-id="7e3bb-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e3bb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3bb-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-191">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e3bb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3bb-192">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3bb-193">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-194">Search-Flags</span></span>           | <span data-ttu-id="7e3bb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bb-195">0x00000000</span></span>                               |
| <span data-ttu-id="7e3bb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-196">System-Flags</span></span>           | <span data-ttu-id="7e3bb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3bb-197">0x00000010</span></span>                               |
| <span data-ttu-id="7e3bb-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e3bb-198">Classes used in</span></span>        | [<span data-ttu-id="7e3bb-199">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-199">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e3bb-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e3bb-200">Windows Server 2008</span></span>



| <span data-ttu-id="7e3bb-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-201">Entry</span></span> | <span data-ttu-id="7e3bb-202">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-202">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e3bb-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e3bb-203">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-204">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3bb-205">System-Only</span></span>            | <span data-ttu-id="7e3bb-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-206">False</span></span>                                    |
| <span data-ttu-id="7e3bb-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e3bb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3bb-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-208">False</span></span>                                    |
| <span data-ttu-id="7e3bb-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e3bb-209">Is Indexed</span></span>             | <span data-ttu-id="7e3bb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-210">False</span></span>                                    |
| <span data-ttu-id="7e3bb-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e3bb-211">In Global Catalog</span></span>      | <span data-ttu-id="7e3bb-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-212">False</span></span>                                    |
| <span data-ttu-id="7e3bb-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e3bb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3bb-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-214">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e3bb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3bb-215">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3bb-216">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-217">Search-Flags</span></span>           | <span data-ttu-id="7e3bb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bb-218">0x00000000</span></span>                               |
| <span data-ttu-id="7e3bb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-219">System-Flags</span></span>           | <span data-ttu-id="7e3bb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3bb-220">0x00000010</span></span>                               |
| <span data-ttu-id="7e3bb-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e3bb-221">Classes used in</span></span>        | [<span data-ttu-id="7e3bb-222">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-222">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e3bb-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e3bb-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e3bb-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-224">Entry</span></span> | <span data-ttu-id="7e3bb-225">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-225">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e3bb-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e3bb-226">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-227">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3bb-228">System-Only</span></span>            | <span data-ttu-id="7e3bb-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-229">False</span></span>                                    |
| <span data-ttu-id="7e3bb-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e3bb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3bb-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-231">False</span></span>                                    |
| <span data-ttu-id="7e3bb-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e3bb-232">Is Indexed</span></span>             | <span data-ttu-id="7e3bb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-233">False</span></span>                                    |
| <span data-ttu-id="7e3bb-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e3bb-234">In Global Catalog</span></span>      | <span data-ttu-id="7e3bb-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-235">False</span></span>                                    |
| <span data-ttu-id="7e3bb-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e3bb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3bb-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-237">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e3bb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3bb-238">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3bb-239">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-240">Search-Flags</span></span>           | <span data-ttu-id="7e3bb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bb-241">0x00000000</span></span>                               |
| <span data-ttu-id="7e3bb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-242">System-Flags</span></span>           | <span data-ttu-id="7e3bb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3bb-243">0x00000010</span></span>                               |
| <span data-ttu-id="7e3bb-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e3bb-244">Classes used in</span></span>        | [<span data-ttu-id="7e3bb-245">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-245">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e3bb-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e3bb-246">Windows Server 2012</span></span>



| <span data-ttu-id="7e3bb-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e3bb-247">Entry</span></span> | <span data-ttu-id="7e3bb-248">Значение</span><span class="sxs-lookup"><span data-stu-id="7e3bb-248">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="7e3bb-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e3bb-249">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e3bb-250">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="7e3bb-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e3bb-251">System-Only</span></span>            | <span data-ttu-id="7e3bb-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-252">False</span></span>                                    |
| <span data-ttu-id="7e3bb-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e3bb-253">Is-Single-Valued</span></span>       | <span data-ttu-id="7e3bb-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-254">False</span></span>                                    |
| <span data-ttu-id="7e3bb-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e3bb-255">Is Indexed</span></span>             | <span data-ttu-id="7e3bb-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-256">False</span></span>                                    |
| <span data-ttu-id="7e3bb-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e3bb-257">In Global Catalog</span></span>      | <span data-ttu-id="7e3bb-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e3bb-258">False</span></span>                                    |
| <span data-ttu-id="7e3bb-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e3bb-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e3bb-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e3bb-260">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="7e3bb-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e3bb-261">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e3bb-262">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="7e3bb-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-263">Search-Flags</span></span>           | <span data-ttu-id="7e3bb-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e3bb-264">0x00000000</span></span>                               |
| <span data-ttu-id="7e3bb-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e3bb-265">System-Flags</span></span>           | <span data-ttu-id="7e3bb-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e3bb-266">0x00000010</span></span>                               |
| <span data-ttu-id="7e3bb-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e3bb-267">Classes used in</span></span>        | [<span data-ttu-id="7e3bb-268">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="7e3bb-268">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





