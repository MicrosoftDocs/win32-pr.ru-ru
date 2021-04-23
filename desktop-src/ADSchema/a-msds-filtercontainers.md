---
title: Атрибут ms-DS-Filter-Containers
description: Строка с несколькими значениями, содержащая имена классов, используемых для определения типов контейнеров, которые должны отображаться при фильтрации с помощью оснастки "пользователи и компьютеры" Active Directory.
ms.assetid: 765ac0e1-59d2-44a9-a01e-9cdf7d040c93
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов контейнеров MS-DS-Filters
- Схема AD атрибута msDS-Филтерконтаинерс
topic_type:
- apiref
api_name:
- ms-DS-Filter-Containers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8156b1baa2fe86ec0322a9161ce5231a7e23f32e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138958"
---
# <a name="ms-ds-filter-containers-attribute"></a><span data-ttu-id="110f6-105">Атрибут ms-DS-Filter-Containers</span><span class="sxs-lookup"><span data-stu-id="110f6-105">ms-DS-Filter-Containers attribute</span></span>

<span data-ttu-id="110f6-106">Строка с несколькими значениями, содержащая имена классов, используемых для определения типов контейнеров, которые должны отображаться при фильтрации с помощью оснастки "пользователи и компьютеры" Active Directory.</span><span class="sxs-lookup"><span data-stu-id="110f6-106">A multiple-valued string that contains the names of classes used to determine which container types should be shown by the Active Directory Users and Computers snap-in when filtering.</span></span>



| <span data-ttu-id="110f6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="110f6-107">Entry</span></span> | <span data-ttu-id="110f6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="110f6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="110f6-109">CN</span><span class="sxs-lookup"><span data-stu-id="110f6-109">CN</span></span>                | <span data-ttu-id="110f6-110">MS-DS-Filter-Containers</span><span class="sxs-lookup"><span data-stu-id="110f6-110">ms-DS-Filter-Containers</span></span>                     |
| <span data-ttu-id="110f6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="110f6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="110f6-112">msDS-Филтерконтаинерс</span><span class="sxs-lookup"><span data-stu-id="110f6-112">msDS-FilterContainers</span></span>                       |
| <span data-ttu-id="110f6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="110f6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="110f6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="110f6-114">Update Privilege</span></span>  | <span data-ttu-id="110f6-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="110f6-115">Domain administrator</span></span>                        |
| <span data-ttu-id="110f6-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="110f6-116">Update Frequency</span></span>  | <span data-ttu-id="110f6-117">При изменении списка типов контейнеров.</span><span class="sxs-lookup"><span data-stu-id="110f6-117">When the list of container types changes.</span></span>   |
| <span data-ttu-id="110f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="110f6-118">Attribute-Id</span></span>      | <span data-ttu-id="110f6-119">1.2.840.113556.1.4.1703</span><span class="sxs-lookup"><span data-stu-id="110f6-119">1.2.840.113556.1.4.1703</span></span>                     |
| <span data-ttu-id="110f6-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="110f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="110f6-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span><span class="sxs-lookup"><span data-stu-id="110f6-121">fb00dcdf-ac37-483a-9c12-ac53a6603033</span></span>        |
| <span data-ttu-id="110f6-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="110f6-122">Syntax</span></span>            | [<span data-ttu-id="110f6-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="110f6-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="110f6-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="110f6-124">Implementations</span></span>

