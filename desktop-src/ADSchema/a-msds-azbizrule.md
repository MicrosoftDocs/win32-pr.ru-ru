---
title: Атрибут ms-DS-AZ-BizTalk-Rule
description: Текст скрипта, реализующего бизнес-правило.
ms.assetid: 884513ae-9600-49b0-a371-6f77b84b54f9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-AZ-BizTalk-Rule
- Схема AD атрибута msDS-Азбизруле
topic_type:
- apiref
api_name:
- ms-DS-Az-Biz-Rule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571ab48c9742ffb93015c433685c01cb3a9666d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138975"
---
# <a name="ms-ds-az-biz-rule-attribute"></a><span data-ttu-id="d0b35-105">Атрибут ms-DS-AZ-BizTalk-Rule</span><span class="sxs-lookup"><span data-stu-id="d0b35-105">ms-DS-Az-Biz-Rule attribute</span></span>

<span data-ttu-id="d0b35-106">Текст скрипта, реализующего бизнес-правило.</span><span class="sxs-lookup"><span data-stu-id="d0b35-106">Text of the script implementing the business rule.</span></span>



| <span data-ttu-id="d0b35-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0b35-107">Entry</span></span> | <span data-ttu-id="d0b35-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b35-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d0b35-109">CN</span><span class="sxs-lookup"><span data-stu-id="d0b35-109">CN</span></span>                | <span data-ttu-id="d0b35-110">MS-DS-AZ-BizTalk-Rule</span><span class="sxs-lookup"><span data-stu-id="d0b35-110">ms-DS-Az-Biz-Rule</span></span>                           |
| <span data-ttu-id="d0b35-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d0b35-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d0b35-112">msDS-Азбизруле</span><span class="sxs-lookup"><span data-stu-id="d0b35-112">msDS-AzBizRule</span></span>                              |
| <span data-ttu-id="d0b35-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d0b35-113">Size</span></span>              | <span data-ttu-id="d0b35-114">128 символов</span><span class="sxs-lookup"><span data-stu-id="d0b35-114">128 characters</span></span>                              |
| <span data-ttu-id="d0b35-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d0b35-115">Update Privilege</span></span>  | <span data-ttu-id="d0b35-116">Администратор Азролес</span><span class="sxs-lookup"><span data-stu-id="d0b35-116">AzRoles admin</span></span>                               |
| <span data-ttu-id="d0b35-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d0b35-117">Update Frequency</span></span>  | <span data-ttu-id="d0b35-118">Во время инициализации или изменения политики.</span><span class="sxs-lookup"><span data-stu-id="d0b35-118">During initialization or policy change.</span></span>     |
| <span data-ttu-id="d0b35-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d0b35-119">Attribute-Id</span></span>      | <span data-ttu-id="d0b35-120">1.2.840.113556.1.4.1801</span><span class="sxs-lookup"><span data-stu-id="d0b35-120">1.2.840.113556.1.4.1801</span></span>                     |
| <span data-ttu-id="d0b35-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d0b35-121">System-Id-Guid</span></span>    | <span data-ttu-id="d0b35-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span><span class="sxs-lookup"><span data-stu-id="d0b35-122">33d41ea8-c0c9-4c92-9494-f104878413fd</span></span>        |
| <span data-ttu-id="d0b35-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0b35-123">Syntax</span></span>            | [<span data-ttu-id="d0b35-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d0b35-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d0b35-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d0b35-125">Implementations</span></span>

-   [<span data-ttu-id="d0b35-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d0b35-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d0b35-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d0b35-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d0b35-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d0b35-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d0b35-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d0b35-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d0b35-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d0b35-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="d0b35-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0b35-131">Windows Server 2003</span></span>



| <span data-ttu-id="d0b35-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0b35-132">Entry</span></span> | <span data-ttu-id="d0b35-133">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b35-133">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="d0b35-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0b35-134">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="d0b35-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0b35-135">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="d0b35-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0b35-136">System-Only</span></span>            | <span data-ttu-id="d0b35-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-137">False</span></span>                                             |
| <span data-ttu-id="d0b35-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0b35-138">Is-Single-Valued</span></span>       | <span data-ttu-id="d0b35-139">True</span><span class="sxs-lookup"><span data-stu-id="d0b35-139">True</span></span>                                              |
| <span data-ttu-id="d0b35-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0b35-140">Is Indexed</span></span>             | <span data-ttu-id="d0b35-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-141">False</span></span>                                             |
| <span data-ttu-id="d0b35-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0b35-142">In Global Catalog</span></span>      | <span data-ttu-id="d0b35-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-143">False</span></span>                                             |
| <span data-ttu-id="d0b35-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0b35-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0b35-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0b35-145">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="d0b35-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0b35-146">Range-Lower</span></span>            | <span data-ttu-id="d0b35-147">0</span><span class="sxs-lookup"><span data-stu-id="d0b35-147">0</span></span>                                                 |
| <span data-ttu-id="d0b35-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0b35-148">Range-Upper</span></span>            | <span data-ttu-id="d0b35-149">65536</span><span class="sxs-lookup"><span data-stu-id="d0b35-149">65536</span></span>                                             |
| <span data-ttu-id="d0b35-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-150">Search-Flags</span></span>           | <span data-ttu-id="d0b35-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0b35-151">0x00000000</span></span>                                        |
| <span data-ttu-id="d0b35-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-152">System-Flags</span></span>           | <span data-ttu-id="d0b35-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0b35-153">0x00000010</span></span>                                        |
| <span data-ttu-id="d0b35-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0b35-154">Classes used in</span></span>        | [<span data-ttu-id="d0b35-155">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="d0b35-155">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d0b35-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d0b35-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d0b35-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0b35-157">Entry</span></span> | <span data-ttu-id="d0b35-158">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b35-158">Value</span></span> |
|------------------------|---------------------------------------------------|
| <span data-ttu-id="d0b35-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0b35-159">Link-Id</span></span>                | \-                                                |
| <span data-ttu-id="d0b35-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0b35-160">MAPI-Id</span></span>                | \-                                                |
| <span data-ttu-id="d0b35-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0b35-161">System-Only</span></span>            | <span data-ttu-id="d0b35-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-162">False</span></span>                                             |
| <span data-ttu-id="d0b35-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0b35-163">Is-Single-Valued</span></span>       | <span data-ttu-id="d0b35-164">True</span><span class="sxs-lookup"><span data-stu-id="d0b35-164">True</span></span>                                              |
| <span data-ttu-id="d0b35-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0b35-165">Is Indexed</span></span>             | <span data-ttu-id="d0b35-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-166">False</span></span>                                             |
| <span data-ttu-id="d0b35-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0b35-167">In Global Catalog</span></span>      | <span data-ttu-id="d0b35-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-168">False</span></span>                                             |
| <span data-ttu-id="d0b35-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0b35-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0b35-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0b35-170">O:BAG:BAD:S:</span></span>                                      |
| <span data-ttu-id="d0b35-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0b35-171">Range-Lower</span></span>            | <span data-ttu-id="d0b35-172">0</span><span class="sxs-lookup"><span data-stu-id="d0b35-172">0</span></span>                                                 |
| <span data-ttu-id="d0b35-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0b35-173">Range-Upper</span></span>            | <span data-ttu-id="d0b35-174">65536</span><span class="sxs-lookup"><span data-stu-id="d0b35-174">65536</span></span>                                             |
| <span data-ttu-id="d0b35-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-175">Search-Flags</span></span>           | <span data-ttu-id="d0b35-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0b35-176">0x00000000</span></span>                                        |
| <span data-ttu-id="d0b35-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-177">System-Flags</span></span>           | <span data-ttu-id="d0b35-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0b35-178">0x00000010</span></span>                                        |
| <span data-ttu-id="d0b35-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0b35-179">Classes used in</span></span>        | [<span data-ttu-id="d0b35-180">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="d0b35-180">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d0b35-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0b35-181">Windows Server 2008</span></span>



| <span data-ttu-id="d0b35-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0b35-182">Entry</span></span> | <span data-ttu-id="d0b35-183">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b35-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b35-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0b35-184">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="d0b35-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0b35-185">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="d0b35-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0b35-186">System-Only</span></span>            | <span data-ttu-id="d0b35-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-187">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0b35-188">Is-Single-Valued</span></span>       | <span data-ttu-id="d0b35-189">True</span><span class="sxs-lookup"><span data-stu-id="d0b35-189">True</span></span>                                                                                  |
| <span data-ttu-id="d0b35-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0b35-190">Is Indexed</span></span>             | <span data-ttu-id="d0b35-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-191">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0b35-192">In Global Catalog</span></span>      | <span data-ttu-id="d0b35-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-193">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0b35-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0b35-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0b35-195">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="d0b35-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0b35-196">Range-Lower</span></span>            | <span data-ttu-id="d0b35-197">0</span><span class="sxs-lookup"><span data-stu-id="d0b35-197">0</span></span>                                                                                     |
| <span data-ttu-id="d0b35-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0b35-198">Range-Upper</span></span>            | <span data-ttu-id="d0b35-199">65536</span><span class="sxs-lookup"><span data-stu-id="d0b35-199">65536</span></span>                                                                                 |
| <span data-ttu-id="d0b35-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-200">Search-Flags</span></span>           | <span data-ttu-id="d0b35-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0b35-201">0x00000000</span></span>                                                                            |
| <span data-ttu-id="d0b35-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-202">System-Flags</span></span>           | <span data-ttu-id="d0b35-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0b35-203">0x00000010</span></span>                                                                            |
| <span data-ttu-id="d0b35-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0b35-204">Classes used in</span></span>        | [<span data-ttu-id="d0b35-205">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d0b35-205">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="d0b35-206">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="d0b35-206">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d0b35-207">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0b35-207">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d0b35-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0b35-208">Entry</span></span> | <span data-ttu-id="d0b35-209">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b35-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b35-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0b35-210">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="d0b35-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0b35-211">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="d0b35-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0b35-212">System-Only</span></span>            | <span data-ttu-id="d0b35-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-213">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0b35-214">Is-Single-Valued</span></span>       | <span data-ttu-id="d0b35-215">True</span><span class="sxs-lookup"><span data-stu-id="d0b35-215">True</span></span>                                                                                  |
| <span data-ttu-id="d0b35-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0b35-216">Is Indexed</span></span>             | <span data-ttu-id="d0b35-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-217">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0b35-218">In Global Catalog</span></span>      | <span data-ttu-id="d0b35-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-219">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0b35-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0b35-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0b35-221">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="d0b35-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0b35-222">Range-Lower</span></span>            | <span data-ttu-id="d0b35-223">0</span><span class="sxs-lookup"><span data-stu-id="d0b35-223">0</span></span>                                                                                     |
| <span data-ttu-id="d0b35-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0b35-224">Range-Upper</span></span>            | <span data-ttu-id="d0b35-225">65536</span><span class="sxs-lookup"><span data-stu-id="d0b35-225">65536</span></span>                                                                                 |
| <span data-ttu-id="d0b35-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-226">Search-Flags</span></span>           | <span data-ttu-id="d0b35-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0b35-227">0x00000000</span></span>                                                                            |
| <span data-ttu-id="d0b35-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-228">System-Flags</span></span>           | <span data-ttu-id="d0b35-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0b35-229">0x00000010</span></span>                                                                            |
| <span data-ttu-id="d0b35-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0b35-230">Classes used in</span></span>        | [<span data-ttu-id="d0b35-231">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d0b35-231">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="d0b35-232">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="d0b35-232">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d0b35-233">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0b35-233">Windows Server 2012</span></span>



| <span data-ttu-id="d0b35-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0b35-234">Entry</span></span> | <span data-ttu-id="d0b35-235">Значение</span><span class="sxs-lookup"><span data-stu-id="d0b35-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b35-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0b35-236">Link-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="d0b35-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0b35-237">MAPI-Id</span></span>                | \-                                                                                    |
| <span data-ttu-id="d0b35-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0b35-238">System-Only</span></span>            | <span data-ttu-id="d0b35-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-239">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0b35-240">Is-Single-Valued</span></span>       | <span data-ttu-id="d0b35-241">True</span><span class="sxs-lookup"><span data-stu-id="d0b35-241">True</span></span>                                                                                  |
| <span data-ttu-id="d0b35-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0b35-242">Is Indexed</span></span>             | <span data-ttu-id="d0b35-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-243">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0b35-244">In Global Catalog</span></span>      | <span data-ttu-id="d0b35-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0b35-245">False</span></span>                                                                                 |
| <span data-ttu-id="d0b35-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0b35-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0b35-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0b35-247">O:BAG:BAD:S:</span></span>                                                                          |
| <span data-ttu-id="d0b35-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0b35-248">Range-Lower</span></span>            | <span data-ttu-id="d0b35-249">0</span><span class="sxs-lookup"><span data-stu-id="d0b35-249">0</span></span>                                                                                     |
| <span data-ttu-id="d0b35-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0b35-250">Range-Upper</span></span>            | <span data-ttu-id="d0b35-251">65536</span><span class="sxs-lookup"><span data-stu-id="d0b35-251">65536</span></span>                                                                                 |
| <span data-ttu-id="d0b35-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-252">Search-Flags</span></span>           | <span data-ttu-id="d0b35-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0b35-253">0x00000000</span></span>                                                                            |
| <span data-ttu-id="d0b35-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0b35-254">System-Flags</span></span>           | <span data-ttu-id="d0b35-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0b35-255">0x00000010</span></span>                                                                            |
| <span data-ttu-id="d0b35-256">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0b35-256">Classes used in</span></span>        | [<span data-ttu-id="d0b35-257">**Группа**</span><span class="sxs-lookup"><span data-stu-id="d0b35-257">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="d0b35-258">**MS-DS-AZ-Task**</span><span class="sxs-lookup"><span data-stu-id="d0b35-258">**ms-DS-Az-Task**</span></span>](c-msds-aztask.md)<br/> |



 

 





