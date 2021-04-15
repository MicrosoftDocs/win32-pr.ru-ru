---
title: атрибут MS-IIS-FTP-dir
description: Этот атрибут определяет домашнюю папку пользователя по отношению к общей папке файлового сервера. Он используется совместно с MS-IIS-FTP-root для определения домашнего каталога пользователя FTP.
ms.assetid: 99b22b79-1d42-440d-b92b-33bac3e811cb
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута MS-IIS-FTP-dir
- Схема AD атрибута Мсиис-Фтпдир
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Dir
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3067476e7dc275dbe14471d6c3c98fa5445a9dfe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535987"
---
# <a name="ms-iis-ftp-dir-attribute"></a><span data-ttu-id="16968-106">атрибут MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="16968-106">ms-IIS-FTP-Dir attribute</span></span>

<span data-ttu-id="16968-107">Этот атрибут определяет домашнюю папку пользователя по отношению к общей папке файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="16968-107">This attribute determines the user home directory relative to the file server share.</span></span> <span data-ttu-id="16968-108">Он используется совместно с MS-IIS-FTP-root для определения домашнего каталога пользователя FTP.</span><span class="sxs-lookup"><span data-stu-id="16968-108">It is used in conjunction with ms-IIS-FTP-Root to determine the FTP user home directory.</span></span>



