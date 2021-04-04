---
title: Атрибут Profile-Path
description: Указывает путь к профилю пользователя. Это значение может быть пустой строкой, локальным абсолютным путем или UNC-путем.
ms.assetid: 03891152-52c6-4799-ae79-3be284204391
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Profile-Path
- Схема AD атрибута filePath
topic_type:
- apiref
api_name:
- Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d1c255843cf578301ce330b79f3ca983030952
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989779"
---
# <a name="profile-path-attribute"></a><span data-ttu-id="094fd-106">Атрибут Profile-Path</span><span class="sxs-lookup"><span data-stu-id="094fd-106">Profile-Path attribute</span></span>

<span data-ttu-id="094fd-107">Указывает путь к профилю пользователя.</span><span class="sxs-lookup"><span data-stu-id="094fd-107">Specifies a path to the user's profile.</span></span> <span data-ttu-id="094fd-108">Это значение может быть пустой строкой, локальным абсолютным путем или UNC-путем.</span><span class="sxs-lookup"><span data-stu-id="094fd-108">This value can be a null string, a local absolute path, or a UNC path.</span></span>



| <span data-ttu-id="094fd-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-109">Entry</span></span> | <span data-ttu-id="094fd-110">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="094fd-111">CN</span><span class="sxs-lookup"><span data-stu-id="094fd-111">CN</span></span>                | <span data-ttu-id="094fd-112">Profile-Path</span><span class="sxs-lookup"><span data-stu-id="094fd-112">Profile-Path</span></span>                                                             |
| <span data-ttu-id="094fd-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="094fd-113">Ldap-Display-Name</span></span> | <span data-ttu-id="094fd-114">Путь к пути</span><span class="sxs-lookup"><span data-stu-id="094fd-114">profilePath</span></span>                                                              |
| <span data-ttu-id="094fd-115">Размер</span><span class="sxs-lookup"><span data-stu-id="094fd-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="094fd-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="094fd-116">Update Privilege</span></span>  | <span data-ttu-id="094fd-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="094fd-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="094fd-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="094fd-118">Update Frequency</span></span>  | <span data-ttu-id="094fd-119">При создании записи пользователя и при необходимости изменения пути.</span><span class="sxs-lookup"><span data-stu-id="094fd-119">When the user's record is created and whenever the path needs to change.</span></span> |
| <span data-ttu-id="094fd-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-120">Attribute-Id</span></span>      | <span data-ttu-id="094fd-121">1.2.840.113556.1.4.139</span><span class="sxs-lookup"><span data-stu-id="094fd-121">1.2.840.113556.1.4.139</span></span>                                                   |
| <span data-ttu-id="094fd-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="094fd-122">System-Id-Guid</span></span>    | <span data-ttu-id="094fd-123">bf967a05-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="094fd-123">bf967a05-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="094fd-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="094fd-124">Syntax</span></span>            | [<span data-ttu-id="094fd-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="094fd-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="094fd-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="094fd-126">Implementations</span></span>

-   [<span data-ttu-id="094fd-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="094fd-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="094fd-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="094fd-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="094fd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="094fd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="094fd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="094fd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="094fd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="094fd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="094fd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="094fd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="094fd-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="094fd-133">Windows 2000 Server</span></span>



| <span data-ttu-id="094fd-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-134">Entry</span></span> | <span data-ttu-id="094fd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="094fd-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="094fd-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="094fd-138">System-Only</span></span>            | <span data-ttu-id="094fd-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-139">False</span></span>                             |
| <span data-ttu-id="094fd-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="094fd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="094fd-141">True</span><span class="sxs-lookup"><span data-stu-id="094fd-141">True</span></span>                              |
| <span data-ttu-id="094fd-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="094fd-142">Is Indexed</span></span>             | <span data-ttu-id="094fd-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-143">False</span></span>                             |
| <span data-ttu-id="094fd-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="094fd-144">In Global Catalog</span></span>      | <span data-ttu-id="094fd-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-145">False</span></span>                             |
| <span data-ttu-id="094fd-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="094fd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="094fd-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="094fd-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="094fd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="094fd-148">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="094fd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="094fd-149">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="094fd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-150">Search-Flags</span></span>           | <span data-ttu-id="094fd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-151">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-152">System-Flags</span></span>           | <span data-ttu-id="094fd-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-153">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="094fd-154">Classes used in</span></span>        | [<span data-ttu-id="094fd-155">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="094fd-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="094fd-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="094fd-156">Windows Server 2003</span></span>



| <span data-ttu-id="094fd-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-157">Entry</span></span> | <span data-ttu-id="094fd-158">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-158">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="094fd-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="094fd-159">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-160">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="094fd-161">System-Only</span></span>            | <span data-ttu-id="094fd-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-162">False</span></span>                             |
| <span data-ttu-id="094fd-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="094fd-163">Is-Single-Valued</span></span>       | <span data-ttu-id="094fd-164">True</span><span class="sxs-lookup"><span data-stu-id="094fd-164">True</span></span>                              |
| <span data-ttu-id="094fd-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="094fd-165">Is Indexed</span></span>             | <span data-ttu-id="094fd-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-166">False</span></span>                             |
| <span data-ttu-id="094fd-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="094fd-167">In Global Catalog</span></span>      | <span data-ttu-id="094fd-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-168">False</span></span>                             |
| <span data-ttu-id="094fd-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="094fd-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="094fd-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="094fd-170">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="094fd-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="094fd-171">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="094fd-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="094fd-172">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="094fd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-173">Search-Flags</span></span>           | <span data-ttu-id="094fd-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-174">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-175">System-Flags</span></span>           | <span data-ttu-id="094fd-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-176">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="094fd-177">Classes used in</span></span>        | [<span data-ttu-id="094fd-178">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="094fd-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="094fd-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="094fd-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="094fd-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-180">Entry</span></span> | <span data-ttu-id="094fd-181">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-181">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="094fd-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="094fd-182">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-183">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="094fd-184">System-Only</span></span>            | <span data-ttu-id="094fd-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-185">False</span></span>                             |
| <span data-ttu-id="094fd-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="094fd-186">Is-Single-Valued</span></span>       | <span data-ttu-id="094fd-187">True</span><span class="sxs-lookup"><span data-stu-id="094fd-187">True</span></span>                              |
| <span data-ttu-id="094fd-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="094fd-188">Is Indexed</span></span>             | <span data-ttu-id="094fd-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-189">False</span></span>                             |
| <span data-ttu-id="094fd-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="094fd-190">In Global Catalog</span></span>      | <span data-ttu-id="094fd-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-191">False</span></span>                             |
| <span data-ttu-id="094fd-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="094fd-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="094fd-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="094fd-193">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="094fd-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="094fd-194">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="094fd-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="094fd-195">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="094fd-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-196">Search-Flags</span></span>           | <span data-ttu-id="094fd-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-197">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-198">System-Flags</span></span>           | <span data-ttu-id="094fd-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-199">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="094fd-200">Classes used in</span></span>        | [<span data-ttu-id="094fd-201">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="094fd-201">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="094fd-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="094fd-202">Windows Server 2008</span></span>



| <span data-ttu-id="094fd-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-203">Entry</span></span> | <span data-ttu-id="094fd-204">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-204">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="094fd-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="094fd-205">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-206">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="094fd-207">System-Only</span></span>            | <span data-ttu-id="094fd-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-208">False</span></span>                             |
| <span data-ttu-id="094fd-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="094fd-209">Is-Single-Valued</span></span>       | <span data-ttu-id="094fd-210">True</span><span class="sxs-lookup"><span data-stu-id="094fd-210">True</span></span>                              |
| <span data-ttu-id="094fd-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="094fd-211">Is Indexed</span></span>             | <span data-ttu-id="094fd-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-212">False</span></span>                             |
| <span data-ttu-id="094fd-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="094fd-213">In Global Catalog</span></span>      | <span data-ttu-id="094fd-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-214">False</span></span>                             |
| <span data-ttu-id="094fd-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="094fd-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="094fd-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="094fd-216">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="094fd-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="094fd-217">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="094fd-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="094fd-218">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="094fd-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-219">Search-Flags</span></span>           | <span data-ttu-id="094fd-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-220">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-221">System-Flags</span></span>           | <span data-ttu-id="094fd-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-222">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="094fd-223">Classes used in</span></span>        | [<span data-ttu-id="094fd-224">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="094fd-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="094fd-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="094fd-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="094fd-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-226">Entry</span></span> | <span data-ttu-id="094fd-227">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-227">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="094fd-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="094fd-228">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-229">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="094fd-230">System-Only</span></span>            | <span data-ttu-id="094fd-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-231">False</span></span>                             |
| <span data-ttu-id="094fd-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="094fd-232">Is-Single-Valued</span></span>       | <span data-ttu-id="094fd-233">True</span><span class="sxs-lookup"><span data-stu-id="094fd-233">True</span></span>                              |
| <span data-ttu-id="094fd-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="094fd-234">Is Indexed</span></span>             | <span data-ttu-id="094fd-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-235">False</span></span>                             |
| <span data-ttu-id="094fd-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="094fd-236">In Global Catalog</span></span>      | <span data-ttu-id="094fd-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-237">False</span></span>                             |
| <span data-ttu-id="094fd-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="094fd-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="094fd-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="094fd-239">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="094fd-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="094fd-240">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="094fd-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="094fd-241">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="094fd-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-242">Search-Flags</span></span>           | <span data-ttu-id="094fd-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-243">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-244">System-Flags</span></span>           | <span data-ttu-id="094fd-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-245">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="094fd-246">Classes used in</span></span>        | [<span data-ttu-id="094fd-247">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="094fd-247">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="094fd-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="094fd-248">Windows Server 2012</span></span>



| <span data-ttu-id="094fd-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="094fd-249">Entry</span></span> | <span data-ttu-id="094fd-250">Значение</span><span class="sxs-lookup"><span data-stu-id="094fd-250">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="094fd-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="094fd-251">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="094fd-252">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="094fd-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="094fd-253">System-Only</span></span>            | <span data-ttu-id="094fd-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-254">False</span></span>                             |
| <span data-ttu-id="094fd-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="094fd-255">Is-Single-Valued</span></span>       | <span data-ttu-id="094fd-256">True</span><span class="sxs-lookup"><span data-stu-id="094fd-256">True</span></span>                              |
| <span data-ttu-id="094fd-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="094fd-257">Is Indexed</span></span>             | <span data-ttu-id="094fd-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-258">False</span></span>                             |
| <span data-ttu-id="094fd-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="094fd-259">In Global Catalog</span></span>      | <span data-ttu-id="094fd-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="094fd-260">False</span></span>                             |
| <span data-ttu-id="094fd-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="094fd-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="094fd-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="094fd-262">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="094fd-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="094fd-263">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="094fd-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="094fd-264">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="094fd-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-265">Search-Flags</span></span>           | <span data-ttu-id="094fd-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-266">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="094fd-267">System-Flags</span></span>           | <span data-ttu-id="094fd-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="094fd-268">0x00000010</span></span>                        |
| <span data-ttu-id="094fd-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="094fd-269">Classes used in</span></span>        | [<span data-ttu-id="094fd-270">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="094fd-270">**User**</span></span>](c-user.md)<br/> |



 

 





