---
title: ACS-не зарезервированный — атрибут частоты пиковой нагрузки
description: Атрибут ACS-не зарезервирован — Пиковая ставка предназначен только для внутреннего использования.
ms.assetid: 4080839c-d99e-4527-8c81-6d23ab0d3d70
ms.tgt_platform: multiple
keywords:
- ACS — незарезервированная — схема AD атрибута "Пиковая частота"
- Схема AD атрибута Акснонресерведпеакрате
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Peak-Rate
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3d2075e90648388a9a1277dbbe768a3fc616f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138330"
---
# <a name="acs-non-reserved-peak-rate-attribute"></a><span data-ttu-id="ee41b-105">ACS-не зарезервированный — атрибут частоты пиковой нагрузки</span><span class="sxs-lookup"><span data-stu-id="ee41b-105">ACS-Non-Reserved-Peak-Rate attribute</span></span>

<span data-ttu-id="ee41b-106">Атрибут **ACS-не зарезервирован — Пиковая ставка** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="ee41b-106">The **ACS-Non-Reserved-Peak-Rate** attribute is for internal use only.</span></span> <span data-ttu-id="ee41b-107">На основе RFC2814.</span><span class="sxs-lookup"><span data-stu-id="ee41b-107">Based on RFC2814.</span></span>



| <span data-ttu-id="ee41b-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-108">Entry</span></span> | <span data-ttu-id="ee41b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ee41b-110">CN</span><span class="sxs-lookup"><span data-stu-id="ee41b-110">CN</span></span>                | <span data-ttu-id="ee41b-111">ACS — не зарезервировано — Пиковая ставка</span><span class="sxs-lookup"><span data-stu-id="ee41b-111">ACS-Non-Reserved-Peak-Rate</span></span>           |
| <span data-ttu-id="ee41b-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ee41b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ee41b-113">акснонресерведпеакрате</span><span class="sxs-lookup"><span data-stu-id="ee41b-113">aCSNonReservedPeakRate</span></span>               |
| <span data-ttu-id="ee41b-114">Размер</span><span class="sxs-lookup"><span data-stu-id="ee41b-114">Size</span></span>              | <span data-ttu-id="ee41b-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="ee41b-115">8 bytes</span></span>                              |
| <span data-ttu-id="ee41b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ee41b-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ee41b-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ee41b-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ee41b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-118">Attribute-Id</span></span>      | <span data-ttu-id="ee41b-119">1.2.840.113556.1.4.1318</span><span class="sxs-lookup"><span data-stu-id="ee41b-119">1.2.840.113556.1.4.1318</span></span>              |
| <span data-ttu-id="ee41b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ee41b-120">System-Id-Guid</span></span>    | <span data-ttu-id="ee41b-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="ee41b-121">a331a73f-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="ee41b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee41b-122">Syntax</span></span>            | [<span data-ttu-id="ee41b-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="ee41b-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="ee41b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ee41b-124">Implementations</span></span>

