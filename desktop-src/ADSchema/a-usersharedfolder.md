---
title: Атрибут общей папки для пользователя
description: Указывает UNC-путь к папке общих документов пользователя. Путь должен представлять собой сетевой UNC-путь к \\ \\ \\ общему \\ каталогу сервера форм. Это значение может быть пустой строкой.
ms.assetid: 23b4177a-0a05-4111-affe-d81bc115580d
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута общей папки пользователя
- Схема AD атрибута Усершаредфолдер
topic_type:
- apiref
api_name:
- User-Shared-Folder
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a20e9772302e79837fccd301943554191cf3b862
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989752"
---
# <a name="user-shared-folder-attribute"></a><span data-ttu-id="49753-107">Атрибут общей папки для пользователя</span><span class="sxs-lookup"><span data-stu-id="49753-107">User-Shared-Folder attribute</span></span>

<span data-ttu-id="49753-108">Указывает UNC-путь к папке общих документов пользователя.</span><span class="sxs-lookup"><span data-stu-id="49753-108">Specifies a UNC path to the user's shared documents folder.</span></span> <span data-ttu-id="49753-109">Путь должен представлять собой сетевой UNC-путь к **\\\\**  *_\\_* _общему_ *_\\_* _каталогу_ сервера форм.</span><span class="sxs-lookup"><span data-stu-id="49753-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="49753-110">Это значение может быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="49753-110">This value can be a null string.</span></span>



