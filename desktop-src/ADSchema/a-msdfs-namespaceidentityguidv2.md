---
title: атрибут MS-DFS-Namespace-Identity-GUID-v2
description: Задается только при создании пространства имен. Стабильны при переименовании или перемещении, пока пространство имен не заменяется другим пространством имен с таким же именем.
ms.assetid: 66907d40-48a7-40ae-9031-1366a4a4d2a2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-DFS-Namespace-Identity-GUID-v2
- Схема AD атрибута Мсдфс-NamespaceIdentityGUIDv2
topic_type:
- apiref
api_name:
- ms-DFS-Namespace-Identity-GUID-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be75ccaa0a8d607502d4709afdf313f0ddfce99
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893886"
---
# <a name="ms-dfs-namespace-identity-guid-v2-attribute"></a><span data-ttu-id="478d3-106">атрибут MS-DFS-Namespace-Identity-GUID-v2</span><span class="sxs-lookup"><span data-stu-id="478d3-106">ms-DFS-Namespace-Identity-GUID-v2 attribute</span></span>

<span data-ttu-id="478d3-107">Задается только при создании пространства имен.</span><span class="sxs-lookup"><span data-stu-id="478d3-107">To be set only when the namespace is created.</span></span> <span data-ttu-id="478d3-108">Стабильны при переименовании или перемещении, пока пространство имен не заменяется другим пространством имен с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="478d3-108">Stable across rename or move as long as the namespace is not replaced by another namespace that has same name.</span></span>



| <span data-ttu-id="478d3-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="478d3-109">Entry</span></span> | <span data-ttu-id="478d3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="478d3-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="478d3-111">CN</span><span class="sxs-lookup"><span data-stu-id="478d3-111">CN</span></span>                | <span data-ttu-id="478d3-112">MS-DFS-Namespace-Identity-GUID-v2</span><span class="sxs-lookup"><span data-stu-id="478d3-112">ms-DFS-Namespace-Identity-GUID-v2</span></span>                     |
| <span data-ttu-id="478d3-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="478d3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="478d3-114">Мсдфс — NamespaceIdentityGUIDv2</span><span class="sxs-lookup"><span data-stu-id="478d3-114">msDFS-NamespaceIdentityGUIDv2</span></span>                         |
| <span data-ttu-id="478d3-115">Размер</span><span class="sxs-lookup"><span data-stu-id="478d3-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="478d3-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="478d3-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="478d3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="478d3-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="478d3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="478d3-118">Attribute-Id</span></span>      | <span data-ttu-id="478d3-119">1.2.840.113556.1.4.2033</span><span class="sxs-lookup"><span data-stu-id="478d3-119">1.2.840.113556.1.4.2033</span></span>                               |
| <span data-ttu-id="478d3-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="478d3-120">System-Id-Guid</span></span>    | <span data-ttu-id="478d3-121">200432ce-ec5f-4931-A525-d7f4afe34e68</span><span class="sxs-lookup"><span data-stu-id="478d3-121">200432ce-ec5f-4931-a525-d7f4afe34e68</span></span>                  |
| <span data-ttu-id="478d3-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="478d3-122">Syntax</span></span>            | [<span data-ttu-id="478d3-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="478d3-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="478d3-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="478d3-124">Implementations</span></span>

