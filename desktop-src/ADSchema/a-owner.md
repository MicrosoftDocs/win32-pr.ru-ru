---
title: Атрибут Owner
description: Различающееся имя объекта, который владеет объектом.
ms.assetid: 37b0e8eb-fe33-494a-9e1f-264cf9211344
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Owner
- Схема AD атрибута Owner
topic_type:
- apiref
api_name:
- Owner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416158fea3fd0e3dfbda1cd60b2543d3df16248
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536191"
---
# <a name="owner-attribute"></a><span data-ttu-id="5f7b7-105">Атрибут Owner</span><span class="sxs-lookup"><span data-stu-id="5f7b7-105">Owner attribute</span></span>

<span data-ttu-id="5f7b7-106">Различающееся имя объекта, который владеет объектом.</span><span class="sxs-lookup"><span data-stu-id="5f7b7-106">The distinguished name of an object that has ownership of an object.</span></span>



| <span data-ttu-id="5f7b7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-107">Entry</span></span> | <span data-ttu-id="5f7b7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="5f7b7-109">CN</span><span class="sxs-lookup"><span data-stu-id="5f7b7-109">CN</span></span>                | <span data-ttu-id="5f7b7-110">Владелец</span><span class="sxs-lookup"><span data-stu-id="5f7b7-110">Owner</span></span>                                   |
| <span data-ttu-id="5f7b7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5f7b7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5f7b7-112">владелец</span><span class="sxs-lookup"><span data-stu-id="5f7b7-112">owner</span></span>                                   |
| <span data-ttu-id="5f7b7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5f7b7-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="5f7b7-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5f7b7-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="5f7b7-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5f7b7-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="5f7b7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-116">Attribute-Id</span></span>      | <span data-ttu-id="5f7b7-117">2.5.4.32</span><span class="sxs-lookup"><span data-stu-id="5f7b7-117">2.5.4.32</span></span>                                |
| <span data-ttu-id="5f7b7-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5f7b7-118">System-Id-Guid</span></span>    | <span data-ttu-id="5f7b7-119">bf9679f3-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5f7b7-119">bf9679f3-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="5f7b7-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f7b7-120">Syntax</span></span>            | [<span data-ttu-id="5f7b7-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="5f7b7-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5f7b7-122">Implementations</span></span>

