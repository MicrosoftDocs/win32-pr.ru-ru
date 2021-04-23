---
title: Атрибут DNS-Tombstoned
description: Значение true, если объект был захоронен. Этот атрибут существует, чтобы упростить и ускорить поиск захороненных записей. Захороненные объекты — это объекты, которые были удалены, но еще не удалены из каталога.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DNS-Tombstoned
- Схема AD атрибута Днстомбстонед
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0dba61706861b808f28d7f6874a9bfd93d4152c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893117"
---
# <a name="dns-tombstoned-attribute"></a><span data-ttu-id="2d366-107">Атрибут DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="2d366-107">DNS-Tombstoned attribute</span></span>

<span data-ttu-id="2d366-108">Значение true, если объект был захоронен.</span><span class="sxs-lookup"><span data-stu-id="2d366-108">True if this object has been tombstoned.</span></span> <span data-ttu-id="2d366-109">Этот атрибут существует, чтобы упростить и ускорить поиск захороненных записей.</span><span class="sxs-lookup"><span data-stu-id="2d366-109">This attribute exists to make searching for tombstoned records easier and faster.</span></span> <span data-ttu-id="2d366-110">Захороненные объекты — это объекты, которые были удалены, но еще не удалены из каталога.</span><span class="sxs-lookup"><span data-stu-id="2d366-110">Tombstoned objects are objects that have been deleted but not yet removed from the directory.</span></span>