-   [<span data-ttu-id="478d3-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="478d3-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="478d3-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="478d3-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="478d3-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="478d3-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="478d3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="478d3-128">Windows Server 2008</span></span>



| <span data-ttu-id="478d3-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="478d3-129">Entry</span></span> | <span data-ttu-id="478d3-130">Значение</span><span class="sxs-lookup"><span data-stu-id="478d3-130">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478d3-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="478d3-131">Link-Id</span></span>                | \-                                                                                                                                                                                   |
| <span data-ttu-id="478d3-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="478d3-132">MAPI-Id</span></span>                | \-                                                                                                                                                                                   |
| <span data-ttu-id="478d3-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="478d3-133">System-Only</span></span>            | <span data-ttu-id="478d3-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-134">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="478d3-135">Is-Single-Valued</span></span>       | <span data-ttu-id="478d3-136">True</span><span class="sxs-lookup"><span data-stu-id="478d3-136">True</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="478d3-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="478d3-137">Is Indexed</span></span>             | <span data-ttu-id="478d3-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-138">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="478d3-139">In Global Catalog</span></span>      | <span data-ttu-id="478d3-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-140">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="478d3-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="478d3-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="478d3-142">O:BAG:BAD:S:</span></span>                                                                                                                                                                         |
| <span data-ttu-id="478d3-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="478d3-143">Range-Lower</span></span>            | <span data-ttu-id="478d3-144">16</span><span class="sxs-lookup"><span data-stu-id="478d3-144">16</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="478d3-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="478d3-145">Range-Upper</span></span>            | <span data-ttu-id="478d3-146">16</span><span class="sxs-lookup"><span data-stu-id="478d3-146">16</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="478d3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="478d3-147">Search-Flags</span></span>           | <span data-ttu-id="478d3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="478d3-148">0x00000000</span></span>                                                                                                                                                                           |
| <span data-ttu-id="478d3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="478d3-149">System-Flags</span></span>           | <span data-ttu-id="478d3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="478d3-150">0x00000010</span></span>                                                                                                                                                                           |
| <span data-ttu-id="478d3-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="478d3-151">Classes used in</span></span>        | [<span data-ttu-id="478d3-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="478d3-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> [<span data-ttu-id="478d3-154">**MS-DFS-Namespace-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-154">**ms-DFS-Namespace-v2**</span></span>](c-msdfs-namespacev2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="478d3-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="478d3-155">Windows Server 2008 R2</span></span>



| <span data-ttu-id="478d3-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="478d3-156">Entry</span></span> | <span data-ttu-id="478d3-157">Значение</span><span class="sxs-lookup"><span data-stu-id="478d3-157">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478d3-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="478d3-158">Link-Id</span></span>                | \-                                                                                                                                                                                   |
| <span data-ttu-id="478d3-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="478d3-159">MAPI-Id</span></span>                | \-                                                                                                                                                                                   |
| <span data-ttu-id="478d3-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="478d3-160">System-Only</span></span>            | <span data-ttu-id="478d3-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-161">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="478d3-162">Is-Single-Valued</span></span>       | <span data-ttu-id="478d3-163">True</span><span class="sxs-lookup"><span data-stu-id="478d3-163">True</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="478d3-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="478d3-164">Is Indexed</span></span>             | <span data-ttu-id="478d3-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-165">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="478d3-166">In Global Catalog</span></span>      | <span data-ttu-id="478d3-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-167">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="478d3-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="478d3-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="478d3-169">O:BAG:BAD:S:</span></span>                                                                                                                                                                         |
| <span data-ttu-id="478d3-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="478d3-170">Range-Lower</span></span>            | <span data-ttu-id="478d3-171">16</span><span class="sxs-lookup"><span data-stu-id="478d3-171">16</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="478d3-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="478d3-172">Range-Upper</span></span>            | <span data-ttu-id="478d3-173">16</span><span class="sxs-lookup"><span data-stu-id="478d3-173">16</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="478d3-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="478d3-174">Search-Flags</span></span>           | <span data-ttu-id="478d3-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="478d3-175">0x00000000</span></span>                                                                                                                                                                           |
| <span data-ttu-id="478d3-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="478d3-176">System-Flags</span></span>           | <span data-ttu-id="478d3-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="478d3-177">0x00000010</span></span>                                                                                                                                                                           |
| <span data-ttu-id="478d3-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="478d3-178">Classes used in</span></span>        | [<span data-ttu-id="478d3-179">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-179">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="478d3-180">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-180">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> [<span data-ttu-id="478d3-181">**MS-DFS-Namespace-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-181">**ms-DFS-Namespace-v2**</span></span>](c-msdfs-namespacev2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="478d3-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="478d3-182">Windows Server 2012</span></span>



| <span data-ttu-id="478d3-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="478d3-183">Entry</span></span> | <span data-ttu-id="478d3-184">Значение</span><span class="sxs-lookup"><span data-stu-id="478d3-184">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478d3-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="478d3-185">Link-Id</span></span>                | \-                                                                                                                                                                                   |
| <span data-ttu-id="478d3-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="478d3-186">MAPI-Id</span></span>                | \-                                                                                                                                                                                   |
| <span data-ttu-id="478d3-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="478d3-187">System-Only</span></span>            | <span data-ttu-id="478d3-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-188">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="478d3-189">Is-Single-Valued</span></span>       | <span data-ttu-id="478d3-190">True</span><span class="sxs-lookup"><span data-stu-id="478d3-190">True</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="478d3-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="478d3-191">Is Indexed</span></span>             | <span data-ttu-id="478d3-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-192">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="478d3-193">In Global Catalog</span></span>      | <span data-ttu-id="478d3-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="478d3-194">False</span></span>                                                                                                                                                                                |
| <span data-ttu-id="478d3-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="478d3-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="478d3-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="478d3-196">O:BAG:BAD:S:</span></span>                                                                                                                                                                         |
| <span data-ttu-id="478d3-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="478d3-197">Range-Lower</span></span>            | <span data-ttu-id="478d3-198">16</span><span class="sxs-lookup"><span data-stu-id="478d3-198">16</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="478d3-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="478d3-199">Range-Upper</span></span>            | <span data-ttu-id="478d3-200">16</span><span class="sxs-lookup"><span data-stu-id="478d3-200">16</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="478d3-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="478d3-201">Search-Flags</span></span>           | <span data-ttu-id="478d3-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="478d3-202">0x00000000</span></span>                                                                                                                                                                           |
| <span data-ttu-id="478d3-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="478d3-203">System-Flags</span></span>           | <span data-ttu-id="478d3-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="478d3-204">0x00000010</span></span>                                                                                                                                                                           |
| <span data-ttu-id="478d3-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="478d3-205">Classes used in</span></span>        | [<span data-ttu-id="478d3-206">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-206">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="478d3-207">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-207">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> [<span data-ttu-id="478d3-208">**MS-DFS-Namespace-v2**</span><span class="sxs-lookup"><span data-stu-id="478d3-208">**ms-DFS-Namespace-v2**</span></span>](c-msdfs-namespacev2.md)<br/> |



 

 