-   [<span data-ttu-id="5f7b7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5f7b7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5f7b7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5f7b7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5f7b7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5f7b7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5f7b7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f7b7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5f7b7-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-130">Entry</span></span> | <span data-ttu-id="5f7b7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7b7-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5f7b7-132">Link-Id</span></span>                | <span data-ttu-id="5f7b7-133">44</span><span class="sxs-lookup"><span data-stu-id="5f7b7-133">44</span></span>                                                                                        |
| <span data-ttu-id="5f7b7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-134">MAPI-Id</span></span>                | \-                                                                                        |
| <span data-ttu-id="5f7b7-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f7b7-135">System-Only</span></span>            | <span data-ttu-id="5f7b7-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-136">False</span></span>                                                                                     |
| <span data-ttu-id="5f7b7-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5f7b7-137">Is-Single-Valued</span></span>       | <span data-ttu-id="5f7b7-138">True</span><span class="sxs-lookup"><span data-stu-id="5f7b7-138">True</span></span>                                                                                      |
| <span data-ttu-id="5f7b7-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5f7b7-139">Is Indexed</span></span>             | <span data-ttu-id="5f7b7-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-140">False</span></span>                                                                                     |
| <span data-ttu-id="5f7b7-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5f7b7-141">In Global Catalog</span></span>      | <span data-ttu-id="5f7b7-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-142">False</span></span>                                                                                     |
| <span data-ttu-id="5f7b7-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5f7b7-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f7b7-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f7b7-144">O:BAG:BAD:S:</span></span>                                                                              |
| <span data-ttu-id="5f7b7-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f7b7-145">Range-Lower</span></span>            | \-                                                                                        |
| <span data-ttu-id="5f7b7-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f7b7-146">Range-Upper</span></span>            | \-                                                                                        |
| <span data-ttu-id="5f7b7-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-147">Search-Flags</span></span>           | <span data-ttu-id="5f7b7-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f7b7-148">0x00000000</span></span>                                                                                |
| <span data-ttu-id="5f7b7-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-149">System-Flags</span></span>           | <span data-ttu-id="5f7b7-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f7b7-150">0x00000010</span></span>                                                                                |
| <span data-ttu-id="5f7b7-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5f7b7-151">Classes used in</span></span>        | [<span data-ttu-id="5f7b7-152">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-152">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="5f7b7-153">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-153">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5f7b7-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5f7b7-154">Windows Server 2003</span></span>



| <span data-ttu-id="5f7b7-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-155">Entry</span></span> | <span data-ttu-id="5f7b7-156">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-156">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7b7-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5f7b7-157">Link-Id</span></span>                | <span data-ttu-id="5f7b7-158">44</span><span class="sxs-lookup"><span data-stu-id="5f7b7-158">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="5f7b7-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-159">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f7b7-160">System-Only</span></span>            | <span data-ttu-id="5f7b7-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-161">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5f7b7-162">Is-Single-Valued</span></span>       | <span data-ttu-id="5f7b7-163">True</span><span class="sxs-lookup"><span data-stu-id="5f7b7-163">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="5f7b7-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5f7b7-164">Is Indexed</span></span>             | <span data-ttu-id="5f7b7-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-165">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5f7b7-166">In Global Catalog</span></span>      | <span data-ttu-id="5f7b7-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-167">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5f7b7-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f7b7-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f7b7-169">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="5f7b7-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f7b7-170">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f7b7-171">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-172">Search-Flags</span></span>           | <span data-ttu-id="5f7b7-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f7b7-173">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-174">System-Flags</span></span>           | <span data-ttu-id="5f7b7-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f7b7-175">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5f7b7-176">Classes used in</span></span>        | [<span data-ttu-id="5f7b7-177">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-177">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="5f7b7-178">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-178">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="5f7b7-179">**граупофуникуенамес**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-179">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5f7b7-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5f7b7-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5f7b7-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-181">Entry</span></span> | <span data-ttu-id="5f7b7-182">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-182">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7b7-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5f7b7-183">Link-Id</span></span>                | <span data-ttu-id="5f7b7-184">44</span><span class="sxs-lookup"><span data-stu-id="5f7b7-184">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="5f7b7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-185">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f7b7-186">System-Only</span></span>            | <span data-ttu-id="5f7b7-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-187">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5f7b7-188">Is-Single-Valued</span></span>       | <span data-ttu-id="5f7b7-189">True</span><span class="sxs-lookup"><span data-stu-id="5f7b7-189">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="5f7b7-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5f7b7-190">Is Indexed</span></span>             | <span data-ttu-id="5f7b7-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-191">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5f7b7-192">In Global Catalog</span></span>      | <span data-ttu-id="5f7b7-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-193">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5f7b7-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f7b7-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f7b7-195">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="5f7b7-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f7b7-196">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f7b7-197">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-198">Search-Flags</span></span>           | <span data-ttu-id="5f7b7-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f7b7-199">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-200">System-Flags</span></span>           | <span data-ttu-id="5f7b7-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f7b7-201">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5f7b7-202">Classes used in</span></span>        | [<span data-ttu-id="5f7b7-203">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-203">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="5f7b7-204">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-204">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="5f7b7-205">**граупофуникуенамес**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-205">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5f7b7-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f7b7-206">Windows Server 2008</span></span>



| <span data-ttu-id="5f7b7-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-207">Entry</span></span> | <span data-ttu-id="5f7b7-208">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7b7-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5f7b7-209">Link-Id</span></span>                | <span data-ttu-id="5f7b7-210">44</span><span class="sxs-lookup"><span data-stu-id="5f7b7-210">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="5f7b7-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-211">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f7b7-212">System-Only</span></span>            | <span data-ttu-id="5f7b7-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-213">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5f7b7-214">Is-Single-Valued</span></span>       | <span data-ttu-id="5f7b7-215">True</span><span class="sxs-lookup"><span data-stu-id="5f7b7-215">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="5f7b7-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5f7b7-216">Is Indexed</span></span>             | <span data-ttu-id="5f7b7-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-217">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5f7b7-218">In Global Catalog</span></span>      | <span data-ttu-id="5f7b7-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-219">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5f7b7-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f7b7-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f7b7-221">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="5f7b7-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f7b7-222">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f7b7-223">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-224">Search-Flags</span></span>           | <span data-ttu-id="5f7b7-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f7b7-225">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-226">System-Flags</span></span>           | <span data-ttu-id="5f7b7-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f7b7-227">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5f7b7-228">Classes used in</span></span>        | [<span data-ttu-id="5f7b7-229">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-229">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="5f7b7-230">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-230">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="5f7b7-231">**граупофуникуенамес**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-231">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5f7b7-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5f7b7-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5f7b7-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-233">Entry</span></span> | <span data-ttu-id="5f7b7-234">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7b7-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5f7b7-235">Link-Id</span></span>                | <span data-ttu-id="5f7b7-236">44</span><span class="sxs-lookup"><span data-stu-id="5f7b7-236">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="5f7b7-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-237">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f7b7-238">System-Only</span></span>            | <span data-ttu-id="5f7b7-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-239">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5f7b7-240">Is-Single-Valued</span></span>       | <span data-ttu-id="5f7b7-241">True</span><span class="sxs-lookup"><span data-stu-id="5f7b7-241">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="5f7b7-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5f7b7-242">Is Indexed</span></span>             | <span data-ttu-id="5f7b7-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-243">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5f7b7-244">In Global Catalog</span></span>      | <span data-ttu-id="5f7b7-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-245">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5f7b7-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f7b7-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f7b7-247">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="5f7b7-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f7b7-248">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f7b7-249">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-250">Search-Flags</span></span>           | <span data-ttu-id="5f7b7-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f7b7-251">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-252">System-Flags</span></span>           | <span data-ttu-id="5f7b7-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f7b7-253">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5f7b7-254">Classes used in</span></span>        | [<span data-ttu-id="5f7b7-255">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-255">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="5f7b7-256">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-256">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="5f7b7-257">**граупофуникуенамес**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-257">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5f7b7-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f7b7-258">Windows Server 2012</span></span>



| <span data-ttu-id="5f7b7-259">Ввод</span><span class="sxs-lookup"><span data-stu-id="5f7b7-259">Entry</span></span> | <span data-ttu-id="5f7b7-260">Значение</span><span class="sxs-lookup"><span data-stu-id="5f7b7-260">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f7b7-261">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5f7b7-261">Link-Id</span></span>                | <span data-ttu-id="5f7b7-262">44</span><span class="sxs-lookup"><span data-stu-id="5f7b7-262">44</span></span>                                                                                                                                                      |
| <span data-ttu-id="5f7b7-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5f7b7-263">MAPI-Id</span></span>                | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="5f7b7-264">System-Only</span></span>            | <span data-ttu-id="5f7b7-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-265">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-266">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5f7b7-266">Is-Single-Valued</span></span>       | <span data-ttu-id="5f7b7-267">True</span><span class="sxs-lookup"><span data-stu-id="5f7b7-267">True</span></span>                                                                                                                                                    |
| <span data-ttu-id="5f7b7-268">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5f7b7-268">Is Indexed</span></span>             | <span data-ttu-id="5f7b7-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-269">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-270">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5f7b7-270">In Global Catalog</span></span>      | <span data-ttu-id="5f7b7-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="5f7b7-271">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="5f7b7-272">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5f7b7-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="5f7b7-273">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5f7b7-273">O:BAG:BAD:S:</span></span>                                                                                                                                            |
| <span data-ttu-id="5f7b7-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5f7b7-274">Range-Lower</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5f7b7-275">Range-Upper</span></span>            | \-                                                                                                                                                      |
| <span data-ttu-id="5f7b7-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-276">Search-Flags</span></span>           | <span data-ttu-id="5f7b7-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5f7b7-277">0x00000000</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5f7b7-278">System-Flags</span></span>           | <span data-ttu-id="5f7b7-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5f7b7-279">0x00000010</span></span>                                                                                                                                              |
| <span data-ttu-id="5f7b7-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5f7b7-280">Classes used in</span></span>        | [<span data-ttu-id="5f7b7-281">**Устройство**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-281">**Device**</span></span>](c-device.md)<br/> [<span data-ttu-id="5f7b7-282">**Группы-имена**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-282">**Group-Of-Names**</span></span>](c-groupofnames.md)<br/> [<span data-ttu-id="5f7b7-283">**граупофуникуенамес**</span><span class="sxs-lookup"><span data-stu-id="5f7b7-283">**groupOfUniqueNames**</span></span>](c-groupofuniquenames.md)<br/> |



 

 





