---
title: Атрибут ms-DS-KrbTgt-Link
description: Используется с контроллером RODC для определения \_ учетной записи KRBTGT XXXX, соответствующей каждому контроллеру домена только для чтения.
ms.assetid: 08c3e50f-7f2a-4746-86b6-77780316679c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-KrbTgt-Link
- Схема AD атрибута msDS-Крбтгтлинк
topic_type:
- apiref
api_name:
- ms-DS-KrbTgt-Link
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcf8ddfee6f15532e4dad91fc1e34e1f136ea99b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893838"
---
# <a name="ms-ds-krbtgt-link-attribute"></a><span data-ttu-id="18583-105">Атрибут ms-DS-KrbTgt-Link</span><span class="sxs-lookup"><span data-stu-id="18583-105">ms-DS-KrbTgt-Link attribute</span></span>

<span data-ttu-id="18583-106">Используется с контроллером RODC для определения \_ учетной записи KRBTGT XXXX, соответствующей каждому контроллеру домена только для чтения.</span><span class="sxs-lookup"><span data-stu-id="18583-106">Used with RODCs to define which krbtgt\_XXXX account corresponds to each RODC.</span></span>



| <span data-ttu-id="18583-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="18583-107">Entry</span></span> | <span data-ttu-id="18583-108">Значение</span><span class="sxs-lookup"><span data-stu-id="18583-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="18583-109">CN</span><span class="sxs-lookup"><span data-stu-id="18583-109">CN</span></span>                | <span data-ttu-id="18583-110">MS-DS-KrbTgt-Link</span><span class="sxs-lookup"><span data-stu-id="18583-110">ms-DS-KrbTgt-Link</span></span>                       |
| <span data-ttu-id="18583-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="18583-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18583-112">msDS-Крбтгтлинк</span><span class="sxs-lookup"><span data-stu-id="18583-112">msDS-KrbTgtLink</span></span>                         |
| <span data-ttu-id="18583-113">Размер</span><span class="sxs-lookup"><span data-stu-id="18583-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="18583-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="18583-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="18583-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="18583-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="18583-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18583-116">Attribute-Id</span></span>      | <span data-ttu-id="18583-117">1.2.840.113556.1.4.1923</span><span class="sxs-lookup"><span data-stu-id="18583-117">1.2.840.113556.1.4.1923</span></span>                 |
| <span data-ttu-id="18583-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="18583-118">System-Id-Guid</span></span>    | <span data-ttu-id="18583-119">778ff5c9-6f4e-4b74-856a-d68383313910</span><span class="sxs-lookup"><span data-stu-id="18583-119">778ff5c9-6f4e-4b74-856a-d68383313910</span></span>    |
| <span data-ttu-id="18583-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18583-120">Syntax</span></span>            | [<span data-ttu-id="18583-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="18583-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="18583-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="18583-122">Implementations</span></span>

-   [<span data-ttu-id="18583-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18583-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18583-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18583-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18583-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18583-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="18583-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18583-126">Windows Server 2008</span></span>



| <span data-ttu-id="18583-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="18583-127">Entry</span></span> | <span data-ttu-id="18583-128">Значение</span><span class="sxs-lookup"><span data-stu-id="18583-128">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="18583-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18583-129">Link-Id</span></span>                | <span data-ttu-id="18583-130">2100</span><span class="sxs-lookup"><span data-stu-id="18583-130">2100</span></span>                                      |
| <span data-ttu-id="18583-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18583-131">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="18583-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="18583-132">System-Only</span></span>            | <span data-ttu-id="18583-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-133">False</span></span>                                     |
| <span data-ttu-id="18583-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18583-134">Is-Single-Valued</span></span>       | <span data-ttu-id="18583-135">True</span><span class="sxs-lookup"><span data-stu-id="18583-135">True</span></span>                                      |
| <span data-ttu-id="18583-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18583-136">Is Indexed</span></span>             | <span data-ttu-id="18583-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-137">False</span></span>                                     |
| <span data-ttu-id="18583-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18583-138">In Global Catalog</span></span>      | <span data-ttu-id="18583-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-139">False</span></span>                                     |
| <span data-ttu-id="18583-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18583-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="18583-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18583-141">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="18583-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18583-142">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="18583-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18583-143">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="18583-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18583-144">Search-Flags</span></span>           | <span data-ttu-id="18583-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18583-145">0x00000000</span></span>                                |
| <span data-ttu-id="18583-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18583-146">System-Flags</span></span>           | <span data-ttu-id="18583-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18583-147">0x00000010</span></span>                                |
| <span data-ttu-id="18583-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18583-148">Classes used in</span></span>        | [<span data-ttu-id="18583-149">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="18583-149">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18583-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18583-150">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18583-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="18583-151">Entry</span></span> | <span data-ttu-id="18583-152">Значение</span><span class="sxs-lookup"><span data-stu-id="18583-152">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="18583-153">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18583-153">Link-Id</span></span>                | <span data-ttu-id="18583-154">2100</span><span class="sxs-lookup"><span data-stu-id="18583-154">2100</span></span>                                      |
| <span data-ttu-id="18583-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18583-155">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="18583-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="18583-156">System-Only</span></span>            | <span data-ttu-id="18583-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-157">False</span></span>                                     |
| <span data-ttu-id="18583-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18583-158">Is-Single-Valued</span></span>       | <span data-ttu-id="18583-159">True</span><span class="sxs-lookup"><span data-stu-id="18583-159">True</span></span>                                      |
| <span data-ttu-id="18583-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18583-160">Is Indexed</span></span>             | <span data-ttu-id="18583-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-161">False</span></span>                                     |
| <span data-ttu-id="18583-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18583-162">In Global Catalog</span></span>      | <span data-ttu-id="18583-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-163">False</span></span>                                     |
| <span data-ttu-id="18583-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18583-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="18583-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18583-165">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="18583-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18583-166">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="18583-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18583-167">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="18583-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18583-168">Search-Flags</span></span>           | <span data-ttu-id="18583-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18583-169">0x00000000</span></span>                                |
| <span data-ttu-id="18583-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18583-170">System-Flags</span></span>           | <span data-ttu-id="18583-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18583-171">0x00000010</span></span>                                |
| <span data-ttu-id="18583-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18583-172">Classes used in</span></span>        | [<span data-ttu-id="18583-173">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="18583-173">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18583-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18583-174">Windows Server 2012</span></span>



| <span data-ttu-id="18583-175">Ввод</span><span class="sxs-lookup"><span data-stu-id="18583-175">Entry</span></span> | <span data-ttu-id="18583-176">Значение</span><span class="sxs-lookup"><span data-stu-id="18583-176">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="18583-177">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18583-177">Link-Id</span></span>                | <span data-ttu-id="18583-178">2100</span><span class="sxs-lookup"><span data-stu-id="18583-178">2100</span></span>                                      |
| <span data-ttu-id="18583-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18583-179">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="18583-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="18583-180">System-Only</span></span>            | <span data-ttu-id="18583-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-181">False</span></span>                                     |
| <span data-ttu-id="18583-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18583-182">Is-Single-Valued</span></span>       | <span data-ttu-id="18583-183">True</span><span class="sxs-lookup"><span data-stu-id="18583-183">True</span></span>                                      |
| <span data-ttu-id="18583-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18583-184">Is Indexed</span></span>             | <span data-ttu-id="18583-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-185">False</span></span>                                     |
| <span data-ttu-id="18583-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18583-186">In Global Catalog</span></span>      | <span data-ttu-id="18583-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="18583-187">False</span></span>                                     |
| <span data-ttu-id="18583-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18583-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="18583-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18583-189">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="18583-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18583-190">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="18583-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18583-191">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="18583-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18583-192">Search-Flags</span></span>           | <span data-ttu-id="18583-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="18583-193">0x00000000</span></span>                                |
| <span data-ttu-id="18583-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18583-194">System-Flags</span></span>           | <span data-ttu-id="18583-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18583-195">0x00000010</span></span>                                |
| <span data-ttu-id="18583-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18583-196">Classes used in</span></span>        | [<span data-ttu-id="18583-197">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="18583-197">**Computer**</span></span>](c-computer.md)<br/> |



 

 





