---
title: ACS-не зарезервированный-min-Attribute-атрибут size
description: Атрибут ACS-не зарезервирован-min-с заданной функцией-size предназначен только для внутреннего использования.
ms.assetid: f5ee29ec-d2a9-4026-a4d1-0484d353efdc
ms.tgt_platform: multiple
keywords:
- ACS-не зарезервировано-минимальная-схема AD атрибута-размера
- Схема AD атрибута Акснонресерведминполицедсизе
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Min-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9fa7794343929aa0f7d7d86f4fc1f1e9a8a5b2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655554"
---
# <a name="acs-non-reserved-min-policed-size-attribute"></a><span data-ttu-id="699c2-105">ACS-не зарезервированный-min-Attribute-атрибут size</span><span class="sxs-lookup"><span data-stu-id="699c2-105">ACS-Non-Reserved-Min-Policed-Size attribute</span></span>

<span data-ttu-id="699c2-106">Атрибут **ACS-не зарезервирован-min-с заданной функцией-size** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="699c2-106">The **ACS-Non-Reserved-Min-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="699c2-107">На основе RFC2814.</span><span class="sxs-lookup"><span data-stu-id="699c2-107">Based on RFC2814.</span></span>



| <span data-ttu-id="699c2-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-108">Entry</span></span> | <span data-ttu-id="699c2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="699c2-110">CN</span><span class="sxs-lookup"><span data-stu-id="699c2-110">CN</span></span>                | <span data-ttu-id="699c2-111">ACS-не зарезервировано-min-with-size</span><span class="sxs-lookup"><span data-stu-id="699c2-111">ACS-Non-Reserved-Min-Policed-Size</span></span>    |
| <span data-ttu-id="699c2-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="699c2-112">Ldap-Display-Name</span></span> | <span data-ttu-id="699c2-113">акснонресерведминполицедсизе</span><span class="sxs-lookup"><span data-stu-id="699c2-113">aCSNonReservedMinPolicedSize</span></span>         |
| <span data-ttu-id="699c2-114">Размер</span><span class="sxs-lookup"><span data-stu-id="699c2-114">Size</span></span>              | <span data-ttu-id="699c2-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="699c2-115">8 bytes</span></span>                              |
| <span data-ttu-id="699c2-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="699c2-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="699c2-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="699c2-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="699c2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-118">Attribute-Id</span></span>      | <span data-ttu-id="699c2-119">1.2.840.113556.1.4.1321</span><span class="sxs-lookup"><span data-stu-id="699c2-119">1.2.840.113556.1.4.1321</span></span>              |
| <span data-ttu-id="699c2-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="699c2-120">System-Id-Guid</span></span>    | <span data-ttu-id="699c2-121">b6873917-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="699c2-121">b6873917-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="699c2-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="699c2-122">Syntax</span></span>            | [<span data-ttu-id="699c2-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="699c2-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="699c2-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="699c2-124">Implementations</span></span>

-   [<span data-ttu-id="699c2-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="699c2-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="699c2-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="699c2-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="699c2-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="699c2-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="699c2-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="699c2-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="699c2-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="699c2-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="699c2-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="699c2-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="699c2-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="699c2-131">Windows 2000 Server</span></span>



| <span data-ttu-id="699c2-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-132">Entry</span></span> | <span data-ttu-id="699c2-133">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="699c2-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c2-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c2-136">System-Only</span></span>            | <span data-ttu-id="699c2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-137">False</span></span>                                        |
| <span data-ttu-id="699c2-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c2-138">Is-Single-Valued</span></span>       | <span data-ttu-id="699c2-139">True</span><span class="sxs-lookup"><span data-stu-id="699c2-139">True</span></span>                                         |
| <span data-ttu-id="699c2-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c2-140">Is Indexed</span></span>             | <span data-ttu-id="699c2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-141">False</span></span>                                        |
| <span data-ttu-id="699c2-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c2-142">In Global Catalog</span></span>      | <span data-ttu-id="699c2-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-143">False</span></span>                                        |
| <span data-ttu-id="699c2-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c2-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c2-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c2-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="699c2-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c2-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="699c2-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c2-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="699c2-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-148">Search-Flags</span></span>           | <span data-ttu-id="699c2-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c2-149">0x00000000</span></span>                                   |
| <span data-ttu-id="699c2-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-150">System-Flags</span></span>           | <span data-ttu-id="699c2-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c2-151">0x00000010</span></span>                                   |
| <span data-ttu-id="699c2-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c2-152">Classes used in</span></span>        | [<span data-ttu-id="699c2-153">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="699c2-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="699c2-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="699c2-154">Windows Server 2003</span></span>



| <span data-ttu-id="699c2-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-155">Entry</span></span> | <span data-ttu-id="699c2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="699c2-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c2-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c2-159">System-Only</span></span>            | <span data-ttu-id="699c2-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-160">False</span></span>                                        |
| <span data-ttu-id="699c2-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c2-161">Is-Single-Valued</span></span>       | <span data-ttu-id="699c2-162">True</span><span class="sxs-lookup"><span data-stu-id="699c2-162">True</span></span>                                         |
| <span data-ttu-id="699c2-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c2-163">Is Indexed</span></span>             | <span data-ttu-id="699c2-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-164">False</span></span>                                        |
| <span data-ttu-id="699c2-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c2-165">In Global Catalog</span></span>      | <span data-ttu-id="699c2-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-166">False</span></span>                                        |
| <span data-ttu-id="699c2-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c2-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c2-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c2-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="699c2-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c2-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="699c2-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c2-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="699c2-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-171">Search-Flags</span></span>           | <span data-ttu-id="699c2-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c2-172">0x00000000</span></span>                                   |
| <span data-ttu-id="699c2-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-173">System-Flags</span></span>           | <span data-ttu-id="699c2-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c2-174">0x00000010</span></span>                                   |
| <span data-ttu-id="699c2-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c2-175">Classes used in</span></span>        | [<span data-ttu-id="699c2-176">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="699c2-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="699c2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="699c2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="699c2-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-178">Entry</span></span> | <span data-ttu-id="699c2-179">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="699c2-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c2-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c2-182">System-Only</span></span>            | <span data-ttu-id="699c2-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-183">False</span></span>                                        |
| <span data-ttu-id="699c2-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="699c2-185">True</span><span class="sxs-lookup"><span data-stu-id="699c2-185">True</span></span>                                         |
| <span data-ttu-id="699c2-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c2-186">Is Indexed</span></span>             | <span data-ttu-id="699c2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-187">False</span></span>                                        |
| <span data-ttu-id="699c2-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c2-188">In Global Catalog</span></span>      | <span data-ttu-id="699c2-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-189">False</span></span>                                        |
| <span data-ttu-id="699c2-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c2-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c2-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="699c2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c2-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="699c2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c2-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="699c2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-194">Search-Flags</span></span>           | <span data-ttu-id="699c2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c2-195">0x00000000</span></span>                                   |
| <span data-ttu-id="699c2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-196">System-Flags</span></span>           | <span data-ttu-id="699c2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c2-197">0x00000010</span></span>                                   |
| <span data-ttu-id="699c2-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c2-198">Classes used in</span></span>        | [<span data-ttu-id="699c2-199">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="699c2-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="699c2-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="699c2-200">Windows Server 2008</span></span>



| <span data-ttu-id="699c2-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-201">Entry</span></span> | <span data-ttu-id="699c2-202">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="699c2-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c2-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c2-205">System-Only</span></span>            | <span data-ttu-id="699c2-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-206">False</span></span>                                        |
| <span data-ttu-id="699c2-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c2-207">Is-Single-Valued</span></span>       | <span data-ttu-id="699c2-208">True</span><span class="sxs-lookup"><span data-stu-id="699c2-208">True</span></span>                                         |
| <span data-ttu-id="699c2-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c2-209">Is Indexed</span></span>             | <span data-ttu-id="699c2-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-210">False</span></span>                                        |
| <span data-ttu-id="699c2-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c2-211">In Global Catalog</span></span>      | <span data-ttu-id="699c2-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-212">False</span></span>                                        |
| <span data-ttu-id="699c2-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c2-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c2-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c2-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="699c2-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c2-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="699c2-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c2-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="699c2-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-217">Search-Flags</span></span>           | <span data-ttu-id="699c2-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c2-218">0x00000000</span></span>                                   |
| <span data-ttu-id="699c2-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-219">System-Flags</span></span>           | <span data-ttu-id="699c2-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c2-220">0x00000010</span></span>                                   |
| <span data-ttu-id="699c2-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c2-221">Classes used in</span></span>        | [<span data-ttu-id="699c2-222">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="699c2-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="699c2-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="699c2-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="699c2-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-224">Entry</span></span> | <span data-ttu-id="699c2-225">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="699c2-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c2-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c2-228">System-Only</span></span>            | <span data-ttu-id="699c2-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-229">False</span></span>                                        |
| <span data-ttu-id="699c2-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c2-230">Is-Single-Valued</span></span>       | <span data-ttu-id="699c2-231">True</span><span class="sxs-lookup"><span data-stu-id="699c2-231">True</span></span>                                         |
| <span data-ttu-id="699c2-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c2-232">Is Indexed</span></span>             | <span data-ttu-id="699c2-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-233">False</span></span>                                        |
| <span data-ttu-id="699c2-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c2-234">In Global Catalog</span></span>      | <span data-ttu-id="699c2-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-235">False</span></span>                                        |
| <span data-ttu-id="699c2-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c2-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c2-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c2-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="699c2-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c2-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="699c2-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c2-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="699c2-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-240">Search-Flags</span></span>           | <span data-ttu-id="699c2-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c2-241">0x00000000</span></span>                                   |
| <span data-ttu-id="699c2-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-242">System-Flags</span></span>           | <span data-ttu-id="699c2-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c2-243">0x00000010</span></span>                                   |
| <span data-ttu-id="699c2-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c2-244">Classes used in</span></span>        | [<span data-ttu-id="699c2-245">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="699c2-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="699c2-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="699c2-246">Windows Server 2012</span></span>



| <span data-ttu-id="699c2-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="699c2-247">Entry</span></span> | <span data-ttu-id="699c2-248">Значение</span><span class="sxs-lookup"><span data-stu-id="699c2-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="699c2-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="699c2-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="699c2-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="699c2-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="699c2-251">System-Only</span></span>            | <span data-ttu-id="699c2-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-252">False</span></span>                                        |
| <span data-ttu-id="699c2-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="699c2-253">Is-Single-Valued</span></span>       | <span data-ttu-id="699c2-254">True</span><span class="sxs-lookup"><span data-stu-id="699c2-254">True</span></span>                                         |
| <span data-ttu-id="699c2-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="699c2-255">Is Indexed</span></span>             | <span data-ttu-id="699c2-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-256">False</span></span>                                        |
| <span data-ttu-id="699c2-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="699c2-257">In Global Catalog</span></span>      | <span data-ttu-id="699c2-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="699c2-258">False</span></span>                                        |
| <span data-ttu-id="699c2-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="699c2-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="699c2-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="699c2-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="699c2-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="699c2-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="699c2-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="699c2-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="699c2-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-263">Search-Flags</span></span>           | <span data-ttu-id="699c2-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="699c2-264">0x00000000</span></span>                                   |
| <span data-ttu-id="699c2-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="699c2-265">System-Flags</span></span>           | <span data-ttu-id="699c2-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="699c2-266">0x00000010</span></span>                                   |
| <span data-ttu-id="699c2-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="699c2-267">Classes used in</span></span>        | [<span data-ttu-id="699c2-268">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="699c2-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





