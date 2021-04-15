---
title: Атрибут Home-Drive
description: Указывает букву диска, с которой будет сопоставлен UNC-путь, заданный параметром Хомедиректори.
ms.assetid: fa402e14-febf-4ed9-bcc6-a6bfd405068c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Home-Drive
- Схема AD атрибута Хомедриве
topic_type:
- apiref
api_name:
- Home-Drive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce9bff87662cc3b9da962b0c5647e79e90a3068
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654821"
---
# <a name="home-drive-attribute"></a><span data-ttu-id="1feb2-105">Атрибут Home-Drive</span><span class="sxs-lookup"><span data-stu-id="1feb2-105">Home-Drive attribute</span></span>

<span data-ttu-id="1feb2-106">Указывает букву диска, с которой будет сопоставлен UNC-путь, заданный параметром [**хомедиректори**](a-homedirectory.md).</span><span class="sxs-lookup"><span data-stu-id="1feb2-106">Specifies the drive letter to which to map the UNC path specified by [**homeDirectory**](a-homedirectory.md).</span></span> <span data-ttu-id="1feb2-107">Буква диска должна быть указана в формате \*буква_диска \* \* \*:\*\*, где \*буква_диска\* — буква диска для отображения.</span><span class="sxs-lookup"><span data-stu-id="1feb2-107">The drive letter must be specified in the form *DriveLetter\*\*\*:*\* where *DriveLetter* is the letter of the drive to map.</span></span> <span data-ttu-id="1feb2-108">Буква « *буква_диска* » должна быть отдельной буквы в верхнем регистре и двоеточием (:) является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1feb2-108">The *DriveLetter* must be a single, uppercase letter and the colon (:) is required.</span></span>



