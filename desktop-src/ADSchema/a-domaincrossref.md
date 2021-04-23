---
title: Домен-атрибут перекрестной ссылки
description: Это ссылка из объекта доверенного домена на объект перекрестной ссылки доверенного домена.
ms.assetid: aa6fe6f9-a45c-448c-9fc5-17bc2994c764
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов перекрестной ссылки в домене
- Схема AD атрибута Домаинкроссреф
topic_type:
- apiref
api_name:
- Domain-Cross-Ref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b85e1293ce8141a3614c9401dbb34c1031de5935
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654865"
---
# <a name="domain-cross-ref-attribute"></a><span data-ttu-id="2c240-105">Домен-атрибут перекрестной ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-105">Domain-Cross-Ref attribute</span></span>

<span data-ttu-id="2c240-106">Это ссылка из объекта доверенного домена на объект перекрестной ссылки доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="2c240-106">This is a reference from a trusted domain object to the cross reference object of the trusted domain.</span></span>



| <span data-ttu-id="2c240-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-107">Entry</span></span> | <span data-ttu-id="2c240-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2c240-109">CN</span><span class="sxs-lookup"><span data-stu-id="2c240-109">CN</span></span>                | <span data-ttu-id="2c240-110">Домен-перекрестная ссылка</span><span class="sxs-lookup"><span data-stu-id="2c240-110">Domain-Cross-Ref</span></span>                        |
| <span data-ttu-id="2c240-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2c240-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2c240-112">домаинкроссреф</span><span class="sxs-lookup"><span data-stu-id="2c240-112">domainCrossRef</span></span>                          |
| <span data-ttu-id="2c240-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2c240-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2c240-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2c240-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2c240-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2c240-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2c240-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-116">Attribute-Id</span></span>      | <span data-ttu-id="2c240-117">1.2.840.113556.1.4.472</span><span class="sxs-lookup"><span data-stu-id="2c240-117">1.2.840.113556.1.4.472</span></span>                  |
| <span data-ttu-id="2c240-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2c240-118">System-Id-Guid</span></span>    | <span data-ttu-id="2c240-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="2c240-119">b000ea7b-a086-11d0-afdd-00c04fd930c9</span></span>    |
| <span data-ttu-id="2c240-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c240-120">Syntax</span></span>            | [<span data-ttu-id="2c240-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2c240-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2c240-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2c240-122">Implementations</span></span>

-   [<span data-ttu-id="2c240-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2c240-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2c240-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2c240-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2c240-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2c240-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2c240-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2c240-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2c240-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2c240-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2c240-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2c240-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2c240-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2c240-129">Windows 2000 Server</span></span>



| <span data-ttu-id="2c240-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-130">Entry</span></span> | <span data-ttu-id="2c240-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2c240-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c240-134">System-Only</span></span>            | <span data-ttu-id="2c240-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-135">False</span></span>                                                |
| <span data-ttu-id="2c240-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c240-136">Is-Single-Valued</span></span>       | <span data-ttu-id="2c240-137">True</span><span class="sxs-lookup"><span data-stu-id="2c240-137">True</span></span>                                                 |
| <span data-ttu-id="2c240-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c240-138">Is Indexed</span></span>             | <span data-ttu-id="2c240-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-139">False</span></span>                                                |
| <span data-ttu-id="2c240-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c240-140">In Global Catalog</span></span>      | <span data-ttu-id="2c240-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-141">False</span></span>                                                |
| <span data-ttu-id="2c240-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c240-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c240-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c240-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2c240-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c240-144">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c240-145">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-146">Search-Flags</span></span>           | <span data-ttu-id="2c240-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c240-147">0x00000000</span></span>                                           |
| <span data-ttu-id="2c240-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-148">System-Flags</span></span>           | <span data-ttu-id="2c240-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c240-149">0x00000010</span></span>                                           |
| <span data-ttu-id="2c240-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c240-150">Classes used in</span></span>        | [<span data-ttu-id="2c240-151">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c240-151">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2c240-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c240-152">Windows Server 2003</span></span>



| <span data-ttu-id="2c240-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-153">Entry</span></span> | <span data-ttu-id="2c240-154">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-154">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2c240-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-155">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-156">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c240-157">System-Only</span></span>            | <span data-ttu-id="2c240-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-158">False</span></span>                                                |
| <span data-ttu-id="2c240-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c240-159">Is-Single-Valued</span></span>       | <span data-ttu-id="2c240-160">True</span><span class="sxs-lookup"><span data-stu-id="2c240-160">True</span></span>                                                 |
| <span data-ttu-id="2c240-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c240-161">Is Indexed</span></span>             | <span data-ttu-id="2c240-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-162">False</span></span>                                                |
| <span data-ttu-id="2c240-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c240-163">In Global Catalog</span></span>      | <span data-ttu-id="2c240-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-164">False</span></span>                                                |
| <span data-ttu-id="2c240-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c240-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c240-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c240-166">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2c240-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c240-167">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c240-168">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-169">Search-Flags</span></span>           | <span data-ttu-id="2c240-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c240-170">0x00000000</span></span>                                           |
| <span data-ttu-id="2c240-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-171">System-Flags</span></span>           | <span data-ttu-id="2c240-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c240-172">0x00000010</span></span>                                           |
| <span data-ttu-id="2c240-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c240-173">Classes used in</span></span>        | [<span data-ttu-id="2c240-174">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c240-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2c240-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2c240-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2c240-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-176">Entry</span></span> | <span data-ttu-id="2c240-177">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-177">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2c240-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-178">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-179">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c240-180">System-Only</span></span>            | <span data-ttu-id="2c240-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-181">False</span></span>                                                |
| <span data-ttu-id="2c240-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c240-182">Is-Single-Valued</span></span>       | <span data-ttu-id="2c240-183">True</span><span class="sxs-lookup"><span data-stu-id="2c240-183">True</span></span>                                                 |
| <span data-ttu-id="2c240-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c240-184">Is Indexed</span></span>             | <span data-ttu-id="2c240-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-185">False</span></span>                                                |
| <span data-ttu-id="2c240-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c240-186">In Global Catalog</span></span>      | <span data-ttu-id="2c240-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-187">False</span></span>                                                |
| <span data-ttu-id="2c240-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c240-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c240-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c240-189">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2c240-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c240-190">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c240-191">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-192">Search-Flags</span></span>           | <span data-ttu-id="2c240-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c240-193">0x00000000</span></span>                                           |
| <span data-ttu-id="2c240-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-194">System-Flags</span></span>           | <span data-ttu-id="2c240-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c240-195">0x00000010</span></span>                                           |
| <span data-ttu-id="2c240-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c240-196">Classes used in</span></span>        | [<span data-ttu-id="2c240-197">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c240-197">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2c240-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c240-198">Windows Server 2008</span></span>



| <span data-ttu-id="2c240-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-199">Entry</span></span> | <span data-ttu-id="2c240-200">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-200">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2c240-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-201">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-202">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c240-203">System-Only</span></span>            | <span data-ttu-id="2c240-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-204">False</span></span>                                                |
| <span data-ttu-id="2c240-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c240-205">Is-Single-Valued</span></span>       | <span data-ttu-id="2c240-206">True</span><span class="sxs-lookup"><span data-stu-id="2c240-206">True</span></span>                                                 |
| <span data-ttu-id="2c240-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c240-207">Is Indexed</span></span>             | <span data-ttu-id="2c240-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-208">False</span></span>                                                |
| <span data-ttu-id="2c240-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c240-209">In Global Catalog</span></span>      | <span data-ttu-id="2c240-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-210">False</span></span>                                                |
| <span data-ttu-id="2c240-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c240-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c240-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c240-212">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2c240-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c240-213">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c240-214">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-215">Search-Flags</span></span>           | <span data-ttu-id="2c240-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c240-216">0x00000000</span></span>                                           |
| <span data-ttu-id="2c240-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-217">System-Flags</span></span>           | <span data-ttu-id="2c240-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c240-218">0x00000010</span></span>                                           |
| <span data-ttu-id="2c240-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c240-219">Classes used in</span></span>        | [<span data-ttu-id="2c240-220">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c240-220">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2c240-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2c240-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2c240-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-222">Entry</span></span> | <span data-ttu-id="2c240-223">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-223">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2c240-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-224">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-225">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c240-226">System-Only</span></span>            | <span data-ttu-id="2c240-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-227">False</span></span>                                                |
| <span data-ttu-id="2c240-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c240-228">Is-Single-Valued</span></span>       | <span data-ttu-id="2c240-229">True</span><span class="sxs-lookup"><span data-stu-id="2c240-229">True</span></span>                                                 |
| <span data-ttu-id="2c240-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c240-230">Is Indexed</span></span>             | <span data-ttu-id="2c240-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-231">False</span></span>                                                |
| <span data-ttu-id="2c240-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c240-232">In Global Catalog</span></span>      | <span data-ttu-id="2c240-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-233">False</span></span>                                                |
| <span data-ttu-id="2c240-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c240-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c240-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c240-235">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2c240-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c240-236">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c240-237">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-238">Search-Flags</span></span>           | <span data-ttu-id="2c240-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c240-239">0x00000000</span></span>                                           |
| <span data-ttu-id="2c240-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-240">System-Flags</span></span>           | <span data-ttu-id="2c240-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c240-241">0x00000010</span></span>                                           |
| <span data-ttu-id="2c240-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c240-242">Classes used in</span></span>        | [<span data-ttu-id="2c240-243">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c240-243">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2c240-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c240-244">Windows Server 2012</span></span>



| <span data-ttu-id="2c240-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="2c240-245">Entry</span></span> | <span data-ttu-id="2c240-246">Значение</span><span class="sxs-lookup"><span data-stu-id="2c240-246">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="2c240-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2c240-247">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2c240-248">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="2c240-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="2c240-249">System-Only</span></span>            | <span data-ttu-id="2c240-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-250">False</span></span>                                                |
| <span data-ttu-id="2c240-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2c240-251">Is-Single-Valued</span></span>       | <span data-ttu-id="2c240-252">True</span><span class="sxs-lookup"><span data-stu-id="2c240-252">True</span></span>                                                 |
| <span data-ttu-id="2c240-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2c240-253">Is Indexed</span></span>             | <span data-ttu-id="2c240-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-254">False</span></span>                                                |
| <span data-ttu-id="2c240-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2c240-255">In Global Catalog</span></span>      | <span data-ttu-id="2c240-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="2c240-256">False</span></span>                                                |
| <span data-ttu-id="2c240-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2c240-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="2c240-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2c240-258">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="2c240-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2c240-259">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2c240-260">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="2c240-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-261">Search-Flags</span></span>           | <span data-ttu-id="2c240-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2c240-262">0x00000000</span></span>                                           |
| <span data-ttu-id="2c240-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2c240-263">System-Flags</span></span>           | <span data-ttu-id="2c240-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2c240-264">0x00000010</span></span>                                           |
| <span data-ttu-id="2c240-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2c240-265">Classes used in</span></span>        | [<span data-ttu-id="2c240-266">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="2c240-266">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