| <span data-ttu-id="2d366-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-111">Entry</span></span> | <span data-ttu-id="2d366-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-112">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2d366-113">CN</span><span class="sxs-lookup"><span data-stu-id="2d366-113">CN</span></span>                | <span data-ttu-id="2d366-114">DNS-Tombstoned</span><span class="sxs-lookup"><span data-stu-id="2d366-114">DNS-Tombstoned</span></span>                       |
| <span data-ttu-id="2d366-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2d366-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2d366-116">днстомбстонед</span><span class="sxs-lookup"><span data-stu-id="2d366-116">dNSTombstoned</span></span>                        |
| <span data-ttu-id="2d366-117">Размер</span><span class="sxs-lookup"><span data-stu-id="2d366-117">Size</span></span>              | <span data-ttu-id="2d366-118">4 байта</span><span class="sxs-lookup"><span data-stu-id="2d366-118">4 bytes</span></span>                              |
| <span data-ttu-id="2d366-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2d366-119">Update Privilege</span></span>  | <span data-ttu-id="2d366-120">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="2d366-120">This value is set by the system.</span></span>     |
| <span data-ttu-id="2d366-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2d366-121">Update Frequency</span></span>  | <span data-ttu-id="2d366-122">При каждом удалении объекта.</span><span class="sxs-lookup"><span data-stu-id="2d366-122">Whenever an object is deleted.</span></span>       |
| <span data-ttu-id="2d366-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-123">Attribute-Id</span></span>      | <span data-ttu-id="2d366-124">1.2.840.113556.1.4.1414</span><span class="sxs-lookup"><span data-stu-id="2d366-124">1.2.840.113556.1.4.1414</span></span>              |
| <span data-ttu-id="2d366-125">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2d366-125">System-Id-Guid</span></span>    | <span data-ttu-id="2d366-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span><span class="sxs-lookup"><span data-stu-id="2d366-126">d5eb2eb7-be4e-463b-a214-634a44d7392e</span></span> |
| <span data-ttu-id="2d366-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d366-127">Syntax</span></span>            | [<span data-ttu-id="2d366-128">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="2d366-128">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="2d366-129">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2d366-129">Implementations</span></span>

-   [<span data-ttu-id="2d366-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d366-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d366-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d366-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d366-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d366-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d366-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d366-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d366-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d366-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d366-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d366-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d366-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d366-136">Windows 2000 Server</span></span>



| <span data-ttu-id="2d366-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-137">Entry</span></span> | <span data-ttu-id="2d366-138">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-138">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d366-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d366-139">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-140">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d366-141">System-Only</span></span>            | <span data-ttu-id="2d366-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-142">False</span></span>                                    |
| <span data-ttu-id="2d366-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d366-143">Is-Single-Valued</span></span>       | <span data-ttu-id="2d366-144">True</span><span class="sxs-lookup"><span data-stu-id="2d366-144">True</span></span>                                     |
| <span data-ttu-id="2d366-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d366-145">Is Indexed</span></span>             | <span data-ttu-id="2d366-146">True</span><span class="sxs-lookup"><span data-stu-id="2d366-146">True</span></span>                                     |
| <span data-ttu-id="2d366-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d366-147">In Global Catalog</span></span>      | <span data-ttu-id="2d366-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-148">False</span></span>                                    |
| <span data-ttu-id="2d366-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d366-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d366-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d366-150">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d366-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d366-151">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d366-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d366-152">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d366-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-153">Search-Flags</span></span>           | <span data-ttu-id="2d366-154">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d366-154">0x00000001</span></span>                               |
| <span data-ttu-id="2d366-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-155">System-Flags</span></span>           | <span data-ttu-id="2d366-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d366-156">0x00000010</span></span>                               |
| <span data-ttu-id="2d366-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d366-157">Classes used in</span></span>        | [<span data-ttu-id="2d366-158">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="2d366-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d366-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d366-159">Windows Server 2003</span></span>



| <span data-ttu-id="2d366-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-160">Entry</span></span> | <span data-ttu-id="2d366-161">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-161">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d366-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d366-162">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-163">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d366-164">System-Only</span></span>            | <span data-ttu-id="2d366-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-165">False</span></span>                                    |
| <span data-ttu-id="2d366-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d366-166">Is-Single-Valued</span></span>       | <span data-ttu-id="2d366-167">True</span><span class="sxs-lookup"><span data-stu-id="2d366-167">True</span></span>                                     |
| <span data-ttu-id="2d366-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d366-168">Is Indexed</span></span>             | <span data-ttu-id="2d366-169">True</span><span class="sxs-lookup"><span data-stu-id="2d366-169">True</span></span>                                     |
| <span data-ttu-id="2d366-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d366-170">In Global Catalog</span></span>      | <span data-ttu-id="2d366-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-171">False</span></span>                                    |
| <span data-ttu-id="2d366-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d366-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d366-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d366-173">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d366-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d366-174">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d366-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d366-175">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d366-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-176">Search-Flags</span></span>           | <span data-ttu-id="2d366-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d366-177">0x00000001</span></span>                               |
| <span data-ttu-id="2d366-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-178">System-Flags</span></span>           | <span data-ttu-id="2d366-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d366-179">0x00000010</span></span>                               |
| <span data-ttu-id="2d366-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d366-180">Classes used in</span></span>        | [<span data-ttu-id="2d366-181">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="2d366-181">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d366-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d366-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d366-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-183">Entry</span></span> | <span data-ttu-id="2d366-184">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-184">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d366-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d366-185">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-186">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d366-187">System-Only</span></span>            | <span data-ttu-id="2d366-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-188">False</span></span>                                    |
| <span data-ttu-id="2d366-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d366-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2d366-190">True</span><span class="sxs-lookup"><span data-stu-id="2d366-190">True</span></span>                                     |
| <span data-ttu-id="2d366-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d366-191">Is Indexed</span></span>             | <span data-ttu-id="2d366-192">True</span><span class="sxs-lookup"><span data-stu-id="2d366-192">True</span></span>                                     |
| <span data-ttu-id="2d366-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d366-193">In Global Catalog</span></span>      | <span data-ttu-id="2d366-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-194">False</span></span>                                    |
| <span data-ttu-id="2d366-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d366-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d366-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d366-196">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d366-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d366-197">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d366-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d366-198">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d366-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-199">Search-Flags</span></span>           | <span data-ttu-id="2d366-200">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d366-200">0x00000001</span></span>                               |
| <span data-ttu-id="2d366-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-201">System-Flags</span></span>           | <span data-ttu-id="2d366-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d366-202">0x00000010</span></span>                               |
| <span data-ttu-id="2d366-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d366-203">Classes used in</span></span>        | [<span data-ttu-id="2d366-204">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="2d366-204">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d366-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d366-205">Windows Server 2008</span></span>



| <span data-ttu-id="2d366-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-206">Entry</span></span> | <span data-ttu-id="2d366-207">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-207">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d366-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d366-208">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-209">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d366-210">System-Only</span></span>            | <span data-ttu-id="2d366-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-211">False</span></span>                                    |
| <span data-ttu-id="2d366-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d366-212">Is-Single-Valued</span></span>       | <span data-ttu-id="2d366-213">True</span><span class="sxs-lookup"><span data-stu-id="2d366-213">True</span></span>                                     |
| <span data-ttu-id="2d366-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d366-214">Is Indexed</span></span>             | <span data-ttu-id="2d366-215">True</span><span class="sxs-lookup"><span data-stu-id="2d366-215">True</span></span>                                     |
| <span data-ttu-id="2d366-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d366-216">In Global Catalog</span></span>      | <span data-ttu-id="2d366-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-217">False</span></span>                                    |
| <span data-ttu-id="2d366-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d366-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d366-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d366-219">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d366-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d366-220">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d366-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d366-221">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d366-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-222">Search-Flags</span></span>           | <span data-ttu-id="2d366-223">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d366-223">0x00000001</span></span>                               |
| <span data-ttu-id="2d366-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-224">System-Flags</span></span>           | <span data-ttu-id="2d366-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d366-225">0x00000010</span></span>                               |
| <span data-ttu-id="2d366-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d366-226">Classes used in</span></span>        | [<span data-ttu-id="2d366-227">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="2d366-227">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d366-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d366-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d366-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-229">Entry</span></span> | <span data-ttu-id="2d366-230">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-230">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d366-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d366-231">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-232">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d366-233">System-Only</span></span>            | <span data-ttu-id="2d366-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-234">False</span></span>                                    |
| <span data-ttu-id="2d366-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d366-235">Is-Single-Valued</span></span>       | <span data-ttu-id="2d366-236">True</span><span class="sxs-lookup"><span data-stu-id="2d366-236">True</span></span>                                     |
| <span data-ttu-id="2d366-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d366-237">Is Indexed</span></span>             | <span data-ttu-id="2d366-238">True</span><span class="sxs-lookup"><span data-stu-id="2d366-238">True</span></span>                                     |
| <span data-ttu-id="2d366-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d366-239">In Global Catalog</span></span>      | <span data-ttu-id="2d366-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-240">False</span></span>                                    |
| <span data-ttu-id="2d366-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d366-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d366-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d366-242">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d366-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d366-243">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d366-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d366-244">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d366-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-245">Search-Flags</span></span>           | <span data-ttu-id="2d366-246">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d366-246">0x00000001</span></span>                               |
| <span data-ttu-id="2d366-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-247">System-Flags</span></span>           | <span data-ttu-id="2d366-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d366-248">0x00000010</span></span>                               |
| <span data-ttu-id="2d366-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d366-249">Classes used in</span></span>        | [<span data-ttu-id="2d366-250">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="2d366-250">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d366-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d366-251">Windows Server 2012</span></span>



| <span data-ttu-id="2d366-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d366-252">Entry</span></span> | <span data-ttu-id="2d366-253">Значение</span><span class="sxs-lookup"><span data-stu-id="2d366-253">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="2d366-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d366-254">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d366-255">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="2d366-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d366-256">System-Only</span></span>            | <span data-ttu-id="2d366-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-257">False</span></span>                                    |
| <span data-ttu-id="2d366-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d366-258">Is-Single-Valued</span></span>       | <span data-ttu-id="2d366-259">True</span><span class="sxs-lookup"><span data-stu-id="2d366-259">True</span></span>                                     |
| <span data-ttu-id="2d366-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d366-260">Is Indexed</span></span>             | <span data-ttu-id="2d366-261">True</span><span class="sxs-lookup"><span data-stu-id="2d366-261">True</span></span>                                     |
| <span data-ttu-id="2d366-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d366-262">In Global Catalog</span></span>      | <span data-ttu-id="2d366-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d366-263">False</span></span>                                    |
| <span data-ttu-id="2d366-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d366-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d366-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d366-265">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="2d366-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d366-266">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="2d366-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d366-267">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="2d366-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-268">Search-Flags</span></span>           | <span data-ttu-id="2d366-269">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2d366-269">0x00000001</span></span>                               |
| <span data-ttu-id="2d366-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d366-270">System-Flags</span></span>           | <span data-ttu-id="2d366-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2d366-271">0x00000010</span></span>                               |
| <span data-ttu-id="2d366-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d366-272">Classes used in</span></span>        | [<span data-ttu-id="2d366-273">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="2d366-273">**Dns-Node**</span></span>](c-dnsnode.md)<br/> |



 

 





