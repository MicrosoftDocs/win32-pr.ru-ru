---
title: Атрибут DNS-Property
description: Используется для хранения двоичных параметров (свойств) в объектах зоны DNS.
ms.assetid: 55ea38cd-6b5b-4500-8e68-ae4d35e4b177
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DNS-Property
- Схема AD атрибута Днспроперти
topic_type:
- apiref
api_name:
- DNS-Property
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f8fd18f4524ec0bf61a609d21a361668ed295b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654869"
---
# <a name="dns-property-attribute"></a><span data-ttu-id="0bbf2-105">Атрибут DNS-Property</span><span class="sxs-lookup"><span data-stu-id="0bbf2-105">DNS-Property attribute</span></span>

<span data-ttu-id="0bbf2-106">Используется для хранения двоичных параметров (свойств) в объектах зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-106">Used to store binary settings (properties) on DNS zone objects.</span></span>



| <span data-ttu-id="0bbf2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-107">Entry</span></span> | <span data-ttu-id="0bbf2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="0bbf2-109">CN</span><span class="sxs-lookup"><span data-stu-id="0bbf2-109">CN</span></span>                | <span data-ttu-id="0bbf2-110">DNS-Property</span><span class="sxs-lookup"><span data-stu-id="0bbf2-110">DNS-Property</span></span>                                          |
| <span data-ttu-id="0bbf2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0bbf2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0bbf2-112">днспроперти</span><span class="sxs-lookup"><span data-stu-id="0bbf2-112">dNSProperty</span></span>                                           |
| <span data-ttu-id="0bbf2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="0bbf2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="0bbf2-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0bbf2-114">Update Privilege</span></span>  | <span data-ttu-id="0bbf2-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="0bbf2-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0bbf2-116">Update Frequency</span></span>  | <span data-ttu-id="0bbf2-117">При каждом изменении записей зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="0bbf2-117">Whenever DNS zone records change.</span></span>                     |
| <span data-ttu-id="0bbf2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-118">Attribute-Id</span></span>      | <span data-ttu-id="0bbf2-119">1.2.840.113556.1.4.1306</span><span class="sxs-lookup"><span data-stu-id="0bbf2-119">1.2.840.113556.1.4.1306</span></span>                               |
| <span data-ttu-id="0bbf2-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0bbf2-120">System-Id-Guid</span></span>    | <span data-ttu-id="0bbf2-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="0bbf2-121">675a15fe-3b70-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="0bbf2-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bbf2-122">Syntax</span></span>            | [<span data-ttu-id="0bbf2-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="0bbf2-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0bbf2-124">Implementations</span></span>

