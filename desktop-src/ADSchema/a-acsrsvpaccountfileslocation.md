---
title: Атрибут расположения ACS-RSVP-Account-Files-Location
description: Расположение файлов учетной записи RSVP в каталоге. По умолчанию используется \ 0034; system32 \ 0034; подкаталог, расположенный в системном каталоге по умолчанию.
ms.assetid: 84303766-0d17-4728-aa61-6a5377b7de04
ms.tgt_platform: multiple
keywords:
- ACS-RSVP-Account-Files-схема AD атрибута Location
- Схема AD атрибута Аксрсвпаккаунтфилеслокатион
topic_type:
- apiref
api_name:
- ACS-RSVP-Account-Files-Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40876018ffeeacc49fe666ab1a9d69363edb73c4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893997"
---
# <a name="acs-rsvp-account-files-location-attribute"></a><span data-ttu-id="fbfce-106">Атрибут расположения ACS-RSVP-Account-Files-Location</span><span class="sxs-lookup"><span data-stu-id="fbfce-106">ACS-RSVP-Account-Files-Location attribute</span></span>

<span data-ttu-id="fbfce-107">Расположение файлов учетной записи RSVP в каталоге.</span><span class="sxs-lookup"><span data-stu-id="fbfce-107">The directory location of RSVP account files.</span></span> <span data-ttu-id="fbfce-108">По умолчанию используется подкаталог System32, расположенный в системном каталоге по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbfce-108">Defaults to the "system32" subdirectory located in the default system directory.</span></span>