-   [<span data-ttu-id="110f6-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="110f6-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="110f6-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="110f6-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="110f6-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="110f6-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="110f6-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="110f6-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="110f6-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="110f6-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="110f6-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="110f6-130">Windows Server 2003</span></span>



| <span data-ttu-id="110f6-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="110f6-131">Entry</span></span> | <span data-ttu-id="110f6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="110f6-132">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="110f6-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="110f6-133">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="110f6-134">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="110f6-135">System-Only</span></span>            | <span data-ttu-id="110f6-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-136">False</span></span>                                               |
| <span data-ttu-id="110f6-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="110f6-137">Is-Single-Valued</span></span>       | <span data-ttu-id="110f6-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-138">False</span></span>                                               |
| <span data-ttu-id="110f6-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="110f6-139">Is Indexed</span></span>             | <span data-ttu-id="110f6-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-140">False</span></span>                                               |
| <span data-ttu-id="110f6-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="110f6-141">In Global Catalog</span></span>      | <span data-ttu-id="110f6-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-142">False</span></span>                                               |
| <span data-ttu-id="110f6-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="110f6-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="110f6-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="110f6-144">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="110f6-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="110f6-145">Range-Lower</span></span>            | <span data-ttu-id="110f6-146">1</span><span class="sxs-lookup"><span data-stu-id="110f6-146">1</span></span>                                                   |
| <span data-ttu-id="110f6-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="110f6-147">Range-Upper</span></span>            | <span data-ttu-id="110f6-148">64</span><span class="sxs-lookup"><span data-stu-id="110f6-148">64</span></span>                                                  |
| <span data-ttu-id="110f6-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-149">Search-Flags</span></span>           | <span data-ttu-id="110f6-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="110f6-150">0x00000000</span></span>                                          |
| <span data-ttu-id="110f6-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-151">System-Flags</span></span>           | <span data-ttu-id="110f6-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="110f6-152">0x00000010</span></span>                                          |
| <span data-ttu-id="110f6-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="110f6-153">Classes used in</span></span>        | [<span data-ttu-id="110f6-154">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="110f6-154">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="110f6-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="110f6-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="110f6-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="110f6-156">Entry</span></span> | <span data-ttu-id="110f6-157">Значение</span><span class="sxs-lookup"><span data-stu-id="110f6-157">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="110f6-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="110f6-158">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="110f6-159">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="110f6-160">System-Only</span></span>            | <span data-ttu-id="110f6-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-161">False</span></span>                                               |
| <span data-ttu-id="110f6-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="110f6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="110f6-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-163">False</span></span>                                               |
| <span data-ttu-id="110f6-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="110f6-164">Is Indexed</span></span>             | <span data-ttu-id="110f6-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-165">False</span></span>                                               |
| <span data-ttu-id="110f6-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="110f6-166">In Global Catalog</span></span>      | <span data-ttu-id="110f6-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-167">False</span></span>                                               |
| <span data-ttu-id="110f6-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="110f6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="110f6-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="110f6-169">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="110f6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="110f6-170">Range-Lower</span></span>            | <span data-ttu-id="110f6-171">1</span><span class="sxs-lookup"><span data-stu-id="110f6-171">1</span></span>                                                   |
| <span data-ttu-id="110f6-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="110f6-172">Range-Upper</span></span>            | <span data-ttu-id="110f6-173">64</span><span class="sxs-lookup"><span data-stu-id="110f6-173">64</span></span>                                                  |
| <span data-ttu-id="110f6-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-174">Search-Flags</span></span>           | <span data-ttu-id="110f6-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="110f6-175">0x00000000</span></span>                                          |
| <span data-ttu-id="110f6-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-176">System-Flags</span></span>           | <span data-ttu-id="110f6-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="110f6-177">0x00000010</span></span>                                          |
| <span data-ttu-id="110f6-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="110f6-178">Classes used in</span></span>        | [<span data-ttu-id="110f6-179">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="110f6-179">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="110f6-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="110f6-180">Windows Server 2008</span></span>



| <span data-ttu-id="110f6-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="110f6-181">Entry</span></span> | <span data-ttu-id="110f6-182">Значение</span><span class="sxs-lookup"><span data-stu-id="110f6-182">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="110f6-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="110f6-183">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="110f6-184">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="110f6-185">System-Only</span></span>            | <span data-ttu-id="110f6-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-186">False</span></span>                                               |
| <span data-ttu-id="110f6-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="110f6-187">Is-Single-Valued</span></span>       | <span data-ttu-id="110f6-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-188">False</span></span>                                               |
| <span data-ttu-id="110f6-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="110f6-189">Is Indexed</span></span>             | <span data-ttu-id="110f6-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-190">False</span></span>                                               |
| <span data-ttu-id="110f6-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="110f6-191">In Global Catalog</span></span>      | <span data-ttu-id="110f6-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-192">False</span></span>                                               |
| <span data-ttu-id="110f6-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="110f6-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="110f6-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="110f6-194">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="110f6-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="110f6-195">Range-Lower</span></span>            | <span data-ttu-id="110f6-196">1</span><span class="sxs-lookup"><span data-stu-id="110f6-196">1</span></span>                                                   |
| <span data-ttu-id="110f6-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="110f6-197">Range-Upper</span></span>            | <span data-ttu-id="110f6-198">64</span><span class="sxs-lookup"><span data-stu-id="110f6-198">64</span></span>                                                  |
| <span data-ttu-id="110f6-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-199">Search-Flags</span></span>           | <span data-ttu-id="110f6-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="110f6-200">0x00000000</span></span>                                          |
| <span data-ttu-id="110f6-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-201">System-Flags</span></span>           | <span data-ttu-id="110f6-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="110f6-202">0x00000010</span></span>                                          |
| <span data-ttu-id="110f6-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="110f6-203">Classes used in</span></span>        | [<span data-ttu-id="110f6-204">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="110f6-204">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="110f6-205">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="110f6-205">Windows Server 2008 R2</span></span>



| <span data-ttu-id="110f6-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="110f6-206">Entry</span></span> | <span data-ttu-id="110f6-207">Значение</span><span class="sxs-lookup"><span data-stu-id="110f6-207">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="110f6-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="110f6-208">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="110f6-209">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="110f6-210">System-Only</span></span>            | <span data-ttu-id="110f6-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-211">False</span></span>                                               |
| <span data-ttu-id="110f6-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="110f6-212">Is-Single-Valued</span></span>       | <span data-ttu-id="110f6-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-213">False</span></span>                                               |
| <span data-ttu-id="110f6-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="110f6-214">Is Indexed</span></span>             | <span data-ttu-id="110f6-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-215">False</span></span>                                               |
| <span data-ttu-id="110f6-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="110f6-216">In Global Catalog</span></span>      | <span data-ttu-id="110f6-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-217">False</span></span>                                               |
| <span data-ttu-id="110f6-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="110f6-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="110f6-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="110f6-219">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="110f6-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="110f6-220">Range-Lower</span></span>            | <span data-ttu-id="110f6-221">1</span><span class="sxs-lookup"><span data-stu-id="110f6-221">1</span></span>                                                   |
| <span data-ttu-id="110f6-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="110f6-222">Range-Upper</span></span>            | <span data-ttu-id="110f6-223">64</span><span class="sxs-lookup"><span data-stu-id="110f6-223">64</span></span>                                                  |
| <span data-ttu-id="110f6-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-224">Search-Flags</span></span>           | <span data-ttu-id="110f6-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="110f6-225">0x00000000</span></span>                                          |
| <span data-ttu-id="110f6-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-226">System-Flags</span></span>           | <span data-ttu-id="110f6-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="110f6-227">0x00000010</span></span>                                          |
| <span data-ttu-id="110f6-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="110f6-228">Classes used in</span></span>        | [<span data-ttu-id="110f6-229">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="110f6-229">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="110f6-230">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="110f6-230">Windows Server 2012</span></span>



| <span data-ttu-id="110f6-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="110f6-231">Entry</span></span> | <span data-ttu-id="110f6-232">Значение</span><span class="sxs-lookup"><span data-stu-id="110f6-232">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="110f6-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="110f6-233">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="110f6-234">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="110f6-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="110f6-235">System-Only</span></span>            | <span data-ttu-id="110f6-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-236">False</span></span>                                               |
| <span data-ttu-id="110f6-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="110f6-237">Is-Single-Valued</span></span>       | <span data-ttu-id="110f6-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-238">False</span></span>                                               |
| <span data-ttu-id="110f6-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="110f6-239">Is Indexed</span></span>             | <span data-ttu-id="110f6-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-240">False</span></span>                                               |
| <span data-ttu-id="110f6-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="110f6-241">In Global Catalog</span></span>      | <span data-ttu-id="110f6-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="110f6-242">False</span></span>                                               |
| <span data-ttu-id="110f6-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="110f6-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="110f6-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="110f6-244">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="110f6-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="110f6-245">Range-Lower</span></span>            | <span data-ttu-id="110f6-246">1</span><span class="sxs-lookup"><span data-stu-id="110f6-246">1</span></span>                                                   |
| <span data-ttu-id="110f6-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="110f6-247">Range-Upper</span></span>            | <span data-ttu-id="110f6-248">64</span><span class="sxs-lookup"><span data-stu-id="110f6-248">64</span></span>                                                  |
| <span data-ttu-id="110f6-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-249">Search-Flags</span></span>           | <span data-ttu-id="110f6-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="110f6-250">0x00000000</span></span>                                          |
| <span data-ttu-id="110f6-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="110f6-251">System-Flags</span></span>           | <span data-ttu-id="110f6-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="110f6-252">0x00000010</span></span>                                          |
| <span data-ttu-id="110f6-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="110f6-253">Classes used in</span></span>        | [<span data-ttu-id="110f6-254">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="110f6-254">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



 

 





