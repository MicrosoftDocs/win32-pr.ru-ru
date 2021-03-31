---
title: Общий атрибут User-Shared-Folder
description: Указывает UNC-путь к папке дополнительных общих документов пользователя. Путь должен представлять собой сетевой UNC-путь к \\ \\ \\ общему \\ каталогу сервера форм. Это значение может быть пустой строкой.
ms.assetid: 7d546cda-b2c1-46a6-a3cf-a7c78ddb1422
ms.tgt_platform: multiple
keywords:
- Пользователь-общая папка-схема AD для других атрибутов
- Схема AD атрибута Усершаредфолдеросер
topic_type:
- apiref
api_name:
- User-Shared-Folder-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6087a28df474ff06c1d8bf54d694176df8591b5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804535"
---
# <a name="user-shared-folder-other-attribute"></a><span data-ttu-id="2ec27-107">Общий атрибут User-Shared-Folder</span><span class="sxs-lookup"><span data-stu-id="2ec27-107">User-Shared-Folder-Other attribute</span></span>

<span data-ttu-id="2ec27-108">Указывает UNC-путь к папке дополнительных общих документов пользователя.</span><span class="sxs-lookup"><span data-stu-id="2ec27-108">Specifies a UNC path to the user's additional shared documents folder.</span></span> <span data-ttu-id="2ec27-109">Путь должен представлять собой сетевой UNC-путь к **\\\\**  *_\\_* _общему_ *_\\_* _каталогу_ сервера форм.</span><span class="sxs-lookup"><span data-stu-id="2ec27-109">The path must be a network UNC path of the form **\\\\**_Server_*_\\_*_Share_*_\\_*_Directory_.</span></span> <span data-ttu-id="2ec27-110">Это значение может быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="2ec27-110">This value can be a null string.</span></span>



