---
title: Атрибут ms-DS-выявил-DSA
description: Обратная ссылка для MS-DS-раскрытых пользователей. Определяет, какой RODC хранит секрет пользователя.
ms.assetid: cd84db75-d961-4290-8aa7-2805febbd842
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MS-DS-выявил-DSA
- Схема AD атрибута msDS-Ревеаледдсас
topic_type:
- apiref
api_name:
- ms-DS-Revealed-DSAs
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e77dfd69fafffc3286f0ff9419965d7ae9daaa0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493803"
---
# <a name="ms-ds-revealed-dsas-attribute"></a><span data-ttu-id="509aa-106">Атрибут ms-DS-выявил-DSA</span><span class="sxs-lookup"><span data-stu-id="509aa-106">ms-DS-Revealed-DSAs attribute</span></span>

<span data-ttu-id="509aa-107">Обратная ссылка для [**MS-DS-раскрытых пользователей**](a-msds-revealedusers.md).</span><span class="sxs-lookup"><span data-stu-id="509aa-107">Backward link for [**ms-DS-Revealed-Users**](a-msds-revealedusers.md).</span></span> <span data-ttu-id="509aa-108">Определяет, какой RODC содержит секрет пользователя.</span><span class="sxs-lookup"><span data-stu-id="509aa-108">Identifies which RODC holds that user's secret.</span></span>



| <span data-ttu-id="509aa-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="509aa-109">Entry</span></span> | <span data-ttu-id="509aa-110">Значение</span><span class="sxs-lookup"><span data-stu-id="509aa-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="509aa-111">CN</span><span class="sxs-lookup"><span data-stu-id="509aa-111">CN</span></span>                | <span data-ttu-id="509aa-112">MS-DS-выявил-DSA</span><span class="sxs-lookup"><span data-stu-id="509aa-112">ms-DS-Revealed-DSAs</span></span>                     |
| <span data-ttu-id="509aa-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="509aa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="509aa-114">msDS-Ревеаледдсас</span><span class="sxs-lookup"><span data-stu-id="509aa-114">msDS-RevealedDSAs</span></span>                       |
| <span data-ttu-id="509aa-115">Размер</span><span class="sxs-lookup"><span data-stu-id="509aa-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="509aa-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="509aa-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="509aa-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="509aa-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="509aa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="509aa-118">Attribute-Id</span></span>      | <span data-ttu-id="509aa-119">1.2.840.113556.1.4.1930</span><span class="sxs-lookup"><span data-stu-id="509aa-119">1.2.840.113556.1.4.1930</span></span>                 |
| <span data-ttu-id="509aa-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="509aa-120">System-Id-Guid</span></span>    | <span data-ttu-id="509aa-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span><span class="sxs-lookup"><span data-stu-id="509aa-121">94f6f2ac-c76d-4b5e-b71f-f332c3e93c22</span></span>    |
| <span data-ttu-id="509aa-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="509aa-122">Syntax</span></span>            | [<span data-ttu-id="509aa-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="509aa-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="509aa-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="509aa-124">Implementations</span></span>

