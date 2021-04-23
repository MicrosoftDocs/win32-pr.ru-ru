---
title: Атрибут ms-DS-NC-RO-Replica-Locations
description: Связанный атрибут для объекта перекрестной ссылки для секции. Выводит список контроллеров домена, которые должны размещать секцию в режиме только для чтения.
ms.assetid: 2473f201-abf7-4fb1-b005-c8db528aeab8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "MS-DS-NC-RO-Replica-Locations"
- Схема AD атрибута msDS-NC-RO-Replica-Locations
topic_type:
- apiref
api_name:
- ms-DS-NC-RO-Replica-Locations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590661cb3dc096caa714066762f7b556e69c5145
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655439"
---
# <a name="ms-ds-nc-ro-replica-locations-attribute"></a><span data-ttu-id="dfed2-106">Атрибут ms-DS-NC-RO-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="dfed2-106">ms-DS-NC-RO-Replica-Locations attribute</span></span>

<span data-ttu-id="dfed2-107">Связанный атрибут для объекта перекрестной ссылки для секции.</span><span class="sxs-lookup"><span data-stu-id="dfed2-107">A linked attribute on a cross reference object for a partition.</span></span> <span data-ttu-id="dfed2-108">Выводит список контроллеров домена, которые должны размещать секцию в режиме только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dfed2-108">Lists the DC that should host the partition in a read-only manner.</span></span>



