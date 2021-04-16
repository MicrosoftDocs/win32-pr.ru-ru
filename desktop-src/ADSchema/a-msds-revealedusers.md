---
title: Атрибут ms-DS-Directory-Users
description: Используется с контроллером RODC для обнаружения объектов пользователя, секреты которых были предоставлены для RODC.
ms.assetid: 92f6d8a9-7829-4400-9b60-f1afe8653bc0
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Directory-Users
- Схема AD атрибута msDS-Ревеаледусерс
topic_type:
- apiref
api_name:
- ms-DS-Revealed-Users
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4900fea126fc45119e5d5825431d788d170ff0bd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655421"
---
# <a name="ms-ds-revealed-users-attribute"></a><span data-ttu-id="fdd75-105">Атрибут ms-DS-Directory-Users</span><span class="sxs-lookup"><span data-stu-id="fdd75-105">ms-DS-Revealed-Users attribute</span></span>

<span data-ttu-id="fdd75-106">Используется с контроллером RODC для обнаружения объектов пользователя, секреты которых были предоставлены для RODC.</span><span class="sxs-lookup"><span data-stu-id="fdd75-106">Used with RODCs to identify the user objects whose secrets have been disclosed to that RODC.</span></span>



| <span data-ttu-id="fdd75-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdd75-107">Entry</span></span> | <span data-ttu-id="fdd75-108">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd75-108">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="fdd75-109">CN</span><span class="sxs-lookup"><span data-stu-id="fdd75-109">CN</span></span>                | <span data-ttu-id="fdd75-110">MS-DS-выявили пользователей</span><span class="sxs-lookup"><span data-stu-id="fdd75-110">ms-DS-Revealed-Users</span></span>                            |
| <span data-ttu-id="fdd75-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fdd75-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fdd75-112">msDS-Ревеаледусерс</span><span class="sxs-lookup"><span data-stu-id="fdd75-112">msDS-RevealedUsers</span></span>                              |
| <span data-ttu-id="fdd75-113">Размер</span><span class="sxs-lookup"><span data-stu-id="fdd75-113">Size</span></span>              | \-                                              |
| <span data-ttu-id="fdd75-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fdd75-114">Update Privilege</span></span>  | \-                                              |
| <span data-ttu-id="fdd75-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fdd75-115">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="fdd75-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fdd75-116">Attribute-Id</span></span>      | <span data-ttu-id="fdd75-117">1.2.840.113556.1.4.1924</span><span class="sxs-lookup"><span data-stu-id="fdd75-117">1.2.840.113556.1.4.1924</span></span>                         |
| <span data-ttu-id="fdd75-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fdd75-118">System-Id-Guid</span></span>    | <span data-ttu-id="fdd75-119">185c7821-3749-443a-bd6a-288899071adb</span><span class="sxs-lookup"><span data-stu-id="fdd75-119">185c7821-3749-443a-bd6a-288899071adb</span></span>            |
| <span data-ttu-id="fdd75-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdd75-120">Syntax</span></span>            | [<span data-ttu-id="fdd75-121">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="fdd75-121">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="fdd75-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fdd75-122">Implementations</span></span>

-   [<span data-ttu-id="fdd75-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fdd75-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fdd75-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fdd75-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fdd75-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fdd75-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="fdd75-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdd75-126">Windows Server 2008</span></span>



| <span data-ttu-id="fdd75-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdd75-127">Entry</span></span> | <span data-ttu-id="fdd75-128">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd75-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd75-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdd75-129">Link-Id</span></span>                | <span data-ttu-id="fdd75-130">2102</span><span class="sxs-lookup"><span data-stu-id="fdd75-130">2102</span></span>                                                                               |
| <span data-ttu-id="fdd75-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd75-131">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="fdd75-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd75-132">System-Only</span></span>            | <span data-ttu-id="fdd75-133">True</span><span class="sxs-lookup"><span data-stu-id="fdd75-133">True</span></span>                                                                               |
| <span data-ttu-id="fdd75-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdd75-134">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd75-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-135">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdd75-136">Is Indexed</span></span>             | <span data-ttu-id="fdd75-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-137">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdd75-138">In Global Catalog</span></span>      | <span data-ttu-id="fdd75-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-139">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdd75-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd75-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd75-141">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="fdd75-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd75-142">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="fdd75-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd75-143">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="fdd75-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd75-144">Search-Flags</span></span>           | <span data-ttu-id="fdd75-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd75-145">0x00000000</span></span>                                                                         |
| <span data-ttu-id="fdd75-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd75-146">System-Flags</span></span>           | <span data-ttu-id="fdd75-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdd75-147">0x00000010</span></span>                                                                         |
| <span data-ttu-id="fdd75-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdd75-148">Classes used in</span></span>        | [<span data-ttu-id="fdd75-149">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="fdd75-149">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="fdd75-150">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fdd75-150">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fdd75-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fdd75-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fdd75-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdd75-152">Entry</span></span> | <span data-ttu-id="fdd75-153">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd75-153">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd75-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdd75-154">Link-Id</span></span>                | <span data-ttu-id="fdd75-155">2102</span><span class="sxs-lookup"><span data-stu-id="fdd75-155">2102</span></span>                                                                               |
| <span data-ttu-id="fdd75-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd75-156">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="fdd75-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd75-157">System-Only</span></span>            | <span data-ttu-id="fdd75-158">True</span><span class="sxs-lookup"><span data-stu-id="fdd75-158">True</span></span>                                                                               |
| <span data-ttu-id="fdd75-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdd75-159">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd75-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-160">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdd75-161">Is Indexed</span></span>             | <span data-ttu-id="fdd75-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-162">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdd75-163">In Global Catalog</span></span>      | <span data-ttu-id="fdd75-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-164">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdd75-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd75-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd75-166">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="fdd75-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd75-167">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="fdd75-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd75-168">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="fdd75-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd75-169">Search-Flags</span></span>           | <span data-ttu-id="fdd75-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd75-170">0x00000000</span></span>                                                                         |
| <span data-ttu-id="fdd75-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd75-171">System-Flags</span></span>           | <span data-ttu-id="fdd75-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdd75-172">0x00000010</span></span>                                                                         |
| <span data-ttu-id="fdd75-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdd75-173">Classes used in</span></span>        | [<span data-ttu-id="fdd75-174">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="fdd75-174">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="fdd75-175">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fdd75-175">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fdd75-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fdd75-176">Windows Server 2012</span></span>



| <span data-ttu-id="fdd75-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="fdd75-177">Entry</span></span> | <span data-ttu-id="fdd75-178">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd75-178">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd75-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fdd75-179">Link-Id</span></span>                | <span data-ttu-id="fdd75-180">2102</span><span class="sxs-lookup"><span data-stu-id="fdd75-180">2102</span></span>                                                                               |
| <span data-ttu-id="fdd75-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fdd75-181">MAPI-Id</span></span>                | \-                                                                                 |
| <span data-ttu-id="fdd75-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fdd75-182">System-Only</span></span>            | <span data-ttu-id="fdd75-183">True</span><span class="sxs-lookup"><span data-stu-id="fdd75-183">True</span></span>                                                                               |
| <span data-ttu-id="fdd75-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fdd75-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fdd75-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-185">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fdd75-186">Is Indexed</span></span>             | <span data-ttu-id="fdd75-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-187">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fdd75-188">In Global Catalog</span></span>      | <span data-ttu-id="fdd75-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="fdd75-189">False</span></span>                                                                              |
| <span data-ttu-id="fdd75-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fdd75-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fdd75-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fdd75-191">O:BAG:BAD:S:</span></span>                                                                       |
| <span data-ttu-id="fdd75-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fdd75-192">Range-Lower</span></span>            | \-                                                                                 |
| <span data-ttu-id="fdd75-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fdd75-193">Range-Upper</span></span>            | \-                                                                                 |
| <span data-ttu-id="fdd75-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd75-194">Search-Flags</span></span>           | <span data-ttu-id="fdd75-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fdd75-195">0x00000000</span></span>                                                                         |
| <span data-ttu-id="fdd75-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fdd75-196">System-Flags</span></span>           | <span data-ttu-id="fdd75-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fdd75-197">0x00000010</span></span>                                                                         |
| <span data-ttu-id="fdd75-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fdd75-198">Classes used in</span></span>        | [<span data-ttu-id="fdd75-199">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="fdd75-199">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="fdd75-200">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="fdd75-200">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