| <span data-ttu-id="49753-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-111">Entry</span></span> | <span data-ttu-id="49753-112">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="49753-113">CN</span><span class="sxs-lookup"><span data-stu-id="49753-113">CN</span></span>                | <span data-ttu-id="49753-114">Общая папка пользователя</span><span class="sxs-lookup"><span data-stu-id="49753-114">User-Shared-Folder</span></span>                                                                |
| <span data-ttu-id="49753-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="49753-115">Ldap-Display-Name</span></span> | <span data-ttu-id="49753-116">усершаредфолдер</span><span class="sxs-lookup"><span data-stu-id="49753-116">userSharedFolder</span></span>                                                                  |
| <span data-ttu-id="49753-117">Размер</span><span class="sxs-lookup"><span data-stu-id="49753-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="49753-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="49753-118">Update Privilege</span></span>  | <span data-ttu-id="49753-119">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="49753-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="49753-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="49753-120">Update Frequency</span></span>  | <span data-ttu-id="49753-121">При создании записи пользователя и при необходимости изменения общей папки.</span><span class="sxs-lookup"><span data-stu-id="49753-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="49753-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="49753-122">Attribute-Id</span></span>      | <span data-ttu-id="49753-123">1.2.840.113556.1.4.751</span><span class="sxs-lookup"><span data-stu-id="49753-123">1.2.840.113556.1.4.751</span></span>                                                            |
| <span data-ttu-id="49753-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="49753-124">System-Id-Guid</span></span>    | <span data-ttu-id="49753-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="49753-125">9a9a021f-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="49753-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49753-126">Syntax</span></span>            | [<span data-ttu-id="49753-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="49753-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="49753-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="49753-128">Implementations</span></span>

-   [<span data-ttu-id="49753-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="49753-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="49753-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="49753-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="49753-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="49753-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="49753-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="49753-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="49753-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="49753-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="49753-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="49753-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="49753-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="49753-135">Windows 2000 Server</span></span>



| <span data-ttu-id="49753-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-136">Entry</span></span> | <span data-ttu-id="49753-137">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="49753-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="49753-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49753-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="49753-140">System-Only</span></span>            | <span data-ttu-id="49753-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-141">False</span></span>                             |
| <span data-ttu-id="49753-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="49753-142">Is-Single-Valued</span></span>       | <span data-ttu-id="49753-143">True</span><span class="sxs-lookup"><span data-stu-id="49753-143">True</span></span>                              |
| <span data-ttu-id="49753-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="49753-144">Is Indexed</span></span>             | <span data-ttu-id="49753-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-145">False</span></span>                             |
| <span data-ttu-id="49753-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="49753-146">In Global Catalog</span></span>      | <span data-ttu-id="49753-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-147">False</span></span>                             |
| <span data-ttu-id="49753-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="49753-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="49753-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="49753-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="49753-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49753-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="49753-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49753-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="49753-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-152">Search-Flags</span></span>           | <span data-ttu-id="49753-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49753-153">0x00000000</span></span>                        |
| <span data-ttu-id="49753-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-154">System-Flags</span></span>           | <span data-ttu-id="49753-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49753-155">0x00000010</span></span>                        |
| <span data-ttu-id="49753-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="49753-156">Classes used in</span></span>        | [<span data-ttu-id="49753-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="49753-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="49753-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49753-158">Windows Server 2003</span></span>



| <span data-ttu-id="49753-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-159">Entry</span></span> | <span data-ttu-id="49753-160">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="49753-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="49753-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49753-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="49753-163">System-Only</span></span>            | <span data-ttu-id="49753-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-164">False</span></span>                             |
| <span data-ttu-id="49753-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="49753-165">Is-Single-Valued</span></span>       | <span data-ttu-id="49753-166">True</span><span class="sxs-lookup"><span data-stu-id="49753-166">True</span></span>                              |
| <span data-ttu-id="49753-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="49753-167">Is Indexed</span></span>             | <span data-ttu-id="49753-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-168">False</span></span>                             |
| <span data-ttu-id="49753-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="49753-169">In Global Catalog</span></span>      | <span data-ttu-id="49753-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-170">False</span></span>                             |
| <span data-ttu-id="49753-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="49753-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="49753-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="49753-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="49753-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49753-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="49753-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49753-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="49753-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-175">Search-Flags</span></span>           | <span data-ttu-id="49753-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49753-176">0x00000000</span></span>                        |
| <span data-ttu-id="49753-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-177">System-Flags</span></span>           | <span data-ttu-id="49753-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49753-178">0x00000010</span></span>                        |
| <span data-ttu-id="49753-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="49753-179">Classes used in</span></span>        | [<span data-ttu-id="49753-180">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="49753-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="49753-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="49753-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="49753-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-182">Entry</span></span> | <span data-ttu-id="49753-183">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="49753-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="49753-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49753-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="49753-186">System-Only</span></span>            | <span data-ttu-id="49753-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-187">False</span></span>                             |
| <span data-ttu-id="49753-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="49753-188">Is-Single-Valued</span></span>       | <span data-ttu-id="49753-189">True</span><span class="sxs-lookup"><span data-stu-id="49753-189">True</span></span>                              |
| <span data-ttu-id="49753-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="49753-190">Is Indexed</span></span>             | <span data-ttu-id="49753-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-191">False</span></span>                             |
| <span data-ttu-id="49753-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="49753-192">In Global Catalog</span></span>      | <span data-ttu-id="49753-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-193">False</span></span>                             |
| <span data-ttu-id="49753-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="49753-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="49753-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="49753-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="49753-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49753-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="49753-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49753-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="49753-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-198">Search-Flags</span></span>           | <span data-ttu-id="49753-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49753-199">0x00000000</span></span>                        |
| <span data-ttu-id="49753-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-200">System-Flags</span></span>           | <span data-ttu-id="49753-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49753-201">0x00000010</span></span>                        |
| <span data-ttu-id="49753-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="49753-202">Classes used in</span></span>        | [<span data-ttu-id="49753-203">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="49753-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="49753-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49753-204">Windows Server 2008</span></span>



| <span data-ttu-id="49753-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-205">Entry</span></span> | <span data-ttu-id="49753-206">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="49753-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="49753-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49753-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="49753-209">System-Only</span></span>            | <span data-ttu-id="49753-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-210">False</span></span>                             |
| <span data-ttu-id="49753-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="49753-211">Is-Single-Valued</span></span>       | <span data-ttu-id="49753-212">True</span><span class="sxs-lookup"><span data-stu-id="49753-212">True</span></span>                              |
| <span data-ttu-id="49753-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="49753-213">Is Indexed</span></span>             | <span data-ttu-id="49753-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-214">False</span></span>                             |
| <span data-ttu-id="49753-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="49753-215">In Global Catalog</span></span>      | <span data-ttu-id="49753-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-216">False</span></span>                             |
| <span data-ttu-id="49753-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="49753-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="49753-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="49753-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="49753-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49753-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="49753-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49753-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="49753-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-221">Search-Flags</span></span>           | <span data-ttu-id="49753-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49753-222">0x00000000</span></span>                        |
| <span data-ttu-id="49753-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-223">System-Flags</span></span>           | <span data-ttu-id="49753-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49753-224">0x00000010</span></span>                        |
| <span data-ttu-id="49753-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="49753-225">Classes used in</span></span>        | [<span data-ttu-id="49753-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="49753-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="49753-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="49753-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="49753-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-228">Entry</span></span> | <span data-ttu-id="49753-229">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="49753-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="49753-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49753-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="49753-232">System-Only</span></span>            | <span data-ttu-id="49753-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-233">False</span></span>                             |
| <span data-ttu-id="49753-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="49753-234">Is-Single-Valued</span></span>       | <span data-ttu-id="49753-235">True</span><span class="sxs-lookup"><span data-stu-id="49753-235">True</span></span>                              |
| <span data-ttu-id="49753-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="49753-236">Is Indexed</span></span>             | <span data-ttu-id="49753-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-237">False</span></span>                             |
| <span data-ttu-id="49753-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="49753-238">In Global Catalog</span></span>      | <span data-ttu-id="49753-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-239">False</span></span>                             |
| <span data-ttu-id="49753-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="49753-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="49753-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="49753-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="49753-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49753-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="49753-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49753-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="49753-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-244">Search-Flags</span></span>           | <span data-ttu-id="49753-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49753-245">0x00000000</span></span>                        |
| <span data-ttu-id="49753-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-246">System-Flags</span></span>           | <span data-ttu-id="49753-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49753-247">0x00000010</span></span>                        |
| <span data-ttu-id="49753-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="49753-248">Classes used in</span></span>        | [<span data-ttu-id="49753-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="49753-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="49753-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="49753-250">Windows Server 2012</span></span>



| <span data-ttu-id="49753-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="49753-251">Entry</span></span> | <span data-ttu-id="49753-252">Значение</span><span class="sxs-lookup"><span data-stu-id="49753-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="49753-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="49753-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="49753-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="49753-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="49753-255">System-Only</span></span>            | <span data-ttu-id="49753-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-256">False</span></span>                             |
| <span data-ttu-id="49753-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="49753-257">Is-Single-Valued</span></span>       | <span data-ttu-id="49753-258">True</span><span class="sxs-lookup"><span data-stu-id="49753-258">True</span></span>                              |
| <span data-ttu-id="49753-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="49753-259">Is Indexed</span></span>             | <span data-ttu-id="49753-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-260">False</span></span>                             |
| <span data-ttu-id="49753-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="49753-261">In Global Catalog</span></span>      | <span data-ttu-id="49753-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="49753-262">False</span></span>                             |
| <span data-ttu-id="49753-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="49753-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="49753-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="49753-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="49753-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="49753-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="49753-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="49753-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="49753-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-267">Search-Flags</span></span>           | <span data-ttu-id="49753-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="49753-268">0x00000000</span></span>                        |
| <span data-ttu-id="49753-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="49753-269">System-Flags</span></span>           | <span data-ttu-id="49753-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="49753-270">0x00000010</span></span>                        |
| <span data-ttu-id="49753-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="49753-271">Classes used in</span></span>        | [<span data-ttu-id="49753-272">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="49753-272">**User**</span></span>](c-user.md)<br/> |



 

 





