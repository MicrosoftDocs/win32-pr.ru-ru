---
title: Атрибут Setup-Command
description: Этот атрибут указывает, требуется ли команда установки для настройки этого приложения.
ms.assetid: f6292605-b392-4de2-b0a0-cae3f0551184
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Setup-Command
- Схема AD атрибута Сетупкомманд
topic_type:
- apiref
api_name:
- Setup-Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acea4a714c4175b77812e05880e8d9e78ca6645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138767"
---
# <a name="setup-command-attribute"></a><span data-ttu-id="9e2c1-105">Атрибут Setup-Command</span><span class="sxs-lookup"><span data-stu-id="9e2c1-105">Setup-Command attribute</span></span>

<span data-ttu-id="9e2c1-106">Этот атрибут указывает, требуется ли команда установки для настройки этого приложения.</span><span class="sxs-lookup"><span data-stu-id="9e2c1-106">This attribute indicates whether a setup command is required to set up this application.</span></span>



| <span data-ttu-id="9e2c1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-107">Entry</span></span> | <span data-ttu-id="9e2c1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="9e2c1-109">CN</span><span class="sxs-lookup"><span data-stu-id="9e2c1-109">CN</span></span>                | <span data-ttu-id="9e2c1-110">Setup-Command</span><span class="sxs-lookup"><span data-stu-id="9e2c1-110">Setup-Command</span></span>                               |
| <span data-ttu-id="9e2c1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9e2c1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9e2c1-112">сетупкомманд</span><span class="sxs-lookup"><span data-stu-id="9e2c1-112">setupCommand</span></span>                                |
| <span data-ttu-id="9e2c1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="9e2c1-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="9e2c1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9e2c1-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="9e2c1-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9e2c1-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="9e2c1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-116">Attribute-Id</span></span>      | <span data-ttu-id="9e2c1-117">1.2.840.113556.1.4.325</span><span class="sxs-lookup"><span data-stu-id="9e2c1-117">1.2.840.113556.1.4.325</span></span>                      |
| <span data-ttu-id="9e2c1-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9e2c1-118">System-Id-Guid</span></span>    | <span data-ttu-id="9e2c1-119">7d6c0e97-7e20-11d0-afd6-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="9e2c1-119">7d6c0e97-7e20-11d0-afd6-00c04fd930c9</span></span>        |
| <span data-ttu-id="9e2c1-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e2c1-120">Syntax</span></span>            | [<span data-ttu-id="9e2c1-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="9e2c1-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9e2c1-122">Implementations</span></span>

-   [<span data-ttu-id="9e2c1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9e2c1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9e2c1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9e2c1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9e2c1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9e2c1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9e2c1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9e2c1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="9e2c1-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-130">Entry</span></span> | <span data-ttu-id="9e2c1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9e2c1-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9e2c1-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2c1-134">System-Only</span></span>            | <span data-ttu-id="9e2c1-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-135">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9e2c1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2c1-137">True</span><span class="sxs-lookup"><span data-stu-id="9e2c1-137">True</span></span>                                                             |
| <span data-ttu-id="9e2c1-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9e2c1-138">Is Indexed</span></span>             | <span data-ttu-id="9e2c1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-139">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9e2c1-140">In Global Catalog</span></span>      | <span data-ttu-id="9e2c1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-141">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9e2c1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2c1-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9e2c1-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9e2c1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2c1-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2c1-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-146">Search-Flags</span></span>           | <span data-ttu-id="9e2c1-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2c1-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="9e2c1-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-148">System-Flags</span></span>           | <span data-ttu-id="9e2c1-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2c1-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="9e2c1-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9e2c1-150">Classes used in</span></span>        | [<span data-ttu-id="9e2c1-151">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9e2c1-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e2c1-152">Windows Server 2003</span></span>



| <span data-ttu-id="9e2c1-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-153">Entry</span></span> | <span data-ttu-id="9e2c1-154">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9e2c1-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9e2c1-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2c1-157">System-Only</span></span>            | <span data-ttu-id="9e2c1-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-158">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9e2c1-159">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2c1-160">True</span><span class="sxs-lookup"><span data-stu-id="9e2c1-160">True</span></span>                                                             |
| <span data-ttu-id="9e2c1-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9e2c1-161">Is Indexed</span></span>             | <span data-ttu-id="9e2c1-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-162">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9e2c1-163">In Global Catalog</span></span>      | <span data-ttu-id="9e2c1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-164">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9e2c1-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2c1-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9e2c1-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9e2c1-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2c1-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2c1-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-169">Search-Flags</span></span>           | <span data-ttu-id="9e2c1-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2c1-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="9e2c1-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-171">System-Flags</span></span>           | <span data-ttu-id="9e2c1-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2c1-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="9e2c1-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9e2c1-173">Classes used in</span></span>        | [<span data-ttu-id="9e2c1-174">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9e2c1-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9e2c1-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9e2c1-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-176">Entry</span></span> | <span data-ttu-id="9e2c1-177">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9e2c1-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9e2c1-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2c1-180">System-Only</span></span>            | <span data-ttu-id="9e2c1-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-181">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9e2c1-182">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2c1-183">True</span><span class="sxs-lookup"><span data-stu-id="9e2c1-183">True</span></span>                                                             |
| <span data-ttu-id="9e2c1-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9e2c1-184">Is Indexed</span></span>             | <span data-ttu-id="9e2c1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-185">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9e2c1-186">In Global Catalog</span></span>      | <span data-ttu-id="9e2c1-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-187">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9e2c1-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2c1-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9e2c1-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9e2c1-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2c1-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2c1-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-192">Search-Flags</span></span>           | <span data-ttu-id="9e2c1-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2c1-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="9e2c1-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-194">System-Flags</span></span>           | <span data-ttu-id="9e2c1-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2c1-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="9e2c1-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9e2c1-196">Classes used in</span></span>        | [<span data-ttu-id="9e2c1-197">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9e2c1-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e2c1-198">Windows Server 2008</span></span>



| <span data-ttu-id="9e2c1-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-199">Entry</span></span> | <span data-ttu-id="9e2c1-200">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9e2c1-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9e2c1-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2c1-203">System-Only</span></span>            | <span data-ttu-id="9e2c1-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-204">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9e2c1-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2c1-206">True</span><span class="sxs-lookup"><span data-stu-id="9e2c1-206">True</span></span>                                                             |
| <span data-ttu-id="9e2c1-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9e2c1-207">Is Indexed</span></span>             | <span data-ttu-id="9e2c1-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-208">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9e2c1-209">In Global Catalog</span></span>      | <span data-ttu-id="9e2c1-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-210">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9e2c1-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2c1-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9e2c1-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9e2c1-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2c1-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2c1-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-215">Search-Flags</span></span>           | <span data-ttu-id="9e2c1-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2c1-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="9e2c1-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-217">System-Flags</span></span>           | <span data-ttu-id="9e2c1-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2c1-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="9e2c1-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9e2c1-219">Classes used in</span></span>        | [<span data-ttu-id="9e2c1-220">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9e2c1-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e2c1-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9e2c1-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-222">Entry</span></span> | <span data-ttu-id="9e2c1-223">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9e2c1-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9e2c1-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2c1-226">System-Only</span></span>            | <span data-ttu-id="9e2c1-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-227">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9e2c1-228">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2c1-229">True</span><span class="sxs-lookup"><span data-stu-id="9e2c1-229">True</span></span>                                                             |
| <span data-ttu-id="9e2c1-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9e2c1-230">Is Indexed</span></span>             | <span data-ttu-id="9e2c1-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-231">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9e2c1-232">In Global Catalog</span></span>      | <span data-ttu-id="9e2c1-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-233">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9e2c1-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2c1-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9e2c1-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9e2c1-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2c1-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2c1-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-238">Search-Flags</span></span>           | <span data-ttu-id="9e2c1-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2c1-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="9e2c1-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-240">System-Flags</span></span>           | <span data-ttu-id="9e2c1-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2c1-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="9e2c1-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9e2c1-242">Classes used in</span></span>        | [<span data-ttu-id="9e2c1-243">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9e2c1-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9e2c1-244">Windows Server 2012</span></span>



| <span data-ttu-id="9e2c1-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="9e2c1-245">Entry</span></span> | <span data-ttu-id="9e2c1-246">Значение</span><span class="sxs-lookup"><span data-stu-id="9e2c1-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="9e2c1-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9e2c1-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9e2c1-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="9e2c1-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="9e2c1-249">System-Only</span></span>            | <span data-ttu-id="9e2c1-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-250">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9e2c1-251">Is-Single-Valued</span></span>       | <span data-ttu-id="9e2c1-252">True</span><span class="sxs-lookup"><span data-stu-id="9e2c1-252">True</span></span>                                                             |
| <span data-ttu-id="9e2c1-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9e2c1-253">Is Indexed</span></span>             | <span data-ttu-id="9e2c1-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-254">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9e2c1-255">In Global Catalog</span></span>      | <span data-ttu-id="9e2c1-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="9e2c1-256">False</span></span>                                                            |
| <span data-ttu-id="9e2c1-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9e2c1-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="9e2c1-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9e2c1-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="9e2c1-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9e2c1-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9e2c1-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="9e2c1-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-261">Search-Flags</span></span>           | <span data-ttu-id="9e2c1-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9e2c1-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="9e2c1-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9e2c1-263">System-Flags</span></span>           | <span data-ttu-id="9e2c1-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9e2c1-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="9e2c1-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9e2c1-265">Classes used in</span></span>        | [<span data-ttu-id="9e2c1-266">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="9e2c1-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





