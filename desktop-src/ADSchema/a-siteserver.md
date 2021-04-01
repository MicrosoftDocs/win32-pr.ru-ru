---
title: Атрибут Site-Server
description: Лицензирование основного сервера для данного сайта.
ms.assetid: bcae8c63-a953-4721-b2d1-96d0376592c6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Site-Server
- Схема AD атрибута siteServer
topic_type:
- apiref
api_name:
- Site-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785057cd9ea23c05d58541450dc4c92a502877e5
ms.sourcegitcommit: f10bb95039c20a9de79f21e3fcb93a543f30a00e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "104262278"
---
# <a name="site-server-attribute"></a><span data-ttu-id="38a80-105">Атрибут Site-Server</span><span class="sxs-lookup"><span data-stu-id="38a80-105">Site-Server attribute</span></span>

<span data-ttu-id="38a80-106">Лицензирование основного сервера для данного сайта.</span><span class="sxs-lookup"><span data-stu-id="38a80-106">Licensing main server for a given Site.</span></span>



| <span data-ttu-id="38a80-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-107">Entry</span></span> | <span data-ttu-id="38a80-108">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-108">Value</span></span> |
|-------------------|----------------------------------------------|
| <span data-ttu-id="38a80-109">CN</span><span class="sxs-lookup"><span data-stu-id="38a80-109">CN</span></span>                | <span data-ttu-id="38a80-110">Site-Server</span><span class="sxs-lookup"><span data-stu-id="38a80-110">Site-Server</span></span>                                  |
| <span data-ttu-id="38a80-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="38a80-111">Ldap-Display-Name</span></span> | <span data-ttu-id="38a80-112">siteServer</span><span class="sxs-lookup"><span data-stu-id="38a80-112">siteServer</span></span>                                   |
| <span data-ttu-id="38a80-113">Размер</span><span class="sxs-lookup"><span data-stu-id="38a80-113">Size</span></span>              | \-                                           |
| <span data-ttu-id="38a80-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="38a80-114">Update Privilege</span></span>  | <span data-ttu-id="38a80-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="38a80-115">Domain administrator</span></span>                         |
| <span data-ttu-id="38a80-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="38a80-116">Update Frequency</span></span>  | <span data-ttu-id="38a80-117">Каждый раз, когда необходимо изменить сайт лицензирования.</span><span class="sxs-lookup"><span data-stu-id="38a80-117">Whenever the licensing site needs to change.</span></span> |
| <span data-ttu-id="38a80-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-118">Attribute-Id</span></span>      | <span data-ttu-id="38a80-119">1.2.840.113556.1.4.494</span><span class="sxs-lookup"><span data-stu-id="38a80-119">1.2.840.113556.1.4.494</span></span>                       |
| <span data-ttu-id="38a80-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="38a80-120">System-Id-Guid</span></span>    | <span data-ttu-id="38a80-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="38a80-121">1be8f17c-a9ff-11d0-afe2-00c04fd930c9</span></span>         |
| <span data-ttu-id="38a80-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38a80-122">Syntax</span></span>            | [<span data-ttu-id="38a80-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="38a80-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)      |



## <a name="implementations"></a><span data-ttu-id="38a80-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="38a80-124">Implementations</span></span>

