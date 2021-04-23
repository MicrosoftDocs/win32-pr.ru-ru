---
title: Атрибут ms-DS-Settings
description: Используется для хранения параметров объекта. Его использование определяется только владельцем объекта. Мы рекомендуем использовать его для хранения пар "имя-значение". Например, синий цвет.
ms.assetid: 44e3a9e2-5528-4328-9cb7-1b6a4a77950a
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Settings
- msDS — параметры схема AD для атрибута
topic_type:
- apiref
api_name:
- ms-DS-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f466bd5aa5a904482ff9c84c1f818c12205f69c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893473"
---
# <a name="ms-ds-settings-attribute"></a><span data-ttu-id="500d4-108">Атрибут ms-DS-Settings</span><span class="sxs-lookup"><span data-stu-id="500d4-108">ms-DS-Settings attribute</span></span>

<span data-ttu-id="500d4-109">Используется для хранения параметров объекта.</span><span class="sxs-lookup"><span data-stu-id="500d4-109">Used to store settings for an object.</span></span> <span data-ttu-id="500d4-110">Его использование определяется только владельцем объекта.</span><span class="sxs-lookup"><span data-stu-id="500d4-110">Its use is solely determined by the object's owner.</span></span> <span data-ttu-id="500d4-111">Мы рекомендуем использовать его для хранения пар "имя-значение".</span><span class="sxs-lookup"><span data-stu-id="500d4-111">We recommend using it to store name/value pairs.</span></span> <span data-ttu-id="500d4-112">Например, цвет = синий.</span><span class="sxs-lookup"><span data-stu-id="500d4-112">For example, color=blue.</span></span>



