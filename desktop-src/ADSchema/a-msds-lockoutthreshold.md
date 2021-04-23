---
title: MS-DS-блокировка-атрибут порогового значения
description: Пороговое значение блокировки для блокировки учетных записей пользователей.
ms.assetid: 040f2c22-413f-4f30-a0ad-7c2411567771
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута порогового значения MS-DS-блокировка
- msDS-схема AD атрибута LockoutThreshold
topic_type:
- apiref
api_name:
- ms-DS-Lockout-Threshold
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae7f3d397982a9e018df73fd3801161436811bb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138655"
---
# <a name="ms-ds-lockout-threshold-attribute"></a><span data-ttu-id="549cd-105">MS-DS-блокировка-атрибут порогового значения</span><span class="sxs-lookup"><span data-stu-id="549cd-105">ms-DS-Lockout-Threshold attribute</span></span>

<span data-ttu-id="549cd-106">Пороговое значение блокировки для блокировки учетных записей пользователей.</span><span class="sxs-lookup"><span data-stu-id="549cd-106">Lockout threshold for the lock out of user accounts.</span></span>



| <span data-ttu-id="549cd-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="549cd-107">Entry</span></span> | <span data-ttu-id="549cd-108">Значение</span><span class="sxs-lookup"><span data-stu-id="549cd-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="549cd-109">CN</span><span class="sxs-lookup"><span data-stu-id="549cd-109">CN</span></span>                | <span data-ttu-id="549cd-110">MS-DS-блокировка-порог</span><span class="sxs-lookup"><span data-stu-id="549cd-110">ms-DS-Lockout-Threshold</span></span>              |
| <span data-ttu-id="549cd-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="549cd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="549cd-112">msDS-LockoutThreshold</span><span class="sxs-lookup"><span data-stu-id="549cd-112">msDS-LockoutThreshold</span></span>                |
| <span data-ttu-id="549cd-113">Размер</span><span class="sxs-lookup"><span data-stu-id="549cd-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="549cd-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="549cd-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="549cd-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="549cd-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="549cd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="549cd-116">Attribute-Id</span></span>      | <span data-ttu-id="549cd-117">1.2.840.113556.1.4.2019</span><span class="sxs-lookup"><span data-stu-id="549cd-117">1.2.840.113556.1.4.2019</span></span>              |
| <span data-ttu-id="549cd-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="549cd-118">System-Id-Guid</span></span>    | <span data-ttu-id="549cd-119">b8c8c35e-4a19-4a95-99d0-69fe4446286f</span><span class="sxs-lookup"><span data-stu-id="549cd-119">b8c8c35e-4a19-4a95-99d0-69fe4446286f</span></span> |
| <span data-ttu-id="549cd-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="549cd-120">Syntax</span></span>            | [<span data-ttu-id="549cd-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="549cd-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="549cd-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="549cd-122">Implementations</span></span>