| <span data-ttu-id="16968-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="16968-109">Entry</span></span> | <span data-ttu-id="16968-110">Значение</span><span class="sxs-lookup"><span data-stu-id="16968-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16968-111">CN</span><span class="sxs-lookup"><span data-stu-id="16968-111">CN</span></span>                | <span data-ttu-id="16968-112">MS-IIS-FTP-dir</span><span class="sxs-lookup"><span data-stu-id="16968-112">ms-IIS-FTP-Dir</span></span>                                                                                                                  |
| <span data-ttu-id="16968-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="16968-113">Ldap-Display-Name</span></span> | <span data-ttu-id="16968-114">Мсиис — Фтпдир</span><span class="sxs-lookup"><span data-stu-id="16968-114">msIIS-FTPDir</span></span>                                                                                                                    |
| <span data-ttu-id="16968-115">Размер</span><span class="sxs-lookup"><span data-stu-id="16968-115">Size</span></span>              | <span data-ttu-id="16968-116">30-50 символов (15-25 символов Юникода для каждого свойства)</span><span class="sxs-lookup"><span data-stu-id="16968-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="16968-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="16968-117">Update Privilege</span></span>  | <span data-ttu-id="16968-118">Администратор домена & локальная система</span><span class="sxs-lookup"><span data-stu-id="16968-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="16968-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="16968-119">Update Frequency</span></span>  | <span data-ttu-id="16968-120">Это свойство задается, когда администратор создает веб-сайт и настраивает изоляцию FTP.</span><span class="sxs-lookup"><span data-stu-id="16968-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="16968-121">Это редко меняется после этого.</span><span class="sxs-lookup"><span data-stu-id="16968-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="16968-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="16968-122">Attribute-Id</span></span>      | <span data-ttu-id="16968-123">1.2.840.113556.1.4.1786</span><span class="sxs-lookup"><span data-stu-id="16968-123">1.2.840.113556.1.4.1786</span></span>                                                                                                         |
| <span data-ttu-id="16968-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="16968-124">System-Id-Guid</span></span>    | <span data-ttu-id="16968-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span><span class="sxs-lookup"><span data-stu-id="16968-125">8a5c99e9-2230-46eb-b8e8-e59d712eb9ee</span></span>                                                                                            |
| <span data-ttu-id="16968-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16968-126">Syntax</span></span>            | [<span data-ttu-id="16968-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="16968-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="16968-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="16968-128">Implementations</span></span>

-   [<span data-ttu-id="16968-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="16968-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="16968-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="16968-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="16968-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="16968-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="16968-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="16968-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="16968-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="16968-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="16968-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16968-134">Windows Server 2003</span></span>



| <span data-ttu-id="16968-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="16968-135">Entry</span></span> | <span data-ttu-id="16968-136">Значение</span><span class="sxs-lookup"><span data-stu-id="16968-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16968-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16968-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16968-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="16968-139">System-Only</span></span>            | <span data-ttu-id="16968-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-140">False</span></span>                             |
| <span data-ttu-id="16968-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16968-141">Is-Single-Valued</span></span>       | <span data-ttu-id="16968-142">True</span><span class="sxs-lookup"><span data-stu-id="16968-142">True</span></span>                              |
| <span data-ttu-id="16968-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16968-143">Is Indexed</span></span>             | <span data-ttu-id="16968-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-144">False</span></span>                             |
| <span data-ttu-id="16968-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16968-145">In Global Catalog</span></span>      | <span data-ttu-id="16968-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-146">False</span></span>                             |
| <span data-ttu-id="16968-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16968-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="16968-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16968-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16968-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16968-149">Range-Lower</span></span>            | <span data-ttu-id="16968-150">1</span><span class="sxs-lookup"><span data-stu-id="16968-150">1</span></span>                                 |
| <span data-ttu-id="16968-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16968-151">Range-Upper</span></span>            | <span data-ttu-id="16968-152">256</span><span class="sxs-lookup"><span data-stu-id="16968-152">256</span></span>                               |
| <span data-ttu-id="16968-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-153">Search-Flags</span></span>           | <span data-ttu-id="16968-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16968-154">0x00000000</span></span>                        |
| <span data-ttu-id="16968-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-155">System-Flags</span></span>           | <span data-ttu-id="16968-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16968-156">0x00000010</span></span>                        |
| <span data-ttu-id="16968-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16968-157">Classes used in</span></span>        | [<span data-ttu-id="16968-158">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="16968-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="16968-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="16968-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="16968-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="16968-160">Entry</span></span> | <span data-ttu-id="16968-161">Значение</span><span class="sxs-lookup"><span data-stu-id="16968-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16968-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16968-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16968-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="16968-164">System-Only</span></span>            | <span data-ttu-id="16968-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-165">False</span></span>                             |
| <span data-ttu-id="16968-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16968-166">Is-Single-Valued</span></span>       | <span data-ttu-id="16968-167">True</span><span class="sxs-lookup"><span data-stu-id="16968-167">True</span></span>                              |
| <span data-ttu-id="16968-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16968-168">Is Indexed</span></span>             | <span data-ttu-id="16968-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-169">False</span></span>                             |
| <span data-ttu-id="16968-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16968-170">In Global Catalog</span></span>      | <span data-ttu-id="16968-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-171">False</span></span>                             |
| <span data-ttu-id="16968-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16968-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="16968-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16968-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16968-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16968-174">Range-Lower</span></span>            | <span data-ttu-id="16968-175">1</span><span class="sxs-lookup"><span data-stu-id="16968-175">1</span></span>                                 |
| <span data-ttu-id="16968-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16968-176">Range-Upper</span></span>            | <span data-ttu-id="16968-177">256</span><span class="sxs-lookup"><span data-stu-id="16968-177">256</span></span>                               |
| <span data-ttu-id="16968-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-178">Search-Flags</span></span>           | <span data-ttu-id="16968-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16968-179">0x00000000</span></span>                        |
| <span data-ttu-id="16968-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-180">System-Flags</span></span>           | <span data-ttu-id="16968-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16968-181">0x00000010</span></span>                        |
| <span data-ttu-id="16968-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16968-182">Classes used in</span></span>        | [<span data-ttu-id="16968-183">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="16968-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="16968-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16968-184">Windows Server 2008</span></span>



| <span data-ttu-id="16968-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="16968-185">Entry</span></span> | <span data-ttu-id="16968-186">Значение</span><span class="sxs-lookup"><span data-stu-id="16968-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16968-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16968-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16968-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="16968-189">System-Only</span></span>            | <span data-ttu-id="16968-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-190">False</span></span>                             |
| <span data-ttu-id="16968-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16968-191">Is-Single-Valued</span></span>       | <span data-ttu-id="16968-192">True</span><span class="sxs-lookup"><span data-stu-id="16968-192">True</span></span>                              |
| <span data-ttu-id="16968-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16968-193">Is Indexed</span></span>             | <span data-ttu-id="16968-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-194">False</span></span>                             |
| <span data-ttu-id="16968-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16968-195">In Global Catalog</span></span>      | <span data-ttu-id="16968-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-196">False</span></span>                             |
| <span data-ttu-id="16968-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16968-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="16968-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16968-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16968-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16968-199">Range-Lower</span></span>            | <span data-ttu-id="16968-200">1</span><span class="sxs-lookup"><span data-stu-id="16968-200">1</span></span>                                 |
| <span data-ttu-id="16968-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16968-201">Range-Upper</span></span>            | <span data-ttu-id="16968-202">256</span><span class="sxs-lookup"><span data-stu-id="16968-202">256</span></span>                               |
| <span data-ttu-id="16968-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-203">Search-Flags</span></span>           | <span data-ttu-id="16968-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16968-204">0x00000000</span></span>                        |
| <span data-ttu-id="16968-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-205">System-Flags</span></span>           | <span data-ttu-id="16968-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16968-206">0x00000010</span></span>                        |
| <span data-ttu-id="16968-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16968-207">Classes used in</span></span>        | [<span data-ttu-id="16968-208">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="16968-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="16968-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16968-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="16968-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="16968-210">Entry</span></span> | <span data-ttu-id="16968-211">Значение</span><span class="sxs-lookup"><span data-stu-id="16968-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16968-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16968-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16968-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="16968-214">System-Only</span></span>            | <span data-ttu-id="16968-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-215">False</span></span>                             |
| <span data-ttu-id="16968-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16968-216">Is-Single-Valued</span></span>       | <span data-ttu-id="16968-217">True</span><span class="sxs-lookup"><span data-stu-id="16968-217">True</span></span>                              |
| <span data-ttu-id="16968-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16968-218">Is Indexed</span></span>             | <span data-ttu-id="16968-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-219">False</span></span>                             |
| <span data-ttu-id="16968-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16968-220">In Global Catalog</span></span>      | <span data-ttu-id="16968-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-221">False</span></span>                             |
| <span data-ttu-id="16968-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16968-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="16968-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16968-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16968-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16968-224">Range-Lower</span></span>            | <span data-ttu-id="16968-225">1</span><span class="sxs-lookup"><span data-stu-id="16968-225">1</span></span>                                 |
| <span data-ttu-id="16968-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16968-226">Range-Upper</span></span>            | <span data-ttu-id="16968-227">256</span><span class="sxs-lookup"><span data-stu-id="16968-227">256</span></span>                               |
| <span data-ttu-id="16968-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-228">Search-Flags</span></span>           | <span data-ttu-id="16968-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16968-229">0x00000000</span></span>                        |
| <span data-ttu-id="16968-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-230">System-Flags</span></span>           | <span data-ttu-id="16968-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16968-231">0x00000010</span></span>                        |
| <span data-ttu-id="16968-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16968-232">Classes used in</span></span>        | [<span data-ttu-id="16968-233">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="16968-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="16968-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16968-234">Windows Server 2012</span></span>



| <span data-ttu-id="16968-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="16968-235">Entry</span></span> | <span data-ttu-id="16968-236">Значение</span><span class="sxs-lookup"><span data-stu-id="16968-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="16968-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="16968-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="16968-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="16968-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="16968-239">System-Only</span></span>            | <span data-ttu-id="16968-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-240">False</span></span>                             |
| <span data-ttu-id="16968-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="16968-241">Is-Single-Valued</span></span>       | <span data-ttu-id="16968-242">True</span><span class="sxs-lookup"><span data-stu-id="16968-242">True</span></span>                              |
| <span data-ttu-id="16968-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="16968-243">Is Indexed</span></span>             | <span data-ttu-id="16968-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-244">False</span></span>                             |
| <span data-ttu-id="16968-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="16968-245">In Global Catalog</span></span>      | <span data-ttu-id="16968-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="16968-246">False</span></span>                             |
| <span data-ttu-id="16968-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="16968-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="16968-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="16968-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="16968-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="16968-249">Range-Lower</span></span>            | <span data-ttu-id="16968-250">1</span><span class="sxs-lookup"><span data-stu-id="16968-250">1</span></span>                                 |
| <span data-ttu-id="16968-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="16968-251">Range-Upper</span></span>            | <span data-ttu-id="16968-252">256</span><span class="sxs-lookup"><span data-stu-id="16968-252">256</span></span>                               |
| <span data-ttu-id="16968-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-253">Search-Flags</span></span>           | <span data-ttu-id="16968-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="16968-254">0x00000000</span></span>                        |
| <span data-ttu-id="16968-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="16968-255">System-Flags</span></span>           | <span data-ttu-id="16968-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="16968-256">0x00000010</span></span>                        |
| <span data-ttu-id="16968-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="16968-257">Classes used in</span></span>        | [<span data-ttu-id="16968-258">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="16968-258">**User**</span></span>](c-user.md)<br/> |



 

 





