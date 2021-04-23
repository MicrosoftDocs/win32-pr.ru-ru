---
title: Атрибут MSI-Script-Name
description: Имя файла скрипта установщика Microsoft Installer для этого приложения.
ms.assetid: f4666441-f416-4103-8ad5-6cdb6f4b0a97
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-Script-Name
- Схема AD атрибута Мсискриптнаме
topic_type:
- apiref
api_name:
- Msi-Script-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f155bd9a1dd62bdd72f5a589c6583742ebaa65
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655406"
---
# <a name="msi-script-name-attribute"></a><span data-ttu-id="0b2db-105">Атрибут MSI-Script-Name</span><span class="sxs-lookup"><span data-stu-id="0b2db-105">Msi-Script-Name attribute</span></span>

<span data-ttu-id="0b2db-106">Имя файла скрипта установщика Microsoft Installer для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="0b2db-106">The name for the Microsoft installer advertisement script file for this application.</span></span>



| <span data-ttu-id="0b2db-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-107">Entry</span></span> | <span data-ttu-id="0b2db-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0b2db-109">CN</span><span class="sxs-lookup"><span data-stu-id="0b2db-109">CN</span></span>                | <span data-ttu-id="0b2db-110">Имя MSI-Script-Name</span><span class="sxs-lookup"><span data-stu-id="0b2db-110">Msi-Script-Name</span></span>                             |
| <span data-ttu-id="0b2db-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0b2db-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0b2db-112">мсискриптнаме</span><span class="sxs-lookup"><span data-stu-id="0b2db-112">msiScriptName</span></span>                               |
| <span data-ttu-id="0b2db-113">Размер</span><span class="sxs-lookup"><span data-stu-id="0b2db-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="0b2db-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0b2db-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0b2db-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0b2db-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0b2db-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-116">Attribute-Id</span></span>      | <span data-ttu-id="0b2db-117">1.2.840.113556.1.4.845</span><span class="sxs-lookup"><span data-stu-id="0b2db-117">1.2.840.113556.1.4.845</span></span>                      |
| <span data-ttu-id="0b2db-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0b2db-118">System-Id-Guid</span></span>    | <span data-ttu-id="0b2db-119">96a7dd62-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="0b2db-119">96a7dd62-9118-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="0b2db-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b2db-120">Syntax</span></span>            | [<span data-ttu-id="0b2db-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="0b2db-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0b2db-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0b2db-122">Implementations</span></span>

-   [<span data-ttu-id="0b2db-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0b2db-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0b2db-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0b2db-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0b2db-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0b2db-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0b2db-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0b2db-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0b2db-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0b2db-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0b2db-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b2db-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0b2db-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0b2db-129">Windows 2000 Server</span></span>



| <span data-ttu-id="0b2db-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-130">Entry</span></span> | <span data-ttu-id="0b2db-131">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0b2db-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b2db-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b2db-134">System-Only</span></span>            | <span data-ttu-id="0b2db-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-135">False</span></span>                                                            |
| <span data-ttu-id="0b2db-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b2db-136">Is-Single-Valued</span></span>       | <span data-ttu-id="0b2db-137">True</span><span class="sxs-lookup"><span data-stu-id="0b2db-137">True</span></span>                                                             |
| <span data-ttu-id="0b2db-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b2db-138">Is Indexed</span></span>             | <span data-ttu-id="0b2db-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-139">False</span></span>                                                            |
| <span data-ttu-id="0b2db-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b2db-140">In Global Catalog</span></span>      | <span data-ttu-id="0b2db-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-141">False</span></span>                                                            |
| <span data-ttu-id="0b2db-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b2db-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b2db-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b2db-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0b2db-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b2db-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b2db-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-146">Search-Flags</span></span>           | <span data-ttu-id="0b2db-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b2db-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="0b2db-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-148">System-Flags</span></span>           | <span data-ttu-id="0b2db-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b2db-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="0b2db-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b2db-150">Classes used in</span></span>        | [<span data-ttu-id="0b2db-151">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="0b2db-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0b2db-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b2db-152">Windows Server 2003</span></span>



| <span data-ttu-id="0b2db-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-153">Entry</span></span> | <span data-ttu-id="0b2db-154">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0b2db-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b2db-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b2db-157">System-Only</span></span>            | <span data-ttu-id="0b2db-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-158">False</span></span>                                                            |
| <span data-ttu-id="0b2db-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b2db-159">Is-Single-Valued</span></span>       | <span data-ttu-id="0b2db-160">True</span><span class="sxs-lookup"><span data-stu-id="0b2db-160">True</span></span>                                                             |
| <span data-ttu-id="0b2db-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b2db-161">Is Indexed</span></span>             | <span data-ttu-id="0b2db-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-162">False</span></span>                                                            |
| <span data-ttu-id="0b2db-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b2db-163">In Global Catalog</span></span>      | <span data-ttu-id="0b2db-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-164">False</span></span>                                                            |
| <span data-ttu-id="0b2db-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b2db-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b2db-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b2db-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0b2db-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b2db-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b2db-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-169">Search-Flags</span></span>           | <span data-ttu-id="0b2db-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b2db-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="0b2db-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-171">System-Flags</span></span>           | <span data-ttu-id="0b2db-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b2db-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="0b2db-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b2db-173">Classes used in</span></span>        | [<span data-ttu-id="0b2db-174">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="0b2db-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0b2db-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0b2db-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0b2db-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-176">Entry</span></span> | <span data-ttu-id="0b2db-177">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0b2db-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b2db-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b2db-180">System-Only</span></span>            | <span data-ttu-id="0b2db-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-181">False</span></span>                                                            |
| <span data-ttu-id="0b2db-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b2db-182">Is-Single-Valued</span></span>       | <span data-ttu-id="0b2db-183">True</span><span class="sxs-lookup"><span data-stu-id="0b2db-183">True</span></span>                                                             |
| <span data-ttu-id="0b2db-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b2db-184">Is Indexed</span></span>             | <span data-ttu-id="0b2db-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-185">False</span></span>                                                            |
| <span data-ttu-id="0b2db-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b2db-186">In Global Catalog</span></span>      | <span data-ttu-id="0b2db-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-187">False</span></span>                                                            |
| <span data-ttu-id="0b2db-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b2db-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b2db-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b2db-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0b2db-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b2db-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b2db-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-192">Search-Flags</span></span>           | <span data-ttu-id="0b2db-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b2db-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="0b2db-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-194">System-Flags</span></span>           | <span data-ttu-id="0b2db-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b2db-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="0b2db-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b2db-196">Classes used in</span></span>        | [<span data-ttu-id="0b2db-197">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="0b2db-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0b2db-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b2db-198">Windows Server 2008</span></span>



| <span data-ttu-id="0b2db-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-199">Entry</span></span> | <span data-ttu-id="0b2db-200">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0b2db-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b2db-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b2db-203">System-Only</span></span>            | <span data-ttu-id="0b2db-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-204">False</span></span>                                                            |
| <span data-ttu-id="0b2db-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b2db-205">Is-Single-Valued</span></span>       | <span data-ttu-id="0b2db-206">True</span><span class="sxs-lookup"><span data-stu-id="0b2db-206">True</span></span>                                                             |
| <span data-ttu-id="0b2db-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b2db-207">Is Indexed</span></span>             | <span data-ttu-id="0b2db-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-208">False</span></span>                                                            |
| <span data-ttu-id="0b2db-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b2db-209">In Global Catalog</span></span>      | <span data-ttu-id="0b2db-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-210">False</span></span>                                                            |
| <span data-ttu-id="0b2db-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b2db-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b2db-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b2db-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0b2db-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b2db-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b2db-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-215">Search-Flags</span></span>           | <span data-ttu-id="0b2db-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b2db-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="0b2db-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-217">System-Flags</span></span>           | <span data-ttu-id="0b2db-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b2db-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="0b2db-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b2db-219">Classes used in</span></span>        | [<span data-ttu-id="0b2db-220">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="0b2db-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0b2db-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0b2db-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0b2db-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-222">Entry</span></span> | <span data-ttu-id="0b2db-223">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0b2db-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b2db-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b2db-226">System-Only</span></span>            | <span data-ttu-id="0b2db-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-227">False</span></span>                                                            |
| <span data-ttu-id="0b2db-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b2db-228">Is-Single-Valued</span></span>       | <span data-ttu-id="0b2db-229">True</span><span class="sxs-lookup"><span data-stu-id="0b2db-229">True</span></span>                                                             |
| <span data-ttu-id="0b2db-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b2db-230">Is Indexed</span></span>             | <span data-ttu-id="0b2db-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-231">False</span></span>                                                            |
| <span data-ttu-id="0b2db-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b2db-232">In Global Catalog</span></span>      | <span data-ttu-id="0b2db-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-233">False</span></span>                                                            |
| <span data-ttu-id="0b2db-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b2db-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b2db-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b2db-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0b2db-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b2db-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b2db-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-238">Search-Flags</span></span>           | <span data-ttu-id="0b2db-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b2db-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="0b2db-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-240">System-Flags</span></span>           | <span data-ttu-id="0b2db-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b2db-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="0b2db-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b2db-242">Classes used in</span></span>        | [<span data-ttu-id="0b2db-243">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="0b2db-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0b2db-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b2db-244">Windows Server 2012</span></span>



| <span data-ttu-id="0b2db-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b2db-245">Entry</span></span> | <span data-ttu-id="0b2db-246">Значение</span><span class="sxs-lookup"><span data-stu-id="0b2db-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="0b2db-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b2db-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b2db-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="0b2db-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b2db-249">System-Only</span></span>            | <span data-ttu-id="0b2db-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-250">False</span></span>                                                            |
| <span data-ttu-id="0b2db-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b2db-251">Is-Single-Valued</span></span>       | <span data-ttu-id="0b2db-252">True</span><span class="sxs-lookup"><span data-stu-id="0b2db-252">True</span></span>                                                             |
| <span data-ttu-id="0b2db-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b2db-253">Is Indexed</span></span>             | <span data-ttu-id="0b2db-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-254">False</span></span>                                                            |
| <span data-ttu-id="0b2db-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b2db-255">In Global Catalog</span></span>      | <span data-ttu-id="0b2db-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b2db-256">False</span></span>                                                            |
| <span data-ttu-id="0b2db-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b2db-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b2db-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b2db-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="0b2db-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b2db-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b2db-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="0b2db-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-261">Search-Flags</span></span>           | <span data-ttu-id="0b2db-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b2db-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="0b2db-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b2db-263">System-Flags</span></span>           | <span data-ttu-id="0b2db-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b2db-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="0b2db-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b2db-265">Classes used in</span></span>        | [<span data-ttu-id="0b2db-266">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="0b2db-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





