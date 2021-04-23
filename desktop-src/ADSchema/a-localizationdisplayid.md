---
title: Атрибут Localization-ID локализации
description: Используется для индексации в файле Extrts.mc для получения локализованного displayName для объектов в целях пользовательского интерфейса.
ms.assetid: ed99d499-0064-4832-81ad-75fb3c8c548d
ms.tgt_platform: multiple
keywords:
- Локализация — схема AD атрибута ID экрана
- Схема AD атрибута Локализатиондисплайид
topic_type:
- apiref
api_name:
- Localization-Display-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4d9453b04bd5c944784b68ff5e4442f00bf65f5
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804751"
---
# <a name="localization-display-id-attribute"></a><span data-ttu-id="5b851-105">Атрибут Localization-ID локализации</span><span class="sxs-lookup"><span data-stu-id="5b851-105">Localization-Display-Id attribute</span></span>

<span data-ttu-id="5b851-106">Используется для индексации в файле Extrts.mc для получения локализованного displayName для объектов в целях пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5b851-106">Used to index into the file Extrts.mc to get the localized displayName for the objects for UI purposes.</span></span>



| <span data-ttu-id="5b851-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-107">Entry</span></span> | <span data-ttu-id="5b851-108">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="5b851-109">CN</span><span class="sxs-lookup"><span data-stu-id="5b851-109">CN</span></span>                | <span data-ttu-id="5b851-110">Локализация — идентификатор экрана</span><span class="sxs-lookup"><span data-stu-id="5b851-110">Localization-Display-Id</span></span>              |
| <span data-ttu-id="5b851-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5b851-111">Ldap-Display-Name</span></span> | <span data-ttu-id="5b851-112">локализатиондисплайид</span><span class="sxs-lookup"><span data-stu-id="5b851-112">localizationDisplayId</span></span>                |
| <span data-ttu-id="5b851-113">Размер</span><span class="sxs-lookup"><span data-stu-id="5b851-113">Size</span></span>              | <span data-ttu-id="5b851-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="5b851-114">4 bytes</span></span>                              |
| <span data-ttu-id="5b851-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5b851-115">Update Privilege</span></span>  | <span data-ttu-id="5b851-116">Администратор схемы</span><span class="sxs-lookup"><span data-stu-id="5b851-116">Schema administrator</span></span>                 |
| <span data-ttu-id="5b851-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5b851-117">Update Frequency</span></span>  | <span data-ttu-id="5b851-118">Идентификатор никогда не должен изменяться.</span><span class="sxs-lookup"><span data-stu-id="5b851-118">An ID should never be changed.</span></span>       |
| <span data-ttu-id="5b851-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-119">Attribute-Id</span></span>      | <span data-ttu-id="5b851-120">1.2.840.113556.1.4.1353</span><span class="sxs-lookup"><span data-stu-id="5b851-120">1.2.840.113556.1.4.1353</span></span>              |
| <span data-ttu-id="5b851-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5b851-121">System-Id-Guid</span></span>    | <span data-ttu-id="5b851-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="5b851-122">a746f0d1-78d0-11d2-9916-0000f87a57d4</span></span> |
| <span data-ttu-id="5b851-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b851-123">Syntax</span></span>            | [<span data-ttu-id="5b851-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="5b851-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="5b851-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5b851-125">Implementations</span></span>

-   [<span data-ttu-id="5b851-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5b851-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5b851-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5b851-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5b851-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="5b851-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="5b851-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5b851-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5b851-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5b851-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5b851-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5b851-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5b851-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5b851-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5b851-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b851-133">Windows 2000 Server</span></span>



| <span data-ttu-id="5b851-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-134">Entry</span></span> | <span data-ttu-id="5b851-135">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-135">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-136">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-137">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-138">System-Only</span></span>            | <span data-ttu-id="5b851-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-139">False</span></span>                                                           |
| <span data-ttu-id="5b851-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-140">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-141">True</span><span class="sxs-lookup"><span data-stu-id="5b851-141">True</span></span>                                                            |
| <span data-ttu-id="5b851-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-142">Is Indexed</span></span>             | <span data-ttu-id="5b851-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-143">False</span></span>                                                           |
| <span data-ttu-id="5b851-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-144">In Global Catalog</span></span>      | <span data-ttu-id="5b851-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-145">False</span></span>                                                           |
| <span data-ttu-id="5b851-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-147">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-148">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-149">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-150">Search-Flags</span></span>           | <span data-ttu-id="5b851-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-151">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-152">System-Flags</span></span>           | <span data-ttu-id="5b851-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-153">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-154">Classes used in</span></span>        | [<span data-ttu-id="5b851-155">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-155">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5b851-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5b851-156">Windows Server 2003</span></span>



| <span data-ttu-id="5b851-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-157">Entry</span></span> | <span data-ttu-id="5b851-158">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-159">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-160">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-161">System-Only</span></span>            | <span data-ttu-id="5b851-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-162">False</span></span>                                                           |
| <span data-ttu-id="5b851-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-163">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-164">True</span><span class="sxs-lookup"><span data-stu-id="5b851-164">True</span></span>                                                            |
| <span data-ttu-id="5b851-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-165">Is Indexed</span></span>             | <span data-ttu-id="5b851-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-166">False</span></span>                                                           |
| <span data-ttu-id="5b851-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-167">In Global Catalog</span></span>      | <span data-ttu-id="5b851-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-168">False</span></span>                                                           |
| <span data-ttu-id="5b851-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-170">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-171">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-172">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-173">Search-Flags</span></span>           | <span data-ttu-id="5b851-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-174">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-175">System-Flags</span></span>           | <span data-ttu-id="5b851-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-176">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-177">Classes used in</span></span>        | [<span data-ttu-id="5b851-178">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-178">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="adam"></a><span data-ttu-id="5b851-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="5b851-179">ADAM</span></span>



| <span data-ttu-id="5b851-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-180">Entry</span></span> | <span data-ttu-id="5b851-181">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-182">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-183">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-184">System-Only</span></span>            | <span data-ttu-id="5b851-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-185">False</span></span>                                                           |
| <span data-ttu-id="5b851-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-186">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-187">True</span><span class="sxs-lookup"><span data-stu-id="5b851-187">True</span></span>                                                            |
| <span data-ttu-id="5b851-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-188">Is Indexed</span></span>             | <span data-ttu-id="5b851-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-189">False</span></span>                                                           |
| <span data-ttu-id="5b851-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-190">In Global Catalog</span></span>      | <span data-ttu-id="5b851-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-191">False</span></span>                                                           |
| <span data-ttu-id="5b851-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-193">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-194">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-195">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-196">Search-Flags</span></span>           | <span data-ttu-id="5b851-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-197">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-198">System-Flags</span></span>           | <span data-ttu-id="5b851-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-199">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-200">Classes used in</span></span>        | [<span data-ttu-id="5b851-201">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-201">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5b851-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5b851-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5b851-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-203">Entry</span></span> | <span data-ttu-id="5b851-204">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-204">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-205">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-206">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-207">System-Only</span></span>            | <span data-ttu-id="5b851-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-208">False</span></span>                                                           |
| <span data-ttu-id="5b851-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-209">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-210">True</span><span class="sxs-lookup"><span data-stu-id="5b851-210">True</span></span>                                                            |
| <span data-ttu-id="5b851-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-211">Is Indexed</span></span>             | <span data-ttu-id="5b851-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-212">False</span></span>                                                           |
| <span data-ttu-id="5b851-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-213">In Global Catalog</span></span>      | <span data-ttu-id="5b851-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-214">False</span></span>                                                           |
| <span data-ttu-id="5b851-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-216">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-217">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-218">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-219">Search-Flags</span></span>           | <span data-ttu-id="5b851-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-220">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-221">System-Flags</span></span>           | <span data-ttu-id="5b851-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-222">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-223">Classes used in</span></span>        | [<span data-ttu-id="5b851-224">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-224">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5b851-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b851-225">Windows Server 2008</span></span>



| <span data-ttu-id="5b851-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-226">Entry</span></span> | <span data-ttu-id="5b851-227">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-227">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-228">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-229">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-230">System-Only</span></span>            | <span data-ttu-id="5b851-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-231">False</span></span>                                                           |
| <span data-ttu-id="5b851-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-232">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-233">True</span><span class="sxs-lookup"><span data-stu-id="5b851-233">True</span></span>                                                            |
| <span data-ttu-id="5b851-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-234">Is Indexed</span></span>             | <span data-ttu-id="5b851-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-235">False</span></span>                                                           |
| <span data-ttu-id="5b851-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-236">In Global Catalog</span></span>      | <span data-ttu-id="5b851-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-237">False</span></span>                                                           |
| <span data-ttu-id="5b851-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-239">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-240">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-241">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-242">Search-Flags</span></span>           | <span data-ttu-id="5b851-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-243">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-244">System-Flags</span></span>           | <span data-ttu-id="5b851-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-245">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-246">Classes used in</span></span>        | [<span data-ttu-id="5b851-247">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-247">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5b851-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5b851-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5b851-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-249">Entry</span></span> | <span data-ttu-id="5b851-250">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-250">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-251">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-252">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-253">System-Only</span></span>            | <span data-ttu-id="5b851-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-254">False</span></span>                                                           |
| <span data-ttu-id="5b851-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-255">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-256">True</span><span class="sxs-lookup"><span data-stu-id="5b851-256">True</span></span>                                                            |
| <span data-ttu-id="5b851-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-257">Is Indexed</span></span>             | <span data-ttu-id="5b851-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-258">False</span></span>                                                           |
| <span data-ttu-id="5b851-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-259">In Global Catalog</span></span>      | <span data-ttu-id="5b851-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-260">False</span></span>                                                           |
| <span data-ttu-id="5b851-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-262">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-263">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-264">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-265">Search-Flags</span></span>           | <span data-ttu-id="5b851-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-266">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-267">System-Flags</span></span>           | <span data-ttu-id="5b851-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-268">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-269">Classes used in</span></span>        | [<span data-ttu-id="5b851-270">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-270">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5b851-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5b851-271">Windows Server 2012</span></span>



| <span data-ttu-id="5b851-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="5b851-272">Entry</span></span> | <span data-ttu-id="5b851-273">Значение</span><span class="sxs-lookup"><span data-stu-id="5b851-273">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="5b851-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5b851-274">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5b851-275">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="5b851-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="5b851-276">System-Only</span></span>            | <span data-ttu-id="5b851-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-277">False</span></span>                                                           |
| <span data-ttu-id="5b851-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5b851-278">Is-Single-Valued</span></span>       | <span data-ttu-id="5b851-279">True</span><span class="sxs-lookup"><span data-stu-id="5b851-279">True</span></span>                                                            |
| <span data-ttu-id="5b851-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5b851-280">Is Indexed</span></span>             | <span data-ttu-id="5b851-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-281">False</span></span>                                                           |
| <span data-ttu-id="5b851-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5b851-282">In Global Catalog</span></span>      | <span data-ttu-id="5b851-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="5b851-283">False</span></span>                                                           |
| <span data-ttu-id="5b851-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5b851-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="5b851-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5b851-285">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="5b851-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5b851-286">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5b851-287">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="5b851-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-288">Search-Flags</span></span>           | <span data-ttu-id="5b851-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5b851-289">0x00000000</span></span>                                                      |
| <span data-ttu-id="5b851-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5b851-290">System-Flags</span></span>           | <span data-ttu-id="5b851-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5b851-291">0x00000010</span></span>                                                      |
| <span data-ttu-id="5b851-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5b851-292">Classes used in</span></span>        | [<span data-ttu-id="5b851-293">**Доступ с правом Control**</span><span class="sxs-lookup"><span data-stu-id="5b851-293">**Control-Access-Right**</span></span>](c-controlaccessright.md)<br/> |



 

 





