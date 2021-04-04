---
title: ACS-не зарезервировано — атрибут размера токена
description: Атрибут ACS-не зарезервирован — маркер-size предназначен только для внутреннего использования.
ms.assetid: 50c11f5f-2188-43ab-9d40-094ca8a3d526
ms.tgt_platform: multiple
keywords:
- Служба ACS — не зарезервировано — схема AD атрибута размера токена
- Схема AD атрибута Акснонресерведтокенсизе
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Token-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90351a660cfbeafbcd468edb1e6eca8c589b5d72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139126"
---
# <a name="acs-non-reserved-token-size-attribute"></a><span data-ttu-id="1d01a-105">ACS-не зарезервировано — атрибут размера токена</span><span class="sxs-lookup"><span data-stu-id="1d01a-105">ACS-Non-Reserved-Token-Size attribute</span></span>

<span data-ttu-id="1d01a-106">Атрибут **ACS-не зарезервирован — маркер-size** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="1d01a-106">The **ACS-Non-Reserved-Token-Size** attribute is for internal use only.</span></span> <span data-ttu-id="1d01a-107">На основе RFC2814.</span><span class="sxs-lookup"><span data-stu-id="1d01a-107">Based on RFC2814.</span></span>



| <span data-ttu-id="1d01a-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-108">Entry</span></span> | <span data-ttu-id="1d01a-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1d01a-110">CN</span><span class="sxs-lookup"><span data-stu-id="1d01a-110">CN</span></span>                | <span data-ttu-id="1d01a-111">ACS — не зарезервировано — размер токена</span><span class="sxs-lookup"><span data-stu-id="1d01a-111">ACS-Non-Reserved-Token-Size</span></span>          |
| <span data-ttu-id="1d01a-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1d01a-112">Ldap-Display-Name</span></span> | <span data-ttu-id="1d01a-113">акснонресерведтокенсизе</span><span class="sxs-lookup"><span data-stu-id="1d01a-113">aCSNonReservedTokenSize</span></span>              |
| <span data-ttu-id="1d01a-114">Размер</span><span class="sxs-lookup"><span data-stu-id="1d01a-114">Size</span></span>              | <span data-ttu-id="1d01a-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="1d01a-115">8 bytes</span></span>                              |
| <span data-ttu-id="1d01a-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1d01a-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1d01a-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1d01a-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1d01a-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-118">Attribute-Id</span></span>      | <span data-ttu-id="1d01a-119">1.2.840.113556.1.4.1319</span><span class="sxs-lookup"><span data-stu-id="1d01a-119">1.2.840.113556.1.4.1319</span></span>              |
| <span data-ttu-id="1d01a-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1d01a-120">System-Id-Guid</span></span>    | <span data-ttu-id="1d01a-121">a916d7c9-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="1d01a-121">a916d7c9-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="1d01a-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d01a-122">Syntax</span></span>            | [<span data-ttu-id="1d01a-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="1d01a-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="1d01a-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1d01a-124">Implementations</span></span>

-   [<span data-ttu-id="1d01a-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1d01a-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1d01a-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1d01a-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1d01a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1d01a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1d01a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1d01a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1d01a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1d01a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1d01a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1d01a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1d01a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1d01a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1d01a-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-132">Entry</span></span> | <span data-ttu-id="1d01a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1d01a-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1d01a-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d01a-136">System-Only</span></span>            | <span data-ttu-id="1d01a-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-137">False</span></span>                                        |
| <span data-ttu-id="1d01a-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1d01a-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1d01a-139">True</span><span class="sxs-lookup"><span data-stu-id="1d01a-139">True</span></span>                                         |
| <span data-ttu-id="1d01a-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1d01a-140">Is Indexed</span></span>             | <span data-ttu-id="1d01a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-141">False</span></span>                                        |
| <span data-ttu-id="1d01a-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1d01a-142">In Global Catalog</span></span>      | <span data-ttu-id="1d01a-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-143">False</span></span>                                        |
| <span data-ttu-id="1d01a-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1d01a-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d01a-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d01a-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1d01a-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d01a-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d01a-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-148">Search-Flags</span></span>           | <span data-ttu-id="1d01a-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d01a-149">0x00000000</span></span>                                   |
| <span data-ttu-id="1d01a-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-150">System-Flags</span></span>           | <span data-ttu-id="1d01a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d01a-151">0x00000010</span></span>                                   |
| <span data-ttu-id="1d01a-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1d01a-152">Classes used in</span></span>        | [<span data-ttu-id="1d01a-153">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1d01a-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1d01a-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d01a-154">Windows Server 2003</span></span>



| <span data-ttu-id="1d01a-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-155">Entry</span></span> | <span data-ttu-id="1d01a-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1d01a-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1d01a-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d01a-159">System-Only</span></span>            | <span data-ttu-id="1d01a-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-160">False</span></span>                                        |
| <span data-ttu-id="1d01a-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1d01a-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1d01a-162">True</span><span class="sxs-lookup"><span data-stu-id="1d01a-162">True</span></span>                                         |
| <span data-ttu-id="1d01a-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1d01a-163">Is Indexed</span></span>             | <span data-ttu-id="1d01a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-164">False</span></span>                                        |
| <span data-ttu-id="1d01a-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1d01a-165">In Global Catalog</span></span>      | <span data-ttu-id="1d01a-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-166">False</span></span>                                        |
| <span data-ttu-id="1d01a-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1d01a-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d01a-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d01a-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1d01a-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d01a-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d01a-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-171">Search-Flags</span></span>           | <span data-ttu-id="1d01a-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d01a-172">0x00000000</span></span>                                   |
| <span data-ttu-id="1d01a-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-173">System-Flags</span></span>           | <span data-ttu-id="1d01a-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d01a-174">0x00000010</span></span>                                   |
| <span data-ttu-id="1d01a-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1d01a-175">Classes used in</span></span>        | [<span data-ttu-id="1d01a-176">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1d01a-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1d01a-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1d01a-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1d01a-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-178">Entry</span></span> | <span data-ttu-id="1d01a-179">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1d01a-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1d01a-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d01a-182">System-Only</span></span>            | <span data-ttu-id="1d01a-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-183">False</span></span>                                        |
| <span data-ttu-id="1d01a-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1d01a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1d01a-185">True</span><span class="sxs-lookup"><span data-stu-id="1d01a-185">True</span></span>                                         |
| <span data-ttu-id="1d01a-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1d01a-186">Is Indexed</span></span>             | <span data-ttu-id="1d01a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-187">False</span></span>                                        |
| <span data-ttu-id="1d01a-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1d01a-188">In Global Catalog</span></span>      | <span data-ttu-id="1d01a-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-189">False</span></span>                                        |
| <span data-ttu-id="1d01a-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1d01a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d01a-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d01a-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1d01a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d01a-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d01a-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-194">Search-Flags</span></span>           | <span data-ttu-id="1d01a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d01a-195">0x00000000</span></span>                                   |
| <span data-ttu-id="1d01a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-196">System-Flags</span></span>           | <span data-ttu-id="1d01a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d01a-197">0x00000010</span></span>                                   |
| <span data-ttu-id="1d01a-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1d01a-198">Classes used in</span></span>        | [<span data-ttu-id="1d01a-199">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1d01a-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1d01a-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d01a-200">Windows Server 2008</span></span>



| <span data-ttu-id="1d01a-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-201">Entry</span></span> | <span data-ttu-id="1d01a-202">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1d01a-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1d01a-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d01a-205">System-Only</span></span>            | <span data-ttu-id="1d01a-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-206">False</span></span>                                        |
| <span data-ttu-id="1d01a-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1d01a-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1d01a-208">True</span><span class="sxs-lookup"><span data-stu-id="1d01a-208">True</span></span>                                         |
| <span data-ttu-id="1d01a-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1d01a-209">Is Indexed</span></span>             | <span data-ttu-id="1d01a-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-210">False</span></span>                                        |
| <span data-ttu-id="1d01a-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1d01a-211">In Global Catalog</span></span>      | <span data-ttu-id="1d01a-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-212">False</span></span>                                        |
| <span data-ttu-id="1d01a-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1d01a-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d01a-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d01a-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1d01a-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d01a-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d01a-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-217">Search-Flags</span></span>           | <span data-ttu-id="1d01a-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d01a-218">0x00000000</span></span>                                   |
| <span data-ttu-id="1d01a-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-219">System-Flags</span></span>           | <span data-ttu-id="1d01a-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d01a-220">0x00000010</span></span>                                   |
| <span data-ttu-id="1d01a-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1d01a-221">Classes used in</span></span>        | [<span data-ttu-id="1d01a-222">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1d01a-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1d01a-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d01a-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1d01a-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-224">Entry</span></span> | <span data-ttu-id="1d01a-225">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1d01a-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1d01a-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d01a-228">System-Only</span></span>            | <span data-ttu-id="1d01a-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-229">False</span></span>                                        |
| <span data-ttu-id="1d01a-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1d01a-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1d01a-231">True</span><span class="sxs-lookup"><span data-stu-id="1d01a-231">True</span></span>                                         |
| <span data-ttu-id="1d01a-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1d01a-232">Is Indexed</span></span>             | <span data-ttu-id="1d01a-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-233">False</span></span>                                        |
| <span data-ttu-id="1d01a-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1d01a-234">In Global Catalog</span></span>      | <span data-ttu-id="1d01a-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-235">False</span></span>                                        |
| <span data-ttu-id="1d01a-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1d01a-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d01a-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d01a-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1d01a-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d01a-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d01a-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-240">Search-Flags</span></span>           | <span data-ttu-id="1d01a-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d01a-241">0x00000000</span></span>                                   |
| <span data-ttu-id="1d01a-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-242">System-Flags</span></span>           | <span data-ttu-id="1d01a-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d01a-243">0x00000010</span></span>                                   |
| <span data-ttu-id="1d01a-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1d01a-244">Classes used in</span></span>        | [<span data-ttu-id="1d01a-245">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1d01a-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1d01a-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d01a-246">Windows Server 2012</span></span>



| <span data-ttu-id="1d01a-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="1d01a-247">Entry</span></span> | <span data-ttu-id="1d01a-248">Значение</span><span class="sxs-lookup"><span data-stu-id="1d01a-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="1d01a-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1d01a-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1d01a-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="1d01a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1d01a-251">System-Only</span></span>            | <span data-ttu-id="1d01a-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-252">False</span></span>                                        |
| <span data-ttu-id="1d01a-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1d01a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1d01a-254">True</span><span class="sxs-lookup"><span data-stu-id="1d01a-254">True</span></span>                                         |
| <span data-ttu-id="1d01a-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1d01a-255">Is Indexed</span></span>             | <span data-ttu-id="1d01a-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-256">False</span></span>                                        |
| <span data-ttu-id="1d01a-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1d01a-257">In Global Catalog</span></span>      | <span data-ttu-id="1d01a-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="1d01a-258">False</span></span>                                        |
| <span data-ttu-id="1d01a-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1d01a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1d01a-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1d01a-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="1d01a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1d01a-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1d01a-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="1d01a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-263">Search-Flags</span></span>           | <span data-ttu-id="1d01a-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1d01a-264">0x00000000</span></span>                                   |
| <span data-ttu-id="1d01a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1d01a-265">System-Flags</span></span>           | <span data-ttu-id="1d01a-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1d01a-266">0x00000010</span></span>                                   |
| <span data-ttu-id="1d01a-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1d01a-267">Classes used in</span></span>        | [<span data-ttu-id="1d01a-268">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="1d01a-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