| <span data-ttu-id="1feb2-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-109">Entry</span></span> | <span data-ttu-id="1feb2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1feb2-111">CN</span><span class="sxs-lookup"><span data-stu-id="1feb2-111">CN</span></span>                | <span data-ttu-id="1feb2-112">Home-Drive</span><span class="sxs-lookup"><span data-stu-id="1feb2-112">Home-Drive</span></span>                                                                        |
| <span data-ttu-id="1feb2-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1feb2-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1feb2-114">хомедриве</span><span class="sxs-lookup"><span data-stu-id="1feb2-114">homeDrive</span></span>                                                                         |
| <span data-ttu-id="1feb2-115">Размер</span><span class="sxs-lookup"><span data-stu-id="1feb2-115">Size</span></span>              | <span data-ttu-id="1feb2-116">2 байта</span><span class="sxs-lookup"><span data-stu-id="1feb2-116">2 bytes</span></span>                                                                           |
| <span data-ttu-id="1feb2-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1feb2-117">Update Privilege</span></span>  | <span data-ttu-id="1feb2-118">Это значение устанавливается администратором домена.</span><span class="sxs-lookup"><span data-stu-id="1feb2-118">The domain administrator sets this value.</span></span>                                         |
| <span data-ttu-id="1feb2-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1feb2-119">Update Frequency</span></span>  | <span data-ttu-id="1feb2-120">При создании записи пользователя и при необходимости изменения домашнего диска.</span><span class="sxs-lookup"><span data-stu-id="1feb2-120">When the record of a user is created and whenever the home drive needs to change.</span></span> |
| <span data-ttu-id="1feb2-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-121">Attribute-Id</span></span>      | <span data-ttu-id="1feb2-122">1.2.840.113556.1.4.45</span><span class="sxs-lookup"><span data-stu-id="1feb2-122">1.2.840.113556.1.4.45</span></span>                                                             |
| <span data-ttu-id="1feb2-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1feb2-123">System-Id-Guid</span></span>    | <span data-ttu-id="1feb2-124">bf967986-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1feb2-124">bf967986-0de6-11d0-a285-00aa003049e2</span></span>                                              |
| <span data-ttu-id="1feb2-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1feb2-125">Syntax</span></span>            | [<span data-ttu-id="1feb2-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="1feb2-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                       |



## <a name="implementations"></a><span data-ttu-id="1feb2-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1feb2-127">Implementations</span></span>

-   [<span data-ttu-id="1feb2-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1feb2-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1feb2-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1feb2-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1feb2-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1feb2-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1feb2-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1feb2-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1feb2-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1feb2-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1feb2-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1feb2-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1feb2-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1feb2-134">Windows 2000 Server</span></span>



| <span data-ttu-id="1feb2-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-135">Entry</span></span> | <span data-ttu-id="1feb2-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1feb2-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1feb2-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1feb2-139">System-Only</span></span>            | <span data-ttu-id="1feb2-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-140">False</span></span>                             |
| <span data-ttu-id="1feb2-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1feb2-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1feb2-142">True</span><span class="sxs-lookup"><span data-stu-id="1feb2-142">True</span></span>                              |
| <span data-ttu-id="1feb2-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1feb2-143">Is Indexed</span></span>             | <span data-ttu-id="1feb2-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-144">False</span></span>                             |
| <span data-ttu-id="1feb2-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1feb2-145">In Global Catalog</span></span>      | <span data-ttu-id="1feb2-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-146">False</span></span>                             |
| <span data-ttu-id="1feb2-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1feb2-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1feb2-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1feb2-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1feb2-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1feb2-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1feb2-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1feb2-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1feb2-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-151">Search-Flags</span></span>           | <span data-ttu-id="1feb2-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-152">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-153">System-Flags</span></span>           | <span data-ttu-id="1feb2-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-154">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1feb2-155">Classes used in</span></span>        | [<span data-ttu-id="1feb2-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1feb2-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1feb2-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1feb2-157">Windows Server 2003</span></span>



| <span data-ttu-id="1feb2-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-158">Entry</span></span> | <span data-ttu-id="1feb2-159">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1feb2-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1feb2-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="1feb2-162">System-Only</span></span>            | <span data-ttu-id="1feb2-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-163">False</span></span>                             |
| <span data-ttu-id="1feb2-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1feb2-164">Is-Single-Valued</span></span>       | <span data-ttu-id="1feb2-165">True</span><span class="sxs-lookup"><span data-stu-id="1feb2-165">True</span></span>                              |
| <span data-ttu-id="1feb2-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1feb2-166">Is Indexed</span></span>             | <span data-ttu-id="1feb2-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-167">False</span></span>                             |
| <span data-ttu-id="1feb2-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1feb2-168">In Global Catalog</span></span>      | <span data-ttu-id="1feb2-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-169">False</span></span>                             |
| <span data-ttu-id="1feb2-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1feb2-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="1feb2-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1feb2-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1feb2-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1feb2-172">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1feb2-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1feb2-173">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1feb2-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-174">Search-Flags</span></span>           | <span data-ttu-id="1feb2-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-175">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-176">System-Flags</span></span>           | <span data-ttu-id="1feb2-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-177">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1feb2-178">Classes used in</span></span>        | [<span data-ttu-id="1feb2-179">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1feb2-179">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1feb2-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1feb2-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1feb2-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-181">Entry</span></span> | <span data-ttu-id="1feb2-182">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-182">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1feb2-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1feb2-183">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-184">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="1feb2-185">System-Only</span></span>            | <span data-ttu-id="1feb2-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-186">False</span></span>                             |
| <span data-ttu-id="1feb2-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1feb2-187">Is-Single-Valued</span></span>       | <span data-ttu-id="1feb2-188">True</span><span class="sxs-lookup"><span data-stu-id="1feb2-188">True</span></span>                              |
| <span data-ttu-id="1feb2-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1feb2-189">Is Indexed</span></span>             | <span data-ttu-id="1feb2-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-190">False</span></span>                             |
| <span data-ttu-id="1feb2-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1feb2-191">In Global Catalog</span></span>      | <span data-ttu-id="1feb2-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-192">False</span></span>                             |
| <span data-ttu-id="1feb2-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1feb2-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="1feb2-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1feb2-194">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1feb2-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1feb2-195">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1feb2-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1feb2-196">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1feb2-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-197">Search-Flags</span></span>           | <span data-ttu-id="1feb2-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-198">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-199">System-Flags</span></span>           | <span data-ttu-id="1feb2-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-200">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1feb2-201">Classes used in</span></span>        | [<span data-ttu-id="1feb2-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1feb2-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1feb2-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1feb2-203">Windows Server 2008</span></span>



| <span data-ttu-id="1feb2-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-204">Entry</span></span> | <span data-ttu-id="1feb2-205">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-205">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1feb2-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1feb2-206">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-207">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="1feb2-208">System-Only</span></span>            | <span data-ttu-id="1feb2-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-209">False</span></span>                             |
| <span data-ttu-id="1feb2-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1feb2-210">Is-Single-Valued</span></span>       | <span data-ttu-id="1feb2-211">True</span><span class="sxs-lookup"><span data-stu-id="1feb2-211">True</span></span>                              |
| <span data-ttu-id="1feb2-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1feb2-212">Is Indexed</span></span>             | <span data-ttu-id="1feb2-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-213">False</span></span>                             |
| <span data-ttu-id="1feb2-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1feb2-214">In Global Catalog</span></span>      | <span data-ttu-id="1feb2-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-215">False</span></span>                             |
| <span data-ttu-id="1feb2-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1feb2-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="1feb2-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1feb2-217">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1feb2-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1feb2-218">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1feb2-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1feb2-219">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1feb2-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-220">Search-Flags</span></span>           | <span data-ttu-id="1feb2-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-221">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-222">System-Flags</span></span>           | <span data-ttu-id="1feb2-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-223">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1feb2-224">Classes used in</span></span>        | [<span data-ttu-id="1feb2-225">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1feb2-225">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1feb2-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1feb2-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1feb2-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-227">Entry</span></span> | <span data-ttu-id="1feb2-228">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-228">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1feb2-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1feb2-229">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-230">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="1feb2-231">System-Only</span></span>            | <span data-ttu-id="1feb2-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-232">False</span></span>                             |
| <span data-ttu-id="1feb2-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1feb2-233">Is-Single-Valued</span></span>       | <span data-ttu-id="1feb2-234">True</span><span class="sxs-lookup"><span data-stu-id="1feb2-234">True</span></span>                              |
| <span data-ttu-id="1feb2-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1feb2-235">Is Indexed</span></span>             | <span data-ttu-id="1feb2-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-236">False</span></span>                             |
| <span data-ttu-id="1feb2-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1feb2-237">In Global Catalog</span></span>      | <span data-ttu-id="1feb2-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-238">False</span></span>                             |
| <span data-ttu-id="1feb2-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1feb2-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="1feb2-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1feb2-240">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1feb2-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1feb2-241">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1feb2-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1feb2-242">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1feb2-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-243">Search-Flags</span></span>           | <span data-ttu-id="1feb2-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-244">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-245">System-Flags</span></span>           | <span data-ttu-id="1feb2-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-246">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1feb2-247">Classes used in</span></span>        | [<span data-ttu-id="1feb2-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1feb2-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1feb2-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1feb2-249">Windows Server 2012</span></span>



| <span data-ttu-id="1feb2-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="1feb2-250">Entry</span></span> | <span data-ttu-id="1feb2-251">Значение</span><span class="sxs-lookup"><span data-stu-id="1feb2-251">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1feb2-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1feb2-252">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1feb2-253">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1feb2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="1feb2-254">System-Only</span></span>            | <span data-ttu-id="1feb2-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-255">False</span></span>                             |
| <span data-ttu-id="1feb2-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1feb2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="1feb2-257">True</span><span class="sxs-lookup"><span data-stu-id="1feb2-257">True</span></span>                              |
| <span data-ttu-id="1feb2-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1feb2-258">Is Indexed</span></span>             | <span data-ttu-id="1feb2-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-259">False</span></span>                             |
| <span data-ttu-id="1feb2-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1feb2-260">In Global Catalog</span></span>      | <span data-ttu-id="1feb2-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="1feb2-261">False</span></span>                             |
| <span data-ttu-id="1feb2-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1feb2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="1feb2-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1feb2-263">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1feb2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1feb2-264">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1feb2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1feb2-265">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1feb2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-266">Search-Flags</span></span>           | <span data-ttu-id="1feb2-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-267">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1feb2-268">System-Flags</span></span>           | <span data-ttu-id="1feb2-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1feb2-269">0x00000010</span></span>                        |
| <span data-ttu-id="1feb2-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1feb2-270">Classes used in</span></span>        | [<span data-ttu-id="1feb2-271">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1feb2-271">**User**</span></span>](c-user.md)<br/> |



## <a name="see-also"></a><span data-ttu-id="1feb2-272">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1feb2-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1feb2-273">**хомедиректори**</span><span class="sxs-lookup"><span data-stu-id="1feb2-273">**homeDirectory**</span></span>](a-homedirectory.md)
</dt> </dl>

 

 





