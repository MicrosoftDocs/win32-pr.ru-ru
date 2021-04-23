---
title: Атрибут Home-Directory
description: Корневой каталог для учетной записи.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Home-Directory
- Схема AD атрибута Хомедиректори
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804787"
---
# <a name="home-directory-attribute"></a><span data-ttu-id="f0362-105">Атрибут Home-Directory</span><span class="sxs-lookup"><span data-stu-id="f0362-105">Home-Directory attribute</span></span>

<span data-ttu-id="f0362-106">Корневой каталог для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f0362-106">The home directory for the account.</span></span> <span data-ttu-id="f0362-107">Если [**хомедриве**](a-homedrive.md) задано и указывает букву диска, **ХОМЕДИРЕКТОРИ** должен быть UNC-путем.</span><span class="sxs-lookup"><span data-stu-id="f0362-107">If [**homeDrive**](a-homedrive.md) is set and specifies a drive letter, **homeDirectory** must be a UNC path.</span></span> <span data-ttu-id="f0362-108">В противном случае **хомедиректори** — это полный локальный путь, включая букву диска (например, папка \*буква_диска \***: \\**_Каталог_\* _\\_ \* ).</span><span class="sxs-lookup"><span data-stu-id="f0362-108">Otherwise, **homeDirectory** is a fully qualified local path including the drive letter (for example, *DriveLetter\***:\\**_Directory_*_\\_\*_Folder_).</span></span> <span data-ttu-id="f0362-109">Это значение может быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="f0362-109">This value can be a null string.</span></span>