-   [<span data-ttu-id="38a80-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="38a80-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="38a80-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="38a80-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="38a80-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="38a80-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="38a80-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="38a80-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="38a80-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="38a80-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="38a80-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="38a80-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="38a80-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="38a80-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="38a80-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="38a80-132">Windows 2000 Server</span></span>



| <span data-ttu-id="38a80-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-133">Entry</span></span> | <span data-ttu-id="38a80-134">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38a80-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-135">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-136">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-137">System-Only</span></span>            | <span data-ttu-id="38a80-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-138">False</span></span>                                                                 |
| <span data-ttu-id="38a80-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-139">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-140">False</span></span>                                                                 |
| <span data-ttu-id="38a80-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-141">Is Indexed</span></span>             | <span data-ttu-id="38a80-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-142">False</span></span>                                                                 |
| <span data-ttu-id="38a80-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-143">In Global Catalog</span></span>      | <span data-ttu-id="38a80-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-144">False</span></span>                                                                 |
| <span data-ttu-id="38a80-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-146">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="38a80-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-147">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-148">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-149">Search-Flags</span></span>           | <span data-ttu-id="38a80-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-150">0x00000000</span></span>                                                            |
| <span data-ttu-id="38a80-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-151">System-Flags</span></span>           | <span data-ttu-id="38a80-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-152">0x00000010</span></span>                                                            |
| <span data-ttu-id="38a80-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-153">Classes used in</span></span>        | [<span data-ttu-id="38a80-154">**Лицензирование-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="38a80-154">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="38a80-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38a80-155">Windows Server 2003</span></span>



| <span data-ttu-id="38a80-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-156">Entry</span></span> | <span data-ttu-id="38a80-157">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38a80-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-158">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-159">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-160">System-Only</span></span>            | <span data-ttu-id="38a80-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-161">False</span></span>                                                                 |
| <span data-ttu-id="38a80-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-162">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-163">False</span></span>                                                                 |
| <span data-ttu-id="38a80-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-164">Is Indexed</span></span>             | <span data-ttu-id="38a80-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-165">False</span></span>                                                                 |
| <span data-ttu-id="38a80-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-166">In Global Catalog</span></span>      | <span data-ttu-id="38a80-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-167">False</span></span>                                                                 |
| <span data-ttu-id="38a80-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-169">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="38a80-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-170">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-171">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-172">Search-Flags</span></span>           | <span data-ttu-id="38a80-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-173">0x00000000</span></span>                                                            |
| <span data-ttu-id="38a80-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-174">System-Flags</span></span>           | <span data-ttu-id="38a80-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-175">0x00000010</span></span>                                                            |
| <span data-ttu-id="38a80-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-176">Classes used in</span></span>        | [<span data-ttu-id="38a80-177">**Лицензирование-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="38a80-177">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="adam"></a><span data-ttu-id="38a80-178">ADAM</span><span class="sxs-lookup"><span data-stu-id="38a80-178">ADAM</span></span>



| <span data-ttu-id="38a80-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-179">Entry</span></span> | <span data-ttu-id="38a80-180">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-180">Value</span></span> |
|------------------------|--------------|
| <span data-ttu-id="38a80-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-181">Link-Id</span></span>                | \-           |
| <span data-ttu-id="38a80-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-182">MAPI-Id</span></span>                | \-           |
| <span data-ttu-id="38a80-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-183">System-Only</span></span>            | <span data-ttu-id="38a80-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-184">False</span></span>        |
| <span data-ttu-id="38a80-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-185">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-186">False</span></span>        |
| <span data-ttu-id="38a80-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-187">Is Indexed</span></span>             | <span data-ttu-id="38a80-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-188">False</span></span>        |
| <span data-ttu-id="38a80-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-189">In Global Catalog</span></span>      | <span data-ttu-id="38a80-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-190">False</span></span>        |
| <span data-ttu-id="38a80-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-192">O:BAG:BAD:S:</span></span> |
| <span data-ttu-id="38a80-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-193">Range-Lower</span></span>            | \-           |
| <span data-ttu-id="38a80-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-194">Range-Upper</span></span>            | \-           |
| <span data-ttu-id="38a80-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-195">Search-Flags</span></span>           | <span data-ttu-id="38a80-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-196">0x00000000</span></span>   |
| <span data-ttu-id="38a80-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-197">System-Flags</span></span>           | <span data-ttu-id="38a80-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-198">0x00000010</span></span>   |
| <span data-ttu-id="38a80-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-199">Classes used in</span></span>        | \-           |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="38a80-200">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="38a80-200">Windows Server 2003 R2</span></span>



| <span data-ttu-id="38a80-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-201">Entry</span></span> | <span data-ttu-id="38a80-202">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-202">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38a80-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-203">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-204">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-205">System-Only</span></span>            | <span data-ttu-id="38a80-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-206">False</span></span>                                                                 |
| <span data-ttu-id="38a80-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-207">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-208">False</span></span>                                                                 |
| <span data-ttu-id="38a80-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-209">Is Indexed</span></span>             | <span data-ttu-id="38a80-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-210">False</span></span>                                                                 |
| <span data-ttu-id="38a80-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-211">In Global Catalog</span></span>      | <span data-ttu-id="38a80-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-212">False</span></span>                                                                 |
| <span data-ttu-id="38a80-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-214">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="38a80-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-215">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-216">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-217">Search-Flags</span></span>           | <span data-ttu-id="38a80-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-218">0x00000000</span></span>                                                            |
| <span data-ttu-id="38a80-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-219">System-Flags</span></span>           | <span data-ttu-id="38a80-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-220">0x00000010</span></span>                                                            |
| <span data-ttu-id="38a80-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-221">Classes used in</span></span>        | [<span data-ttu-id="38a80-222">**Лицензирование-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="38a80-222">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="38a80-223">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38a80-223">Windows Server 2008</span></span>



| <span data-ttu-id="38a80-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-224">Entry</span></span> | <span data-ttu-id="38a80-225">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-225">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38a80-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-226">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-227">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-228">System-Only</span></span>            | <span data-ttu-id="38a80-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-229">False</span></span>                                                                 |
| <span data-ttu-id="38a80-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-230">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-231">False</span></span>                                                                 |
| <span data-ttu-id="38a80-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-232">Is Indexed</span></span>             | <span data-ttu-id="38a80-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-233">False</span></span>                                                                 |
| <span data-ttu-id="38a80-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-234">In Global Catalog</span></span>      | <span data-ttu-id="38a80-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-235">False</span></span>                                                                 |
| <span data-ttu-id="38a80-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-237">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="38a80-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-238">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-239">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-240">Search-Flags</span></span>           | <span data-ttu-id="38a80-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-241">0x00000000</span></span>                                                            |
| <span data-ttu-id="38a80-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-242">System-Flags</span></span>           | <span data-ttu-id="38a80-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-243">0x00000010</span></span>                                                            |
| <span data-ttu-id="38a80-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-244">Classes used in</span></span>        | [<span data-ttu-id="38a80-245">**Лицензирование-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="38a80-245">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="38a80-246">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38a80-246">Windows Server 2008 R2</span></span>



| <span data-ttu-id="38a80-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-247">Entry</span></span> | <span data-ttu-id="38a80-248">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-248">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38a80-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-249">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-250">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-251">System-Only</span></span>            | <span data-ttu-id="38a80-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-252">False</span></span>                                                                 |
| <span data-ttu-id="38a80-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-253">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-254">False</span></span>                                                                 |
| <span data-ttu-id="38a80-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-255">Is Indexed</span></span>             | <span data-ttu-id="38a80-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-256">False</span></span>                                                                 |
| <span data-ttu-id="38a80-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-257">In Global Catalog</span></span>      | <span data-ttu-id="38a80-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-258">False</span></span>                                                                 |
| <span data-ttu-id="38a80-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-260">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="38a80-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-261">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-262">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-263">Search-Flags</span></span>           | <span data-ttu-id="38a80-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-264">0x00000000</span></span>                                                            |
| <span data-ttu-id="38a80-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-265">System-Flags</span></span>           | <span data-ttu-id="38a80-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-266">0x00000010</span></span>                                                            |
| <span data-ttu-id="38a80-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-267">Classes used in</span></span>        | [<span data-ttu-id="38a80-268">**Лицензирование-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="38a80-268">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="38a80-269">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="38a80-269">Windows Server 2012</span></span>



| <span data-ttu-id="38a80-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="38a80-270">Entry</span></span> | <span data-ttu-id="38a80-271">Значение</span><span class="sxs-lookup"><span data-stu-id="38a80-271">Value</span></span> |
|------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="38a80-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="38a80-272">Link-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="38a80-273">MAPI-Id</span></span>                | \-                                                                    |
| <span data-ttu-id="38a80-274">System-Only</span><span class="sxs-lookup"><span data-stu-id="38a80-274">System-Only</span></span>            | <span data-ttu-id="38a80-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-275">False</span></span>                                                                 |
| <span data-ttu-id="38a80-276">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="38a80-276">Is-Single-Valued</span></span>       | <span data-ttu-id="38a80-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-277">False</span></span>                                                                 |
| <span data-ttu-id="38a80-278">Индексируется</span><span class="sxs-lookup"><span data-stu-id="38a80-278">Is Indexed</span></span>             | <span data-ttu-id="38a80-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-279">False</span></span>                                                                 |
| <span data-ttu-id="38a80-280">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="38a80-280">In Global Catalog</span></span>      | <span data-ttu-id="38a80-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="38a80-281">False</span></span>                                                                 |
| <span data-ttu-id="38a80-282">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="38a80-282">NT-Security-Descriptor</span></span> | <span data-ttu-id="38a80-283">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="38a80-283">O:BAG:BAD:S:</span></span>                                                          |
| <span data-ttu-id="38a80-284">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="38a80-284">Range-Lower</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-285">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="38a80-285">Range-Upper</span></span>            | \-                                                                    |
| <span data-ttu-id="38a80-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-286">Search-Flags</span></span>           | <span data-ttu-id="38a80-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="38a80-287">0x00000000</span></span>                                                            |
| <span data-ttu-id="38a80-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="38a80-288">System-Flags</span></span>           | <span data-ttu-id="38a80-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="38a80-289">0x00000010</span></span>                                                            |
| <span data-ttu-id="38a80-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="38a80-290">Classes used in</span></span>        | [<span data-ttu-id="38a80-291">**Лицензирование-Site-Settings**</span><span class="sxs-lookup"><span data-stu-id="38a80-291">**Licensing-Site-Settings**</span></span>](c-licensingsitesettings.md)<br/> |



 

 