-   [<span data-ttu-id="ee41b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ee41b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ee41b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ee41b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ee41b-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ee41b-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ee41b-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ee41b-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ee41b-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ee41b-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ee41b-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ee41b-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ee41b-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee41b-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ee41b-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-132">Entry</span></span> | <span data-ttu-id="ee41b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee41b-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ee41b-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee41b-136">System-Only</span></span>            | <span data-ttu-id="ee41b-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-137">False</span></span>                                        |
| <span data-ttu-id="ee41b-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ee41b-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ee41b-139">True</span><span class="sxs-lookup"><span data-stu-id="ee41b-139">True</span></span>                                         |
| <span data-ttu-id="ee41b-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ee41b-140">Is Indexed</span></span>             | <span data-ttu-id="ee41b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-141">False</span></span>                                        |
| <span data-ttu-id="ee41b-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ee41b-142">In Global Catalog</span></span>      | <span data-ttu-id="ee41b-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-143">False</span></span>                                        |
| <span data-ttu-id="ee41b-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ee41b-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee41b-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee41b-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee41b-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee41b-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee41b-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-148">Search-Flags</span></span>           | <span data-ttu-id="ee41b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee41b-149">0x00000000</span></span>                                   |
| <span data-ttu-id="ee41b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-150">System-Flags</span></span>           | <span data-ttu-id="ee41b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee41b-151">0x00000010</span></span>                                   |
| <span data-ttu-id="ee41b-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ee41b-152">Classes used in</span></span>        | [<span data-ttu-id="ee41b-153">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ee41b-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ee41b-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee41b-154">Windows Server 2003</span></span>



| <span data-ttu-id="ee41b-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-155">Entry</span></span> | <span data-ttu-id="ee41b-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee41b-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ee41b-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee41b-159">System-Only</span></span>            | <span data-ttu-id="ee41b-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-160">False</span></span>                                        |
| <span data-ttu-id="ee41b-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ee41b-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ee41b-162">True</span><span class="sxs-lookup"><span data-stu-id="ee41b-162">True</span></span>                                         |
| <span data-ttu-id="ee41b-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ee41b-163">Is Indexed</span></span>             | <span data-ttu-id="ee41b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-164">False</span></span>                                        |
| <span data-ttu-id="ee41b-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ee41b-165">In Global Catalog</span></span>      | <span data-ttu-id="ee41b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-166">False</span></span>                                        |
| <span data-ttu-id="ee41b-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ee41b-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee41b-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee41b-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee41b-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee41b-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee41b-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-171">Search-Flags</span></span>           | <span data-ttu-id="ee41b-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee41b-172">0x00000000</span></span>                                   |
| <span data-ttu-id="ee41b-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-173">System-Flags</span></span>           | <span data-ttu-id="ee41b-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee41b-174">0x00000010</span></span>                                   |
| <span data-ttu-id="ee41b-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ee41b-175">Classes used in</span></span>        | [<span data-ttu-id="ee41b-176">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ee41b-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ee41b-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ee41b-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ee41b-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-178">Entry</span></span> | <span data-ttu-id="ee41b-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee41b-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ee41b-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee41b-182">System-Only</span></span>            | <span data-ttu-id="ee41b-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-183">False</span></span>                                        |
| <span data-ttu-id="ee41b-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ee41b-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ee41b-185">True</span><span class="sxs-lookup"><span data-stu-id="ee41b-185">True</span></span>                                         |
| <span data-ttu-id="ee41b-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ee41b-186">Is Indexed</span></span>             | <span data-ttu-id="ee41b-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-187">False</span></span>                                        |
| <span data-ttu-id="ee41b-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ee41b-188">In Global Catalog</span></span>      | <span data-ttu-id="ee41b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-189">False</span></span>                                        |
| <span data-ttu-id="ee41b-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ee41b-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee41b-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee41b-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee41b-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee41b-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee41b-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-194">Search-Flags</span></span>           | <span data-ttu-id="ee41b-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee41b-195">0x00000000</span></span>                                   |
| <span data-ttu-id="ee41b-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-196">System-Flags</span></span>           | <span data-ttu-id="ee41b-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee41b-197">0x00000010</span></span>                                   |
| <span data-ttu-id="ee41b-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ee41b-198">Classes used in</span></span>        | [<span data-ttu-id="ee41b-199">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ee41b-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ee41b-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee41b-200">Windows Server 2008</span></span>



| <span data-ttu-id="ee41b-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-201">Entry</span></span> | <span data-ttu-id="ee41b-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee41b-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ee41b-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee41b-205">System-Only</span></span>            | <span data-ttu-id="ee41b-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-206">False</span></span>                                        |
| <span data-ttu-id="ee41b-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ee41b-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ee41b-208">True</span><span class="sxs-lookup"><span data-stu-id="ee41b-208">True</span></span>                                         |
| <span data-ttu-id="ee41b-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ee41b-209">Is Indexed</span></span>             | <span data-ttu-id="ee41b-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-210">False</span></span>                                        |
| <span data-ttu-id="ee41b-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ee41b-211">In Global Catalog</span></span>      | <span data-ttu-id="ee41b-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-212">False</span></span>                                        |
| <span data-ttu-id="ee41b-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ee41b-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee41b-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee41b-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee41b-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee41b-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee41b-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-217">Search-Flags</span></span>           | <span data-ttu-id="ee41b-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee41b-218">0x00000000</span></span>                                   |
| <span data-ttu-id="ee41b-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-219">System-Flags</span></span>           | <span data-ttu-id="ee41b-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee41b-220">0x00000010</span></span>                                   |
| <span data-ttu-id="ee41b-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ee41b-221">Classes used in</span></span>        | [<span data-ttu-id="ee41b-222">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ee41b-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ee41b-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee41b-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ee41b-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-224">Entry</span></span> | <span data-ttu-id="ee41b-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee41b-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ee41b-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee41b-228">System-Only</span></span>            | <span data-ttu-id="ee41b-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-229">False</span></span>                                        |
| <span data-ttu-id="ee41b-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ee41b-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ee41b-231">True</span><span class="sxs-lookup"><span data-stu-id="ee41b-231">True</span></span>                                         |
| <span data-ttu-id="ee41b-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ee41b-232">Is Indexed</span></span>             | <span data-ttu-id="ee41b-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-233">False</span></span>                                        |
| <span data-ttu-id="ee41b-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ee41b-234">In Global Catalog</span></span>      | <span data-ttu-id="ee41b-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-235">False</span></span>                                        |
| <span data-ttu-id="ee41b-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ee41b-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee41b-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee41b-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee41b-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee41b-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee41b-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-240">Search-Flags</span></span>           | <span data-ttu-id="ee41b-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee41b-241">0x00000000</span></span>                                   |
| <span data-ttu-id="ee41b-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-242">System-Flags</span></span>           | <span data-ttu-id="ee41b-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee41b-243">0x00000010</span></span>                                   |
| <span data-ttu-id="ee41b-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ee41b-244">Classes used in</span></span>        | [<span data-ttu-id="ee41b-245">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ee41b-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ee41b-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee41b-246">Windows Server 2012</span></span>



| <span data-ttu-id="ee41b-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee41b-247">Entry</span></span> | <span data-ttu-id="ee41b-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ee41b-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ee41b-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ee41b-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ee41b-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ee41b-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ee41b-251">System-Only</span></span>            | <span data-ttu-id="ee41b-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-252">False</span></span>                                        |
| <span data-ttu-id="ee41b-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ee41b-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ee41b-254">True</span><span class="sxs-lookup"><span data-stu-id="ee41b-254">True</span></span>                                         |
| <span data-ttu-id="ee41b-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ee41b-255">Is Indexed</span></span>             | <span data-ttu-id="ee41b-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-256">False</span></span>                                        |
| <span data-ttu-id="ee41b-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ee41b-257">In Global Catalog</span></span>      | <span data-ttu-id="ee41b-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="ee41b-258">False</span></span>                                        |
| <span data-ttu-id="ee41b-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ee41b-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ee41b-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ee41b-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ee41b-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ee41b-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ee41b-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ee41b-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-263">Search-Flags</span></span>           | <span data-ttu-id="ee41b-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ee41b-264">0x00000000</span></span>                                   |
| <span data-ttu-id="ee41b-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ee41b-265">System-Flags</span></span>           | <span data-ttu-id="ee41b-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ee41b-266">0x00000010</span></span>                                   |
| <span data-ttu-id="ee41b-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ee41b-267">Classes used in</span></span>        | [<span data-ttu-id="ee41b-268">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ee41b-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





