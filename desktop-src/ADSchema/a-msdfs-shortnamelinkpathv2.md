---
title: атрибут MS-DFS-Short-Name-Link-Path-v2
description: Короткое имя путь ссылки DFS относительно корневой общей папки DFS (т. е. без компонентов имени сервера/домена и пространства имен DFS). Используйте косую черту (/) вместо обратных косых черт ( \) , чтобы поиск LDAP мог быть выполнен без использования escape-символов.
ms.assetid: 0589d3f5-9734-4f95-bba9-22f13bb1c9f1
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута MS-DFS-Short-Name-Link-Path-v2
- Схема AD атрибута Мсдфс-ShortNameLinkPathv2
topic_type:
- apiref
api_name:
- ms-DFS-Short-Name-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a536abdf13bed7acc99c1036d3c259493994b28
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655485"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="e4e88-106">атрибут MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="e4e88-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="e4e88-107">Короткое имя путь ссылки DFS относительно корневой общей папки DFS (т. е. без компонентов имени сервера/домена и пространства имен DFS).</span><span class="sxs-lookup"><span data-stu-id="e4e88-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="e4e88-108">Используйте косую черту (/) вместо обратных косых черт ( \) , чтобы поиск LDAP мог быть выполнен без использования escape-символов.</span><span class="sxs-lookup"><span data-stu-id="e4e88-108">Use forward slashes (/) instead of backslashes (\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="e4e88-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="e4e88-109">Entry</span></span> | <span data-ttu-id="e4e88-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e88-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e4e88-111">CN</span><span class="sxs-lookup"><span data-stu-id="e4e88-111">CN</span></span>                | <span data-ttu-id="e4e88-112">MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="e4e88-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="e4e88-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e4e88-113">Ldap-Display-Name</span></span> | <span data-ttu-id="e4e88-114">Мсдфс — ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="e4e88-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="e4e88-115">Размер</span><span class="sxs-lookup"><span data-stu-id="e4e88-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="e4e88-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e4e88-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e4e88-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e4e88-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e4e88-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e4e88-118">Attribute-Id</span></span>      | <span data-ttu-id="e4e88-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="e4e88-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="e4e88-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e4e88-120">System-Id-Guid</span></span>    | <span data-ttu-id="e4e88-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="e4e88-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="e4e88-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4e88-122">Syntax</span></span>            | [<span data-ttu-id="e4e88-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e4e88-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e4e88-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e4e88-124">Implementations</span></span>

-   [<span data-ttu-id="e4e88-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e4e88-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e4e88-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e4e88-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e4e88-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="e4e88-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4e88-128">Windows Server 2008</span></span>



| <span data-ttu-id="e4e88-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="e4e88-129">Entry</span></span> | <span data-ttu-id="e4e88-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e88-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e88-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e4e88-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e4e88-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4e88-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e4e88-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4e88-133">System-Only</span></span>            | <span data-ttu-id="e4e88-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e4e88-135">Is-Single-Valued</span></span>       | <span data-ttu-id="e4e88-136">True</span><span class="sxs-lookup"><span data-stu-id="e4e88-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="e4e88-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e4e88-137">Is Indexed</span></span>             | <span data-ttu-id="e4e88-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e4e88-139">In Global Catalog</span></span>      | <span data-ttu-id="e4e88-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e4e88-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4e88-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e4e88-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e4e88-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4e88-143">Range-Lower</span></span>            | <span data-ttu-id="e4e88-144">0</span><span class="sxs-lookup"><span data-stu-id="e4e88-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="e4e88-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4e88-145">Range-Upper</span></span>            | <span data-ttu-id="e4e88-146">32766</span><span class="sxs-lookup"><span data-stu-id="e4e88-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4e88-147">Search-Flags</span></span>           | <span data-ttu-id="e4e88-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4e88-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e4e88-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4e88-149">System-Flags</span></span>           | <span data-ttu-id="e4e88-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4e88-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e4e88-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e4e88-151">Classes used in</span></span>        | [<span data-ttu-id="e4e88-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="e4e88-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e4e88-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e4e88-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e4e88-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e4e88-155">Entry</span></span> | <span data-ttu-id="e4e88-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e88-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e88-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e4e88-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e4e88-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4e88-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e4e88-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4e88-159">System-Only</span></span>            | <span data-ttu-id="e4e88-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e4e88-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e4e88-162">True</span><span class="sxs-lookup"><span data-stu-id="e4e88-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="e4e88-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e4e88-163">Is Indexed</span></span>             | <span data-ttu-id="e4e88-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e4e88-165">In Global Catalog</span></span>      | <span data-ttu-id="e4e88-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e4e88-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4e88-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e4e88-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e4e88-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4e88-169">Range-Lower</span></span>            | <span data-ttu-id="e4e88-170">0</span><span class="sxs-lookup"><span data-stu-id="e4e88-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="e4e88-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4e88-171">Range-Upper</span></span>            | <span data-ttu-id="e4e88-172">32766</span><span class="sxs-lookup"><span data-stu-id="e4e88-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4e88-173">Search-Flags</span></span>           | <span data-ttu-id="e4e88-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4e88-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e4e88-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4e88-175">System-Flags</span></span>           | <span data-ttu-id="e4e88-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4e88-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e4e88-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e4e88-177">Classes used in</span></span>        | [<span data-ttu-id="e4e88-178">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="e4e88-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e4e88-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4e88-180">Windows Server 2012</span></span>



| <span data-ttu-id="e4e88-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="e4e88-181">Entry</span></span> | <span data-ttu-id="e4e88-182">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e88-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e88-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e4e88-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e4e88-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e4e88-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="e4e88-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="e4e88-185">System-Only</span></span>            | <span data-ttu-id="e4e88-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e4e88-187">Is-Single-Valued</span></span>       | <span data-ttu-id="e4e88-188">True</span><span class="sxs-lookup"><span data-stu-id="e4e88-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="e4e88-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e4e88-189">Is Indexed</span></span>             | <span data-ttu-id="e4e88-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e4e88-191">In Global Catalog</span></span>      | <span data-ttu-id="e4e88-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="e4e88-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e4e88-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="e4e88-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e4e88-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="e4e88-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e4e88-195">Range-Lower</span></span>            | <span data-ttu-id="e4e88-196">0</span><span class="sxs-lookup"><span data-stu-id="e4e88-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="e4e88-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e4e88-197">Range-Upper</span></span>            | <span data-ttu-id="e4e88-198">32766</span><span class="sxs-lookup"><span data-stu-id="e4e88-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="e4e88-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e4e88-199">Search-Flags</span></span>           | <span data-ttu-id="e4e88-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e4e88-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="e4e88-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e4e88-201">System-Flags</span></span>           | <span data-ttu-id="e4e88-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e4e88-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="e4e88-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e4e88-203">Classes used in</span></span>        | [<span data-ttu-id="e4e88-204">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="e4e88-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="e4e88-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





