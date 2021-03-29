---
title: атрибут MS-ФВЕ-VolumeGuid
description: Содержит идентификатор GUID, связанный с Томом диска, поддерживаемым BitLocker.
ms.assetid: fe54beb4-8352-4ec5-9c9a-22ac19ee3cab
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-ФВЕ-VolumeGuid
- Схема AD атрибута Мсфве-VolumeGuid
topic_type:
- apiref
api_name:
- ms-FVE-VolumeGuid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2413ef17a489c495e7279455f6b2092127550665
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893790"
---
# <a name="ms-fve-volumeguid-attribute"></a><span data-ttu-id="f2512-105">атрибут MS-ФВЕ-VolumeGuid</span><span class="sxs-lookup"><span data-stu-id="f2512-105">ms-FVE-VolumeGuid attribute</span></span>

<span data-ttu-id="f2512-106">Содержит идентификатор GUID, связанный с Томом диска, поддерживаемым BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f2512-106">Contains the GUID associated with a BitLocker-supported disk volume.</span></span>



| <span data-ttu-id="f2512-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2512-107">Entry</span></span> | <span data-ttu-id="f2512-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f2512-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f2512-109">CN</span><span class="sxs-lookup"><span data-stu-id="f2512-109">CN</span></span>                | <span data-ttu-id="f2512-110">MS-ФВЕ-VolumeGuid</span><span class="sxs-lookup"><span data-stu-id="f2512-110">ms-FVE-VolumeGuid</span></span>                                     |
| <span data-ttu-id="f2512-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f2512-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f2512-112">Мсфве — VolumeGuid</span><span class="sxs-lookup"><span data-stu-id="f2512-112">msFVE-VolumeGuid</span></span>                                      |
| <span data-ttu-id="f2512-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f2512-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f2512-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f2512-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="f2512-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f2512-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f2512-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2512-116">Attribute-Id</span></span>      | <span data-ttu-id="f2512-117">1.2.840.113556.1.4.1998</span><span class="sxs-lookup"><span data-stu-id="f2512-117">1.2.840.113556.1.4.1998</span></span>                               |
| <span data-ttu-id="f2512-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f2512-118">System-Id-Guid</span></span>    | <span data-ttu-id="f2512-119">85e5a5cf-dcee-4075-9cfd-ac9db6a2f245</span><span class="sxs-lookup"><span data-stu-id="f2512-119">85e5a5cf-dcee-4075-9cfd-ac9db6a2f245</span></span>                  |
| <span data-ttu-id="f2512-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2512-120">Syntax</span></span>            | [<span data-ttu-id="f2512-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="f2512-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f2512-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f2512-122">Implementations</span></span>

-   [<span data-ttu-id="f2512-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2512-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2512-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2512-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2512-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2512-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="f2512-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2512-126">Windows Server 2008</span></span>



| <span data-ttu-id="f2512-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2512-127">Entry</span></span> | <span data-ttu-id="f2512-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f2512-128">Value</span></span> |
|------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f2512-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2512-129">Link-Id</span></span>                | \-                                                                           |
| <span data-ttu-id="f2512-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2512-130">MAPI-Id</span></span>                | \-                                                                           |
| <span data-ttu-id="f2512-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2512-131">System-Only</span></span>            | <span data-ttu-id="f2512-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2512-132">False</span></span>                                                                        |
| <span data-ttu-id="f2512-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2512-133">Is-Single-Valued</span></span>       | <span data-ttu-id="f2512-134">True</span><span class="sxs-lookup"><span data-stu-id="f2512-134">True</span></span>                                                                         |
| <span data-ttu-id="f2512-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2512-135">Is Indexed</span></span>             | <span data-ttu-id="f2512-136">True</span><span class="sxs-lookup"><span data-stu-id="f2512-136">True</span></span>                                                                         |
| <span data-ttu-id="f2512-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2512-137">In Global Catalog</span></span>      | <span data-ttu-id="f2512-138">True</span><span class="sxs-lookup"><span data-stu-id="f2512-138">True</span></span>                                                                         |
| <span data-ttu-id="f2512-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2512-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2512-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2512-140">O:BAG:BAD:S:</span></span>                                                                 |
| <span data-ttu-id="f2512-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2512-141">Range-Lower</span></span>            | \-                                                                           |
| <span data-ttu-id="f2512-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2512-142">Range-Upper</span></span>            | \-                                                                           |
| <span data-ttu-id="f2512-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2512-143">Search-Flags</span></span>           | <span data-ttu-id="f2512-144">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="f2512-144">0x0000001B</span></span>                                                                   |
| <span data-ttu-id="f2512-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2512-145">System-Flags</span></span>           | <span data-ttu-id="f2512-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2512-146">0x00000010</span></span>                                                                   |
| <span data-ttu-id="f2512-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2512-147">Classes used in</span></span>        | [<span data-ttu-id="f2512-148">**MS-ФВЕ-Рековеринформатион**</span><span class="sxs-lookup"><span data-stu-id="f2512-148">**ms-FVE-RecoveryInformation**</span></span>](c-msfve-recoveryinformation.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2512-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2512-149">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2512-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2512-150">Entry</span></span> | <span data-ttu-id="f2512-151">Значение</span><span class="sxs-lookup"><span data-stu-id="f2512-151">Value</span></span> |
|------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f2512-152">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2512-152">Link-Id</span></span>                | \-                                                                           |
| <span data-ttu-id="f2512-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2512-153">MAPI-Id</span></span>                | \-                                                                           |
| <span data-ttu-id="f2512-154">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2512-154">System-Only</span></span>            | <span data-ttu-id="f2512-155">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2512-155">False</span></span>                                                                        |
| <span data-ttu-id="f2512-156">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2512-156">Is-Single-Valued</span></span>       | <span data-ttu-id="f2512-157">True</span><span class="sxs-lookup"><span data-stu-id="f2512-157">True</span></span>                                                                         |
| <span data-ttu-id="f2512-158">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2512-158">Is Indexed</span></span>             | <span data-ttu-id="f2512-159">True</span><span class="sxs-lookup"><span data-stu-id="f2512-159">True</span></span>                                                                         |
| <span data-ttu-id="f2512-160">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2512-160">In Global Catalog</span></span>      | <span data-ttu-id="f2512-161">True</span><span class="sxs-lookup"><span data-stu-id="f2512-161">True</span></span>                                                                         |
| <span data-ttu-id="f2512-162">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2512-162">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2512-163">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2512-163">O:BAG:BAD:S:</span></span>                                                                 |
| <span data-ttu-id="f2512-164">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2512-164">Range-Lower</span></span>            | \-                                                                           |
| <span data-ttu-id="f2512-165">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2512-165">Range-Upper</span></span>            | \-                                                                           |
| <span data-ttu-id="f2512-166">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2512-166">Search-Flags</span></span>           | <span data-ttu-id="f2512-167">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="f2512-167">0x0000001B</span></span>                                                                   |
| <span data-ttu-id="f2512-168">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2512-168">System-Flags</span></span>           | <span data-ttu-id="f2512-169">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2512-169">0x00000010</span></span>                                                                   |
| <span data-ttu-id="f2512-170">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2512-170">Classes used in</span></span>        | [<span data-ttu-id="f2512-171">**MS-ФВЕ-Рековеринформатион**</span><span class="sxs-lookup"><span data-stu-id="f2512-171">**ms-FVE-RecoveryInformation**</span></span>](c-msfve-recoveryinformation.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2512-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2512-172">Windows Server 2012</span></span>



| <span data-ttu-id="f2512-173">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2512-173">Entry</span></span> | <span data-ttu-id="f2512-174">Значение</span><span class="sxs-lookup"><span data-stu-id="f2512-174">Value</span></span> |
|------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f2512-175">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2512-175">Link-Id</span></span>                | \-                                                                           |
| <span data-ttu-id="f2512-176">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2512-176">MAPI-Id</span></span>                | \-                                                                           |
| <span data-ttu-id="f2512-177">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2512-177">System-Only</span></span>            | <span data-ttu-id="f2512-178">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2512-178">False</span></span>                                                                        |
| <span data-ttu-id="f2512-179">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2512-179">Is-Single-Valued</span></span>       | <span data-ttu-id="f2512-180">True</span><span class="sxs-lookup"><span data-stu-id="f2512-180">True</span></span>                                                                         |
| <span data-ttu-id="f2512-181">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2512-181">Is Indexed</span></span>             | <span data-ttu-id="f2512-182">True</span><span class="sxs-lookup"><span data-stu-id="f2512-182">True</span></span>                                                                         |
| <span data-ttu-id="f2512-183">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2512-183">In Global Catalog</span></span>      | <span data-ttu-id="f2512-184">True</span><span class="sxs-lookup"><span data-stu-id="f2512-184">True</span></span>                                                                         |
| <span data-ttu-id="f2512-185">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2512-185">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2512-186">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2512-186">O:BAG:BAD:S:</span></span>                                                                 |
| <span data-ttu-id="f2512-187">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2512-187">Range-Lower</span></span>            | \-                                                                           |
| <span data-ttu-id="f2512-188">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2512-188">Range-Upper</span></span>            | \-                                                                           |
| <span data-ttu-id="f2512-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2512-189">Search-Flags</span></span>           | <span data-ttu-id="f2512-190">0x0000001B</span><span class="sxs-lookup"><span data-stu-id="f2512-190">0x0000001B</span></span>                                                                   |
| <span data-ttu-id="f2512-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2512-191">System-Flags</span></span>           | <span data-ttu-id="f2512-192">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2512-192">0x00000010</span></span>                                                                   |
| <span data-ttu-id="f2512-193">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2512-193">Classes used in</span></span>        | [<span data-ttu-id="f2512-194">**MS-ФВЕ-Рековеринформатион**</span><span class="sxs-lookup"><span data-stu-id="f2512-194">**ms-FVE-RecoveryInformation**</span></span>](c-msfve-recoveryinformation.md)<br/> |



 

 





