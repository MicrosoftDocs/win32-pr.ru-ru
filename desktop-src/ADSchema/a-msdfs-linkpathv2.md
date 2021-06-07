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
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386863"
---
# <a name="ms-dfs-link-path-v2-attribute"></a><span data-ttu-id="dbc3f-106">атрибут MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="dbc3f-106">ms-DFS-Link-Path-v2 attribute</span></span>

<span data-ttu-id="dbc3f-107">Путь ссылки DFS относительно корневой общей папки DFS (то есть без компонентов имени сервера/домена и пространства имен DFS).</span><span class="sxs-lookup"><span data-stu-id="dbc3f-107">DFS link path relative to the DFS root target share (that is, without the server/domain and DFS namespace name components).</span></span> <span data-ttu-id="dbc3f-108">Используйте косую черту (/) вместо обратных косых черт ( \\ ), чтобы поиск LDAP можно было выполнять без использования escape-символов.</span><span class="sxs-lookup"><span data-stu-id="dbc3f-108">Use forward slashes (/) instead of backslashes (\\), so that LDAP searches can be done without having to use escapes.</span></span>



| <span data-ttu-id="dbc3f-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="dbc3f-109">Entry</span></span> | <span data-ttu-id="dbc3f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc3f-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="dbc3f-111">CN</span><span class="sxs-lookup"><span data-stu-id="dbc3f-111">CN</span></span>                | <span data-ttu-id="dbc3f-112">MS-DFS-Link-Path-v2</span><span class="sxs-lookup"><span data-stu-id="dbc3f-112">ms-DFS-Link-Path-v2</span></span>                         |
| <span data-ttu-id="dbc3f-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="dbc3f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="dbc3f-114">Мсдфс — LinkPathv2</span><span class="sxs-lookup"><span data-stu-id="dbc3f-114">msDFS-LinkPathv2</span></span>                            |
| <span data-ttu-id="dbc3f-115">Размер</span><span class="sxs-lookup"><span data-stu-id="dbc3f-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="dbc3f-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="dbc3f-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="dbc3f-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="dbc3f-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="dbc3f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dbc3f-118">Attribute-Id</span></span>      | <span data-ttu-id="dbc3f-119">1.2.840.113556.1.4.2039</span><span class="sxs-lookup"><span data-stu-id="dbc3f-119">1.2.840.113556.1.4.2039</span></span>                     |
| <span data-ttu-id="dbc3f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="dbc3f-120">System-Id-Guid</span></span>    | <span data-ttu-id="dbc3f-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span><span class="sxs-lookup"><span data-stu-id="dbc3f-121">86b021f6-10ab-40a2-a252-1dc0cc3be6a9</span></span>        |
| <span data-ttu-id="dbc3f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbc3f-122">Syntax</span></span>            | [<span data-ttu-id="dbc3f-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="dbc3f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="dbc3f-124">Implementations</span></span>

-   [<span data-ttu-id="dbc3f-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dbc3f-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dbc3f-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="dbc3f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbc3f-128">Windows Server 2008</span></span>



| <span data-ttu-id="dbc3f-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="dbc3f-129">Entry</span></span> | <span data-ttu-id="dbc3f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc3f-130">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc3f-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dbc3f-131">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dbc3f-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbc3f-132">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dbc3f-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbc3f-133">System-Only</span></span>            | <span data-ttu-id="dbc3f-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-134">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dbc3f-135">Is-Single-Valued</span></span>       | <span data-ttu-id="dbc3f-136">True</span><span class="sxs-lookup"><span data-stu-id="dbc3f-136">True</span></span>                                                                                                                   |
| <span data-ttu-id="dbc3f-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dbc3f-137">Is Indexed</span></span>             | <span data-ttu-id="dbc3f-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-138">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dbc3f-139">In Global Catalog</span></span>      | <span data-ttu-id="dbc3f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-140">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dbc3f-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbc3f-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dbc3f-142">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="dbc3f-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbc3f-143">Range-Lower</span></span>            | <span data-ttu-id="dbc3f-144">0</span><span class="sxs-lookup"><span data-stu-id="dbc3f-144">0</span></span>                                                                                                                      |
| <span data-ttu-id="dbc3f-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbc3f-145">Range-Upper</span></span>            | <span data-ttu-id="dbc3f-146">32766</span><span class="sxs-lookup"><span data-stu-id="dbc3f-146">32766</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbc3f-147">Search-Flags</span></span>           | <span data-ttu-id="dbc3f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbc3f-148">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="dbc3f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbc3f-149">System-Flags</span></span>           | <span data-ttu-id="dbc3f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbc3f-150">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="dbc3f-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dbc3f-151">Classes used in</span></span>        | [<span data-ttu-id="dbc3f-152">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-152">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="dbc3f-153">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-153">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dbc3f-154">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbc3f-154">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dbc3f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="dbc3f-155">Entry</span></span> | <span data-ttu-id="dbc3f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc3f-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc3f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dbc3f-157">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dbc3f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbc3f-158">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dbc3f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbc3f-159">System-Only</span></span>            | <span data-ttu-id="dbc3f-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-160">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dbc3f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="dbc3f-162">True</span><span class="sxs-lookup"><span data-stu-id="dbc3f-162">True</span></span>                                                                                                                   |
| <span data-ttu-id="dbc3f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dbc3f-163">Is Indexed</span></span>             | <span data-ttu-id="dbc3f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-164">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dbc3f-165">In Global Catalog</span></span>      | <span data-ttu-id="dbc3f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dbc3f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbc3f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dbc3f-168">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="dbc3f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbc3f-169">Range-Lower</span></span>            | <span data-ttu-id="dbc3f-170">0</span><span class="sxs-lookup"><span data-stu-id="dbc3f-170">0</span></span>                                                                                                                      |
| <span data-ttu-id="dbc3f-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbc3f-171">Range-Upper</span></span>            | <span data-ttu-id="dbc3f-172">32766</span><span class="sxs-lookup"><span data-stu-id="dbc3f-172">32766</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbc3f-173">Search-Flags</span></span>           | <span data-ttu-id="dbc3f-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbc3f-174">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="dbc3f-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbc3f-175">System-Flags</span></span>           | <span data-ttu-id="dbc3f-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbc3f-176">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="dbc3f-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dbc3f-177">Classes used in</span></span>        | [<span data-ttu-id="dbc3f-178">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-178">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="dbc3f-179">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-179">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dbc3f-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dbc3f-180">Windows Server 2012</span></span>



| <span data-ttu-id="dbc3f-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="dbc3f-181">Entry</span></span> | <span data-ttu-id="dbc3f-182">Значение</span><span class="sxs-lookup"><span data-stu-id="dbc3f-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc3f-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dbc3f-183">Link-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dbc3f-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dbc3f-184">MAPI-Id</span></span>                | \-                                                                                                                     |
| <span data-ttu-id="dbc3f-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="dbc3f-185">System-Only</span></span>            | <span data-ttu-id="dbc3f-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-186">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dbc3f-187">Is-Single-Valued</span></span>       | <span data-ttu-id="dbc3f-188">True</span><span class="sxs-lookup"><span data-stu-id="dbc3f-188">True</span></span>                                                                                                                   |
| <span data-ttu-id="dbc3f-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dbc3f-189">Is Indexed</span></span>             | <span data-ttu-id="dbc3f-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-190">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dbc3f-191">In Global Catalog</span></span>      | <span data-ttu-id="dbc3f-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="dbc3f-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dbc3f-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="dbc3f-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dbc3f-194">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="dbc3f-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dbc3f-195">Range-Lower</span></span>            | <span data-ttu-id="dbc3f-196">0</span><span class="sxs-lookup"><span data-stu-id="dbc3f-196">0</span></span>                                                                                                                      |
| <span data-ttu-id="dbc3f-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dbc3f-197">Range-Upper</span></span>            | <span data-ttu-id="dbc3f-198">32766</span><span class="sxs-lookup"><span data-stu-id="dbc3f-198">32766</span></span>                                                                                                                  |
| <span data-ttu-id="dbc3f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dbc3f-199">Search-Flags</span></span>           | <span data-ttu-id="dbc3f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dbc3f-200">0x00000000</span></span>                                                                                                             |
| <span data-ttu-id="dbc3f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dbc3f-201">System-Flags</span></span>           | <span data-ttu-id="dbc3f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="dbc3f-202">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="dbc3f-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dbc3f-203">Classes used in</span></span>        | [<span data-ttu-id="dbc3f-204">**MS-DFS-Deleted-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-204">**ms-DFS-Deleted-Link-v2**</span></span>](c-msdfs-deletedlinkv2.md)<br/> [<span data-ttu-id="dbc3f-205">**MS-DFS-Link-v2**</span><span class="sxs-lookup"><span data-stu-id="dbc3f-205">**ms-DFS-Link-v2**</span></span>](c-msdfs-linkv2.md)<br/> |



 

 





