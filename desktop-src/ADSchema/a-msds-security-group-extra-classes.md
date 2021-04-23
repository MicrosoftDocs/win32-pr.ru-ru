---
title: Атрибут ms-DS-Security-Group-лишнюю-classes
description: Общие имена нестандартных классов, которые можно добавить в группу безопасности с помощью оснастки "Active Directory пользователи и компьютеры".
ms.assetid: 3808cb03-3d54-46ca-bad8-23120ed2ca07
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-Security-Group-classes
- msDS-Security-Group-classes атрибут AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Security-Group-Extra-Classes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3860cc80c669eaad30262cce63aff6dca3a2a8f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138939"
---
# <a name="ms-ds-security-group-extra-classes-attribute"></a><span data-ttu-id="a9d8a-105">Атрибут ms-DS-Security-Group-лишнюю-classes</span><span class="sxs-lookup"><span data-stu-id="a9d8a-105">ms-DS-Security-Group-Extra-Classes attribute</span></span>

<span data-ttu-id="a9d8a-106">Общие имена нестандартных классов, которые можно добавить в группу безопасности с помощью оснастки "Active Directory пользователи и компьютеры".</span><span class="sxs-lookup"><span data-stu-id="a9d8a-106">The common names of the nonstandard classes that can be added to a security group through the Active Directory Users and Computers snap-in.</span></span>



