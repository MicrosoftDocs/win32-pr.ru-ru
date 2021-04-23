---
title: атрибут MS-IIS-FTP-root
description: Этот атрибут определяет общую папку файлового сервера. Он используется совместно с MS-IIS-FTP-dir для определения домашнего каталога пользователя FTP.
ms.assetid: b86dcafb-0b0d-4225-924c-690f739092a8
ms.tgt_platform: multiple
keywords:
- Схема AD корневого атрибута MS-IIS-FTP
- Схема AD атрибута Мсиис-Фтпрут
topic_type:
- apiref
api_name:
- ms-IIS-FTP-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c55980b8b08865889f7567fa6bdb4dcf7bde1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493998"
---
# <a name="ms-iis-ftp-root-attribute"></a><span data-ttu-id="4993c-106">атрибут MS-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="4993c-106">ms-IIS-FTP-Root attribute</span></span>

<span data-ttu-id="4993c-107">Этот атрибут определяет общую папку файлового сервера.</span><span class="sxs-lookup"><span data-stu-id="4993c-107">This attribute determines the file server share.</span></span> <span data-ttu-id="4993c-108">Он используется совместно с MS-IIS-FTP-dir для определения домашнего каталога пользователя FTP.</span><span class="sxs-lookup"><span data-stu-id="4993c-108">It is used in conjunction with ms-IIS-FTP-Dir to determine the FTP user home directory.</span></span>



