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
ms.openlocfilehash: 663ee1ff2dac67eff7bd9eca87aa8eacf40436ff
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386853"
---
# <a name="ms-dfs-short-name-link-path-v2-attribute"></a><span data-ttu-id="ad8fe-106">атрибут MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="ad8fe-106">ms-DFS-Short-Name-Link-Path-v2 attribute</span></span>

<span data-ttu-id="ad8fe-107">Короткое имя путь ссылки DFS относительно корневой общей папки DFS (т. е. без компонентов имени сервера/домена и пространства имен DFS).</span><span class="sxs-lookup"><span data-stu-id="ad8fe-107">Short Name DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="ad8fe-108">Используйте косую черту (/) вместо обратных косых черт ( \\ ), чтобы поиск LDAP можно было выполнять без использования escape-символов.</span><span class="sxs-lookup"><span data-stu-id="ad8fe-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="ad8fe-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad8fe-109">Entry</span></span> | <span data-ttu-id="ad8fe-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ad8fe-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="ad8fe-111">CN</span><span class="sxs-lookup"><span data-stu-id="ad8fe-111">CN</span></span>                | <span data-ttu-id="ad8fe-112">MS-DFS-Short-Name-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="ad8fe-112">ms-DFS-Short-Name-Link-Path-v2</span></span>              |
| <span data-ttu-id="ad8fe-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ad8fe-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ad8fe-114">Мсдфс — ShortNameLinkPathv2</span><span class="sxs-lookup"><span data-stu-id="ad8fe-114">msDFS-ShortNameLinkPathv2</span></span>                   |
| <span data-ttu-id="ad8fe-115">Размер</span><span class="sxs-lookup"><span data-stu-id="ad8fe-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="ad8fe-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ad8fe-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="ad8fe-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ad8fe-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="ad8fe-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ad8fe-118">Attribute-Id</span></span>      | <span data-ttu-id="ad8fe-119">1.2.840.113556.1.4.2042</span><span class="sxs-lookup"><span data-stu-id="ad8fe-119">1.2.840.113556.1.4.2042</span></span>                     |
| <span data-ttu-id="ad8fe-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ad8fe-120">System-Id-Guid</span></span>    | <span data-ttu-id="ad8fe-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span><span class="sxs-lookup"><span data-stu-id="ad8fe-121">2d7826f0-4cf7-42e9-a039-1110e0d9ca99</span></span>        |
| <span data-ttu-id="ad8fe-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad8fe-122">Syntax</span></span>            | [<span data-ttu-id="ad8fe-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="ad8fe-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ad8fe-124">Implementations</span></span>

-   [<span data-ttu-id="ad8fe-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ad8fe-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ad8fe-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="ad8fe-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad8fe-128">Windows Server 2008</span></span>



| <span data-ttu-id="ad8fe-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad8fe-129">Entry</span></span> | <span data-ttu-id="ad8fe-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ad8fe-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8fe-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad8fe-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ad8fe-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8fe-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ad8fe-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8fe-133">System-Only</span></span>            | <span data-ttu-id="ad8fe-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad8fe-135">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8fe-136">True</span><span class="sxs-lookup"><span data-stu-id="ad8fe-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="ad8fe-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad8fe-137">Is Indexed</span></span>             | <span data-ttu-id="ad8fe-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad8fe-139">In Global Catalog</span></span>      | <span data-ttu-id="ad8fe-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad8fe-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8fe-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad8fe-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="ad8fe-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8fe-143">Range-Lower</span></span>            | <span data-ttu-id="ad8fe-144">0</span><span class="sxs-lookup"><span data-stu-id="ad8fe-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="ad8fe-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8fe-145">Range-Upper</span></span>            | <span data-ttu-id="ad8fe-146">32766</span><span class="sxs-lookup"><span data-stu-id="ad8fe-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8fe-147">Search-Flags</span></span>           | <span data-ttu-id="ad8fe-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad8fe-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="ad8fe-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8fe-149">System-Flags</span></span>           | <span data-ttu-id="ad8fe-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8fe-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="ad8fe-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad8fe-151">Classes used in</span></span>        | [<span data-ttu-id="ad8fe-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="ad8fe-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ad8fe-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ad8fe-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ad8fe-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad8fe-155">Entry</span></span> | <span data-ttu-id="ad8fe-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ad8fe-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8fe-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad8fe-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ad8fe-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8fe-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ad8fe-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8fe-159">System-Only</span></span>            | <span data-ttu-id="ad8fe-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad8fe-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8fe-162">True</span><span class="sxs-lookup"><span data-stu-id="ad8fe-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="ad8fe-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad8fe-163">Is Indexed</span></span>             | <span data-ttu-id="ad8fe-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad8fe-165">In Global Catalog</span></span>      | <span data-ttu-id="ad8fe-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad8fe-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8fe-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad8fe-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="ad8fe-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8fe-169">Range-Lower</span></span>            | <span data-ttu-id="ad8fe-170">0</span><span class="sxs-lookup"><span data-stu-id="ad8fe-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="ad8fe-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8fe-171">Range-Upper</span></span>            | <span data-ttu-id="ad8fe-172">32766</span><span class="sxs-lookup"><span data-stu-id="ad8fe-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8fe-173">Search-Flags</span></span>           | <span data-ttu-id="ad8fe-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad8fe-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="ad8fe-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8fe-175">System-Flags</span></span>           | <span data-ttu-id="ad8fe-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8fe-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="ad8fe-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad8fe-177">Classes used in</span></span>        | [<span data-ttu-id="ad8fe-178">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="ad8fe-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ad8fe-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad8fe-180">Windows Server 2012</span></span>



| <span data-ttu-id="ad8fe-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="ad8fe-181">Entry</span></span> | <span data-ttu-id="ad8fe-182">Значение</span><span class="sxs-lookup"><span data-stu-id="ad8fe-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8fe-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ad8fe-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ad8fe-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ad8fe-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="ad8fe-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="ad8fe-185">System-Only</span></span>            | <span data-ttu-id="ad8fe-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ad8fe-187">Is-Single-Valued</span></span>       | <span data-ttu-id="ad8fe-188">True</span><span class="sxs-lookup"><span data-stu-id="ad8fe-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="ad8fe-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ad8fe-189">Is Indexed</span></span>             | <span data-ttu-id="ad8fe-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ad8fe-191">In Global Catalog</span></span>      | <span data-ttu-id="ad8fe-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="ad8fe-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ad8fe-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="ad8fe-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ad8fe-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="ad8fe-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ad8fe-195">Range-Lower</span></span>            | <span data-ttu-id="ad8fe-196">0</span><span class="sxs-lookup"><span data-stu-id="ad8fe-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="ad8fe-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ad8fe-197">Range-Upper</span></span>            | <span data-ttu-id="ad8fe-198">32766</span><span class="sxs-lookup"><span data-stu-id="ad8fe-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="ad8fe-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8fe-199">Search-Flags</span></span>           | <span data-ttu-id="ad8fe-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ad8fe-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="ad8fe-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ad8fe-201">System-Flags</span></span>           | <span data-ttu-id="ad8fe-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ad8fe-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="ad8fe-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ad8fe-203">Classes used in</span></span>        | [<span data-ttu-id="ad8fe-204">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="ad8fe-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="ad8fe-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