| <span data-ttu-id="dfed2-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="dfed2-109">Entry</span></span> | <span data-ttu-id="dfed2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="dfed2-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="dfed2-111">CN</span><span class="sxs-lookup"><span data-stu-id="dfed2-111">CN</span></span>                | <span data-ttu-id="dfed2-112">MS-DS-NC-RO-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="dfed2-112">ms-DS-NC-RO-Replica-Locations</span></span>           |
| <span data-ttu-id="dfed2-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="dfed2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dfed2-114">msDS-NC-RO-Replica-Locations</span><span class="sxs-lookup"><span data-stu-id="dfed2-114">msDS-NC-RO-Replica-Locations</span></span>            |
| <span data-ttu-id="dfed2-115">Размер</span><span class="sxs-lookup"><span data-stu-id="dfed2-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="dfed2-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="dfed2-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="dfed2-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="dfed2-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="dfed2-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dfed2-118">Attribute-Id</span></span>      | <span data-ttu-id="dfed2-119">1.2.840.113556.1.4.1967</span><span class="sxs-lookup"><span data-stu-id="dfed2-119">1.2.840.113556.1.4.1967</span></span>                 |
| <span data-ttu-id="dfed2-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="dfed2-120">System-Id-Guid</span></span>    | <span data-ttu-id="dfed2-121">3df793df-9858-4417-A701-735a1ecebf74</span><span class="sxs-lookup"><span data-stu-id="dfed2-121">3df793df-9858-4417-a701-735a1ecebf74</span></span>    |
| <span data-ttu-id="dfed2-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfed2-122">Syntax</span></span>            | [<span data-ttu-id="dfed2-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="dfed2-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="dfed2-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="dfed2-124">Implementations</span></span>

-   [<span data-ttu-id="dfed2-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dfed2-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dfed2-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dfed2-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dfed2-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dfed2-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="dfed2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfed2-128">Windows Server 2008</span></span>



| <span data-ttu-id="dfed2-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="dfed2-129">Entry</span></span> | <span data-ttu-id="dfed2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="dfed2-130">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="dfed2-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dfed2-131">Link-Id</span></span>                | <span data-ttu-id="dfed2-132">2114</span><span class="sxs-lookup"><span data-stu-id="dfed2-132">2114</span></span>                                       |
| <span data-ttu-id="dfed2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfed2-133">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="dfed2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfed2-134">System-Only</span></span>            | <span data-ttu-id="dfed2-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-135">False</span></span>                                      |
| <span data-ttu-id="dfed2-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dfed2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="dfed2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-137">False</span></span>                                      |
| <span data-ttu-id="dfed2-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dfed2-138">Is Indexed</span></span>             | <span data-ttu-id="dfed2-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-139">False</span></span>                                      |
| <span data-ttu-id="dfed2-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dfed2-140">In Global Catalog</span></span>      | <span data-ttu-id="dfed2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-141">False</span></span>                                      |
| <span data-ttu-id="dfed2-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dfed2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfed2-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dfed2-143">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="dfed2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfed2-144">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="dfed2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfed2-145">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="dfed2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfed2-146">Search-Flags</span></span>           | <span data-ttu-id="dfed2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfed2-147">0x00000000</span></span>                                 |
| <span data-ttu-id="dfed2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfed2-148">System-Flags</span></span>           | <span data-ttu-id="dfed2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfed2-149">0x00000010</span></span>                                 |
| <span data-ttu-id="dfed2-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dfed2-150">Classes used in</span></span>        | [<span data-ttu-id="dfed2-151">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="dfed2-151">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dfed2-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dfed2-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dfed2-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="dfed2-153">Entry</span></span> | <span data-ttu-id="dfed2-154">Значение</span><span class="sxs-lookup"><span data-stu-id="dfed2-154">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="dfed2-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dfed2-155">Link-Id</span></span>                | <span data-ttu-id="dfed2-156">2114</span><span class="sxs-lookup"><span data-stu-id="dfed2-156">2114</span></span>                                       |
| <span data-ttu-id="dfed2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfed2-157">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="dfed2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfed2-158">System-Only</span></span>            | <span data-ttu-id="dfed2-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-159">False</span></span>                                      |
| <span data-ttu-id="dfed2-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dfed2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="dfed2-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-161">False</span></span>                                      |
| <span data-ttu-id="dfed2-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dfed2-162">Is Indexed</span></span>             | <span data-ttu-id="dfed2-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-163">False</span></span>                                      |
| <span data-ttu-id="dfed2-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dfed2-164">In Global Catalog</span></span>      | <span data-ttu-id="dfed2-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-165">False</span></span>                                      |
| <span data-ttu-id="dfed2-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dfed2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfed2-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dfed2-167">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="dfed2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfed2-168">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="dfed2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfed2-169">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="dfed2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfed2-170">Search-Flags</span></span>           | <span data-ttu-id="dfed2-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfed2-171">0x00000000</span></span>                                 |
| <span data-ttu-id="dfed2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfed2-172">System-Flags</span></span>           | <span data-ttu-id="dfed2-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfed2-173">0x00000010</span></span>                                 |
| <span data-ttu-id="dfed2-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dfed2-174">Classes used in</span></span>        | [<span data-ttu-id="dfed2-175">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="dfed2-175">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dfed2-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfed2-176">Windows Server 2012</span></span>



| <span data-ttu-id="dfed2-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="dfed2-177">Entry</span></span> | <span data-ttu-id="dfed2-178">Значение</span><span class="sxs-lookup"><span data-stu-id="dfed2-178">Value</span></span> |
|------------------------|--------------------------------------------|
| <span data-ttu-id="dfed2-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dfed2-179">Link-Id</span></span>                | <span data-ttu-id="dfed2-180">2114</span><span class="sxs-lookup"><span data-stu-id="dfed2-180">2114</span></span>                                       |
| <span data-ttu-id="dfed2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dfed2-181">MAPI-Id</span></span>                | \-                                         |
| <span data-ttu-id="dfed2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="dfed2-182">System-Only</span></span>            | <span data-ttu-id="dfed2-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-183">False</span></span>                                      |
| <span data-ttu-id="dfed2-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dfed2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="dfed2-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-185">False</span></span>                                      |
| <span data-ttu-id="dfed2-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dfed2-186">Is Indexed</span></span>             | <span data-ttu-id="dfed2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-187">False</span></span>                                      |
| <span data-ttu-id="dfed2-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dfed2-188">In Global Catalog</span></span>      | <span data-ttu-id="dfed2-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="dfed2-189">False</span></span>                                      |
| <span data-ttu-id="dfed2-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dfed2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="dfed2-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dfed2-191">O:BAG:BAD:S:</span></span>                               |
| <span data-ttu-id="dfed2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dfed2-192">Range-Lower</span></span>            | \-                                         |
| <span data-ttu-id="dfed2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dfed2-193">Range-Upper</span></span>            | \-                                         |
| <span data-ttu-id="dfed2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dfed2-194">Search-Flags</span></span>           | <span data-ttu-id="dfed2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dfed2-195">0x00000000</span></span>                                 |
| <span data-ttu-id="dfed2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dfed2-196">System-Flags</span></span>           | <span data-ttu-id="dfed2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dfed2-197">0x00000010</span></span>                                 |
| <span data-ttu-id="dfed2-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dfed2-198">Classes used in</span></span>        | [<span data-ttu-id="dfed2-199">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="dfed2-199">**Cross-Ref**</span></span>](c-crossref.md)<br/> |



 

 





