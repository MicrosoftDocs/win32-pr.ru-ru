---
title: Атрибут ms-DS-раскрыть-OnDemand-Group
description: Используется с контроллером RODC для определения пользователей, компьютеров и групп, которым разрешено кэширование паролей на контроллере домена только для чтения.
ms.assetid: ee31957c-66a2-49d8-865c-7f599754dcdd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-раскрыть-OnDemand-Group
- Схема AD атрибута msDS-Ревеалондемандграуп
topic_type:
- apiref
api_name:
- ms-DS-Reveal-OnDemand-Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc89e0aabf1d82a9b7171530c5d297c668dbcb99
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893474"
---
# <a name="ms-ds-reveal-ondemand-group-attribute"></a><span data-ttu-id="c149a-105">Атрибут ms-DS-раскрыть-OnDemand-Group</span><span class="sxs-lookup"><span data-stu-id="c149a-105">ms-DS-Reveal-OnDemand-Group attribute</span></span>

<span data-ttu-id="c149a-106">Используется с контроллером RODC для определения пользователей, компьютеров и групп, которым разрешено кэширование паролей на контроллере домена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c149a-106">Used with RODCs to define which users, computers, and groups are allowed to have their passwords cached on an RODC.</span></span>



| <span data-ttu-id="c149a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c149a-107">Entry</span></span> | <span data-ttu-id="c149a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c149a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c149a-109">CN</span><span class="sxs-lookup"><span data-stu-id="c149a-109">CN</span></span>                | <span data-ttu-id="c149a-110">MS-DS-раскрыть-OnDemand-Group</span><span class="sxs-lookup"><span data-stu-id="c149a-110">ms-DS-Reveal-OnDemand-Group</span></span>             |
| <span data-ttu-id="c149a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c149a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c149a-112">msDS-Ревеалондемандграуп</span><span class="sxs-lookup"><span data-stu-id="c149a-112">msDS-RevealOnDemandGroup</span></span>                |
| <span data-ttu-id="c149a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c149a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c149a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c149a-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c149a-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c149a-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c149a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c149a-116">Attribute-Id</span></span>      | <span data-ttu-id="c149a-117">1.2.840.113556.1.4.1928</span><span class="sxs-lookup"><span data-stu-id="c149a-117">1.2.840.113556.1.4.1928</span></span>                 |
| <span data-ttu-id="c149a-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c149a-118">System-Id-Guid</span></span>    | <span data-ttu-id="c149a-119">303d9f4a-1dd6-4b38-8fc5-33afe8c988ad</span><span class="sxs-lookup"><span data-stu-id="c149a-119">303d9f4a-1dd6-4b38-8fc5-33afe8c988ad</span></span>    |
| <span data-ttu-id="c149a-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c149a-120">Syntax</span></span>            | [<span data-ttu-id="c149a-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c149a-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c149a-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c149a-122">Implementations</span></span>

-   [<span data-ttu-id="c149a-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c149a-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c149a-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c149a-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c149a-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c149a-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="c149a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c149a-126">Windows Server 2008</span></span>



| <span data-ttu-id="c149a-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="c149a-127">Entry</span></span> | <span data-ttu-id="c149a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c149a-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c149a-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c149a-129">Link-Id</span></span>                | <span data-ttu-id="c149a-130">2110</span><span class="sxs-lookup"><span data-stu-id="c149a-130">2110</span></span>                                                                               |
| <span data-ttu-id="c149a-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c149a-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="c149a-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="c149a-132">System-Only</span></span>            | <span data-ttu-id="c149a-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-133">False</span></span>                                                                              |
| <span data-ttu-id="c149a-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c149a-134">Is-Single-Valued</span></span>       | <span data-ttu-id="c149a-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-135">False</span></span>                                                                              |
| <span data-ttu-id="c149a-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c149a-136">Is Indexed</span></span>             | <span data-ttu-id="c149a-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-137">False</span></span>                                                                              |
| <span data-ttu-id="c149a-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c149a-138">In Global Catalog</span></span>      | <span data-ttu-id="c149a-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-139">False</span></span>                                                                              |
| <span data-ttu-id="c149a-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c149a-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="c149a-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c149a-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="c149a-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c149a-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="c149a-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c149a-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="c149a-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c149a-144">Search-Flags</span></span>           | <span data-ttu-id="c149a-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c149a-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="c149a-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c149a-146">System-Flags</span></span>           | <span data-ttu-id="c149a-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c149a-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="c149a-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c149a-148">Classes used in</span></span>        | [<span data-ttu-id="c149a-149">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c149a-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c149a-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c149a-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c149a-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c149a-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c149a-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="c149a-152">Entry</span></span> | <span data-ttu-id="c149a-153">Значение</span><span class="sxs-lookup"><span data-stu-id="c149a-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c149a-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c149a-154">Link-Id</span></span>                | <span data-ttu-id="c149a-155">2110</span><span class="sxs-lookup"><span data-stu-id="c149a-155">2110</span></span>                                                                               |
| <span data-ttu-id="c149a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c149a-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="c149a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c149a-157">System-Only</span></span>            | <span data-ttu-id="c149a-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-158">False</span></span>                                                                              |
| <span data-ttu-id="c149a-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c149a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c149a-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-160">False</span></span>                                                                              |
| <span data-ttu-id="c149a-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c149a-161">Is Indexed</span></span>             | <span data-ttu-id="c149a-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-162">False</span></span>                                                                              |
| <span data-ttu-id="c149a-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c149a-163">In Global Catalog</span></span>      | <span data-ttu-id="c149a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-164">False</span></span>                                                                              |
| <span data-ttu-id="c149a-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c149a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c149a-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c149a-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="c149a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c149a-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="c149a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c149a-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="c149a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c149a-169">Search-Flags</span></span>           | <span data-ttu-id="c149a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c149a-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="c149a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c149a-171">System-Flags</span></span>           | <span data-ttu-id="c149a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c149a-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="c149a-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c149a-173">Classes used in</span></span>        | [<span data-ttu-id="c149a-174">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c149a-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c149a-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c149a-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c149a-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c149a-176">Windows Server 2012</span></span>



| <span data-ttu-id="c149a-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="c149a-177">Entry</span></span> | <span data-ttu-id="c149a-178">Значение</span><span class="sxs-lookup"><span data-stu-id="c149a-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c149a-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c149a-179">Link-Id</span></span>                | <span data-ttu-id="c149a-180">2110</span><span class="sxs-lookup"><span data-stu-id="c149a-180">2110</span></span>                                                                               |
| <span data-ttu-id="c149a-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c149a-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="c149a-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="c149a-182">System-Only</span></span>            | <span data-ttu-id="c149a-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-183">False</span></span>                                                                              |
| <span data-ttu-id="c149a-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c149a-184">Is-Single-Valued</span></span>       | <span data-ttu-id="c149a-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-185">False</span></span>                                                                              |
| <span data-ttu-id="c149a-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c149a-186">Is Indexed</span></span>             | <span data-ttu-id="c149a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-187">False</span></span>                                                                              |
| <span data-ttu-id="c149a-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c149a-188">In Global Catalog</span></span>      | <span data-ttu-id="c149a-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c149a-189">False</span></span>                                                                              |
| <span data-ttu-id="c149a-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c149a-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="c149a-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c149a-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="c149a-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c149a-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="c149a-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c149a-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="c149a-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c149a-194">Search-Flags</span></span>           | <span data-ttu-id="c149a-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c149a-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="c149a-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c149a-196">System-Flags</span></span>           | <span data-ttu-id="c149a-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c149a-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="c149a-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c149a-198">Classes used in</span></span>        | [<span data-ttu-id="c149a-199">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c149a-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c149a-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="c149a-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