| <span data-ttu-id="4993c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="4993c-109">Entry</span></span> | <span data-ttu-id="4993c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4993c-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4993c-111">CN</span><span class="sxs-lookup"><span data-stu-id="4993c-111">CN</span></span>                | <span data-ttu-id="4993c-112">MS-IIS-FTP-root</span><span class="sxs-lookup"><span data-stu-id="4993c-112">ms-IIS-FTP-Root</span></span>                                                                                                                 |
| <span data-ttu-id="4993c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4993c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4993c-114">Мсиис — Фтпрут</span><span class="sxs-lookup"><span data-stu-id="4993c-114">msIIS-FTPRoot</span></span>                                                                                                                   |
| <span data-ttu-id="4993c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="4993c-115">Size</span></span>              | <span data-ttu-id="4993c-116">30-50 символов (15-25 символов Юникода для каждого свойства)</span><span class="sxs-lookup"><span data-stu-id="4993c-116">30-50 characters (15-25 Unicode characters for each property)</span></span>                                                                   |
| <span data-ttu-id="4993c-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4993c-117">Update Privilege</span></span>  | <span data-ttu-id="4993c-118">Администратор домена & локальная система</span><span class="sxs-lookup"><span data-stu-id="4993c-118">Domain administrator & local system</span></span>                                                                                             |
| <span data-ttu-id="4993c-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4993c-119">Update Frequency</span></span>  | <span data-ttu-id="4993c-120">Это свойство задается, когда администратор создает веб-сайт и настраивает изоляцию FTP.</span><span class="sxs-lookup"><span data-stu-id="4993c-120">This property is set when the administrator creates the website and sets FTP isolation.</span></span> <span data-ttu-id="4993c-121">Это редко меняется после этого.</span><span class="sxs-lookup"><span data-stu-id="4993c-121">It's rarely going to change after that.</span></span> |
| <span data-ttu-id="4993c-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4993c-122">Attribute-Id</span></span>      | <span data-ttu-id="4993c-123">1.2.840.113556.1.4.1785</span><span class="sxs-lookup"><span data-stu-id="4993c-123">1.2.840.113556.1.4.1785</span></span>                                                                                                         |
| <span data-ttu-id="4993c-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4993c-124">System-Id-Guid</span></span>    | <span data-ttu-id="4993c-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span><span class="sxs-lookup"><span data-stu-id="4993c-125">2a7827a4-1483-49a5-9d84-52e3812156b4</span></span>                                                                                            |
| <span data-ttu-id="4993c-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4993c-126">Syntax</span></span>            | [<span data-ttu-id="4993c-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="4993c-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                     |



## <a name="implementations"></a><span data-ttu-id="4993c-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4993c-128">Implementations</span></span>

-   [<span data-ttu-id="4993c-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4993c-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4993c-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4993c-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4993c-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4993c-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4993c-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4993c-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4993c-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4993c-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4993c-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4993c-134">Windows Server 2003</span></span>



| <span data-ttu-id="4993c-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="4993c-135">Entry</span></span> | <span data-ttu-id="4993c-136">Значение</span><span class="sxs-lookup"><span data-stu-id="4993c-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4993c-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4993c-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4993c-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="4993c-139">System-Only</span></span>            | <span data-ttu-id="4993c-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-140">False</span></span>                             |
| <span data-ttu-id="4993c-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4993c-141">Is-Single-Valued</span></span>       | <span data-ttu-id="4993c-142">True</span><span class="sxs-lookup"><span data-stu-id="4993c-142">True</span></span>                              |
| <span data-ttu-id="4993c-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4993c-143">Is Indexed</span></span>             | <span data-ttu-id="4993c-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-144">False</span></span>                             |
| <span data-ttu-id="4993c-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4993c-145">In Global Catalog</span></span>      | <span data-ttu-id="4993c-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-146">False</span></span>                             |
| <span data-ttu-id="4993c-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4993c-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="4993c-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4993c-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4993c-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4993c-149">Range-Lower</span></span>            | <span data-ttu-id="4993c-150">1</span><span class="sxs-lookup"><span data-stu-id="4993c-150">1</span></span>                                 |
| <span data-ttu-id="4993c-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4993c-151">Range-Upper</span></span>            | <span data-ttu-id="4993c-152">256</span><span class="sxs-lookup"><span data-stu-id="4993c-152">256</span></span>                               |
| <span data-ttu-id="4993c-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-153">Search-Flags</span></span>           | <span data-ttu-id="4993c-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4993c-154">0x00000000</span></span>                        |
| <span data-ttu-id="4993c-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-155">System-Flags</span></span>           | <span data-ttu-id="4993c-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4993c-156">0x00000010</span></span>                        |
| <span data-ttu-id="4993c-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4993c-157">Classes used in</span></span>        | [<span data-ttu-id="4993c-158">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4993c-158">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4993c-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4993c-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4993c-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="4993c-160">Entry</span></span> | <span data-ttu-id="4993c-161">Значение</span><span class="sxs-lookup"><span data-stu-id="4993c-161">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4993c-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4993c-162">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4993c-163">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="4993c-164">System-Only</span></span>            | <span data-ttu-id="4993c-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-165">False</span></span>                             |
| <span data-ttu-id="4993c-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4993c-166">Is-Single-Valued</span></span>       | <span data-ttu-id="4993c-167">True</span><span class="sxs-lookup"><span data-stu-id="4993c-167">True</span></span>                              |
| <span data-ttu-id="4993c-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4993c-168">Is Indexed</span></span>             | <span data-ttu-id="4993c-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-169">False</span></span>                             |
| <span data-ttu-id="4993c-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4993c-170">In Global Catalog</span></span>      | <span data-ttu-id="4993c-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-171">False</span></span>                             |
| <span data-ttu-id="4993c-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4993c-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="4993c-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4993c-173">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4993c-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4993c-174">Range-Lower</span></span>            | <span data-ttu-id="4993c-175">1</span><span class="sxs-lookup"><span data-stu-id="4993c-175">1</span></span>                                 |
| <span data-ttu-id="4993c-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4993c-176">Range-Upper</span></span>            | <span data-ttu-id="4993c-177">256</span><span class="sxs-lookup"><span data-stu-id="4993c-177">256</span></span>                               |
| <span data-ttu-id="4993c-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-178">Search-Flags</span></span>           | <span data-ttu-id="4993c-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4993c-179">0x00000000</span></span>                        |
| <span data-ttu-id="4993c-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-180">System-Flags</span></span>           | <span data-ttu-id="4993c-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4993c-181">0x00000010</span></span>                        |
| <span data-ttu-id="4993c-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4993c-182">Classes used in</span></span>        | [<span data-ttu-id="4993c-183">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4993c-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4993c-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4993c-184">Windows Server 2008</span></span>



| <span data-ttu-id="4993c-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="4993c-185">Entry</span></span> | <span data-ttu-id="4993c-186">Значение</span><span class="sxs-lookup"><span data-stu-id="4993c-186">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4993c-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4993c-187">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4993c-188">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="4993c-189">System-Only</span></span>            | <span data-ttu-id="4993c-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-190">False</span></span>                             |
| <span data-ttu-id="4993c-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4993c-191">Is-Single-Valued</span></span>       | <span data-ttu-id="4993c-192">True</span><span class="sxs-lookup"><span data-stu-id="4993c-192">True</span></span>                              |
| <span data-ttu-id="4993c-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4993c-193">Is Indexed</span></span>             | <span data-ttu-id="4993c-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-194">False</span></span>                             |
| <span data-ttu-id="4993c-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4993c-195">In Global Catalog</span></span>      | <span data-ttu-id="4993c-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-196">False</span></span>                             |
| <span data-ttu-id="4993c-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4993c-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="4993c-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4993c-198">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4993c-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4993c-199">Range-Lower</span></span>            | <span data-ttu-id="4993c-200">1</span><span class="sxs-lookup"><span data-stu-id="4993c-200">1</span></span>                                 |
| <span data-ttu-id="4993c-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4993c-201">Range-Upper</span></span>            | <span data-ttu-id="4993c-202">256</span><span class="sxs-lookup"><span data-stu-id="4993c-202">256</span></span>                               |
| <span data-ttu-id="4993c-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-203">Search-Flags</span></span>           | <span data-ttu-id="4993c-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4993c-204">0x00000000</span></span>                        |
| <span data-ttu-id="4993c-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-205">System-Flags</span></span>           | <span data-ttu-id="4993c-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4993c-206">0x00000010</span></span>                        |
| <span data-ttu-id="4993c-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4993c-207">Classes used in</span></span>        | [<span data-ttu-id="4993c-208">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4993c-208">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4993c-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4993c-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4993c-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="4993c-210">Entry</span></span> | <span data-ttu-id="4993c-211">Значение</span><span class="sxs-lookup"><span data-stu-id="4993c-211">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4993c-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4993c-212">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4993c-213">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="4993c-214">System-Only</span></span>            | <span data-ttu-id="4993c-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-215">False</span></span>                             |
| <span data-ttu-id="4993c-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4993c-216">Is-Single-Valued</span></span>       | <span data-ttu-id="4993c-217">True</span><span class="sxs-lookup"><span data-stu-id="4993c-217">True</span></span>                              |
| <span data-ttu-id="4993c-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4993c-218">Is Indexed</span></span>             | <span data-ttu-id="4993c-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-219">False</span></span>                             |
| <span data-ttu-id="4993c-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4993c-220">In Global Catalog</span></span>      | <span data-ttu-id="4993c-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-221">False</span></span>                             |
| <span data-ttu-id="4993c-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4993c-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="4993c-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4993c-223">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4993c-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4993c-224">Range-Lower</span></span>            | <span data-ttu-id="4993c-225">1</span><span class="sxs-lookup"><span data-stu-id="4993c-225">1</span></span>                                 |
| <span data-ttu-id="4993c-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4993c-226">Range-Upper</span></span>            | <span data-ttu-id="4993c-227">256</span><span class="sxs-lookup"><span data-stu-id="4993c-227">256</span></span>                               |
| <span data-ttu-id="4993c-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-228">Search-Flags</span></span>           | <span data-ttu-id="4993c-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4993c-229">0x00000000</span></span>                        |
| <span data-ttu-id="4993c-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-230">System-Flags</span></span>           | <span data-ttu-id="4993c-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4993c-231">0x00000010</span></span>                        |
| <span data-ttu-id="4993c-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4993c-232">Classes used in</span></span>        | [<span data-ttu-id="4993c-233">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4993c-233">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4993c-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4993c-234">Windows Server 2012</span></span>



| <span data-ttu-id="4993c-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="4993c-235">Entry</span></span> | <span data-ttu-id="4993c-236">Значение</span><span class="sxs-lookup"><span data-stu-id="4993c-236">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="4993c-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4993c-237">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4993c-238">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="4993c-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="4993c-239">System-Only</span></span>            | <span data-ttu-id="4993c-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-240">False</span></span>                             |
| <span data-ttu-id="4993c-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4993c-241">Is-Single-Valued</span></span>       | <span data-ttu-id="4993c-242">True</span><span class="sxs-lookup"><span data-stu-id="4993c-242">True</span></span>                              |
| <span data-ttu-id="4993c-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4993c-243">Is Indexed</span></span>             | <span data-ttu-id="4993c-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-244">False</span></span>                             |
| <span data-ttu-id="4993c-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4993c-245">In Global Catalog</span></span>      | <span data-ttu-id="4993c-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="4993c-246">False</span></span>                             |
| <span data-ttu-id="4993c-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4993c-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="4993c-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4993c-248">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="4993c-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4993c-249">Range-Lower</span></span>            | <span data-ttu-id="4993c-250">1</span><span class="sxs-lookup"><span data-stu-id="4993c-250">1</span></span>                                 |
| <span data-ttu-id="4993c-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4993c-251">Range-Upper</span></span>            | <span data-ttu-id="4993c-252">256</span><span class="sxs-lookup"><span data-stu-id="4993c-252">256</span></span>                               |
| <span data-ttu-id="4993c-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-253">Search-Flags</span></span>           | <span data-ttu-id="4993c-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4993c-254">0x00000000</span></span>                        |
| <span data-ttu-id="4993c-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4993c-255">System-Flags</span></span>           | <span data-ttu-id="4993c-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4993c-256">0x00000010</span></span>                        |
| <span data-ttu-id="4993c-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4993c-257">Classes used in</span></span>        | [<span data-ttu-id="4993c-258">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="4993c-258">**User**</span></span>](c-user.md)<br/> |



 

 