-   [<span data-ttu-id="0bbf2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0bbf2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0bbf2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0bbf2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0bbf2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0bbf2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0bbf2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0bbf2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="0bbf2-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-132">Entry</span></span> | <span data-ttu-id="0bbf2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0bbf2-134">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-135">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbf2-136">System-Only</span></span>            | <span data-ttu-id="0bbf2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-137">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0bbf2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbf2-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-139">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0bbf2-140">Is Indexed</span></span>             | <span data-ttu-id="0bbf2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-141">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0bbf2-142">In Global Catalog</span></span>      | <span data-ttu-id="0bbf2-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-143">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0bbf2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbf2-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-145">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="0bbf2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbf2-146">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbf2-147">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-148">Search-Flags</span></span>           | <span data-ttu-id="0bbf2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbf2-149">0x00000000</span></span>                                                                        |
| <span data-ttu-id="0bbf2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-150">System-Flags</span></span>           | <span data-ttu-id="0bbf2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbf2-151">0x00000010</span></span>                                                                        |
| <span data-ttu-id="0bbf2-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0bbf2-152">Classes used in</span></span>        | [<span data-ttu-id="0bbf2-153">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-153">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="0bbf2-154">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-154">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0bbf2-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0bbf2-155">Windows Server 2003</span></span>



| <span data-ttu-id="0bbf2-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-156">Entry</span></span> | <span data-ttu-id="0bbf2-157">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0bbf2-158">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-159">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbf2-160">System-Only</span></span>            | <span data-ttu-id="0bbf2-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-161">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0bbf2-162">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbf2-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-163">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0bbf2-164">Is Indexed</span></span>             | <span data-ttu-id="0bbf2-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-165">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0bbf2-166">In Global Catalog</span></span>      | <span data-ttu-id="0bbf2-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-167">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0bbf2-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbf2-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-169">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="0bbf2-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbf2-170">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbf2-171">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-172">Search-Flags</span></span>           | <span data-ttu-id="0bbf2-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbf2-173">0x00000000</span></span>                                                                        |
| <span data-ttu-id="0bbf2-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-174">System-Flags</span></span>           | <span data-ttu-id="0bbf2-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbf2-175">0x00000010</span></span>                                                                        |
| <span data-ttu-id="0bbf2-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0bbf2-176">Classes used in</span></span>        | [<span data-ttu-id="0bbf2-177">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-177">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="0bbf2-178">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-178">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0bbf2-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0bbf2-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0bbf2-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-180">Entry</span></span> | <span data-ttu-id="0bbf2-181">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0bbf2-182">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-183">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbf2-184">System-Only</span></span>            | <span data-ttu-id="0bbf2-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-185">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0bbf2-186">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbf2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-187">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0bbf2-188">Is Indexed</span></span>             | <span data-ttu-id="0bbf2-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-189">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0bbf2-190">In Global Catalog</span></span>      | <span data-ttu-id="0bbf2-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-191">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0bbf2-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbf2-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-193">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="0bbf2-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbf2-194">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbf2-195">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-196">Search-Flags</span></span>           | <span data-ttu-id="0bbf2-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbf2-197">0x00000000</span></span>                                                                        |
| <span data-ttu-id="0bbf2-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-198">System-Flags</span></span>           | <span data-ttu-id="0bbf2-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbf2-199">0x00000010</span></span>                                                                        |
| <span data-ttu-id="0bbf2-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0bbf2-200">Classes used in</span></span>        | [<span data-ttu-id="0bbf2-201">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-201">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="0bbf2-202">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-202">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0bbf2-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bbf2-203">Windows Server 2008</span></span>



| <span data-ttu-id="0bbf2-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-204">Entry</span></span> | <span data-ttu-id="0bbf2-205">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0bbf2-206">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-207">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbf2-208">System-Only</span></span>            | <span data-ttu-id="0bbf2-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-209">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0bbf2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbf2-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-211">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0bbf2-212">Is Indexed</span></span>             | <span data-ttu-id="0bbf2-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-213">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0bbf2-214">In Global Catalog</span></span>      | <span data-ttu-id="0bbf2-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-215">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0bbf2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbf2-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-217">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="0bbf2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbf2-218">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbf2-219">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-220">Search-Flags</span></span>           | <span data-ttu-id="0bbf2-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbf2-221">0x00000000</span></span>                                                                        |
| <span data-ttu-id="0bbf2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-222">System-Flags</span></span>           | <span data-ttu-id="0bbf2-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbf2-223">0x00000010</span></span>                                                                        |
| <span data-ttu-id="0bbf2-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0bbf2-224">Classes used in</span></span>        | [<span data-ttu-id="0bbf2-225">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-225">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="0bbf2-226">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-226">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0bbf2-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0bbf2-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0bbf2-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-228">Entry</span></span> | <span data-ttu-id="0bbf2-229">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0bbf2-230">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-231">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbf2-232">System-Only</span></span>            | <span data-ttu-id="0bbf2-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-233">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0bbf2-234">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbf2-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-235">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0bbf2-236">Is Indexed</span></span>             | <span data-ttu-id="0bbf2-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-237">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0bbf2-238">In Global Catalog</span></span>      | <span data-ttu-id="0bbf2-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-239">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0bbf2-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbf2-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-241">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="0bbf2-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbf2-242">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbf2-243">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-244">Search-Flags</span></span>           | <span data-ttu-id="0bbf2-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbf2-245">0x00000000</span></span>                                                                        |
| <span data-ttu-id="0bbf2-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-246">System-Flags</span></span>           | <span data-ttu-id="0bbf2-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbf2-247">0x00000010</span></span>                                                                        |
| <span data-ttu-id="0bbf2-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0bbf2-248">Classes used in</span></span>        | [<span data-ttu-id="0bbf2-249">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-249">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="0bbf2-250">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-250">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0bbf2-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0bbf2-251">Windows Server 2012</span></span>



| <span data-ttu-id="0bbf2-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="0bbf2-252">Entry</span></span> | <span data-ttu-id="0bbf2-253">Значение</span><span class="sxs-lookup"><span data-stu-id="0bbf2-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0bbf2-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0bbf2-254">Link-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0bbf2-255">MAPI-Id</span></span>                | \-                                                                                |
| <span data-ttu-id="0bbf2-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="0bbf2-256">System-Only</span></span>            | <span data-ttu-id="0bbf2-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-257">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0bbf2-258">Is-Single-Valued</span></span>       | <span data-ttu-id="0bbf2-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-259">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0bbf2-260">Is Indexed</span></span>             | <span data-ttu-id="0bbf2-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-261">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0bbf2-262">In Global Catalog</span></span>      | <span data-ttu-id="0bbf2-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="0bbf2-263">False</span></span>                                                                             |
| <span data-ttu-id="0bbf2-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0bbf2-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="0bbf2-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0bbf2-265">O:BAG:BAD:S:</span></span>                                                                      |
| <span data-ttu-id="0bbf2-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0bbf2-266">Range-Lower</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0bbf2-267">Range-Upper</span></span>            | \-                                                                                |
| <span data-ttu-id="0bbf2-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-268">Search-Flags</span></span>           | <span data-ttu-id="0bbf2-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0bbf2-269">0x00000000</span></span>                                                                        |
| <span data-ttu-id="0bbf2-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0bbf2-270">System-Flags</span></span>           | <span data-ttu-id="0bbf2-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0bbf2-271">0x00000010</span></span>                                                                        |
| <span data-ttu-id="0bbf2-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0bbf2-272">Classes used in</span></span>        | [<span data-ttu-id="0bbf2-273">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="0bbf2-274">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="0bbf2-274">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





