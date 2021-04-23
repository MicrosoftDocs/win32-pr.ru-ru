---
title: Атрибут ms-DS-with-Domain-NC
description: Сведения о репликации службы каталогов, в которых содержатся сведения о контекстах именования доменов, имеющихся на определенном сервере.
ms.assetid: e5a7c371-5a37-466e-b56f-ee261b48e3b2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-in-Domain-NC
- Схема AD атрибута msDS-Хасдомаиннкс
topic_type:
- apiref
api_name:
- ms-DS-Has-Domain-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b946286974cc6ba4e6d30484e7768a1daeccb6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493824"
---
# <a name="ms-ds-has-domain-ncs-attribute"></a><span data-ttu-id="8528e-105">Атрибут ms-DS-with-Domain-NC</span><span class="sxs-lookup"><span data-stu-id="8528e-105">ms-DS-Has-Domain-NCs attribute</span></span>

<span data-ttu-id="8528e-106">Сведения о репликации службы каталогов, в которых содержатся сведения о контекстах именования доменов, имеющихся на определенном сервере.</span><span class="sxs-lookup"><span data-stu-id="8528e-106">Directory service replication information that details the domain naming contexts present on a particular server.</span></span>



| <span data-ttu-id="8528e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-107">Entry</span></span> | <span data-ttu-id="8528e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="8528e-109">CN</span><span class="sxs-lookup"><span data-stu-id="8528e-109">CN</span></span>                | <span data-ttu-id="8528e-110">MS-DS-имеет-Domain-NC</span><span class="sxs-lookup"><span data-stu-id="8528e-110">ms-DS-Has-Domain-NCs</span></span>                                |
| <span data-ttu-id="8528e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8528e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8528e-112">msDS-Хасдомаиннкс</span><span class="sxs-lookup"><span data-stu-id="8528e-112">msDS-HasDomainNCs</span></span>                                   |
| <span data-ttu-id="8528e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8528e-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="8528e-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8528e-114">Update Privilege</span></span>  | <span data-ttu-id="8528e-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="8528e-115">This value is set by the system</span></span>                     |
| <span data-ttu-id="8528e-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8528e-116">Update Frequency</span></span>  | <span data-ttu-id="8528e-117">Он задается DCPromo и не изменяется в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="8528e-117">It is set by DCPromo and never modified thereafter.</span></span> |
| <span data-ttu-id="8528e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-118">Attribute-Id</span></span>      | <span data-ttu-id="8528e-119">1.2.840.113556.1.4.1820</span><span class="sxs-lookup"><span data-stu-id="8528e-119">1.2.840.113556.1.4.1820</span></span>                             |
| <span data-ttu-id="8528e-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8528e-120">System-Id-Guid</span></span>    | <span data-ttu-id="8528e-121">6f17e347-a842-4498-b8b3-15e007da4fed</span><span class="sxs-lookup"><span data-stu-id="8528e-121">6f17e347-a842-4498-b8b3-15e007da4fed</span></span>                |
| <span data-ttu-id="8528e-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8528e-122">Syntax</span></span>            | [<span data-ttu-id="8528e-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8528e-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)             |



## <a name="implementations"></a><span data-ttu-id="8528e-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8528e-124">Implementations</span></span>

-   [<span data-ttu-id="8528e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8528e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8528e-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8528e-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8528e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8528e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8528e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8528e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8528e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8528e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8528e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8528e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8528e-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8528e-131">Windows Server 2003</span></span>



| <span data-ttu-id="8528e-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-132">Entry</span></span> | <span data-ttu-id="8528e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-133">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8528e-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8528e-134">Link-Id</span></span>                | <span data-ttu-id="8528e-135">2026</span><span class="sxs-lookup"><span data-stu-id="8528e-135">2026</span></span>                                     |
| <span data-ttu-id="8528e-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-136">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8528e-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8528e-137">System-Only</span></span>            | <span data-ttu-id="8528e-138">True</span><span class="sxs-lookup"><span data-stu-id="8528e-138">True</span></span>                                     |
| <span data-ttu-id="8528e-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8528e-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8528e-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-140">False</span></span>                                    |
| <span data-ttu-id="8528e-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8528e-141">Is Indexed</span></span>             | <span data-ttu-id="8528e-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-142">False</span></span>                                    |
| <span data-ttu-id="8528e-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8528e-143">In Global Catalog</span></span>      | <span data-ttu-id="8528e-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-144">False</span></span>                                    |
| <span data-ttu-id="8528e-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8528e-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8528e-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8528e-146">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8528e-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8528e-147">Range-Lower</span></span>            | <span data-ttu-id="8528e-148">4</span><span class="sxs-lookup"><span data-stu-id="8528e-148">4</span></span>                                        |
| <span data-ttu-id="8528e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8528e-149">Range-Upper</span></span>            | <span data-ttu-id="8528e-150">4</span><span class="sxs-lookup"><span data-stu-id="8528e-150">4</span></span>                                        |
| <span data-ttu-id="8528e-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-151">Search-Flags</span></span>           | <span data-ttu-id="8528e-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8528e-152">0x00000000</span></span>                               |
| <span data-ttu-id="8528e-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-153">System-Flags</span></span>           | <span data-ttu-id="8528e-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8528e-154">0x00000010</span></span>                               |
| <span data-ttu-id="8528e-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8528e-155">Classes used in</span></span>        | [<span data-ttu-id="8528e-156">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8528e-156">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8528e-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="8528e-157">ADAM</span></span>



| <span data-ttu-id="8528e-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-158">Entry</span></span> | <span data-ttu-id="8528e-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-159">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8528e-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8528e-160">Link-Id</span></span>                | <span data-ttu-id="8528e-161">2026</span><span class="sxs-lookup"><span data-stu-id="8528e-161">2026</span></span>                                     |
| <span data-ttu-id="8528e-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-162">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8528e-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="8528e-163">System-Only</span></span>            | <span data-ttu-id="8528e-164">True</span><span class="sxs-lookup"><span data-stu-id="8528e-164">True</span></span>                                     |
| <span data-ttu-id="8528e-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8528e-165">Is-Single-Valued</span></span>       | <span data-ttu-id="8528e-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-166">False</span></span>                                    |
| <span data-ttu-id="8528e-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8528e-167">Is Indexed</span></span>             | <span data-ttu-id="8528e-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-168">False</span></span>                                    |
| <span data-ttu-id="8528e-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8528e-169">In Global Catalog</span></span>      | <span data-ttu-id="8528e-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-170">False</span></span>                                    |
| <span data-ttu-id="8528e-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8528e-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="8528e-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8528e-172">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8528e-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8528e-173">Range-Lower</span></span>            | <span data-ttu-id="8528e-174">4</span><span class="sxs-lookup"><span data-stu-id="8528e-174">4</span></span>                                        |
| <span data-ttu-id="8528e-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8528e-175">Range-Upper</span></span>            | <span data-ttu-id="8528e-176">4</span><span class="sxs-lookup"><span data-stu-id="8528e-176">4</span></span>                                        |
| <span data-ttu-id="8528e-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-177">Search-Flags</span></span>           | <span data-ttu-id="8528e-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8528e-178">0x00000000</span></span>                               |
| <span data-ttu-id="8528e-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-179">System-Flags</span></span>           | <span data-ttu-id="8528e-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8528e-180">0x00000010</span></span>                               |
| <span data-ttu-id="8528e-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8528e-181">Classes used in</span></span>        | [<span data-ttu-id="8528e-182">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8528e-182">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8528e-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8528e-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8528e-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-184">Entry</span></span> | <span data-ttu-id="8528e-185">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-185">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8528e-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8528e-186">Link-Id</span></span>                | <span data-ttu-id="8528e-187">2026</span><span class="sxs-lookup"><span data-stu-id="8528e-187">2026</span></span>                                     |
| <span data-ttu-id="8528e-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-188">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8528e-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="8528e-189">System-Only</span></span>            | <span data-ttu-id="8528e-190">True</span><span class="sxs-lookup"><span data-stu-id="8528e-190">True</span></span>                                     |
| <span data-ttu-id="8528e-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8528e-191">Is-Single-Valued</span></span>       | <span data-ttu-id="8528e-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-192">False</span></span>                                    |
| <span data-ttu-id="8528e-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8528e-193">Is Indexed</span></span>             | <span data-ttu-id="8528e-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-194">False</span></span>                                    |
| <span data-ttu-id="8528e-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8528e-195">In Global Catalog</span></span>      | <span data-ttu-id="8528e-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-196">False</span></span>                                    |
| <span data-ttu-id="8528e-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8528e-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="8528e-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8528e-198">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8528e-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8528e-199">Range-Lower</span></span>            | <span data-ttu-id="8528e-200">4</span><span class="sxs-lookup"><span data-stu-id="8528e-200">4</span></span>                                        |
| <span data-ttu-id="8528e-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8528e-201">Range-Upper</span></span>            | <span data-ttu-id="8528e-202">4</span><span class="sxs-lookup"><span data-stu-id="8528e-202">4</span></span>                                        |
| <span data-ttu-id="8528e-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-203">Search-Flags</span></span>           | <span data-ttu-id="8528e-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8528e-204">0x00000000</span></span>                               |
| <span data-ttu-id="8528e-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-205">System-Flags</span></span>           | <span data-ttu-id="8528e-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8528e-206">0x00000010</span></span>                               |
| <span data-ttu-id="8528e-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8528e-207">Classes used in</span></span>        | [<span data-ttu-id="8528e-208">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8528e-208">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8528e-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8528e-209">Windows Server 2008</span></span>



| <span data-ttu-id="8528e-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-210">Entry</span></span> | <span data-ttu-id="8528e-211">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-211">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8528e-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8528e-212">Link-Id</span></span>                | <span data-ttu-id="8528e-213">2026</span><span class="sxs-lookup"><span data-stu-id="8528e-213">2026</span></span>                                     |
| <span data-ttu-id="8528e-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-214">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8528e-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="8528e-215">System-Only</span></span>            | <span data-ttu-id="8528e-216">True</span><span class="sxs-lookup"><span data-stu-id="8528e-216">True</span></span>                                     |
| <span data-ttu-id="8528e-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8528e-217">Is-Single-Valued</span></span>       | <span data-ttu-id="8528e-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-218">False</span></span>                                    |
| <span data-ttu-id="8528e-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8528e-219">Is Indexed</span></span>             | <span data-ttu-id="8528e-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-220">False</span></span>                                    |
| <span data-ttu-id="8528e-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8528e-221">In Global Catalog</span></span>      | <span data-ttu-id="8528e-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-222">False</span></span>                                    |
| <span data-ttu-id="8528e-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8528e-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="8528e-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8528e-224">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8528e-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8528e-225">Range-Lower</span></span>            | <span data-ttu-id="8528e-226">4</span><span class="sxs-lookup"><span data-stu-id="8528e-226">4</span></span>                                        |
| <span data-ttu-id="8528e-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8528e-227">Range-Upper</span></span>            | <span data-ttu-id="8528e-228">4</span><span class="sxs-lookup"><span data-stu-id="8528e-228">4</span></span>                                        |
| <span data-ttu-id="8528e-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-229">Search-Flags</span></span>           | <span data-ttu-id="8528e-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8528e-230">0x00000000</span></span>                               |
| <span data-ttu-id="8528e-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-231">System-Flags</span></span>           | <span data-ttu-id="8528e-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8528e-232">0x00000010</span></span>                               |
| <span data-ttu-id="8528e-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8528e-233">Classes used in</span></span>        | [<span data-ttu-id="8528e-234">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8528e-234">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8528e-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8528e-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8528e-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-236">Entry</span></span> | <span data-ttu-id="8528e-237">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-237">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8528e-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8528e-238">Link-Id</span></span>                | <span data-ttu-id="8528e-239">2026</span><span class="sxs-lookup"><span data-stu-id="8528e-239">2026</span></span>                                     |
| <span data-ttu-id="8528e-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-240">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8528e-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="8528e-241">System-Only</span></span>            | <span data-ttu-id="8528e-242">True</span><span class="sxs-lookup"><span data-stu-id="8528e-242">True</span></span>                                     |
| <span data-ttu-id="8528e-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8528e-243">Is-Single-Valued</span></span>       | <span data-ttu-id="8528e-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-244">False</span></span>                                    |
| <span data-ttu-id="8528e-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8528e-245">Is Indexed</span></span>             | <span data-ttu-id="8528e-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-246">False</span></span>                                    |
| <span data-ttu-id="8528e-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8528e-247">In Global Catalog</span></span>      | <span data-ttu-id="8528e-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-248">False</span></span>                                    |
| <span data-ttu-id="8528e-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8528e-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="8528e-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8528e-250">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8528e-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8528e-251">Range-Lower</span></span>            | <span data-ttu-id="8528e-252">4</span><span class="sxs-lookup"><span data-stu-id="8528e-252">4</span></span>                                        |
| <span data-ttu-id="8528e-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8528e-253">Range-Upper</span></span>            | <span data-ttu-id="8528e-254">4</span><span class="sxs-lookup"><span data-stu-id="8528e-254">4</span></span>                                        |
| <span data-ttu-id="8528e-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-255">Search-Flags</span></span>           | <span data-ttu-id="8528e-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8528e-256">0x00000000</span></span>                               |
| <span data-ttu-id="8528e-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-257">System-Flags</span></span>           | <span data-ttu-id="8528e-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8528e-258">0x00000010</span></span>                               |
| <span data-ttu-id="8528e-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8528e-259">Classes used in</span></span>        | [<span data-ttu-id="8528e-260">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8528e-260">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8528e-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8528e-261">Windows Server 2012</span></span>



| <span data-ttu-id="8528e-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="8528e-262">Entry</span></span> | <span data-ttu-id="8528e-263">Значение</span><span class="sxs-lookup"><span data-stu-id="8528e-263">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8528e-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8528e-264">Link-Id</span></span>                | <span data-ttu-id="8528e-265">2026</span><span class="sxs-lookup"><span data-stu-id="8528e-265">2026</span></span>                                     |
| <span data-ttu-id="8528e-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8528e-266">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8528e-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="8528e-267">System-Only</span></span>            | <span data-ttu-id="8528e-268">True</span><span class="sxs-lookup"><span data-stu-id="8528e-268">True</span></span>                                     |
| <span data-ttu-id="8528e-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8528e-269">Is-Single-Valued</span></span>       | <span data-ttu-id="8528e-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-270">False</span></span>                                    |
| <span data-ttu-id="8528e-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8528e-271">Is Indexed</span></span>             | <span data-ttu-id="8528e-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-272">False</span></span>                                    |
| <span data-ttu-id="8528e-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8528e-273">In Global Catalog</span></span>      | <span data-ttu-id="8528e-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="8528e-274">False</span></span>                                    |
| <span data-ttu-id="8528e-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8528e-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="8528e-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8528e-276">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8528e-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8528e-277">Range-Lower</span></span>            | <span data-ttu-id="8528e-278">4</span><span class="sxs-lookup"><span data-stu-id="8528e-278">4</span></span>                                        |
| <span data-ttu-id="8528e-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8528e-279">Range-Upper</span></span>            | <span data-ttu-id="8528e-280">4</span><span class="sxs-lookup"><span data-stu-id="8528e-280">4</span></span>                                        |
| <span data-ttu-id="8528e-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-281">Search-Flags</span></span>           | <span data-ttu-id="8528e-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8528e-282">0x00000000</span></span>                               |
| <span data-ttu-id="8528e-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8528e-283">System-Flags</span></span>           | <span data-ttu-id="8528e-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8528e-284">0x00000010</span></span>                               |
| <span data-ttu-id="8528e-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8528e-285">Classes used in</span></span>        | [<span data-ttu-id="8528e-286">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="8528e-286">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