-   [<span data-ttu-id="549cd-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="549cd-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="549cd-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="549cd-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="549cd-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="549cd-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="549cd-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="549cd-126">Windows Server 2008</span></span>



| <span data-ttu-id="549cd-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="549cd-127">Entry</span></span> | <span data-ttu-id="549cd-128">Значение</span><span class="sxs-lookup"><span data-stu-id="549cd-128">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="549cd-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="549cd-129">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="549cd-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="549cd-130">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="549cd-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="549cd-131">System-Only</span></span>            | <span data-ttu-id="549cd-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-132">False</span></span>                                                                 |
| <span data-ttu-id="549cd-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="549cd-133">Is-Single-Valued</span></span>       | <span data-ttu-id="549cd-134">True</span><span class="sxs-lookup"><span data-stu-id="549cd-134">True</span></span>                                                                  |
| <span data-ttu-id="549cd-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="549cd-135">Is Indexed</span></span>             | <span data-ttu-id="549cd-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-136">False</span></span>                                                                 |
| <span data-ttu-id="549cd-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="549cd-137">In Global Catalog</span></span>      | <span data-ttu-id="549cd-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-138">False</span></span>                                                                 |
| <span data-ttu-id="549cd-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="549cd-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="549cd-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="549cd-140">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="549cd-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="549cd-141">Range-Lower</span></span>            | <span data-ttu-id="549cd-142">0</span><span class="sxs-lookup"><span data-stu-id="549cd-142">0</span></span>                                                                     |
| <span data-ttu-id="549cd-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="549cd-143">Range-Upper</span></span>            | <span data-ttu-id="549cd-144">65535</span><span class="sxs-lookup"><span data-stu-id="549cd-144">65535</span></span>                                                                 |
| <span data-ttu-id="549cd-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="549cd-145">Search-Flags</span></span>           | <span data-ttu-id="549cd-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="549cd-146">0x00000000</span></span>                                                            |
| <span data-ttu-id="549cd-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="549cd-147">System-Flags</span></span>           | <span data-ttu-id="549cd-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="549cd-148">0x00000010</span></span>                                                            |
| <span data-ttu-id="549cd-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="549cd-149">Classes used in</span></span>        | [<span data-ttu-id="549cd-150">**MS-DS-Password-параметры**</span><span class="sxs-lookup"><span data-stu-id="549cd-150">**ms-DS-Password-Settings**</span></span>](c-msds-passwordsettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="549cd-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="549cd-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="549cd-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="549cd-152">Entry</span></span> | <span data-ttu-id="549cd-153">Значение</span><span class="sxs-lookup"><span data-stu-id="549cd-153">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="549cd-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="549cd-154">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="549cd-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="549cd-155">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="549cd-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="549cd-156">System-Only</span></span>            | <span data-ttu-id="549cd-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-157">False</span></span>                                                                 |
| <span data-ttu-id="549cd-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="549cd-158">Is-Single-Valued</span></span>       | <span data-ttu-id="549cd-159">True</span><span class="sxs-lookup"><span data-stu-id="549cd-159">True</span></span>                                                                  |
| <span data-ttu-id="549cd-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="549cd-160">Is Indexed</span></span>             | <span data-ttu-id="549cd-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-161">False</span></span>                                                                 |
| <span data-ttu-id="549cd-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="549cd-162">In Global Catalog</span></span>      | <span data-ttu-id="549cd-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-163">False</span></span>                                                                 |
| <span data-ttu-id="549cd-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="549cd-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="549cd-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="549cd-165">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="549cd-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="549cd-166">Range-Lower</span></span>            | <span data-ttu-id="549cd-167">0</span><span class="sxs-lookup"><span data-stu-id="549cd-167">0</span></span>                                                                     |
| <span data-ttu-id="549cd-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="549cd-168">Range-Upper</span></span>            | <span data-ttu-id="549cd-169">65535</span><span class="sxs-lookup"><span data-stu-id="549cd-169">65535</span></span>                                                                 |
| <span data-ttu-id="549cd-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="549cd-170">Search-Flags</span></span>           | <span data-ttu-id="549cd-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="549cd-171">0x00000000</span></span>                                                            |
| <span data-ttu-id="549cd-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="549cd-172">System-Flags</span></span>           | <span data-ttu-id="549cd-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="549cd-173">0x00000010</span></span>                                                            |
| <span data-ttu-id="549cd-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="549cd-174">Classes used in</span></span>        | [<span data-ttu-id="549cd-175">**MS-DS-Password-параметры**</span><span class="sxs-lookup"><span data-stu-id="549cd-175">**ms-DS-Password-Settings**</span></span>](c-msds-passwordsettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="549cd-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="549cd-176">Windows Server 2012</span></span>



| <span data-ttu-id="549cd-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="549cd-177">Entry</span></span> | <span data-ttu-id="549cd-178">Значение</span><span class="sxs-lookup"><span data-stu-id="549cd-178">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="549cd-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="549cd-179">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="549cd-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="549cd-180">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="549cd-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="549cd-181">System-Only</span></span>            | <span data-ttu-id="549cd-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-182">False</span></span>                                                                 |
| <span data-ttu-id="549cd-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="549cd-183">Is-Single-Valued</span></span>       | <span data-ttu-id="549cd-184">True</span><span class="sxs-lookup"><span data-stu-id="549cd-184">True</span></span>                                                                  |
| <span data-ttu-id="549cd-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="549cd-185">Is Indexed</span></span>             | <span data-ttu-id="549cd-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-186">False</span></span>                                                                 |
| <span data-ttu-id="549cd-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="549cd-187">In Global Catalog</span></span>      | <span data-ttu-id="549cd-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="549cd-188">False</span></span>                                                                 |
| <span data-ttu-id="549cd-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="549cd-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="549cd-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="549cd-190">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="549cd-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="549cd-191">Range-Lower</span></span>            | <span data-ttu-id="549cd-192">0</span><span class="sxs-lookup"><span data-stu-id="549cd-192">0</span></span>                                                                     |
| <span data-ttu-id="549cd-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="549cd-193">Range-Upper</span></span>            | <span data-ttu-id="549cd-194">65535</span><span class="sxs-lookup"><span data-stu-id="549cd-194">65535</span></span>                                                                 |
| <span data-ttu-id="549cd-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="549cd-195">Search-Flags</span></span>           | <span data-ttu-id="549cd-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="549cd-196">0x00000000</span></span>                                                            |
| <span data-ttu-id="549cd-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="549cd-197">System-Flags</span></span>           | <span data-ttu-id="549cd-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="549cd-198">0x00000010</span></span>                                                            |
| <span data-ttu-id="549cd-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="549cd-199">Classes used in</span></span>        | [<span data-ttu-id="549cd-200">**MS-DS-Password-параметры**</span><span class="sxs-lookup"><span data-stu-id="549cd-200">**ms-DS-Password-Settings**</span></span>](c-msds-passwordsettings.md)<br/> |



 

 