| <span data-ttu-id="a9d8a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9d8a-107">Entry</span></span> | <span data-ttu-id="a9d8a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d8a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a9d8a-109">CN</span><span class="sxs-lookup"><span data-stu-id="a9d8a-109">CN</span></span>                | <span data-ttu-id="a9d8a-110">MS-DS-Security-Group-дополнительные классы</span><span class="sxs-lookup"><span data-stu-id="a9d8a-110">ms-DS-Security-Group-Extra-Classes</span></span>          |
| <span data-ttu-id="a9d8a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a9d8a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a9d8a-112">msDS-Security-Group-дополнительные классы</span><span class="sxs-lookup"><span data-stu-id="a9d8a-112">msDS-Security-Group-Extra-Classes</span></span>           |
| <span data-ttu-id="a9d8a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="a9d8a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="a9d8a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a9d8a-114">Update Privilege</span></span>  | <span data-ttu-id="a9d8a-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="a9d8a-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="a9d8a-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a9d8a-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="a9d8a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a9d8a-117">Attribute-Id</span></span>      | <span data-ttu-id="a9d8a-118">1.2.840.113556.1.4.1688</span><span class="sxs-lookup"><span data-stu-id="a9d8a-118">1.2.840.113556.1.4.1688</span></span>                     |
| <span data-ttu-id="a9d8a-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a9d8a-119">System-Id-Guid</span></span>    | <span data-ttu-id="a9d8a-120">4f146ae8-a4fe-4801-A731-f51848a4f4e4</span><span class="sxs-lookup"><span data-stu-id="a9d8a-120">4f146ae8-a4fe-4801-a731-f51848a4f4e4</span></span>        |
| <span data-ttu-id="a9d8a-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9d8a-121">Syntax</span></span>            | [<span data-ttu-id="a9d8a-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a9d8a-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a9d8a-123">Implementations</span></span>

-   [<span data-ttu-id="a9d8a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a9d8a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a9d8a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a9d8a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a9d8a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a9d8a-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9d8a-129">Windows Server 2003</span></span>



| <span data-ttu-id="a9d8a-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9d8a-130">Entry</span></span> | <span data-ttu-id="a9d8a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d8a-131">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="a9d8a-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9d8a-132">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d8a-133">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d8a-134">System-Only</span></span>            | <span data-ttu-id="a9d8a-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-135">False</span></span>                                               |
| <span data-ttu-id="a9d8a-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9d8a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d8a-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-137">False</span></span>                                               |
| <span data-ttu-id="a9d8a-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9d8a-138">Is Indexed</span></span>             | <span data-ttu-id="a9d8a-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-139">False</span></span>                                               |
| <span data-ttu-id="a9d8a-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9d8a-140">In Global Catalog</span></span>      | <span data-ttu-id="a9d8a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-141">False</span></span>                                               |
| <span data-ttu-id="a9d8a-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9d8a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d8a-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d8a-143">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="a9d8a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d8a-144">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d8a-145">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-146">Search-Flags</span></span>           | <span data-ttu-id="a9d8a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d8a-147">0x00000000</span></span>                                          |
| <span data-ttu-id="a9d8a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-148">System-Flags</span></span>           | <span data-ttu-id="a9d8a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d8a-149">0x00000010</span></span>                                          |
| <span data-ttu-id="a9d8a-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9d8a-150">Classes used in</span></span>        | [<span data-ttu-id="a9d8a-151">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-151">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a9d8a-152">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a9d8a-152">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a9d8a-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9d8a-153">Entry</span></span> | <span data-ttu-id="a9d8a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d8a-154">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="a9d8a-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9d8a-155">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d8a-156">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d8a-157">System-Only</span></span>            | <span data-ttu-id="a9d8a-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-158">False</span></span>                                               |
| <span data-ttu-id="a9d8a-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9d8a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d8a-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-160">False</span></span>                                               |
| <span data-ttu-id="a9d8a-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9d8a-161">Is Indexed</span></span>             | <span data-ttu-id="a9d8a-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-162">False</span></span>                                               |
| <span data-ttu-id="a9d8a-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9d8a-163">In Global Catalog</span></span>      | <span data-ttu-id="a9d8a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-164">False</span></span>                                               |
| <span data-ttu-id="a9d8a-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9d8a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d8a-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d8a-166">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="a9d8a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d8a-167">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d8a-168">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-169">Search-Flags</span></span>           | <span data-ttu-id="a9d8a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d8a-170">0x00000000</span></span>                                          |
| <span data-ttu-id="a9d8a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-171">System-Flags</span></span>           | <span data-ttu-id="a9d8a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d8a-172">0x00000010</span></span>                                          |
| <span data-ttu-id="a9d8a-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9d8a-173">Classes used in</span></span>        | [<span data-ttu-id="a9d8a-174">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-174">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a9d8a-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9d8a-175">Windows Server 2008</span></span>



| <span data-ttu-id="a9d8a-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9d8a-176">Entry</span></span> | <span data-ttu-id="a9d8a-177">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d8a-177">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="a9d8a-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9d8a-178">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d8a-179">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d8a-180">System-Only</span></span>            | <span data-ttu-id="a9d8a-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-181">False</span></span>                                               |
| <span data-ttu-id="a9d8a-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9d8a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d8a-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-183">False</span></span>                                               |
| <span data-ttu-id="a9d8a-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9d8a-184">Is Indexed</span></span>             | <span data-ttu-id="a9d8a-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-185">False</span></span>                                               |
| <span data-ttu-id="a9d8a-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9d8a-186">In Global Catalog</span></span>      | <span data-ttu-id="a9d8a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-187">False</span></span>                                               |
| <span data-ttu-id="a9d8a-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9d8a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d8a-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d8a-189">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="a9d8a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d8a-190">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d8a-191">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-192">Search-Flags</span></span>           | <span data-ttu-id="a9d8a-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d8a-193">0x00000000</span></span>                                          |
| <span data-ttu-id="a9d8a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-194">System-Flags</span></span>           | <span data-ttu-id="a9d8a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d8a-195">0x00000010</span></span>                                          |
| <span data-ttu-id="a9d8a-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9d8a-196">Classes used in</span></span>        | [<span data-ttu-id="a9d8a-197">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-197">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a9d8a-198">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9d8a-198">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a9d8a-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9d8a-199">Entry</span></span> | <span data-ttu-id="a9d8a-200">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d8a-200">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="a9d8a-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9d8a-201">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d8a-202">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d8a-203">System-Only</span></span>            | <span data-ttu-id="a9d8a-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-204">False</span></span>                                               |
| <span data-ttu-id="a9d8a-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9d8a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d8a-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-206">False</span></span>                                               |
| <span data-ttu-id="a9d8a-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9d8a-207">Is Indexed</span></span>             | <span data-ttu-id="a9d8a-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-208">False</span></span>                                               |
| <span data-ttu-id="a9d8a-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9d8a-209">In Global Catalog</span></span>      | <span data-ttu-id="a9d8a-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-210">False</span></span>                                               |
| <span data-ttu-id="a9d8a-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9d8a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d8a-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d8a-212">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="a9d8a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d8a-213">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d8a-214">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-215">Search-Flags</span></span>           | <span data-ttu-id="a9d8a-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d8a-216">0x00000000</span></span>                                          |
| <span data-ttu-id="a9d8a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-217">System-Flags</span></span>           | <span data-ttu-id="a9d8a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d8a-218">0x00000010</span></span>                                          |
| <span data-ttu-id="a9d8a-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9d8a-219">Classes used in</span></span>        | [<span data-ttu-id="a9d8a-220">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-220">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a9d8a-221">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9d8a-221">Windows Server 2012</span></span>



| <span data-ttu-id="a9d8a-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="a9d8a-222">Entry</span></span> | <span data-ttu-id="a9d8a-223">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d8a-223">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="a9d8a-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a9d8a-224">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a9d8a-225">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="a9d8a-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="a9d8a-226">System-Only</span></span>            | <span data-ttu-id="a9d8a-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-227">False</span></span>                                               |
| <span data-ttu-id="a9d8a-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a9d8a-228">Is-Single-Valued</span></span>       | <span data-ttu-id="a9d8a-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-229">False</span></span>                                               |
| <span data-ttu-id="a9d8a-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a9d8a-230">Is Indexed</span></span>             | <span data-ttu-id="a9d8a-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-231">False</span></span>                                               |
| <span data-ttu-id="a9d8a-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a9d8a-232">In Global Catalog</span></span>      | <span data-ttu-id="a9d8a-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a9d8a-233">False</span></span>                                               |
| <span data-ttu-id="a9d8a-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a9d8a-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="a9d8a-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a9d8a-235">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="a9d8a-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a9d8a-236">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a9d8a-237">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="a9d8a-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-238">Search-Flags</span></span>           | <span data-ttu-id="a9d8a-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a9d8a-239">0x00000000</span></span>                                          |
| <span data-ttu-id="a9d8a-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a9d8a-240">System-Flags</span></span>           | <span data-ttu-id="a9d8a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a9d8a-241">0x00000010</span></span>                                          |
| <span data-ttu-id="a9d8a-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a9d8a-242">Classes used in</span></span>        | [<span data-ttu-id="a9d8a-243">**DS-UI-параметры**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-243">**DS-UI-Settings**</span></span>](c-dsuisettings.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a9d8a-244">Remarks</span><span class="sxs-lookup"><span data-stu-id="a9d8a-244">Remarks</span></span>

<span data-ttu-id="a9d8a-245">В следующем списке перечислены стандартные классы, которые можно добавить в группу с помощью оснастки «Active Directory пользователи и компьютеры».</span><span class="sxs-lookup"><span data-stu-id="a9d8a-245">The following list identifies the standard classes that can be added to a group through the Active Directory Users and Computers snap-in.</span></span>

-   [<span data-ttu-id="a9d8a-246">**Сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-246">**Group**</span></span>](c-group.md)
-   [<span data-ttu-id="a9d8a-247">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-247">**User**</span></span>](c-user.md)
-   [<span data-ttu-id="a9d8a-248">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-248">**inetOrgPerson**</span></span>](c-inetorgperson.md)
-   [<span data-ttu-id="a9d8a-249">**Contact**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-249">**Contact**</span></span>](c-contact.md)
-   [<span data-ttu-id="a9d8a-250">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-250">**Computer**</span></span>](c-computer.md)

## <a name="see-also"></a><span data-ttu-id="a9d8a-251">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9d8a-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d8a-252">**MS-DS-non-Security-Group-classes — классы**</span><span class="sxs-lookup"><span data-stu-id="a9d8a-252">**ms-DS-Non-Security-Group-Extra-Classes**</span></span>](a-msds-non-security-group-extra-classes.md)
</dt> </dl>

 

 