-   [<span data-ttu-id="509aa-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="509aa-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="509aa-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="509aa-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="509aa-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="509aa-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="509aa-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="509aa-128">Windows Server 2008</span></span>



| <span data-ttu-id="509aa-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="509aa-129">Entry</span></span> | <span data-ttu-id="509aa-130">Значение</span><span class="sxs-lookup"><span data-stu-id="509aa-130">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="509aa-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="509aa-131">Link-Id</span></span>                | <span data-ttu-id="509aa-132">2103</span><span class="sxs-lookup"><span data-stu-id="509aa-132">2103</span></span>                            |
| <span data-ttu-id="509aa-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="509aa-133">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="509aa-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="509aa-134">System-Only</span></span>            | <span data-ttu-id="509aa-135">True</span><span class="sxs-lookup"><span data-stu-id="509aa-135">True</span></span>                            |
| <span data-ttu-id="509aa-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="509aa-136">Is-Single-Valued</span></span>       | <span data-ttu-id="509aa-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-137">False</span></span>                           |
| <span data-ttu-id="509aa-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="509aa-138">Is Indexed</span></span>             | <span data-ttu-id="509aa-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-139">False</span></span>                           |
| <span data-ttu-id="509aa-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="509aa-140">In Global Catalog</span></span>      | <span data-ttu-id="509aa-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-141">False</span></span>                           |
| <span data-ttu-id="509aa-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="509aa-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="509aa-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="509aa-143">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="509aa-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="509aa-144">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="509aa-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="509aa-145">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="509aa-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="509aa-146">Search-Flags</span></span>           | <span data-ttu-id="509aa-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="509aa-147">0x00000000</span></span>                      |
| <span data-ttu-id="509aa-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="509aa-148">System-Flags</span></span>           | <span data-ttu-id="509aa-149">0x00000011</span><span class="sxs-lookup"><span data-stu-id="509aa-149">0x00000011</span></span>                      |
| <span data-ttu-id="509aa-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="509aa-150">Classes used in</span></span>        | [<span data-ttu-id="509aa-151">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="509aa-151">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="509aa-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="509aa-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="509aa-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="509aa-153">Entry</span></span> | <span data-ttu-id="509aa-154">Значение</span><span class="sxs-lookup"><span data-stu-id="509aa-154">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="509aa-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="509aa-155">Link-Id</span></span>                | <span data-ttu-id="509aa-156">2103</span><span class="sxs-lookup"><span data-stu-id="509aa-156">2103</span></span>                            |
| <span data-ttu-id="509aa-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="509aa-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="509aa-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="509aa-158">System-Only</span></span>            | <span data-ttu-id="509aa-159">True</span><span class="sxs-lookup"><span data-stu-id="509aa-159">True</span></span>                            |
| <span data-ttu-id="509aa-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="509aa-160">Is-Single-Valued</span></span>       | <span data-ttu-id="509aa-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-161">False</span></span>                           |
| <span data-ttu-id="509aa-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="509aa-162">Is Indexed</span></span>             | <span data-ttu-id="509aa-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-163">False</span></span>                           |
| <span data-ttu-id="509aa-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="509aa-164">In Global Catalog</span></span>      | <span data-ttu-id="509aa-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-165">False</span></span>                           |
| <span data-ttu-id="509aa-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="509aa-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="509aa-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="509aa-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="509aa-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="509aa-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="509aa-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="509aa-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="509aa-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="509aa-170">Search-Flags</span></span>           | <span data-ttu-id="509aa-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="509aa-171">0x00000000</span></span>                      |
| <span data-ttu-id="509aa-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="509aa-172">System-Flags</span></span>           | <span data-ttu-id="509aa-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="509aa-173">0x00000011</span></span>                      |
| <span data-ttu-id="509aa-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="509aa-174">Classes used in</span></span>        | [<span data-ttu-id="509aa-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="509aa-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="509aa-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="509aa-176">Windows Server 2012</span></span>



| <span data-ttu-id="509aa-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="509aa-177">Entry</span></span> | <span data-ttu-id="509aa-178">Значение</span><span class="sxs-lookup"><span data-stu-id="509aa-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="509aa-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="509aa-179">Link-Id</span></span>                | <span data-ttu-id="509aa-180">2103</span><span class="sxs-lookup"><span data-stu-id="509aa-180">2103</span></span>                            |
| <span data-ttu-id="509aa-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="509aa-181">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="509aa-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="509aa-182">System-Only</span></span>            | <span data-ttu-id="509aa-183">True</span><span class="sxs-lookup"><span data-stu-id="509aa-183">True</span></span>                            |
| <span data-ttu-id="509aa-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="509aa-184">Is-Single-Valued</span></span>       | <span data-ttu-id="509aa-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-185">False</span></span>                           |
| <span data-ttu-id="509aa-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="509aa-186">Is Indexed</span></span>             | <span data-ttu-id="509aa-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-187">False</span></span>                           |
| <span data-ttu-id="509aa-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="509aa-188">In Global Catalog</span></span>      | <span data-ttu-id="509aa-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="509aa-189">False</span></span>                           |
| <span data-ttu-id="509aa-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="509aa-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="509aa-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="509aa-191">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="509aa-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="509aa-192">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="509aa-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="509aa-193">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="509aa-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="509aa-194">Search-Flags</span></span>           | <span data-ttu-id="509aa-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="509aa-195">0x00000000</span></span>                      |
| <span data-ttu-id="509aa-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="509aa-196">System-Flags</span></span>           | <span data-ttu-id="509aa-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="509aa-197">0x00000011</span></span>                      |
| <span data-ttu-id="509aa-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="509aa-198">Classes used in</span></span>        | [<span data-ttu-id="509aa-199">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="509aa-199">**Top**</span></span>](c-top.md)<br/> |



 

 