| <span data-ttu-id="2ec27-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-111">Entry</span></span> | <span data-ttu-id="2ec27-112">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2ec27-113">CN</span><span class="sxs-lookup"><span data-stu-id="2ec27-113">CN</span></span>                | <span data-ttu-id="2ec27-114">Общая папка для пользователя</span><span class="sxs-lookup"><span data-stu-id="2ec27-114">User-Shared-Folder-Other</span></span>                                                          |
| <span data-ttu-id="2ec27-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2ec27-115">Ldap-Display-Name</span></span> | <span data-ttu-id="2ec27-116">усершаредфолдеросер</span><span class="sxs-lookup"><span data-stu-id="2ec27-116">userSharedFolderOther</span></span>                                                             |
| <span data-ttu-id="2ec27-117">Размер</span><span class="sxs-lookup"><span data-stu-id="2ec27-117">Size</span></span>              | \-                                                                                |
| <span data-ttu-id="2ec27-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2ec27-118">Update Privilege</span></span>  | <span data-ttu-id="2ec27-119">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2ec27-119">Domain administrator or account owner.</span></span>                                            |
| <span data-ttu-id="2ec27-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2ec27-120">Update Frequency</span></span>  | <span data-ttu-id="2ec27-121">При создании записи пользователя и при необходимости изменения общей папки.</span><span class="sxs-lookup"><span data-stu-id="2ec27-121">When the user's record is created and whenever the shared folder needs to change.</span></span> |
| <span data-ttu-id="2ec27-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-122">Attribute-Id</span></span>      | <span data-ttu-id="2ec27-123">1.2.840.113556.1.4.752</span><span class="sxs-lookup"><span data-stu-id="2ec27-123">1.2.840.113556.1.4.752</span></span>                                                            |
| <span data-ttu-id="2ec27-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2ec27-124">System-Id-Guid</span></span>    | <span data-ttu-id="2ec27-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2ec27-125">9a9a0220-4a5b-11d1-a9c3-0000f80367c1</span></span>                                              |
| <span data-ttu-id="2ec27-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ec27-126">Syntax</span></span>            | [<span data-ttu-id="2ec27-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2ec27-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="2ec27-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2ec27-128">Implementations</span></span>

-   [<span data-ttu-id="2ec27-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2ec27-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2ec27-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2ec27-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2ec27-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2ec27-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2ec27-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2ec27-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2ec27-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2ec27-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2ec27-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2ec27-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2ec27-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ec27-135">Windows 2000 Server</span></span>



| <span data-ttu-id="2ec27-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-136">Entry</span></span> | <span data-ttu-id="2ec27-137">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2ec27-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ec27-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ec27-140">System-Only</span></span>            | <span data-ttu-id="2ec27-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-141">False</span></span>                             |
| <span data-ttu-id="2ec27-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ec27-142">Is-Single-Valued</span></span>       | <span data-ttu-id="2ec27-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-143">False</span></span>                             |
| <span data-ttu-id="2ec27-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ec27-144">Is Indexed</span></span>             | <span data-ttu-id="2ec27-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-145">False</span></span>                             |
| <span data-ttu-id="2ec27-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ec27-146">In Global Catalog</span></span>      | <span data-ttu-id="2ec27-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-147">False</span></span>                             |
| <span data-ttu-id="2ec27-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ec27-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ec27-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ec27-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2ec27-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ec27-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2ec27-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ec27-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2ec27-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-152">Search-Flags</span></span>           | <span data-ttu-id="2ec27-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ec27-153">0x00000000</span></span>                        |
| <span data-ttu-id="2ec27-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-154">System-Flags</span></span>           | <span data-ttu-id="2ec27-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ec27-155">0x00000010</span></span>                        |
| <span data-ttu-id="2ec27-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ec27-156">Classes used in</span></span>        | [<span data-ttu-id="2ec27-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2ec27-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2ec27-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ec27-158">Windows Server 2003</span></span>



| <span data-ttu-id="2ec27-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-159">Entry</span></span> | <span data-ttu-id="2ec27-160">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2ec27-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ec27-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ec27-163">System-Only</span></span>            | <span data-ttu-id="2ec27-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-164">False</span></span>                             |
| <span data-ttu-id="2ec27-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ec27-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2ec27-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-166">False</span></span>                             |
| <span data-ttu-id="2ec27-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ec27-167">Is Indexed</span></span>             | <span data-ttu-id="2ec27-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-168">False</span></span>                             |
| <span data-ttu-id="2ec27-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ec27-169">In Global Catalog</span></span>      | <span data-ttu-id="2ec27-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-170">False</span></span>                             |
| <span data-ttu-id="2ec27-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ec27-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ec27-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ec27-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2ec27-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ec27-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2ec27-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ec27-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2ec27-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-175">Search-Flags</span></span>           | <span data-ttu-id="2ec27-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ec27-176">0x00000000</span></span>                        |
| <span data-ttu-id="2ec27-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-177">System-Flags</span></span>           | <span data-ttu-id="2ec27-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ec27-178">0x00000010</span></span>                        |
| <span data-ttu-id="2ec27-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ec27-179">Classes used in</span></span>        | [<span data-ttu-id="2ec27-180">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2ec27-180">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2ec27-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2ec27-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2ec27-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-182">Entry</span></span> | <span data-ttu-id="2ec27-183">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2ec27-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ec27-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ec27-186">System-Only</span></span>            | <span data-ttu-id="2ec27-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-187">False</span></span>                             |
| <span data-ttu-id="2ec27-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ec27-188">Is-Single-Valued</span></span>       | <span data-ttu-id="2ec27-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-189">False</span></span>                             |
| <span data-ttu-id="2ec27-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ec27-190">Is Indexed</span></span>             | <span data-ttu-id="2ec27-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-191">False</span></span>                             |
| <span data-ttu-id="2ec27-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ec27-192">In Global Catalog</span></span>      | <span data-ttu-id="2ec27-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-193">False</span></span>                             |
| <span data-ttu-id="2ec27-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ec27-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ec27-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ec27-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2ec27-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ec27-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2ec27-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ec27-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2ec27-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-198">Search-Flags</span></span>           | <span data-ttu-id="2ec27-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ec27-199">0x00000000</span></span>                        |
| <span data-ttu-id="2ec27-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-200">System-Flags</span></span>           | <span data-ttu-id="2ec27-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ec27-201">0x00000010</span></span>                        |
| <span data-ttu-id="2ec27-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ec27-202">Classes used in</span></span>        | [<span data-ttu-id="2ec27-203">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2ec27-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2ec27-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ec27-204">Windows Server 2008</span></span>



| <span data-ttu-id="2ec27-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-205">Entry</span></span> | <span data-ttu-id="2ec27-206">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2ec27-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ec27-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ec27-209">System-Only</span></span>            | <span data-ttu-id="2ec27-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-210">False</span></span>                             |
| <span data-ttu-id="2ec27-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ec27-211">Is-Single-Valued</span></span>       | <span data-ttu-id="2ec27-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-212">False</span></span>                             |
| <span data-ttu-id="2ec27-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ec27-213">Is Indexed</span></span>             | <span data-ttu-id="2ec27-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-214">False</span></span>                             |
| <span data-ttu-id="2ec27-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ec27-215">In Global Catalog</span></span>      | <span data-ttu-id="2ec27-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-216">False</span></span>                             |
| <span data-ttu-id="2ec27-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ec27-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ec27-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ec27-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2ec27-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ec27-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2ec27-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ec27-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2ec27-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-221">Search-Flags</span></span>           | <span data-ttu-id="2ec27-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ec27-222">0x00000000</span></span>                        |
| <span data-ttu-id="2ec27-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-223">System-Flags</span></span>           | <span data-ttu-id="2ec27-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ec27-224">0x00000010</span></span>                        |
| <span data-ttu-id="2ec27-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ec27-225">Classes used in</span></span>        | [<span data-ttu-id="2ec27-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2ec27-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2ec27-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2ec27-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2ec27-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-228">Entry</span></span> | <span data-ttu-id="2ec27-229">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2ec27-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ec27-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ec27-232">System-Only</span></span>            | <span data-ttu-id="2ec27-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-233">False</span></span>                             |
| <span data-ttu-id="2ec27-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ec27-234">Is-Single-Valued</span></span>       | <span data-ttu-id="2ec27-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-235">False</span></span>                             |
| <span data-ttu-id="2ec27-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ec27-236">Is Indexed</span></span>             | <span data-ttu-id="2ec27-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-237">False</span></span>                             |
| <span data-ttu-id="2ec27-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ec27-238">In Global Catalog</span></span>      | <span data-ttu-id="2ec27-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-239">False</span></span>                             |
| <span data-ttu-id="2ec27-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ec27-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ec27-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ec27-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2ec27-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ec27-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2ec27-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ec27-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2ec27-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-244">Search-Flags</span></span>           | <span data-ttu-id="2ec27-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ec27-245">0x00000000</span></span>                        |
| <span data-ttu-id="2ec27-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-246">System-Flags</span></span>           | <span data-ttu-id="2ec27-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ec27-247">0x00000010</span></span>                        |
| <span data-ttu-id="2ec27-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ec27-248">Classes used in</span></span>        | [<span data-ttu-id="2ec27-249">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="2ec27-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2ec27-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ec27-250">Windows Server 2012</span></span>



| <span data-ttu-id="2ec27-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="2ec27-251">Entry</span></span> | <span data-ttu-id="2ec27-252">Значение</span><span class="sxs-lookup"><span data-stu-id="2ec27-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="2ec27-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2ec27-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2ec27-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="2ec27-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="2ec27-255">System-Only</span></span>            | <span data-ttu-id="2ec27-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-256">False</span></span>                             |
| <span data-ttu-id="2ec27-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2ec27-257">Is-Single-Valued</span></span>       | <span data-ttu-id="2ec27-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-258">False</span></span>                             |
| <span data-ttu-id="2ec27-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2ec27-259">Is Indexed</span></span>             | <span data-ttu-id="2ec27-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-260">False</span></span>                             |
| <span data-ttu-id="2ec27-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2ec27-261">In Global Catalog</span></span>      | <span data-ttu-id="2ec27-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="2ec27-262">False</span></span>                             |
| <span data-ttu-id="2ec27-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2ec27-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="2ec27-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2ec27-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="2ec27-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2ec27-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="2ec27-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2ec27-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="2ec27-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-267">Search-Flags</span></span>           | <span data-ttu-id="2ec27-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ec27-268">0x00000000</span></span>                        |
| <span data-ttu-id="2ec27-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2ec27-269">System-Flags</span></span>           | <span data-ttu-id="2ec27-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2ec27-270">0x00000010</span></span>                        |
| <span data-ttu-id="2ec27-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2ec27-271">Classes used in</span></span>        | [<span data-ttu-id="2ec27-272">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="2ec27-272">**User**</span></span>](c-user.md)<br/> |



 

 