| <span data-ttu-id="500d4-113">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-113">Entry</span></span> | <span data-ttu-id="500d4-114">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-114">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="500d4-115">CN</span><span class="sxs-lookup"><span data-stu-id="500d4-115">CN</span></span>                | <span data-ttu-id="500d4-116">MS-DS-параметры</span><span class="sxs-lookup"><span data-stu-id="500d4-116">ms-DS-Settings</span></span>                              |
| <span data-ttu-id="500d4-117">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="500d4-117">Ldap-Display-Name</span></span> | <span data-ttu-id="500d4-118">msDS-параметры</span><span class="sxs-lookup"><span data-stu-id="500d4-118">msDS-Settings</span></span>                               |
| <span data-ttu-id="500d4-119">Размер</span><span class="sxs-lookup"><span data-stu-id="500d4-119">Size</span></span>              | \-                                          |
| <span data-ttu-id="500d4-120">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="500d4-120">Update Privilege</span></span>  | <span data-ttu-id="500d4-121">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="500d4-121">Domain administrator</span></span>                        |
| <span data-ttu-id="500d4-122">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="500d4-122">Update Frequency</span></span>  | <span data-ttu-id="500d4-123">При каждом изменении значений параметров.</span><span class="sxs-lookup"><span data-stu-id="500d4-123">Each time the settings values change.</span></span>       |
| <span data-ttu-id="500d4-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-124">Attribute-Id</span></span>      | <span data-ttu-id="500d4-125">1.2.840.113556.1.4.1697</span><span class="sxs-lookup"><span data-stu-id="500d4-125">1.2.840.113556.1.4.1697</span></span>                     |
| <span data-ttu-id="500d4-126">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="500d4-126">System-Id-Guid</span></span>    | <span data-ttu-id="500d4-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span><span class="sxs-lookup"><span data-stu-id="500d4-127">0e1b47d7-40a3-4b48-8d1b-4cac0c1cdf21</span></span>        |
| <span data-ttu-id="500d4-128">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="500d4-128">Syntax</span></span>            | [<span data-ttu-id="500d4-129">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="500d4-129">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="500d4-130">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="500d4-130">Implementations</span></span>

-   [<span data-ttu-id="500d4-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="500d4-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="500d4-132">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="500d4-132">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="500d4-133">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="500d4-133">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="500d4-134">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="500d4-134">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="500d4-135">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="500d4-135">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="500d4-136">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="500d4-136">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="500d4-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="500d4-137">Windows Server 2003</span></span>



| <span data-ttu-id="500d4-138">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-138">Entry</span></span> | <span data-ttu-id="500d4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-139">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500d4-140">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500d4-140">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-141">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-141">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="500d4-142">System-Only</span></span>            | <span data-ttu-id="500d4-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-143">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-144">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500d4-144">Is-Single-Valued</span></span>       | <span data-ttu-id="500d4-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-145">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-146">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500d4-146">Is Indexed</span></span>             | <span data-ttu-id="500d4-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-147">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-148">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500d4-148">In Global Catalog</span></span>      | <span data-ttu-id="500d4-149">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-149">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-150">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500d4-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="500d4-151">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500d4-151">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="500d4-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500d4-152">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500d4-153">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-154">Search-Flags</span></span>           | <span data-ttu-id="500d4-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-155">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-156">System-Flags</span></span>           | <span data-ttu-id="500d4-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-157">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500d4-158">Classes used in</span></span>        | [<span data-ttu-id="500d4-159">**Параметры приложения**</span><span class="sxs-lookup"><span data-stu-id="500d4-159">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="500d4-160">**Точка соединения**</span><span class="sxs-lookup"><span data-stu-id="500d4-160">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="adam"></a><span data-ttu-id="500d4-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="500d4-161">ADAM</span></span>



| <span data-ttu-id="500d4-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-162">Entry</span></span> | <span data-ttu-id="500d4-163">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-163">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="500d4-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500d4-164">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="500d4-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-165">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="500d4-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="500d4-166">System-Only</span></span>            | <span data-ttu-id="500d4-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-167">False</span></span>                                                            |
| <span data-ttu-id="500d4-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500d4-168">Is-Single-Valued</span></span>       | <span data-ttu-id="500d4-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-169">False</span></span>                                                            |
| <span data-ttu-id="500d4-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500d4-170">Is Indexed</span></span>             | <span data-ttu-id="500d4-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-171">False</span></span>                                                            |
| <span data-ttu-id="500d4-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500d4-172">In Global Catalog</span></span>      | <span data-ttu-id="500d4-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-173">False</span></span>                                                            |
| <span data-ttu-id="500d4-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500d4-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="500d4-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500d4-175">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="500d4-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500d4-176">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="500d4-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500d4-177">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="500d4-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-178">Search-Flags</span></span>           | <span data-ttu-id="500d4-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-179">0x00000000</span></span>                                                       |
| <span data-ttu-id="500d4-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-180">System-Flags</span></span>           | <span data-ttu-id="500d4-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-181">0x00000000</span></span>                                                       |
| <span data-ttu-id="500d4-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500d4-182">Classes used in</span></span>        | [<span data-ttu-id="500d4-183">**Параметры приложения**</span><span class="sxs-lookup"><span data-stu-id="500d4-183">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="500d4-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="500d4-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="500d4-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-185">Entry</span></span> | <span data-ttu-id="500d4-186">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-186">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500d4-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500d4-187">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-188">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="500d4-189">System-Only</span></span>            | <span data-ttu-id="500d4-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-190">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500d4-191">Is-Single-Valued</span></span>       | <span data-ttu-id="500d4-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-192">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500d4-193">Is Indexed</span></span>             | <span data-ttu-id="500d4-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-194">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500d4-195">In Global Catalog</span></span>      | <span data-ttu-id="500d4-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-196">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500d4-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="500d4-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500d4-198">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="500d4-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500d4-199">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500d4-200">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-201">Search-Flags</span></span>           | <span data-ttu-id="500d4-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-202">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-203">System-Flags</span></span>           | <span data-ttu-id="500d4-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-204">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500d4-205">Classes used in</span></span>        | [<span data-ttu-id="500d4-206">**Параметры приложения**</span><span class="sxs-lookup"><span data-stu-id="500d4-206">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="500d4-207">**Точка соединения**</span><span class="sxs-lookup"><span data-stu-id="500d4-207">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="500d4-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="500d4-208">Windows Server 2008</span></span>



| <span data-ttu-id="500d4-209">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-209">Entry</span></span> | <span data-ttu-id="500d4-210">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-210">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500d4-211">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500d4-211">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-212">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="500d4-213">System-Only</span></span>            | <span data-ttu-id="500d4-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-214">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500d4-215">Is-Single-Valued</span></span>       | <span data-ttu-id="500d4-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-216">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500d4-217">Is Indexed</span></span>             | <span data-ttu-id="500d4-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-218">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500d4-219">In Global Catalog</span></span>      | <span data-ttu-id="500d4-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-220">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500d4-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="500d4-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500d4-222">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="500d4-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500d4-223">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500d4-224">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-225">Search-Flags</span></span>           | <span data-ttu-id="500d4-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-226">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-227">System-Flags</span></span>           | <span data-ttu-id="500d4-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-228">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500d4-229">Classes used in</span></span>        | [<span data-ttu-id="500d4-230">**Параметры приложения**</span><span class="sxs-lookup"><span data-stu-id="500d4-230">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="500d4-231">**Точка соединения**</span><span class="sxs-lookup"><span data-stu-id="500d4-231">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="500d4-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="500d4-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="500d4-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-233">Entry</span></span> | <span data-ttu-id="500d4-234">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-234">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500d4-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500d4-235">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-236">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="500d4-237">System-Only</span></span>            | <span data-ttu-id="500d4-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-238">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500d4-239">Is-Single-Valued</span></span>       | <span data-ttu-id="500d4-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-240">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500d4-241">Is Indexed</span></span>             | <span data-ttu-id="500d4-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-242">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500d4-243">In Global Catalog</span></span>      | <span data-ttu-id="500d4-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-244">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500d4-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="500d4-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500d4-246">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="500d4-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500d4-247">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500d4-248">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-249">Search-Flags</span></span>           | <span data-ttu-id="500d4-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-250">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-251">System-Flags</span></span>           | <span data-ttu-id="500d4-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-252">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500d4-253">Classes used in</span></span>        | [<span data-ttu-id="500d4-254">**Параметры приложения**</span><span class="sxs-lookup"><span data-stu-id="500d4-254">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="500d4-255">**Точка соединения**</span><span class="sxs-lookup"><span data-stu-id="500d4-255">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="500d4-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="500d4-256">Windows Server 2012</span></span>



| <span data-ttu-id="500d4-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="500d4-257">Entry</span></span> | <span data-ttu-id="500d4-258">Значение</span><span class="sxs-lookup"><span data-stu-id="500d4-258">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500d4-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500d4-259">Link-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500d4-260">MAPI-Id</span></span>                | \-                                                                                                                        |
| <span data-ttu-id="500d4-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="500d4-261">System-Only</span></span>            | <span data-ttu-id="500d4-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-262">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500d4-263">Is-Single-Valued</span></span>       | <span data-ttu-id="500d4-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-264">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500d4-265">Is Indexed</span></span>             | <span data-ttu-id="500d4-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-266">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500d4-267">In Global Catalog</span></span>      | <span data-ttu-id="500d4-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="500d4-268">False</span></span>                                                                                                                     |
| <span data-ttu-id="500d4-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500d4-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="500d4-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500d4-270">O:BAG:BAD:S:</span></span>                                                                                                              |
| <span data-ttu-id="500d4-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500d4-271">Range-Lower</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500d4-272">Range-Upper</span></span>            | \-                                                                                                                        |
| <span data-ttu-id="500d4-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-273">Search-Flags</span></span>           | <span data-ttu-id="500d4-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-274">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500d4-275">System-Flags</span></span>           | <span data-ttu-id="500d4-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500d4-276">0x00000000</span></span>                                                                                                                |
| <span data-ttu-id="500d4-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500d4-277">Classes used in</span></span>        | [<span data-ttu-id="500d4-278">**Параметры приложения**</span><span class="sxs-lookup"><span data-stu-id="500d4-278">**Application-Settings**</span></span>](c-applicationsettings.md)<br/> [<span data-ttu-id="500d4-279">**Точка соединения**</span><span class="sxs-lookup"><span data-stu-id="500d4-279">**Connection-Point**</span></span>](c-connectionpoint.md)<br/> |



 

 





