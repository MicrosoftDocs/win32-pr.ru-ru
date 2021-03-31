---
title: MS-DS-целостность-атрибут GUID
description: Этот атрибут используется для проверки согласованности между каталогом и другим объектом, базой данных или приложением путем сравнения идентификаторов GUID.
ms.assetid: 1372f46a-5569-4b06-9803-7d3862cdb745
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута GUID в MS-DS-целостности
- Схема AD атрибута mS-DS-ConsistencyGuid
topic_type:
- apiref
api_name:
- MS-DS-Consistency-Guid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbea1e9fba4ac28f968fdd61a054f55fe47deb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893562"
---
# <a name="ms-ds-consistency-guid-attribute"></a><span data-ttu-id="eebd4-105">MS-DS-целостность-атрибут GUID</span><span class="sxs-lookup"><span data-stu-id="eebd4-105">MS-DS-Consistency-Guid attribute</span></span>

<span data-ttu-id="eebd4-106">Этот атрибут используется для проверки согласованности между каталогом и другим объектом, базой данных или приложением путем сравнения идентификаторов GUID.</span><span class="sxs-lookup"><span data-stu-id="eebd4-106">This attribute is used to check consistency between the directory and another object, database, or application, by comparing GUIDs.</span></span>



| <span data-ttu-id="eebd4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-107">Entry</span></span> | <span data-ttu-id="eebd4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="eebd4-109">CN</span><span class="sxs-lookup"><span data-stu-id="eebd4-109">CN</span></span>                | <span data-ttu-id="eebd4-110">MS-DS-Consistencу-Guid</span><span class="sxs-lookup"><span data-stu-id="eebd4-110">MS-DS-Consistency-Guid</span></span>                                |
| <span data-ttu-id="eebd4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="eebd4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eebd4-112">mS-DS-ConsistencyGuid</span><span class="sxs-lookup"><span data-stu-id="eebd4-112">mS-DS-ConsistencyGuid</span></span>                                 |
| <span data-ttu-id="eebd4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="eebd4-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="eebd4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="eebd4-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="eebd4-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="eebd4-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="eebd4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-116">Attribute-Id</span></span>      | <span data-ttu-id="eebd4-117">1.2.840.113556.1.4.1360</span><span class="sxs-lookup"><span data-stu-id="eebd4-117">1.2.840.113556.1.4.1360</span></span>                               |
| <span data-ttu-id="eebd4-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="eebd4-118">System-Id-Guid</span></span>    | <span data-ttu-id="eebd4-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="eebd4-119">23773dc2-b63a-11d2-90e1-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="eebd4-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eebd4-120">Syntax</span></span>            | [<span data-ttu-id="eebd4-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="eebd4-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="eebd4-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="eebd4-122">Implementations</span></span>

-   [<span data-ttu-id="eebd4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eebd4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eebd4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eebd4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eebd4-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="eebd4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="eebd4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eebd4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eebd4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eebd4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eebd4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eebd4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eebd4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eebd4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eebd4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eebd4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="eebd4-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-131">Entry</span></span> | <span data-ttu-id="eebd4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-135">System-Only</span></span>            | <span data-ttu-id="eebd4-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-136">False</span></span>                           |
| <span data-ttu-id="eebd4-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-138">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-138">True</span></span>                            |
| <span data-ttu-id="eebd4-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-139">Is Indexed</span></span>             | <span data-ttu-id="eebd4-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-140">False</span></span>                           |
| <span data-ttu-id="eebd4-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-141">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-142">False</span></span>                           |
| <span data-ttu-id="eebd4-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-147">Search-Flags</span></span>           | <span data-ttu-id="eebd4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-148">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-149">System-Flags</span></span>           | <span data-ttu-id="eebd4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-150">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-151">Classes used in</span></span>        | [<span data-ttu-id="eebd4-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eebd4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eebd4-153">Windows Server 2003</span></span>



| <span data-ttu-id="eebd4-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-154">Entry</span></span> | <span data-ttu-id="eebd4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-158">System-Only</span></span>            | <span data-ttu-id="eebd4-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-159">False</span></span>                           |
| <span data-ttu-id="eebd4-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-161">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-161">True</span></span>                            |
| <span data-ttu-id="eebd4-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-162">Is Indexed</span></span>             | <span data-ttu-id="eebd4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-163">False</span></span>                           |
| <span data-ttu-id="eebd4-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-164">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-165">False</span></span>                           |
| <span data-ttu-id="eebd4-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-170">Search-Flags</span></span>           | <span data-ttu-id="eebd4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-171">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-172">System-Flags</span></span>           | <span data-ttu-id="eebd4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-173">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-174">Classes used in</span></span>        | [<span data-ttu-id="eebd4-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="eebd4-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="eebd4-176">ADAM</span></span>



| <span data-ttu-id="eebd4-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-177">Entry</span></span> | <span data-ttu-id="eebd4-178">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-181">System-Only</span></span>            | <span data-ttu-id="eebd4-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-182">False</span></span>                           |
| <span data-ttu-id="eebd4-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-184">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-184">True</span></span>                            |
| <span data-ttu-id="eebd4-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-185">Is Indexed</span></span>             | <span data-ttu-id="eebd4-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-186">False</span></span>                           |
| <span data-ttu-id="eebd4-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-187">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-188">False</span></span>                           |
| <span data-ttu-id="eebd4-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-193">Search-Flags</span></span>           | <span data-ttu-id="eebd4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-194">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-195">System-Flags</span></span>           | <span data-ttu-id="eebd4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-196">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-197">Classes used in</span></span>        | [<span data-ttu-id="eebd4-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eebd4-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eebd4-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eebd4-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-200">Entry</span></span> | <span data-ttu-id="eebd4-201">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-204">System-Only</span></span>            | <span data-ttu-id="eebd4-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-205">False</span></span>                           |
| <span data-ttu-id="eebd4-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-207">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-207">True</span></span>                            |
| <span data-ttu-id="eebd4-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-208">Is Indexed</span></span>             | <span data-ttu-id="eebd4-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-209">False</span></span>                           |
| <span data-ttu-id="eebd4-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-210">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-211">False</span></span>                           |
| <span data-ttu-id="eebd4-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-216">Search-Flags</span></span>           | <span data-ttu-id="eebd4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-217">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-218">System-Flags</span></span>           | <span data-ttu-id="eebd4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-219">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-220">Classes used in</span></span>        | [<span data-ttu-id="eebd4-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eebd4-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eebd4-222">Windows Server 2008</span></span>



| <span data-ttu-id="eebd4-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-223">Entry</span></span> | <span data-ttu-id="eebd4-224">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-227">System-Only</span></span>            | <span data-ttu-id="eebd4-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-228">False</span></span>                           |
| <span data-ttu-id="eebd4-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-230">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-230">True</span></span>                            |
| <span data-ttu-id="eebd4-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-231">Is Indexed</span></span>             | <span data-ttu-id="eebd4-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-232">False</span></span>                           |
| <span data-ttu-id="eebd4-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-233">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-234">False</span></span>                           |
| <span data-ttu-id="eebd4-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-239">Search-Flags</span></span>           | <span data-ttu-id="eebd4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-240">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-241">System-Flags</span></span>           | <span data-ttu-id="eebd4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-242">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-243">Classes used in</span></span>        | [<span data-ttu-id="eebd4-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eebd4-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eebd4-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eebd4-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-246">Entry</span></span> | <span data-ttu-id="eebd4-247">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-250">System-Only</span></span>            | <span data-ttu-id="eebd4-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-251">False</span></span>                           |
| <span data-ttu-id="eebd4-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-253">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-253">True</span></span>                            |
| <span data-ttu-id="eebd4-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-254">Is Indexed</span></span>             | <span data-ttu-id="eebd4-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-255">False</span></span>                           |
| <span data-ttu-id="eebd4-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-256">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-257">False</span></span>                           |
| <span data-ttu-id="eebd4-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-262">Search-Flags</span></span>           | <span data-ttu-id="eebd4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-263">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-264">System-Flags</span></span>           | <span data-ttu-id="eebd4-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-265">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-266">Classes used in</span></span>        | [<span data-ttu-id="eebd4-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eebd4-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eebd4-268">Windows Server 2012</span></span>



| <span data-ttu-id="eebd4-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="eebd4-269">Entry</span></span> | <span data-ttu-id="eebd4-270">Значение</span><span class="sxs-lookup"><span data-stu-id="eebd4-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="eebd4-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eebd4-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eebd4-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="eebd4-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="eebd4-273">System-Only</span></span>            | <span data-ttu-id="eebd4-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-274">False</span></span>                           |
| <span data-ttu-id="eebd4-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eebd4-275">Is-Single-Valued</span></span>       | <span data-ttu-id="eebd4-276">True</span><span class="sxs-lookup"><span data-stu-id="eebd4-276">True</span></span>                            |
| <span data-ttu-id="eebd4-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eebd4-277">Is Indexed</span></span>             | <span data-ttu-id="eebd4-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-278">False</span></span>                           |
| <span data-ttu-id="eebd4-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eebd4-279">In Global Catalog</span></span>      | <span data-ttu-id="eebd4-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="eebd4-280">False</span></span>                           |
| <span data-ttu-id="eebd4-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eebd4-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="eebd4-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eebd4-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="eebd4-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eebd4-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="eebd4-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eebd4-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="eebd4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-285">Search-Flags</span></span>           | <span data-ttu-id="eebd4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eebd4-286">0x00000000</span></span>                      |
| <span data-ttu-id="eebd4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eebd4-287">System-Flags</span></span>           | <span data-ttu-id="eebd4-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eebd4-288">0x00000010</span></span>                      |
| <span data-ttu-id="eebd4-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eebd4-289">Classes used in</span></span>        | [<span data-ttu-id="eebd4-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="eebd4-290">**Top**</span></span>](c-top.md)<br/> |



 

 