| <span data-ttu-id="fbfce-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-109">Entry</span></span> | <span data-ttu-id="fbfce-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="fbfce-111">CN</span><span class="sxs-lookup"><span data-stu-id="fbfce-111">CN</span></span>                | <span data-ttu-id="fbfce-112">ACS-RSVP-Account-Files-Location</span><span class="sxs-lookup"><span data-stu-id="fbfce-112">ACS-RSVP-Account-Files-Location</span></span>             |
| <span data-ttu-id="fbfce-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fbfce-113">Ldap-Display-Name</span></span> | <span data-ttu-id="fbfce-114">аксрсвпаккаунтфилеслокатион</span><span class="sxs-lookup"><span data-stu-id="fbfce-114">aCSRSVPAccountFilesLocation</span></span>                 |
| <span data-ttu-id="fbfce-115">Размер</span><span class="sxs-lookup"><span data-stu-id="fbfce-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="fbfce-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fbfce-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="fbfce-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fbfce-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="fbfce-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-118">Attribute-Id</span></span>      | <span data-ttu-id="fbfce-119">1.2.840.113556.1.4.900</span><span class="sxs-lookup"><span data-stu-id="fbfce-119">1.2.840.113556.1.4.900</span></span>                      |
| <span data-ttu-id="fbfce-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fbfce-120">System-Id-Guid</span></span>    | <span data-ttu-id="fbfce-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="fbfce-121">f072230f-aef5-11d1-bdcf-0000f80367c1</span></span>        |
| <span data-ttu-id="fbfce-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbfce-122">Syntax</span></span>            | [<span data-ttu-id="fbfce-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="fbfce-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="fbfce-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fbfce-124">Implementations</span></span>

-   [<span data-ttu-id="fbfce-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="fbfce-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="fbfce-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fbfce-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fbfce-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fbfce-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fbfce-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fbfce-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fbfce-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fbfce-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fbfce-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fbfce-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="fbfce-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fbfce-131">Windows 2000 Server</span></span>



| <span data-ttu-id="fbfce-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-132">Entry</span></span> | <span data-ttu-id="fbfce-133">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfce-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfce-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfce-136">System-Only</span></span>            | <span data-ttu-id="fbfce-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-137">False</span></span>                                        |
| <span data-ttu-id="fbfce-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfce-138">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfce-139">True</span><span class="sxs-lookup"><span data-stu-id="fbfce-139">True</span></span>                                         |
| <span data-ttu-id="fbfce-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfce-140">Is Indexed</span></span>             | <span data-ttu-id="fbfce-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-141">False</span></span>                                        |
| <span data-ttu-id="fbfce-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfce-142">In Global Catalog</span></span>      | <span data-ttu-id="fbfce-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-143">False</span></span>                                        |
| <span data-ttu-id="fbfce-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfce-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfce-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfce-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfce-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfce-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfce-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-148">Search-Flags</span></span>           | <span data-ttu-id="fbfce-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfce-149">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfce-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-150">System-Flags</span></span>           | <span data-ttu-id="fbfce-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfce-151">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfce-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfce-152">Classes used in</span></span>        | [<span data-ttu-id="fbfce-153">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="fbfce-153">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="fbfce-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbfce-154">Windows Server 2003</span></span>



| <span data-ttu-id="fbfce-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-155">Entry</span></span> | <span data-ttu-id="fbfce-156">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfce-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfce-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfce-159">System-Only</span></span>            | <span data-ttu-id="fbfce-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-160">False</span></span>                                        |
| <span data-ttu-id="fbfce-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfce-161">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfce-162">True</span><span class="sxs-lookup"><span data-stu-id="fbfce-162">True</span></span>                                         |
| <span data-ttu-id="fbfce-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfce-163">Is Indexed</span></span>             | <span data-ttu-id="fbfce-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-164">False</span></span>                                        |
| <span data-ttu-id="fbfce-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfce-165">In Global Catalog</span></span>      | <span data-ttu-id="fbfce-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-166">False</span></span>                                        |
| <span data-ttu-id="fbfce-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfce-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfce-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfce-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfce-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfce-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfce-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-171">Search-Flags</span></span>           | <span data-ttu-id="fbfce-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfce-172">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfce-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-173">System-Flags</span></span>           | <span data-ttu-id="fbfce-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfce-174">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfce-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfce-175">Classes used in</span></span>        | [<span data-ttu-id="fbfce-176">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="fbfce-176">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fbfce-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fbfce-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fbfce-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-178">Entry</span></span> | <span data-ttu-id="fbfce-179">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfce-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfce-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfce-182">System-Only</span></span>            | <span data-ttu-id="fbfce-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-183">False</span></span>                                        |
| <span data-ttu-id="fbfce-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfce-184">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfce-185">True</span><span class="sxs-lookup"><span data-stu-id="fbfce-185">True</span></span>                                         |
| <span data-ttu-id="fbfce-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfce-186">Is Indexed</span></span>             | <span data-ttu-id="fbfce-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-187">False</span></span>                                        |
| <span data-ttu-id="fbfce-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfce-188">In Global Catalog</span></span>      | <span data-ttu-id="fbfce-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-189">False</span></span>                                        |
| <span data-ttu-id="fbfce-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfce-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfce-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfce-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfce-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfce-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfce-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-194">Search-Flags</span></span>           | <span data-ttu-id="fbfce-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfce-195">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfce-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-196">System-Flags</span></span>           | <span data-ttu-id="fbfce-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfce-197">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfce-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfce-198">Classes used in</span></span>        | [<span data-ttu-id="fbfce-199">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="fbfce-199">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fbfce-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbfce-200">Windows Server 2008</span></span>



| <span data-ttu-id="fbfce-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-201">Entry</span></span> | <span data-ttu-id="fbfce-202">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfce-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfce-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfce-205">System-Only</span></span>            | <span data-ttu-id="fbfce-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-206">False</span></span>                                        |
| <span data-ttu-id="fbfce-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfce-207">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfce-208">True</span><span class="sxs-lookup"><span data-stu-id="fbfce-208">True</span></span>                                         |
| <span data-ttu-id="fbfce-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfce-209">Is Indexed</span></span>             | <span data-ttu-id="fbfce-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-210">False</span></span>                                        |
| <span data-ttu-id="fbfce-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfce-211">In Global Catalog</span></span>      | <span data-ttu-id="fbfce-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-212">False</span></span>                                        |
| <span data-ttu-id="fbfce-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfce-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfce-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfce-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfce-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfce-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfce-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-217">Search-Flags</span></span>           | <span data-ttu-id="fbfce-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfce-218">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfce-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-219">System-Flags</span></span>           | <span data-ttu-id="fbfce-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfce-220">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfce-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfce-221">Classes used in</span></span>        | [<span data-ttu-id="fbfce-222">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="fbfce-222">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fbfce-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbfce-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fbfce-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-224">Entry</span></span> | <span data-ttu-id="fbfce-225">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfce-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfce-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfce-228">System-Only</span></span>            | <span data-ttu-id="fbfce-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-229">False</span></span>                                        |
| <span data-ttu-id="fbfce-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfce-230">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfce-231">True</span><span class="sxs-lookup"><span data-stu-id="fbfce-231">True</span></span>                                         |
| <span data-ttu-id="fbfce-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfce-232">Is Indexed</span></span>             | <span data-ttu-id="fbfce-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-233">False</span></span>                                        |
| <span data-ttu-id="fbfce-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfce-234">In Global Catalog</span></span>      | <span data-ttu-id="fbfce-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-235">False</span></span>                                        |
| <span data-ttu-id="fbfce-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfce-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfce-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfce-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfce-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfce-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfce-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-240">Search-Flags</span></span>           | <span data-ttu-id="fbfce-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfce-241">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfce-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-242">System-Flags</span></span>           | <span data-ttu-id="fbfce-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfce-243">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfce-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfce-244">Classes used in</span></span>        | [<span data-ttu-id="fbfce-245">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="fbfce-245">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fbfce-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbfce-246">Windows Server 2012</span></span>



| <span data-ttu-id="fbfce-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfce-247">Entry</span></span> | <span data-ttu-id="fbfce-248">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfce-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfce-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfce-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfce-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfce-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfce-251">System-Only</span></span>            | <span data-ttu-id="fbfce-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-252">False</span></span>                                        |
| <span data-ttu-id="fbfce-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfce-253">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfce-254">True</span><span class="sxs-lookup"><span data-stu-id="fbfce-254">True</span></span>                                         |
| <span data-ttu-id="fbfce-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfce-255">Is Indexed</span></span>             | <span data-ttu-id="fbfce-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-256">False</span></span>                                        |
| <span data-ttu-id="fbfce-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfce-257">In Global Catalog</span></span>      | <span data-ttu-id="fbfce-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfce-258">False</span></span>                                        |
| <span data-ttu-id="fbfce-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfce-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfce-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfce-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfce-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfce-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfce-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfce-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-263">Search-Flags</span></span>           | <span data-ttu-id="fbfce-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfce-264">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfce-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfce-265">System-Flags</span></span>           | <span data-ttu-id="fbfce-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfce-266">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfce-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfce-267">Classes used in</span></span>        | [<span data-ttu-id="fbfce-268">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="fbfce-268">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





