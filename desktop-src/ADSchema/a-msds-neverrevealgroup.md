---
title: Атрибут ms-DS-Never-раскрыть-Group
description: Используется с контроллером RODC для определения пользователей, компьютеров и групп, которые не могут кэшировать пароли в RODC.
ms.assetid: 203a660b-503e-4cf1-a796-eac024629b3e
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута группы MS-DS-Never-раскрыть
- Схема AD атрибута msDS-Неверревеалграуп
topic_type:
- apiref
api_name:
- ms-DS-Never-Reveal-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1308fb1bc0818601a037e66b764e607c0a32532
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655180"
---
# <a name="ms-ds-never-reveal-group-attribute"></a><span data-ttu-id="77f21-105">Атрибут ms-DS-Never-раскрыть-Group</span><span class="sxs-lookup"><span data-stu-id="77f21-105">ms-DS-Never-Reveal-Group attribute</span></span>

<span data-ttu-id="77f21-106">Используется с контроллером RODC для определения пользователей, компьютеров и групп, которые не могут кэшировать пароли в RODC.</span><span class="sxs-lookup"><span data-stu-id="77f21-106">Used with RODCs to define which users, computers, and groups are not allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="77f21-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="77f21-107">Entry</span></span> | <span data-ttu-id="77f21-108">Значение</span><span class="sxs-lookup"><span data-stu-id="77f21-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="77f21-109">CN</span><span class="sxs-lookup"><span data-stu-id="77f21-109">CN</span></span>                | <span data-ttu-id="77f21-110">MS-DS-Never-раскрыть — группа</span><span class="sxs-lookup"><span data-stu-id="77f21-110">ms-DS-Never-Reveal-Group</span></span>                |
| <span data-ttu-id="77f21-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="77f21-111">Ldap-Display-Name</span></span> | <span data-ttu-id="77f21-112">msDS-Неверревеалграуп</span><span class="sxs-lookup"><span data-stu-id="77f21-112">msDS-NeverRevealGroup</span></span>                   |
| <span data-ttu-id="77f21-113">Размер</span><span class="sxs-lookup"><span data-stu-id="77f21-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="77f21-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="77f21-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="77f21-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="77f21-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="77f21-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="77f21-116">Attribute-Id</span></span>      | <span data-ttu-id="77f21-117">1.2.840.113556.1.4.1926</span><span class="sxs-lookup"><span data-stu-id="77f21-117">1.2.840.113556.1.4.1926</span></span>                 |
| <span data-ttu-id="77f21-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="77f21-118">System-Id-Guid</span></span>    | <span data-ttu-id="77f21-119">15585999-fd49-4d66-b25d-eeb96aba8174</span><span class="sxs-lookup"><span data-stu-id="77f21-119">15585999-fd49-4d66-b25d-eeb96aba8174</span></span>    |
| <span data-ttu-id="77f21-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77f21-120">Syntax</span></span>            | [<span data-ttu-id="77f21-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="77f21-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="77f21-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="77f21-122">Implementations</span></span>

-   [<span data-ttu-id="77f21-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="77f21-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="77f21-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="77f21-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="77f21-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="77f21-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="77f21-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77f21-126">Windows Server 2008</span></span>



| <span data-ttu-id="77f21-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="77f21-127">Entry</span></span> | <span data-ttu-id="77f21-128">Значение</span><span class="sxs-lookup"><span data-stu-id="77f21-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77f21-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="77f21-129">Link-Id</span></span>                | <span data-ttu-id="77f21-130">2106</span><span class="sxs-lookup"><span data-stu-id="77f21-130">2106</span></span>                                                                               |
| <span data-ttu-id="77f21-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77f21-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="77f21-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="77f21-132">System-Only</span></span>            | <span data-ttu-id="77f21-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-133">False</span></span>                                                                              |
| <span data-ttu-id="77f21-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="77f21-134">Is-Single-Valued</span></span>       | <span data-ttu-id="77f21-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-135">False</span></span>                                                                              |
| <span data-ttu-id="77f21-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="77f21-136">Is Indexed</span></span>             | <span data-ttu-id="77f21-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-137">False</span></span>                                                                              |
| <span data-ttu-id="77f21-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="77f21-138">In Global Catalog</span></span>      | <span data-ttu-id="77f21-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-139">False</span></span>                                                                              |
| <span data-ttu-id="77f21-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="77f21-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="77f21-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="77f21-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="77f21-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77f21-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="77f21-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77f21-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="77f21-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77f21-144">Search-Flags</span></span>           | <span data-ttu-id="77f21-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77f21-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="77f21-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77f21-146">System-Flags</span></span>           | <span data-ttu-id="77f21-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77f21-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="77f21-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="77f21-148">Classes used in</span></span>        | [<span data-ttu-id="77f21-149">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="77f21-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="77f21-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="77f21-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="77f21-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77f21-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="77f21-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="77f21-152">Entry</span></span> | <span data-ttu-id="77f21-153">Значение</span><span class="sxs-lookup"><span data-stu-id="77f21-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77f21-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="77f21-154">Link-Id</span></span>                | <span data-ttu-id="77f21-155">2106</span><span class="sxs-lookup"><span data-stu-id="77f21-155">2106</span></span>                                                                               |
| <span data-ttu-id="77f21-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77f21-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="77f21-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="77f21-157">System-Only</span></span>            | <span data-ttu-id="77f21-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-158">False</span></span>                                                                              |
| <span data-ttu-id="77f21-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="77f21-159">Is-Single-Valued</span></span>       | <span data-ttu-id="77f21-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-160">False</span></span>                                                                              |
| <span data-ttu-id="77f21-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="77f21-161">Is Indexed</span></span>             | <span data-ttu-id="77f21-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-162">False</span></span>                                                                              |
| <span data-ttu-id="77f21-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="77f21-163">In Global Catalog</span></span>      | <span data-ttu-id="77f21-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-164">False</span></span>                                                                              |
| <span data-ttu-id="77f21-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="77f21-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="77f21-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="77f21-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="77f21-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77f21-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="77f21-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77f21-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="77f21-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77f21-169">Search-Flags</span></span>           | <span data-ttu-id="77f21-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77f21-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="77f21-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77f21-171">System-Flags</span></span>           | <span data-ttu-id="77f21-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77f21-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="77f21-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="77f21-173">Classes used in</span></span>        | [<span data-ttu-id="77f21-174">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="77f21-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="77f21-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="77f21-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="77f21-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="77f21-176">Windows Server 2012</span></span>



| <span data-ttu-id="77f21-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="77f21-177">Entry</span></span> | <span data-ttu-id="77f21-178">Значение</span><span class="sxs-lookup"><span data-stu-id="77f21-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77f21-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="77f21-179">Link-Id</span></span>                | <span data-ttu-id="77f21-180">2106</span><span class="sxs-lookup"><span data-stu-id="77f21-180">2106</span></span>                                                                               |
| <span data-ttu-id="77f21-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="77f21-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="77f21-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="77f21-182">System-Only</span></span>            | <span data-ttu-id="77f21-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-183">False</span></span>                                                                              |
| <span data-ttu-id="77f21-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="77f21-184">Is-Single-Valued</span></span>       | <span data-ttu-id="77f21-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-185">False</span></span>                                                                              |
| <span data-ttu-id="77f21-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="77f21-186">Is Indexed</span></span>             | <span data-ttu-id="77f21-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-187">False</span></span>                                                                              |
| <span data-ttu-id="77f21-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="77f21-188">In Global Catalog</span></span>      | <span data-ttu-id="77f21-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="77f21-189">False</span></span>                                                                              |
| <span data-ttu-id="77f21-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="77f21-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="77f21-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="77f21-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="77f21-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="77f21-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="77f21-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="77f21-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="77f21-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="77f21-194">Search-Flags</span></span>           | <span data-ttu-id="77f21-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="77f21-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="77f21-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="77f21-196">System-Flags</span></span>           | <span data-ttu-id="77f21-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77f21-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="77f21-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="77f21-198">Classes used in</span></span>        | [<span data-ttu-id="77f21-199">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="77f21-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="77f21-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="77f21-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