| <span data-ttu-id="f0362-110">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-110">Entry</span></span> | <span data-ttu-id="f0362-111">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0362-112">CN</span><span class="sxs-lookup"><span data-stu-id="f0362-112">CN</span></span>                | <span data-ttu-id="f0362-113">Home-Directory</span><span class="sxs-lookup"><span data-stu-id="f0362-113">Home-Directory</span></span>                                                                     |
| <span data-ttu-id="f0362-114">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f0362-114">Ldap-Display-Name</span></span> | <span data-ttu-id="f0362-115">хомедиректори</span><span class="sxs-lookup"><span data-stu-id="f0362-115">homeDirectory</span></span>                                                                      |
| <span data-ttu-id="f0362-116">Размер</span><span class="sxs-lookup"><span data-stu-id="f0362-116">Size</span></span>              | \-                                                                                 |
| <span data-ttu-id="f0362-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f0362-117">Update Privilege</span></span>  | <span data-ttu-id="f0362-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="f0362-118">Domain administrator</span></span>                                                               |
| <span data-ttu-id="f0362-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f0362-119">Update Frequency</span></span>  | <span data-ttu-id="f0362-120">При создании записи пользователя и при необходимости изменения домашнего каталога.</span><span class="sxs-lookup"><span data-stu-id="f0362-120">When the user's record is created and whenever the home directory needs to change.</span></span> |
| <span data-ttu-id="f0362-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-121">Attribute-Id</span></span>      | <span data-ttu-id="f0362-122">1.2.840.113556.1.4.44</span><span class="sxs-lookup"><span data-stu-id="f0362-122">1.2.840.113556.1.4.44</span></span>                                                              |
| <span data-ttu-id="f0362-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f0362-123">System-Id-Guid</span></span>    | <span data-ttu-id="f0362-124">bf967985-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f0362-124">bf967985-0de6-11d0-a285-00aa003049e2</span></span>                                               |
| <span data-ttu-id="f0362-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0362-125">Syntax</span></span>            | [<span data-ttu-id="f0362-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="f0362-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                        |



## <a name="implementations"></a><span data-ttu-id="f0362-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f0362-127">Implementations</span></span>

-   [<span data-ttu-id="f0362-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f0362-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f0362-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0362-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0362-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0362-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0362-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0362-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0362-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0362-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0362-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0362-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f0362-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0362-134">Windows 2000 Server</span></span>



| <span data-ttu-id="f0362-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-135">Entry</span></span> | <span data-ttu-id="f0362-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0362-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0362-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0362-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0362-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0362-139">System-Only</span></span>            | <span data-ttu-id="f0362-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-140">False</span></span>                             |
| <span data-ttu-id="f0362-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0362-141">Is-Single-Valued</span></span>       | <span data-ttu-id="f0362-142">True</span><span class="sxs-lookup"><span data-stu-id="f0362-142">True</span></span>                              |
| <span data-ttu-id="f0362-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0362-143">Is Indexed</span></span>             | <span data-ttu-id="f0362-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-144">False</span></span>                             |
| <span data-ttu-id="f0362-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0362-145">In Global Catalog</span></span>      | <span data-ttu-id="f0362-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-146">False</span></span>                             |
| <span data-ttu-id="f0362-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0362-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0362-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0362-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0362-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0362-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0362-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0362-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0362-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-151">Search-Flags</span></span>           | <span data-ttu-id="f0362-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-152">0x00000010</span></span>                        |
| <span data-ttu-id="f0362-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-153">System-Flags</span></span>           | <span data-ttu-id="f0362-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-154">0x00000010</span></span>                        |
| <span data-ttu-id="f0362-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0362-155">Classes used in</span></span>        | [<span data-ttu-id="f0362-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f0362-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f0362-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0362-157">Windows Server 2003</span></span>



| <span data-ttu-id="f0362-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-158">Entry</span></span> | <span data-ttu-id="f0362-159">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="f0362-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0362-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="f0362-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="f0362-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0362-162">System-Only</span></span>            | <span data-ttu-id="f0362-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-163">False</span></span>                             |
| <span data-ttu-id="f0362-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0362-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f0362-165">True</span><span class="sxs-lookup"><span data-stu-id="f0362-165">True</span></span>                              |
| <span data-ttu-id="f0362-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0362-166">Is Indexed</span></span>             | <span data-ttu-id="f0362-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-167">False</span></span>                             |
| <span data-ttu-id="f0362-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0362-168">In Global Catalog</span></span>      | <span data-ttu-id="f0362-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-169">False</span></span>                             |
| <span data-ttu-id="f0362-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0362-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0362-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0362-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="f0362-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0362-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="f0362-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0362-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="f0362-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-174">Search-Flags</span></span>           | <span data-ttu-id="f0362-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-175">0x00000010</span></span>                        |
| <span data-ttu-id="f0362-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-176">System-Flags</span></span>           | <span data-ttu-id="f0362-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-177">0x00000010</span></span>                        |
| <span data-ttu-id="f0362-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0362-178">Classes used in</span></span>        | [<span data-ttu-id="f0362-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f0362-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0362-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0362-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0362-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-181">Entry</span></span> | <span data-ttu-id="f0362-182">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-182">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0362-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0362-183">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-184">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0362-185">System-Only</span></span>            | <span data-ttu-id="f0362-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-186">False</span></span>                                                                               |
| <span data-ttu-id="f0362-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0362-187">Is-Single-Valued</span></span>       | <span data-ttu-id="f0362-188">True</span><span class="sxs-lookup"><span data-stu-id="f0362-188">True</span></span>                                                                                |
| <span data-ttu-id="f0362-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0362-189">Is Indexed</span></span>             | <span data-ttu-id="f0362-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-190">False</span></span>                                                                               |
| <span data-ttu-id="f0362-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0362-191">In Global Catalog</span></span>      | <span data-ttu-id="f0362-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-192">False</span></span>                                                                               |
| <span data-ttu-id="f0362-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0362-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0362-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0362-194">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f0362-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0362-195">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0362-196">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-197">Search-Flags</span></span>           | <span data-ttu-id="f0362-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-198">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-199">System-Flags</span></span>           | <span data-ttu-id="f0362-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-200">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0362-201">Classes used in</span></span>        | [<span data-ttu-id="f0362-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f0362-202">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="f0362-203">**посиксаккаунт**</span><span class="sxs-lookup"><span data-stu-id="f0362-203">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0362-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0362-204">Windows Server 2008</span></span>



| <span data-ttu-id="f0362-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-205">Entry</span></span> | <span data-ttu-id="f0362-206">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0362-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0362-207">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-208">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0362-209">System-Only</span></span>            | <span data-ttu-id="f0362-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-210">False</span></span>                                                                               |
| <span data-ttu-id="f0362-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0362-211">Is-Single-Valued</span></span>       | <span data-ttu-id="f0362-212">True</span><span class="sxs-lookup"><span data-stu-id="f0362-212">True</span></span>                                                                                |
| <span data-ttu-id="f0362-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0362-213">Is Indexed</span></span>             | <span data-ttu-id="f0362-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-214">False</span></span>                                                                               |
| <span data-ttu-id="f0362-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0362-215">In Global Catalog</span></span>      | <span data-ttu-id="f0362-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-216">False</span></span>                                                                               |
| <span data-ttu-id="f0362-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0362-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0362-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0362-218">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f0362-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0362-219">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0362-220">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-221">Search-Flags</span></span>           | <span data-ttu-id="f0362-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-222">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-223">System-Flags</span></span>           | <span data-ttu-id="f0362-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-224">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0362-225">Classes used in</span></span>        | [<span data-ttu-id="f0362-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f0362-226">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="f0362-227">**посиксаккаунт**</span><span class="sxs-lookup"><span data-stu-id="f0362-227">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0362-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0362-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0362-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-229">Entry</span></span> | <span data-ttu-id="f0362-230">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-230">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0362-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0362-231">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-232">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0362-233">System-Only</span></span>            | <span data-ttu-id="f0362-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-234">False</span></span>                                                                               |
| <span data-ttu-id="f0362-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0362-235">Is-Single-Valued</span></span>       | <span data-ttu-id="f0362-236">True</span><span class="sxs-lookup"><span data-stu-id="f0362-236">True</span></span>                                                                                |
| <span data-ttu-id="f0362-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0362-237">Is Indexed</span></span>             | <span data-ttu-id="f0362-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-238">False</span></span>                                                                               |
| <span data-ttu-id="f0362-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0362-239">In Global Catalog</span></span>      | <span data-ttu-id="f0362-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-240">False</span></span>                                                                               |
| <span data-ttu-id="f0362-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0362-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0362-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0362-242">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f0362-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0362-243">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0362-244">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-245">Search-Flags</span></span>           | <span data-ttu-id="f0362-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-246">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-247">System-Flags</span></span>           | <span data-ttu-id="f0362-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-248">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0362-249">Classes used in</span></span>        | [<span data-ttu-id="f0362-250">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f0362-250">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="f0362-251">**посиксаккаунт**</span><span class="sxs-lookup"><span data-stu-id="f0362-251">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0362-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0362-252">Windows Server 2012</span></span>



| <span data-ttu-id="f0362-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0362-253">Entry</span></span> | <span data-ttu-id="f0362-254">Значение</span><span class="sxs-lookup"><span data-stu-id="f0362-254">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0362-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0362-255">Link-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0362-256">MAPI-Id</span></span>                | \-                                                                                  |
| <span data-ttu-id="f0362-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0362-257">System-Only</span></span>            | <span data-ttu-id="f0362-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-258">False</span></span>                                                                               |
| <span data-ttu-id="f0362-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0362-259">Is-Single-Valued</span></span>       | <span data-ttu-id="f0362-260">True</span><span class="sxs-lookup"><span data-stu-id="f0362-260">True</span></span>                                                                                |
| <span data-ttu-id="f0362-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0362-261">Is Indexed</span></span>             | <span data-ttu-id="f0362-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-262">False</span></span>                                                                               |
| <span data-ttu-id="f0362-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0362-263">In Global Catalog</span></span>      | <span data-ttu-id="f0362-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0362-264">False</span></span>                                                                               |
| <span data-ttu-id="f0362-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0362-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0362-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0362-266">O:BAG:BAD:S:</span></span>                                                                        |
| <span data-ttu-id="f0362-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0362-267">Range-Lower</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0362-268">Range-Upper</span></span>            | \-                                                                                  |
| <span data-ttu-id="f0362-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-269">Search-Flags</span></span>           | <span data-ttu-id="f0362-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-270">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0362-271">System-Flags</span></span>           | <span data-ttu-id="f0362-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0362-272">0x00000010</span></span>                                                                          |
| <span data-ttu-id="f0362-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0362-273">Classes used in</span></span>        | [<span data-ttu-id="f0362-274">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="f0362-274">**User**</span></span>](c-user.md)<br/> [<span data-ttu-id="f0362-275">**посиксаккаунт**</span><span class="sxs-lookup"><span data-stu-id="f0362-275">**posixAccount**</span></span>](c-posixaccount.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="f0362-276">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0362-276">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0362-277">**хомедриве**</span><span class="sxs-lookup"><span data-stu-id="f0362-277">**homeDrive**</span></span>](a-homedrive.md)
</dt> </dl>

 

 





