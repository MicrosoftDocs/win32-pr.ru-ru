---
title: Атрибут Mastered-By
description: Обратная ссылка для атрибута с параметром-Master-NC. Различающееся имя для объектов параметров NTDS.
ms.assetid: bd14998c-1691-4167-83c4-3c1ec1181b7f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Mastered-By
- Схема AD атрибута Мастередби
topic_type:
- apiref
api_name:
- Mastered-By
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cf02f78363e1e8db06bddfb2c389cc78077090
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138262"
---
# <a name="mastered-by-attribute"></a><span data-ttu-id="64f4b-106">Атрибут Mastered-By</span><span class="sxs-lookup"><span data-stu-id="64f4b-106">Mastered-By attribute</span></span>

<span data-ttu-id="64f4b-107">Обратная ссылка для атрибута с параметром-Master-NC.</span><span class="sxs-lookup"><span data-stu-id="64f4b-107">Backward link for Has-Master-NCs attribute.</span></span> <span data-ttu-id="64f4b-108">Различающееся имя для объектов параметров NTDS.</span><span class="sxs-lookup"><span data-stu-id="64f4b-108">The distinguished name for its NTDS Settings objects.</span></span>



| <span data-ttu-id="64f4b-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-109">Entry</span></span> | <span data-ttu-id="64f4b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="64f4b-111">CN</span><span class="sxs-lookup"><span data-stu-id="64f4b-111">CN</span></span>                | <span data-ttu-id="64f4b-112">Mastered-By</span><span class="sxs-lookup"><span data-stu-id="64f4b-112">Mastered-By</span></span>                             |
| <span data-ttu-id="64f4b-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="64f4b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="64f4b-114">мастередби</span><span class="sxs-lookup"><span data-stu-id="64f4b-114">masteredBy</span></span>                              |
| <span data-ttu-id="64f4b-115">Размер</span><span class="sxs-lookup"><span data-stu-id="64f4b-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="64f4b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="64f4b-116">Update Privilege</span></span>  | <span data-ttu-id="64f4b-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="64f4b-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="64f4b-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="64f4b-118">Update Frequency</span></span>  | <span data-ttu-id="64f4b-119">При создании контекста именования.</span><span class="sxs-lookup"><span data-stu-id="64f4b-119">When the Naming Context is created.</span></span>     |
| <span data-ttu-id="64f4b-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-120">Attribute-Id</span></span>      | <span data-ttu-id="64f4b-121">1.2.840.113556.1.4.1409</span><span class="sxs-lookup"><span data-stu-id="64f4b-121">1.2.840.113556.1.4.1409</span></span>                 |
| <span data-ttu-id="64f4b-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="64f4b-122">System-Id-Guid</span></span>    | <span data-ttu-id="64f4b-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="64f4b-123">e48e64e0-12c9-11d3-9102-00c04fd91ab1</span></span>    |
| <span data-ttu-id="64f4b-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64f4b-124">Syntax</span></span>            | [<span data-ttu-id="64f4b-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="64f4b-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="64f4b-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="64f4b-126">Implementations</span></span>

-   [<span data-ttu-id="64f4b-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="64f4b-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="64f4b-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="64f4b-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="64f4b-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="64f4b-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="64f4b-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="64f4b-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="64f4b-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="64f4b-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="64f4b-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="64f4b-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="64f4b-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="64f4b-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="64f4b-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64f4b-134">Windows 2000 Server</span></span>



| <span data-ttu-id="64f4b-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-135">Entry</span></span> | <span data-ttu-id="64f4b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-137">Link-Id</span></span>                | <span data-ttu-id="64f4b-138">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-138">77</span></span>                              |
| <span data-ttu-id="64f4b-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-139">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-140">System-Only</span></span>            | <span data-ttu-id="64f4b-141">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-141">True</span></span>                            |
| <span data-ttu-id="64f4b-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-142">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-143">False</span></span>                           |
| <span data-ttu-id="64f4b-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-144">Is Indexed</span></span>             | <span data-ttu-id="64f4b-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-145">False</span></span>                           |
| <span data-ttu-id="64f4b-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-146">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-147">False</span></span>                           |
| <span data-ttu-id="64f4b-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-152">Search-Flags</span></span>           | <span data-ttu-id="64f4b-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-153">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-154">System-Flags</span></span>           | <span data-ttu-id="64f4b-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-155">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-156">Classes used in</span></span>        | [<span data-ttu-id="64f4b-157">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="64f4b-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="64f4b-158">Windows Server 2003</span></span>



| <span data-ttu-id="64f4b-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-159">Entry</span></span> | <span data-ttu-id="64f4b-160">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-161">Link-Id</span></span>                | <span data-ttu-id="64f4b-162">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-162">77</span></span>                              |
| <span data-ttu-id="64f4b-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-163">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-164">System-Only</span></span>            | <span data-ttu-id="64f4b-165">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-165">True</span></span>                            |
| <span data-ttu-id="64f4b-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-166">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-167">False</span></span>                           |
| <span data-ttu-id="64f4b-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-168">Is Indexed</span></span>             | <span data-ttu-id="64f4b-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-169">False</span></span>                           |
| <span data-ttu-id="64f4b-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-170">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-171">False</span></span>                           |
| <span data-ttu-id="64f4b-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-176">Search-Flags</span></span>           | <span data-ttu-id="64f4b-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-177">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-178">System-Flags</span></span>           | <span data-ttu-id="64f4b-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-179">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-180">Classes used in</span></span>        | [<span data-ttu-id="64f4b-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="64f4b-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="64f4b-182">ADAM</span></span>



| <span data-ttu-id="64f4b-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-183">Entry</span></span> | <span data-ttu-id="64f4b-184">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-185">Link-Id</span></span>                | <span data-ttu-id="64f4b-186">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-186">77</span></span>                              |
| <span data-ttu-id="64f4b-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-187">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-188">System-Only</span></span>            | <span data-ttu-id="64f4b-189">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-189">True</span></span>                            |
| <span data-ttu-id="64f4b-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-190">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-191">False</span></span>                           |
| <span data-ttu-id="64f4b-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-192">Is Indexed</span></span>             | <span data-ttu-id="64f4b-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-193">False</span></span>                           |
| <span data-ttu-id="64f4b-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-194">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-195">False</span></span>                           |
| <span data-ttu-id="64f4b-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-200">Search-Flags</span></span>           | <span data-ttu-id="64f4b-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-201">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-202">System-Flags</span></span>           | <span data-ttu-id="64f4b-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-203">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-204">Classes used in</span></span>        | [<span data-ttu-id="64f4b-205">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="64f4b-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="64f4b-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="64f4b-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-207">Entry</span></span> | <span data-ttu-id="64f4b-208">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-209">Link-Id</span></span>                | <span data-ttu-id="64f4b-210">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-210">77</span></span>                              |
| <span data-ttu-id="64f4b-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-212">System-Only</span></span>            | <span data-ttu-id="64f4b-213">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-213">True</span></span>                            |
| <span data-ttu-id="64f4b-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-214">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-215">False</span></span>                           |
| <span data-ttu-id="64f4b-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-216">Is Indexed</span></span>             | <span data-ttu-id="64f4b-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-217">False</span></span>                           |
| <span data-ttu-id="64f4b-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-218">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-219">False</span></span>                           |
| <span data-ttu-id="64f4b-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-224">Search-Flags</span></span>           | <span data-ttu-id="64f4b-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-225">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-226">System-Flags</span></span>           | <span data-ttu-id="64f4b-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-227">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-228">Classes used in</span></span>        | [<span data-ttu-id="64f4b-229">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="64f4b-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64f4b-230">Windows Server 2008</span></span>



| <span data-ttu-id="64f4b-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-231">Entry</span></span> | <span data-ttu-id="64f4b-232">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-233">Link-Id</span></span>                | <span data-ttu-id="64f4b-234">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-234">77</span></span>                              |
| <span data-ttu-id="64f4b-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-235">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-236">System-Only</span></span>            | <span data-ttu-id="64f4b-237">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-237">True</span></span>                            |
| <span data-ttu-id="64f4b-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-238">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-239">False</span></span>                           |
| <span data-ttu-id="64f4b-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-240">Is Indexed</span></span>             | <span data-ttu-id="64f4b-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-241">False</span></span>                           |
| <span data-ttu-id="64f4b-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-242">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-243">False</span></span>                           |
| <span data-ttu-id="64f4b-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-248">Search-Flags</span></span>           | <span data-ttu-id="64f4b-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-249">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-250">System-Flags</span></span>           | <span data-ttu-id="64f4b-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-251">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-252">Classes used in</span></span>        | [<span data-ttu-id="64f4b-253">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="64f4b-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="64f4b-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="64f4b-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-255">Entry</span></span> | <span data-ttu-id="64f4b-256">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-257">Link-Id</span></span>                | <span data-ttu-id="64f4b-258">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-258">77</span></span>                              |
| <span data-ttu-id="64f4b-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-259">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-260">System-Only</span></span>            | <span data-ttu-id="64f4b-261">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-261">True</span></span>                            |
| <span data-ttu-id="64f4b-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-262">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-263">False</span></span>                           |
| <span data-ttu-id="64f4b-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-264">Is Indexed</span></span>             | <span data-ttu-id="64f4b-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-265">False</span></span>                           |
| <span data-ttu-id="64f4b-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-266">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-267">False</span></span>                           |
| <span data-ttu-id="64f4b-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-272">Search-Flags</span></span>           | <span data-ttu-id="64f4b-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-273">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-274">System-Flags</span></span>           | <span data-ttu-id="64f4b-275">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-275">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-276">Classes used in</span></span>        | [<span data-ttu-id="64f4b-277">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="64f4b-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="64f4b-278">Windows Server 2012</span></span>



| <span data-ttu-id="64f4b-279">Ввод</span><span class="sxs-lookup"><span data-stu-id="64f4b-279">Entry</span></span> | <span data-ttu-id="64f4b-280">Значение</span><span class="sxs-lookup"><span data-stu-id="64f4b-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="64f4b-281">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="64f4b-281">Link-Id</span></span>                | <span data-ttu-id="64f4b-282">77</span><span class="sxs-lookup"><span data-stu-id="64f4b-282">77</span></span>                              |
| <span data-ttu-id="64f4b-283">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="64f4b-283">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="64f4b-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="64f4b-284">System-Only</span></span>            | <span data-ttu-id="64f4b-285">True</span><span class="sxs-lookup"><span data-stu-id="64f4b-285">True</span></span>                            |
| <span data-ttu-id="64f4b-286">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="64f4b-286">Is-Single-Valued</span></span>       | <span data-ttu-id="64f4b-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-287">False</span></span>                           |
| <span data-ttu-id="64f4b-288">Индексируется</span><span class="sxs-lookup"><span data-stu-id="64f4b-288">Is Indexed</span></span>             | <span data-ttu-id="64f4b-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-289">False</span></span>                           |
| <span data-ttu-id="64f4b-290">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="64f4b-290">In Global Catalog</span></span>      | <span data-ttu-id="64f4b-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="64f4b-291">False</span></span>                           |
| <span data-ttu-id="64f4b-292">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="64f4b-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="64f4b-293">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="64f4b-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="64f4b-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="64f4b-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="64f4b-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="64f4b-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="64f4b-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-296">Search-Flags</span></span>           | <span data-ttu-id="64f4b-297">0x00000000</span><span class="sxs-lookup"><span data-stu-id="64f4b-297">0x00000000</span></span>                      |
| <span data-ttu-id="64f4b-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="64f4b-298">System-Flags</span></span>           | <span data-ttu-id="64f4b-299">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64f4b-299">0x00000010</span></span>                      |
| <span data-ttu-id="64f4b-300">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="64f4b-300">Classes used in</span></span>        | [<span data-ttu-id="64f4b-301">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="64f4b-301">**Top**</span></span>](c-top.md)<br/> |



 

 





