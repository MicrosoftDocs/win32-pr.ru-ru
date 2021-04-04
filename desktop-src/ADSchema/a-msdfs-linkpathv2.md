---
title: атрибут MS-DFS-Link-Path-v2
description: Путь ссылки DFS относительно корневой общей папки DFS (то есть без компонентов имени сервера/домена и пространства имен DFS). Используйте косую черту (/) вместо обратных косых черт ( \) , чтобы поиск LDAP мог быть выполнен без использования escape-символов.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-DFS-Link-Path-v2
- Схема AD атрибута Мсдфс-LinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138998"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="5b6f5-106">атрибут MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="5b6f5-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="5b6f5-107">Путь ссылки DFS относительно корневой общей папки DFS (то есть без компонентов имени сервера/домена и пространства имен DFS).</span><span class="sxs-lookup"><span data-stu-id="5b6f5-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="5b6f5-108">Используйте косую черту (/) вместо обратных косых черт ( \) , чтобы поиск LDAP мог быть выполнен без использования escape-символов.</span><span class="sxs-lookup"><span data-stu-id="5b6f5-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="5b6f5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b6f5-109">Entry</span></span> | <span data-ttu-id="5b6f5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5b6f5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5b6f5-111">CN</span><span class="sxs-lookup"><span data-stu-id="5b6f5-111">CN</span></span>                | <span data-ttu-id="5b6f5-112">MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="5b6f5-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="5b6f5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5b6f5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="5b6f5-114">Мсдфс — LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="5b6f5-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="5b6f5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="5b6f5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="5b6f5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5b6f5-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5b6f5-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5b6f5-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5b6f5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5b6f5-118">Attribute-Id</span></span>      | <span data-ttu-id="5b6f5-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="5b6f5-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="5b6f5-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5b6f5-120">System-Id-Guid</span></span>    | <span data-ttu-id="5b6f5-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="5b6f5-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="5b6f5-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b6f5-122">Syntax</span></span>            | [<span data-ttu-id="5b6f5-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5b6f5-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5b6f5-124">Implementations</span></span>

-   [<span data-ttu-id="5b6f5-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5b6f5-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5b6f5-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="5b6f5-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b6f5-128">Windows Server 2008</span></span>



| <span data-ttu-id="5b6f5-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b6f5-129">Entry</span></span> | <span data-ttu-id="5b6f5-130">Значение</span><span class="sxs-lookup"><span data-stu-id="5b6f5-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f5-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b6f5-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5b6f5-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b6f5-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5b6f5-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b6f5-133">System-Only</span></span>            | <span data-ttu-id="5b6f5-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b6f5-135">Is-Single-Valued</span></span>       | <span data-ttu-id="5b6f5-136">True</span><span class="sxs-lookup"><span data-stu-id="5b6f5-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="5b6f5-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b6f5-137">Is Indexed</span></span>             | <span data-ttu-id="5b6f5-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b6f5-139">In Global Catalog</span></span>      | <span data-ttu-id="5b6f5-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b6f5-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b6f5-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b6f5-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5b6f5-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b6f5-143">Range-Lower</span></span>            | <span data-ttu-id="5b6f5-144">0</span><span class="sxs-lookup"><span data-stu-id="5b6f5-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="5b6f5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b6f5-145">Range-Upper</span></span>            | <span data-ttu-id="5b6f5-146">32766</span><span class="sxs-lookup"><span data-stu-id="5b6f5-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b6f5-147">Search-Flags</span></span>           | <span data-ttu-id="5b6f5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b6f5-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5b6f5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b6f5-149">System-Flags</span></span>           | <span data-ttu-id="5b6f5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b6f5-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5b6f5-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b6f5-151">Classes used in</span></span>        | [<span data-ttu-id="5b6f5-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5b6f5-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5b6f5-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b6f5-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5b6f5-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b6f5-155">Entry</span></span> | <span data-ttu-id="5b6f5-156">Значение</span><span class="sxs-lookup"><span data-stu-id="5b6f5-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f5-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b6f5-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5b6f5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b6f5-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5b6f5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b6f5-159">System-Only</span></span>            | <span data-ttu-id="5b6f5-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b6f5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="5b6f5-162">True</span><span class="sxs-lookup"><span data-stu-id="5b6f5-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="5b6f5-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b6f5-163">Is Indexed</span></span>             | <span data-ttu-id="5b6f5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b6f5-165">In Global Catalog</span></span>      | <span data-ttu-id="5b6f5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b6f5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b6f5-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b6f5-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5b6f5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b6f5-169">Range-Lower</span></span>            | <span data-ttu-id="5b6f5-170">0</span><span class="sxs-lookup"><span data-stu-id="5b6f5-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="5b6f5-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b6f5-171">Range-Upper</span></span>            | <span data-ttu-id="5b6f5-172">32766</span><span class="sxs-lookup"><span data-stu-id="5b6f5-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b6f5-173">Search-Flags</span></span>           | <span data-ttu-id="5b6f5-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b6f5-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5b6f5-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b6f5-175">System-Flags</span></span>           | <span data-ttu-id="5b6f5-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b6f5-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5b6f5-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b6f5-177">Classes used in</span></span>        | [<span data-ttu-id="5b6f5-178">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5b6f5-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5b6f5-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b6f5-180">Windows Server 2012</span></span>



| <span data-ttu-id="5b6f5-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b6f5-181">Entry</span></span> | <span data-ttu-id="5b6f5-182">Значение</span><span class="sxs-lookup"><span data-stu-id="5b6f5-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6f5-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b6f5-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5b6f5-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b6f5-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="5b6f5-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b6f5-185">System-Only</span></span>            | <span data-ttu-id="5b6f5-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b6f5-187">Is-Single-Valued</span></span>       | <span data-ttu-id="5b6f5-188">True</span><span class="sxs-lookup"><span data-stu-id="5b6f5-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="5b6f5-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b6f5-189">Is Indexed</span></span>             | <span data-ttu-id="5b6f5-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b6f5-191">In Global Catalog</span></span>      | <span data-ttu-id="5b6f5-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b6f5-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b6f5-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b6f5-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b6f5-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="5b6f5-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b6f5-195">Range-Lower</span></span>            | <span data-ttu-id="5b6f5-196">0</span><span class="sxs-lookup"><span data-stu-id="5b6f5-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="5b6f5-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b6f5-197">Range-Upper</span></span>            | <span data-ttu-id="5b6f5-198">32766</span><span class="sxs-lookup"><span data-stu-id="5b6f5-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="5b6f5-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b6f5-199">Search-Flags</span></span>           | <span data-ttu-id="5b6f5-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b6f5-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="5b6f5-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b6f5-201">System-Flags</span></span>           | <span data-ttu-id="5b6f5-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b6f5-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="5b6f5-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b6f5-203">Classes used in</span></span>        | [<span data-ttu-id="5b6f5-204">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="5b6f5-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="5b6f5-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





