---
title: Атрибут ms-DS-с полными репликами и NC
description: Определяет разделы, хранимые в качестве полных реплик.
ms.assetid: 217c5e8f-7022-4750-bb0d-ba92c6715c66
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-с полными репликами и NC
- Схема AD атрибута msDS-Хасфуллрепликанкс
topic_type:
- apiref
api_name:
- ms-DS-Has-Full-Replica-NCs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9df567ece1b49e359983518140b1daa9b461dd7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655449"
---
# <a name="ms-ds-has-full-replica-ncs-attribute"></a><span data-ttu-id="d70c4-105">Атрибут ms-DS-с полными репликами и NC</span><span class="sxs-lookup"><span data-stu-id="d70c4-105">ms-DS-Has-Full-Replica-NCs attribute</span></span>

<span data-ttu-id="d70c4-106">Определяет разделы, хранимые в качестве полных реплик.</span><span class="sxs-lookup"><span data-stu-id="d70c4-106">Identifies the partitions held as full replicas.</span></span>



| <span data-ttu-id="d70c4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d70c4-107">Entry</span></span> | <span data-ttu-id="d70c4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d70c4-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="d70c4-109">CN</span><span class="sxs-lookup"><span data-stu-id="d70c4-109">CN</span></span>                | <span data-ttu-id="d70c4-110">MS-DS-имеет-Full-реплика-NC</span><span class="sxs-lookup"><span data-stu-id="d70c4-110">ms-DS-Has-Full-Replica-NCs</span></span>              |
| <span data-ttu-id="d70c4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d70c4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d70c4-112">msDS-Хасфуллрепликанкс</span><span class="sxs-lookup"><span data-stu-id="d70c4-112">msDS-hasFullReplicaNCs</span></span>                  |
| <span data-ttu-id="d70c4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d70c4-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="d70c4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d70c4-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="d70c4-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d70c4-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="d70c4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d70c4-116">Attribute-Id</span></span>      | <span data-ttu-id="d70c4-117">1.2.840.113556.1.4.1925</span><span class="sxs-lookup"><span data-stu-id="d70c4-117">1.2.840.113556.1.4.1925</span></span>                 |
| <span data-ttu-id="d70c4-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d70c4-118">System-Id-Guid</span></span>    | <span data-ttu-id="d70c4-119">1d3c2d18-42d0-4868-99fe-0eca1e6fa9f3</span><span class="sxs-lookup"><span data-stu-id="d70c4-119">1d3c2d18-42d0-4868-99fe-0eca1e6fa9f3</span></span>    |
| <span data-ttu-id="d70c4-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d70c4-120">Syntax</span></span>            | [<span data-ttu-id="d70c4-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="d70c4-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="d70c4-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d70c4-122">Implementations</span></span>

-   [<span data-ttu-id="d70c4-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d70c4-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d70c4-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d70c4-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d70c4-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d70c4-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="d70c4-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d70c4-126">Windows Server 2008</span></span>



| <span data-ttu-id="d70c4-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="d70c4-127">Entry</span></span> | <span data-ttu-id="d70c4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d70c4-128">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d70c4-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d70c4-129">Link-Id</span></span>                | <span data-ttu-id="d70c4-130">2104</span><span class="sxs-lookup"><span data-stu-id="d70c4-130">2104</span></span>                                     |
| <span data-ttu-id="d70c4-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d70c4-131">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d70c4-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="d70c4-132">System-Only</span></span>            | <span data-ttu-id="d70c4-133">True</span><span class="sxs-lookup"><span data-stu-id="d70c4-133">True</span></span>                                     |
| <span data-ttu-id="d70c4-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d70c4-134">Is-Single-Valued</span></span>       | <span data-ttu-id="d70c4-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-135">False</span></span>                                    |
| <span data-ttu-id="d70c4-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d70c4-136">Is Indexed</span></span>             | <span data-ttu-id="d70c4-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-137">False</span></span>                                    |
| <span data-ttu-id="d70c4-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d70c4-138">In Global Catalog</span></span>      | <span data-ttu-id="d70c4-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-139">False</span></span>                                    |
| <span data-ttu-id="d70c4-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d70c4-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="d70c4-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d70c4-141">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d70c4-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d70c4-142">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d70c4-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d70c4-143">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d70c4-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d70c4-144">Search-Flags</span></span>           | <span data-ttu-id="d70c4-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d70c4-145">0x00000000</span></span>                               |
| <span data-ttu-id="d70c4-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d70c4-146">System-Flags</span></span>           | <span data-ttu-id="d70c4-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d70c4-147">0x00000010</span></span>                               |
| <span data-ttu-id="d70c4-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d70c4-148">Classes used in</span></span>        | [<span data-ttu-id="d70c4-149">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d70c4-149">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d70c4-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d70c4-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d70c4-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="d70c4-151">Entry</span></span> | <span data-ttu-id="d70c4-152">Значение</span><span class="sxs-lookup"><span data-stu-id="d70c4-152">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d70c4-153">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d70c4-153">Link-Id</span></span>                | <span data-ttu-id="d70c4-154">2104</span><span class="sxs-lookup"><span data-stu-id="d70c4-154">2104</span></span>                                     |
| <span data-ttu-id="d70c4-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d70c4-155">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d70c4-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="d70c4-156">System-Only</span></span>            | <span data-ttu-id="d70c4-157">True</span><span class="sxs-lookup"><span data-stu-id="d70c4-157">True</span></span>                                     |
| <span data-ttu-id="d70c4-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d70c4-158">Is-Single-Valued</span></span>       | <span data-ttu-id="d70c4-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-159">False</span></span>                                    |
| <span data-ttu-id="d70c4-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d70c4-160">Is Indexed</span></span>             | <span data-ttu-id="d70c4-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-161">False</span></span>                                    |
| <span data-ttu-id="d70c4-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d70c4-162">In Global Catalog</span></span>      | <span data-ttu-id="d70c4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-163">False</span></span>                                    |
| <span data-ttu-id="d70c4-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d70c4-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="d70c4-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d70c4-165">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d70c4-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d70c4-166">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d70c4-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d70c4-167">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d70c4-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d70c4-168">Search-Flags</span></span>           | <span data-ttu-id="d70c4-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d70c4-169">0x00000000</span></span>                               |
| <span data-ttu-id="d70c4-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d70c4-170">System-Flags</span></span>           | <span data-ttu-id="d70c4-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d70c4-171">0x00000010</span></span>                               |
| <span data-ttu-id="d70c4-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d70c4-172">Classes used in</span></span>        | [<span data-ttu-id="d70c4-173">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d70c4-173">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d70c4-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d70c4-174">Windows Server 2012</span></span>



| <span data-ttu-id="d70c4-175">Ввод</span><span class="sxs-lookup"><span data-stu-id="d70c4-175">Entry</span></span> | <span data-ttu-id="d70c4-176">Значение</span><span class="sxs-lookup"><span data-stu-id="d70c4-176">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="d70c4-177">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d70c4-177">Link-Id</span></span>                | <span data-ttu-id="d70c4-178">2104</span><span class="sxs-lookup"><span data-stu-id="d70c4-178">2104</span></span>                                     |
| <span data-ttu-id="d70c4-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d70c4-179">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="d70c4-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="d70c4-180">System-Only</span></span>            | <span data-ttu-id="d70c4-181">True</span><span class="sxs-lookup"><span data-stu-id="d70c4-181">True</span></span>                                     |
| <span data-ttu-id="d70c4-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d70c4-182">Is-Single-Valued</span></span>       | <span data-ttu-id="d70c4-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-183">False</span></span>                                    |
| <span data-ttu-id="d70c4-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d70c4-184">Is Indexed</span></span>             | <span data-ttu-id="d70c4-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-185">False</span></span>                                    |
| <span data-ttu-id="d70c4-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d70c4-186">In Global Catalog</span></span>      | <span data-ttu-id="d70c4-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="d70c4-187">False</span></span>                                    |
| <span data-ttu-id="d70c4-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d70c4-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="d70c4-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d70c4-189">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="d70c4-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d70c4-190">Range-Lower</span></span>            | \-                                       |
| <span data-ttu-id="d70c4-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d70c4-191">Range-Upper</span></span>            | \-                                       |
| <span data-ttu-id="d70c4-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d70c4-192">Search-Flags</span></span>           | <span data-ttu-id="d70c4-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d70c4-193">0x00000000</span></span>                               |
| <span data-ttu-id="d70c4-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d70c4-194">System-Flags</span></span>           | <span data-ttu-id="d70c4-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d70c4-195">0x00000010</span></span>                               |
| <span data-ttu-id="d70c4-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d70c4-196">Classes used in</span></span>        | [<span data-ttu-id="d70c4-197">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="d70c4-197">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> |



 

 





