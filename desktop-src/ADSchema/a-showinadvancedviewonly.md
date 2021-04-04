---
title: Атрибут "Показать в режиме" — "только просмотр"
description: Значение TRUE, если этот атрибут должен быть видимым в расширенном режиме пользовательского интерфейса.
ms.assetid: af2e3b9c-50ad-40e4-88b7-155f792965f1
ms.tgt_platform: multiple
keywords:
- Схема AD с атрибутом "Показать в режиме расширенного просмотра"
- Схема AD атрибута Шовинадванцедвиевонли
topic_type:
- apiref
api_name:
- Show-In-Advanced-View-Only
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fb466371183aad02613ee1454f1e0b40a410625
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989766"
---
# <a name="show-in-advanced-view-only-attribute"></a><span data-ttu-id="18b4e-105">Атрибут "Показать в режиме" — "только просмотр"</span><span class="sxs-lookup"><span data-stu-id="18b4e-105">Show-In-Advanced-View-Only attribute</span></span>

<span data-ttu-id="18b4e-106">**Значение true** , если этот атрибут должен быть видимым в расширенном режиме пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18b4e-106">**TRUE** if this attribute is to be visible in the Advanced mode of the UI.</span></span>



| <span data-ttu-id="18b4e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-107">Entry</span></span> | <span data-ttu-id="18b4e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18b4e-109">CN</span><span class="sxs-lookup"><span data-stu-id="18b4e-109">CN</span></span>                | <span data-ttu-id="18b4e-110">"Показать" — "Расширенный просмотр"</span><span class="sxs-lookup"><span data-stu-id="18b4e-110">Show-In-Advanced-View-Only</span></span>                                                              |
| <span data-ttu-id="18b4e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="18b4e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="18b4e-112">showInAdvancedViewOnly</span><span class="sxs-lookup"><span data-stu-id="18b4e-112">showInAdvancedViewOnly</span></span>                                                                  |
| <span data-ttu-id="18b4e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="18b4e-113">Size</span></span>              | <span data-ttu-id="18b4e-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="18b4e-114">4 bytes</span></span>                                                                                 |
| <span data-ttu-id="18b4e-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="18b4e-115">Update Privilege</span></span>  | <span data-ttu-id="18b4e-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="18b4e-116">Domain administrator</span></span>                                                                    |
| <span data-ttu-id="18b4e-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="18b4e-117">Update Frequency</span></span>  | <span data-ttu-id="18b4e-118">При создании объекта или при необходимости изменения аспектов просмотра атрибута.</span><span class="sxs-lookup"><span data-stu-id="18b4e-118">When the object is created or when the viewing aspects of the attribute need to change.</span></span> |
| <span data-ttu-id="18b4e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-119">Attribute-Id</span></span>      | <span data-ttu-id="18b4e-120">1.2.840.113556.1.2.169</span><span class="sxs-lookup"><span data-stu-id="18b4e-120">1.2.840.113556.1.2.169</span></span>                                                                  |
| <span data-ttu-id="18b4e-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="18b4e-121">System-Id-Guid</span></span>    | <span data-ttu-id="18b4e-122">bf967984-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="18b4e-122">bf967984-0de6-11d0-a285-00aa003049e2</span></span>                                                    |
| <span data-ttu-id="18b4e-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18b4e-123">Syntax</span></span>            | [<span data-ttu-id="18b4e-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="18b4e-124">**Boolean**</span></span>](s-boolean.md)                                                            |



## <a name="implementations"></a><span data-ttu-id="18b4e-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="18b4e-125">Implementations</span></span>

-   [<span data-ttu-id="18b4e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="18b4e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="18b4e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="18b4e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="18b4e-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="18b4e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="18b4e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="18b4e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="18b4e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="18b4e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="18b4e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="18b4e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="18b4e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="18b4e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="18b4e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="18b4e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="18b4e-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-134">Entry</span></span> | <span data-ttu-id="18b4e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-138">System-Only</span></span>            | <span data-ttu-id="18b4e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-139">False</span></span>                           |
| <span data-ttu-id="18b4e-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-141">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-141">True</span></span>                            |
| <span data-ttu-id="18b4e-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-142">Is Indexed</span></span>             | <span data-ttu-id="18b4e-143">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-143">True</span></span>                            |
| <span data-ttu-id="18b4e-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-144">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-145">False</span></span>                           |
| <span data-ttu-id="18b4e-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-150">Search-Flags</span></span>           | <span data-ttu-id="18b4e-151">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-151">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-152">System-Flags</span></span>           | <span data-ttu-id="18b4e-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-153">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-154">Classes used in</span></span>        | [<span data-ttu-id="18b4e-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="18b4e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="18b4e-156">Windows Server 2003</span></span>



| <span data-ttu-id="18b4e-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-157">Entry</span></span> | <span data-ttu-id="18b4e-158">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-160">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-161">System-Only</span></span>            | <span data-ttu-id="18b4e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-162">False</span></span>                           |
| <span data-ttu-id="18b4e-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-164">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-164">True</span></span>                            |
| <span data-ttu-id="18b4e-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-165">Is Indexed</span></span>             | <span data-ttu-id="18b4e-166">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-166">True</span></span>                            |
| <span data-ttu-id="18b4e-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-167">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-168">False</span></span>                           |
| <span data-ttu-id="18b4e-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-170">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-171">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-172">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-173">Search-Flags</span></span>           | <span data-ttu-id="18b4e-174">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-174">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-175">System-Flags</span></span>           | <span data-ttu-id="18b4e-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-176">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-177">Classes used in</span></span>        | [<span data-ttu-id="18b4e-178">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-178">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="18b4e-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="18b4e-179">ADAM</span></span>



| <span data-ttu-id="18b4e-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-180">Entry</span></span> | <span data-ttu-id="18b4e-181">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-181">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-182">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-183">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-184">System-Only</span></span>            | <span data-ttu-id="18b4e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-185">False</span></span>                           |
| <span data-ttu-id="18b4e-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-187">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-187">True</span></span>                            |
| <span data-ttu-id="18b4e-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-188">Is Indexed</span></span>             | <span data-ttu-id="18b4e-189">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-189">True</span></span>                            |
| <span data-ttu-id="18b4e-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-190">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-191">False</span></span>                           |
| <span data-ttu-id="18b4e-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-193">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-194">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-195">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-196">Search-Flags</span></span>           | <span data-ttu-id="18b4e-197">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-197">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-198">System-Flags</span></span>           | <span data-ttu-id="18b4e-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-199">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-200">Classes used in</span></span>        | [<span data-ttu-id="18b4e-201">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-201">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="18b4e-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="18b4e-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="18b4e-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-203">Entry</span></span> | <span data-ttu-id="18b4e-204">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-204">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-205">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-206">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-207">System-Only</span></span>            | <span data-ttu-id="18b4e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-208">False</span></span>                           |
| <span data-ttu-id="18b4e-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-210">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-210">True</span></span>                            |
| <span data-ttu-id="18b4e-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-211">Is Indexed</span></span>             | <span data-ttu-id="18b4e-212">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-212">True</span></span>                            |
| <span data-ttu-id="18b4e-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-213">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-214">False</span></span>                           |
| <span data-ttu-id="18b4e-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-216">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-217">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-218">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-219">Search-Flags</span></span>           | <span data-ttu-id="18b4e-220">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-220">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-221">System-Flags</span></span>           | <span data-ttu-id="18b4e-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-222">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-223">Classes used in</span></span>        | [<span data-ttu-id="18b4e-224">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-224">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="18b4e-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18b4e-225">Windows Server 2008</span></span>



| <span data-ttu-id="18b4e-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-226">Entry</span></span> | <span data-ttu-id="18b4e-227">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-227">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-228">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-229">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-230">System-Only</span></span>            | <span data-ttu-id="18b4e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-231">False</span></span>                           |
| <span data-ttu-id="18b4e-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-232">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-233">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-233">True</span></span>                            |
| <span data-ttu-id="18b4e-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-234">Is Indexed</span></span>             | <span data-ttu-id="18b4e-235">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-235">True</span></span>                            |
| <span data-ttu-id="18b4e-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-236">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-237">False</span></span>                           |
| <span data-ttu-id="18b4e-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-239">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-240">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-241">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-242">Search-Flags</span></span>           | <span data-ttu-id="18b4e-243">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-243">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-244">System-Flags</span></span>           | <span data-ttu-id="18b4e-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-245">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-246">Classes used in</span></span>        | [<span data-ttu-id="18b4e-247">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-247">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="18b4e-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="18b4e-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="18b4e-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-249">Entry</span></span> | <span data-ttu-id="18b4e-250">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-250">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-251">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-252">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-253">System-Only</span></span>            | <span data-ttu-id="18b4e-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-254">False</span></span>                           |
| <span data-ttu-id="18b4e-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-255">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-256">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-256">True</span></span>                            |
| <span data-ttu-id="18b4e-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-257">Is Indexed</span></span>             | <span data-ttu-id="18b4e-258">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-258">True</span></span>                            |
| <span data-ttu-id="18b4e-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-259">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-260">False</span></span>                           |
| <span data-ttu-id="18b4e-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-262">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-263">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-264">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-265">Search-Flags</span></span>           | <span data-ttu-id="18b4e-266">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-266">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-267">System-Flags</span></span>           | <span data-ttu-id="18b4e-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-268">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-269">Classes used in</span></span>        | [<span data-ttu-id="18b4e-270">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-270">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="18b4e-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18b4e-271">Windows Server 2012</span></span>



| <span data-ttu-id="18b4e-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="18b4e-272">Entry</span></span> | <span data-ttu-id="18b4e-273">Значение</span><span class="sxs-lookup"><span data-stu-id="18b4e-273">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="18b4e-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="18b4e-274">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="18b4e-275">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="18b4e-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="18b4e-276">System-Only</span></span>            | <span data-ttu-id="18b4e-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-277">False</span></span>                           |
| <span data-ttu-id="18b4e-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="18b4e-278">Is-Single-Valued</span></span>       | <span data-ttu-id="18b4e-279">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-279">True</span></span>                            |
| <span data-ttu-id="18b4e-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="18b4e-280">Is Indexed</span></span>             | <span data-ttu-id="18b4e-281">True</span><span class="sxs-lookup"><span data-stu-id="18b4e-281">True</span></span>                            |
| <span data-ttu-id="18b4e-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="18b4e-282">In Global Catalog</span></span>      | <span data-ttu-id="18b4e-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="18b4e-283">False</span></span>                           |
| <span data-ttu-id="18b4e-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="18b4e-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="18b4e-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="18b4e-285">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="18b4e-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="18b4e-286">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="18b4e-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="18b4e-287">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="18b4e-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-288">Search-Flags</span></span>           | <span data-ttu-id="18b4e-289">0x00000011</span><span class="sxs-lookup"><span data-stu-id="18b4e-289">0x00000011</span></span>                      |
| <span data-ttu-id="18b4e-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="18b4e-290">System-Flags</span></span>           | <span data-ttu-id="18b4e-291">0x00000010</span><span class="sxs-lookup"><span data-stu-id="18b4e-291">0x00000010</span></span>                      |
| <span data-ttu-id="18b4e-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="18b4e-292">Classes used in</span></span>        | [<span data-ttu-id="18b4e-293">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="18b4e-293">**Top**</span></span>](c-top.md)<br/> |



 

 





