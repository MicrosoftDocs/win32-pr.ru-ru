---
title: ACS-минимальная-политика-атрибут размера
description: Атрибут "ACS-Minimum-with-size" предназначен только для внутреннего использования.
ms.assetid: 27b4273a-a625-430b-baa0-a6037e2aac1e
ms.tgt_platform: multiple
keywords:
- ACS-минимальная-политика-схема AD атрибута
- Схема AD атрибута Аксминимумполицедсизе
topic_type:
- apiref
api_name:
- ACS-Minimum-Policed-Size
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3de4bb2b33a45ab7d10bad72ba286d1695b980a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655553"
---
# <a name="acs-minimum-policed-size-attribute"></a><span data-ttu-id="74dac-105">ACS-минимальная-политика-атрибут размера</span><span class="sxs-lookup"><span data-stu-id="74dac-105">ACS-Minimum-Policed-Size attribute</span></span>

<span data-ttu-id="74dac-106">Атрибут " **ACS-Minimum-with-size** " предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="74dac-106">The **ACS-Minimum-Policed-Size** attribute is for internal use only.</span></span> <span data-ttu-id="74dac-107">На основе RFC2210.</span><span class="sxs-lookup"><span data-stu-id="74dac-107">Based on RFC2210.</span></span>



| <span data-ttu-id="74dac-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-108">Entry</span></span> | <span data-ttu-id="74dac-109">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="74dac-110">CN</span><span class="sxs-lookup"><span data-stu-id="74dac-110">CN</span></span>                | <span data-ttu-id="74dac-111">ACS — минимальная политика-размер</span><span class="sxs-lookup"><span data-stu-id="74dac-111">ACS-Minimum-Policed-Size</span></span>             |
| <span data-ttu-id="74dac-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="74dac-112">Ldap-Display-Name</span></span> | <span data-ttu-id="74dac-113">аксминимумполицедсизе</span><span class="sxs-lookup"><span data-stu-id="74dac-113">aCSMinimumPolicedSize</span></span>                |
| <span data-ttu-id="74dac-114">Размер</span><span class="sxs-lookup"><span data-stu-id="74dac-114">Size</span></span>              | <span data-ttu-id="74dac-115">8 байт</span><span class="sxs-lookup"><span data-stu-id="74dac-115">8 bytes</span></span>                              |
| <span data-ttu-id="74dac-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="74dac-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="74dac-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="74dac-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="74dac-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-118">Attribute-Id</span></span>      | <span data-ttu-id="74dac-119">1.2.840.113556.1.4.1315</span><span class="sxs-lookup"><span data-stu-id="74dac-119">1.2.840.113556.1.4.1315</span></span>              |
| <span data-ttu-id="74dac-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="74dac-120">System-Id-Guid</span></span>    | <span data-ttu-id="74dac-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="74dac-121">8d0e7195-3b90-11d2-90cc-00c04fd91ab1</span></span> |
| <span data-ttu-id="74dac-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74dac-122">Syntax</span></span>            | [<span data-ttu-id="74dac-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="74dac-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="74dac-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="74dac-124">Implementations</span></span>

-   [<span data-ttu-id="74dac-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="74dac-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="74dac-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74dac-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74dac-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74dac-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74dac-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74dac-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74dac-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74dac-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74dac-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74dac-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="74dac-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="74dac-131">Windows 2000 Server</span></span>



| <span data-ttu-id="74dac-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-132">Entry</span></span> | <span data-ttu-id="74dac-133">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="74dac-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74dac-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="74dac-136">System-Only</span></span>            | <span data-ttu-id="74dac-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-137">False</span></span>                                        |
| <span data-ttu-id="74dac-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74dac-138">Is-Single-Valued</span></span>       | <span data-ttu-id="74dac-139">True</span><span class="sxs-lookup"><span data-stu-id="74dac-139">True</span></span>                                         |
| <span data-ttu-id="74dac-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74dac-140">Is Indexed</span></span>             | <span data-ttu-id="74dac-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-141">False</span></span>                                        |
| <span data-ttu-id="74dac-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74dac-142">In Global Catalog</span></span>      | <span data-ttu-id="74dac-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-143">False</span></span>                                        |
| <span data-ttu-id="74dac-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74dac-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="74dac-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74dac-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="74dac-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74dac-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="74dac-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74dac-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="74dac-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-148">Search-Flags</span></span>           | <span data-ttu-id="74dac-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74dac-149">0x00000000</span></span>                                   |
| <span data-ttu-id="74dac-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-150">System-Flags</span></span>           | <span data-ttu-id="74dac-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74dac-151">0x00000010</span></span>                                   |
| <span data-ttu-id="74dac-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74dac-152">Classes used in</span></span>        | [<span data-ttu-id="74dac-153">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="74dac-153">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="74dac-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74dac-154">Windows Server 2003</span></span>



| <span data-ttu-id="74dac-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-155">Entry</span></span> | <span data-ttu-id="74dac-156">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="74dac-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74dac-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="74dac-159">System-Only</span></span>            | <span data-ttu-id="74dac-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-160">False</span></span>                                        |
| <span data-ttu-id="74dac-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74dac-161">Is-Single-Valued</span></span>       | <span data-ttu-id="74dac-162">True</span><span class="sxs-lookup"><span data-stu-id="74dac-162">True</span></span>                                         |
| <span data-ttu-id="74dac-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74dac-163">Is Indexed</span></span>             | <span data-ttu-id="74dac-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-164">False</span></span>                                        |
| <span data-ttu-id="74dac-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74dac-165">In Global Catalog</span></span>      | <span data-ttu-id="74dac-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-166">False</span></span>                                        |
| <span data-ttu-id="74dac-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74dac-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="74dac-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74dac-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="74dac-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74dac-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="74dac-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74dac-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="74dac-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-171">Search-Flags</span></span>           | <span data-ttu-id="74dac-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74dac-172">0x00000000</span></span>                                   |
| <span data-ttu-id="74dac-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-173">System-Flags</span></span>           | <span data-ttu-id="74dac-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74dac-174">0x00000010</span></span>                                   |
| <span data-ttu-id="74dac-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74dac-175">Classes used in</span></span>        | [<span data-ttu-id="74dac-176">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="74dac-176">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74dac-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74dac-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74dac-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-178">Entry</span></span> | <span data-ttu-id="74dac-179">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="74dac-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74dac-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="74dac-182">System-Only</span></span>            | <span data-ttu-id="74dac-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-183">False</span></span>                                        |
| <span data-ttu-id="74dac-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74dac-184">Is-Single-Valued</span></span>       | <span data-ttu-id="74dac-185">True</span><span class="sxs-lookup"><span data-stu-id="74dac-185">True</span></span>                                         |
| <span data-ttu-id="74dac-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74dac-186">Is Indexed</span></span>             | <span data-ttu-id="74dac-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-187">False</span></span>                                        |
| <span data-ttu-id="74dac-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74dac-188">In Global Catalog</span></span>      | <span data-ttu-id="74dac-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-189">False</span></span>                                        |
| <span data-ttu-id="74dac-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74dac-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="74dac-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74dac-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="74dac-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74dac-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="74dac-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74dac-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="74dac-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-194">Search-Flags</span></span>           | <span data-ttu-id="74dac-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74dac-195">0x00000000</span></span>                                   |
| <span data-ttu-id="74dac-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-196">System-Flags</span></span>           | <span data-ttu-id="74dac-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74dac-197">0x00000010</span></span>                                   |
| <span data-ttu-id="74dac-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74dac-198">Classes used in</span></span>        | [<span data-ttu-id="74dac-199">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="74dac-199">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74dac-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74dac-200">Windows Server 2008</span></span>



| <span data-ttu-id="74dac-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-201">Entry</span></span> | <span data-ttu-id="74dac-202">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="74dac-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74dac-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="74dac-205">System-Only</span></span>            | <span data-ttu-id="74dac-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-206">False</span></span>                                        |
| <span data-ttu-id="74dac-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74dac-207">Is-Single-Valued</span></span>       | <span data-ttu-id="74dac-208">True</span><span class="sxs-lookup"><span data-stu-id="74dac-208">True</span></span>                                         |
| <span data-ttu-id="74dac-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74dac-209">Is Indexed</span></span>             | <span data-ttu-id="74dac-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-210">False</span></span>                                        |
| <span data-ttu-id="74dac-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74dac-211">In Global Catalog</span></span>      | <span data-ttu-id="74dac-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-212">False</span></span>                                        |
| <span data-ttu-id="74dac-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74dac-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="74dac-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74dac-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="74dac-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74dac-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="74dac-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74dac-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="74dac-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-217">Search-Flags</span></span>           | <span data-ttu-id="74dac-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74dac-218">0x00000000</span></span>                                   |
| <span data-ttu-id="74dac-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-219">System-Flags</span></span>           | <span data-ttu-id="74dac-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74dac-220">0x00000010</span></span>                                   |
| <span data-ttu-id="74dac-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74dac-221">Classes used in</span></span>        | [<span data-ttu-id="74dac-222">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="74dac-222">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74dac-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74dac-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74dac-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-224">Entry</span></span> | <span data-ttu-id="74dac-225">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="74dac-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74dac-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="74dac-228">System-Only</span></span>            | <span data-ttu-id="74dac-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-229">False</span></span>                                        |
| <span data-ttu-id="74dac-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74dac-230">Is-Single-Valued</span></span>       | <span data-ttu-id="74dac-231">True</span><span class="sxs-lookup"><span data-stu-id="74dac-231">True</span></span>                                         |
| <span data-ttu-id="74dac-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74dac-232">Is Indexed</span></span>             | <span data-ttu-id="74dac-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-233">False</span></span>                                        |
| <span data-ttu-id="74dac-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74dac-234">In Global Catalog</span></span>      | <span data-ttu-id="74dac-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-235">False</span></span>                                        |
| <span data-ttu-id="74dac-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74dac-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="74dac-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74dac-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="74dac-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74dac-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="74dac-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74dac-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="74dac-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-240">Search-Flags</span></span>           | <span data-ttu-id="74dac-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74dac-241">0x00000000</span></span>                                   |
| <span data-ttu-id="74dac-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-242">System-Flags</span></span>           | <span data-ttu-id="74dac-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74dac-243">0x00000010</span></span>                                   |
| <span data-ttu-id="74dac-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74dac-244">Classes used in</span></span>        | [<span data-ttu-id="74dac-245">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="74dac-245">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74dac-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74dac-246">Windows Server 2012</span></span>



| <span data-ttu-id="74dac-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="74dac-247">Entry</span></span> | <span data-ttu-id="74dac-248">Значение</span><span class="sxs-lookup"><span data-stu-id="74dac-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="74dac-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74dac-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74dac-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="74dac-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="74dac-251">System-Only</span></span>            | <span data-ttu-id="74dac-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-252">False</span></span>                                        |
| <span data-ttu-id="74dac-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74dac-253">Is-Single-Valued</span></span>       | <span data-ttu-id="74dac-254">True</span><span class="sxs-lookup"><span data-stu-id="74dac-254">True</span></span>                                         |
| <span data-ttu-id="74dac-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74dac-255">Is Indexed</span></span>             | <span data-ttu-id="74dac-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-256">False</span></span>                                        |
| <span data-ttu-id="74dac-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74dac-257">In Global Catalog</span></span>      | <span data-ttu-id="74dac-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="74dac-258">False</span></span>                                        |
| <span data-ttu-id="74dac-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74dac-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="74dac-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74dac-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="74dac-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74dac-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="74dac-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74dac-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="74dac-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-263">Search-Flags</span></span>           | <span data-ttu-id="74dac-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74dac-264">0x00000000</span></span>                                   |
| <span data-ttu-id="74dac-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74dac-265">System-Flags</span></span>           | <span data-ttu-id="74dac-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74dac-266">0x00000010</span></span>                                   |
| <span data-ttu-id="74dac-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74dac-267">Classes used in</span></span>        | [<span data-ttu-id="74dac-268">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="74dac-268">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





