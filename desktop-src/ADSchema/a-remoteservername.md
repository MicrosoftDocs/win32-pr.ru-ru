---
title: Атрибут Remote-Server-Name
description: Используется везде, где необходимо хранить одно или несколько имен компьютеров.
ms.assetid: d09fe925-2137-478d-8630-5220fadedeab
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Remote-Server-Name
- Схема AD атрибута Ремотесервернаме
topic_type:
- apiref
api_name:
- Remote-Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02362c7ef3ba485795a2f27005a8fa2a793f004b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989505"
---
# <a name="remote-server-name-attribute"></a><span data-ttu-id="5b7c6-105">Атрибут Remote-Server-Name</span><span class="sxs-lookup"><span data-stu-id="5b7c6-105">Remote-Server-Name attribute</span></span>

<span data-ttu-id="5b7c6-106">Используется везде, где необходимо хранить одно или несколько имен компьютеров.</span><span class="sxs-lookup"><span data-stu-id="5b7c6-106">Used wherever one or more computer names must be stored.</span></span>



| <span data-ttu-id="5b7c6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-107">Entry</span></span> | <span data-ttu-id="5b7c6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="5b7c6-109">CN</span><span class="sxs-lookup"><span data-stu-id="5b7c6-109">CN</span></span>                | <span data-ttu-id="5b7c6-110">Имя удаленного сервера</span><span class="sxs-lookup"><span data-stu-id="5b7c6-110">Remote-Server-Name</span></span>                          |
| <span data-ttu-id="5b7c6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5b7c6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5b7c6-112">ремотесервернаме</span><span class="sxs-lookup"><span data-stu-id="5b7c6-112">remoteServerName</span></span>                            |
| <span data-ttu-id="5b7c6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5b7c6-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="5b7c6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5b7c6-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="5b7c6-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5b7c6-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="5b7c6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-116">Attribute-Id</span></span>      | <span data-ttu-id="5b7c6-117">1.2.840.113556.1.4.105</span><span class="sxs-lookup"><span data-stu-id="5b7c6-117">1.2.840.113556.1.4.105</span></span>                      |
| <span data-ttu-id="5b7c6-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5b7c6-118">System-Id-Guid</span></span>    | <span data-ttu-id="5b7c6-119">bf967a12-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="5b7c6-119">bf967a12-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="5b7c6-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b7c6-120">Syntax</span></span>            | [<span data-ttu-id="5b7c6-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="5b7c6-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5b7c6-122">Implementations</span></span>

-   [<span data-ttu-id="5b7c6-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5b7c6-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5b7c6-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5b7c6-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5b7c6-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5b7c6-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5b7c6-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b7c6-129">Windows 2000 Server</span></span>



| <span data-ttu-id="5b7c6-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-130">Entry</span></span> | <span data-ttu-id="5b7c6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-131">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="5b7c6-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b7c6-132">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-133">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7c6-134">System-Only</span></span>            | <span data-ttu-id="5b7c6-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-135">False</span></span>                                |
| <span data-ttu-id="5b7c6-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b7c6-136">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7c6-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-137">False</span></span>                                |
| <span data-ttu-id="5b7c6-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b7c6-138">Is Indexed</span></span>             | <span data-ttu-id="5b7c6-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-139">False</span></span>                                |
| <span data-ttu-id="5b7c6-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b7c6-140">In Global Catalog</span></span>      | <span data-ttu-id="5b7c6-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-141">False</span></span>                                |
| <span data-ttu-id="5b7c6-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b7c6-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7c6-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b7c6-143">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="5b7c6-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7c6-144">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7c6-145">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-146">Search-Flags</span></span>           | <span data-ttu-id="5b7c6-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7c6-147">0x00000000</span></span>                           |
| <span data-ttu-id="5b7c6-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-148">System-Flags</span></span>           | <span data-ttu-id="5b7c6-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b7c6-149">0x00000010</span></span>                           |
| <span data-ttu-id="5b7c6-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b7c6-150">Classes used in</span></span>        | [<span data-ttu-id="5b7c6-151">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-151">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5b7c6-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5b7c6-152">Windows Server 2003</span></span>



| <span data-ttu-id="5b7c6-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-153">Entry</span></span> | <span data-ttu-id="5b7c6-154">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-154">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="5b7c6-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b7c6-155">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-156">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7c6-157">System-Only</span></span>            | <span data-ttu-id="5b7c6-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-158">False</span></span>                                |
| <span data-ttu-id="5b7c6-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b7c6-159">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7c6-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-160">False</span></span>                                |
| <span data-ttu-id="5b7c6-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b7c6-161">Is Indexed</span></span>             | <span data-ttu-id="5b7c6-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-162">False</span></span>                                |
| <span data-ttu-id="5b7c6-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b7c6-163">In Global Catalog</span></span>      | <span data-ttu-id="5b7c6-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-164">False</span></span>                                |
| <span data-ttu-id="5b7c6-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b7c6-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7c6-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b7c6-166">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="5b7c6-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7c6-167">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7c6-168">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-169">Search-Flags</span></span>           | <span data-ttu-id="5b7c6-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7c6-170">0x00000000</span></span>                           |
| <span data-ttu-id="5b7c6-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-171">System-Flags</span></span>           | <span data-ttu-id="5b7c6-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b7c6-172">0x00000010</span></span>                           |
| <span data-ttu-id="5b7c6-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b7c6-173">Classes used in</span></span>        | [<span data-ttu-id="5b7c6-174">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-174">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5b7c6-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5b7c6-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5b7c6-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-176">Entry</span></span> | <span data-ttu-id="5b7c6-177">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-177">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="5b7c6-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b7c6-178">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-179">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7c6-180">System-Only</span></span>            | <span data-ttu-id="5b7c6-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-181">False</span></span>                                |
| <span data-ttu-id="5b7c6-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b7c6-182">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7c6-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-183">False</span></span>                                |
| <span data-ttu-id="5b7c6-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b7c6-184">Is Indexed</span></span>             | <span data-ttu-id="5b7c6-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-185">False</span></span>                                |
| <span data-ttu-id="5b7c6-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b7c6-186">In Global Catalog</span></span>      | <span data-ttu-id="5b7c6-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-187">False</span></span>                                |
| <span data-ttu-id="5b7c6-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b7c6-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7c6-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b7c6-189">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="5b7c6-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7c6-190">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7c6-191">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-192">Search-Flags</span></span>           | <span data-ttu-id="5b7c6-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7c6-193">0x00000000</span></span>                           |
| <span data-ttu-id="5b7c6-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-194">System-Flags</span></span>           | <span data-ttu-id="5b7c6-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b7c6-195">0x00000010</span></span>                           |
| <span data-ttu-id="5b7c6-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b7c6-196">Classes used in</span></span>        | [<span data-ttu-id="5b7c6-197">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-197">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5b7c6-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b7c6-198">Windows Server 2008</span></span>



| <span data-ttu-id="5b7c6-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-199">Entry</span></span> | <span data-ttu-id="5b7c6-200">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-200">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="5b7c6-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b7c6-201">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-202">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7c6-203">System-Only</span></span>            | <span data-ttu-id="5b7c6-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-204">False</span></span>                                |
| <span data-ttu-id="5b7c6-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b7c6-205">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7c6-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-206">False</span></span>                                |
| <span data-ttu-id="5b7c6-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b7c6-207">Is Indexed</span></span>             | <span data-ttu-id="5b7c6-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-208">False</span></span>                                |
| <span data-ttu-id="5b7c6-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b7c6-209">In Global Catalog</span></span>      | <span data-ttu-id="5b7c6-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-210">False</span></span>                                |
| <span data-ttu-id="5b7c6-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b7c6-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7c6-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b7c6-212">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="5b7c6-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7c6-213">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7c6-214">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-215">Search-Flags</span></span>           | <span data-ttu-id="5b7c6-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7c6-216">0x00000000</span></span>                           |
| <span data-ttu-id="5b7c6-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-217">System-Flags</span></span>           | <span data-ttu-id="5b7c6-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b7c6-218">0x00000010</span></span>                           |
| <span data-ttu-id="5b7c6-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b7c6-219">Classes used in</span></span>        | [<span data-ttu-id="5b7c6-220">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-220">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5b7c6-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b7c6-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5b7c6-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-222">Entry</span></span> | <span data-ttu-id="5b7c6-223">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-223">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="5b7c6-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b7c6-224">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-225">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7c6-226">System-Only</span></span>            | <span data-ttu-id="5b7c6-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-227">False</span></span>                                |
| <span data-ttu-id="5b7c6-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b7c6-228">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7c6-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-229">False</span></span>                                |
| <span data-ttu-id="5b7c6-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b7c6-230">Is Indexed</span></span>             | <span data-ttu-id="5b7c6-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-231">False</span></span>                                |
| <span data-ttu-id="5b7c6-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b7c6-232">In Global Catalog</span></span>      | <span data-ttu-id="5b7c6-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-233">False</span></span>                                |
| <span data-ttu-id="5b7c6-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b7c6-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7c6-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b7c6-235">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="5b7c6-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7c6-236">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7c6-237">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-238">Search-Flags</span></span>           | <span data-ttu-id="5b7c6-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7c6-239">0x00000000</span></span>                           |
| <span data-ttu-id="5b7c6-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-240">System-Flags</span></span>           | <span data-ttu-id="5b7c6-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b7c6-241">0x00000010</span></span>                           |
| <span data-ttu-id="5b7c6-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b7c6-242">Classes used in</span></span>        | [<span data-ttu-id="5b7c6-243">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-243">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5b7c6-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b7c6-244">Windows Server 2012</span></span>



| <span data-ttu-id="5b7c6-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b7c6-245">Entry</span></span> | <span data-ttu-id="5b7c6-246">Значение</span><span class="sxs-lookup"><span data-stu-id="5b7c6-246">Value</span></span> |
|------------------------|--------------------------------------|
| <span data-ttu-id="5b7c6-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b7c6-247">Link-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b7c6-248">MAPI-Id</span></span>                | \-                                   |
| <span data-ttu-id="5b7c6-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b7c6-249">System-Only</span></span>            | <span data-ttu-id="5b7c6-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-250">False</span></span>                                |
| <span data-ttu-id="5b7c6-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b7c6-251">Is-Single-Valued</span></span>       | <span data-ttu-id="5b7c6-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-252">False</span></span>                                |
| <span data-ttu-id="5b7c6-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b7c6-253">Is Indexed</span></span>             | <span data-ttu-id="5b7c6-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-254">False</span></span>                                |
| <span data-ttu-id="5b7c6-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b7c6-255">In Global Catalog</span></span>      | <span data-ttu-id="5b7c6-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b7c6-256">False</span></span>                                |
| <span data-ttu-id="5b7c6-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b7c6-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b7c6-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b7c6-258">O:BAG:BAD:S:</span></span>                         |
| <span data-ttu-id="5b7c6-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b7c6-259">Range-Lower</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b7c6-260">Range-Upper</span></span>            | \-                                   |
| <span data-ttu-id="5b7c6-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-261">Search-Flags</span></span>           | <span data-ttu-id="5b7c6-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b7c6-262">0x00000000</span></span>                           |
| <span data-ttu-id="5b7c6-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b7c6-263">System-Flags</span></span>           | <span data-ttu-id="5b7c6-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b7c6-264">0x00000010</span></span>                           |
| <span data-ttu-id="5b7c6-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b7c6-265">Classes used in</span></span>        | [<span data-ttu-id="5b7c6-266">**FT-DFS**</span><span class="sxs-lookup"><span data-stu-id="5b7c6-266">**FT-Dfs**</span></span>](c-ftdfs.md)<br/> |



 

 





