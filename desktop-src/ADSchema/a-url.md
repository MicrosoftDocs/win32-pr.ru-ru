---
title: WWW-Page-другой атрибут
description: Список альтернативных веб-страниц.
ms.assetid: 834a0020-2f0c-41e5-a0b0-5ef393df2b47
ms.tgt_platform: multiple
keywords:
- WWW-Page-другая схема AD атрибутов
- Схема AD атрибута URL
topic_type:
- apiref
api_name:
- WWW-Page-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc607dfb29f1448138d29c47ec8bd17a2fcd00
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493668"
---
# <a name="www-page-other-attribute"></a><span data-ttu-id="28b59-105">WWW-Page-другой атрибут</span><span class="sxs-lookup"><span data-stu-id="28b59-105">WWW-Page-Other attribute</span></span>

<span data-ttu-id="28b59-106">Список альтернативных веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="28b59-106">A list of alternate webpages.</span></span>



| <span data-ttu-id="28b59-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-107">Entry</span></span> | <span data-ttu-id="28b59-108">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="28b59-109">CN</span><span class="sxs-lookup"><span data-stu-id="28b59-109">CN</span></span>                | <span data-ttu-id="28b59-110">WWW-Page — другие</span><span class="sxs-lookup"><span data-stu-id="28b59-110">WWW-Page-Other</span></span>                                                              |
| <span data-ttu-id="28b59-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="28b59-111">Ldap-Display-Name</span></span> | <span data-ttu-id="28b59-112">url</span><span class="sxs-lookup"><span data-stu-id="28b59-112">url</span></span>                                                                         |
| <span data-ttu-id="28b59-113">Размер</span><span class="sxs-lookup"><span data-stu-id="28b59-113">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="28b59-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="28b59-114">Update Privilege</span></span>  | <span data-ttu-id="28b59-115">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="28b59-115">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="28b59-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="28b59-116">Update Frequency</span></span>  | <span data-ttu-id="28b59-117">Когда создается запись пользователя и каждый раз, когда необходимо изменить веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="28b59-117">When the user's record is created and whenever the webpage needs to change.</span></span> |
| <span data-ttu-id="28b59-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-118">Attribute-Id</span></span>      | <span data-ttu-id="28b59-119">1.2.840.113556.1.4.749</span><span class="sxs-lookup"><span data-stu-id="28b59-119">1.2.840.113556.1.4.749</span></span>                                                      |
| <span data-ttu-id="28b59-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="28b59-120">System-Id-Guid</span></span>    | <span data-ttu-id="28b59-121">9a9a0221-4a5b-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="28b59-121">9a9a0221-4a5b-11d1-a9c3-0000f80367c1</span></span>                                        |
| <span data-ttu-id="28b59-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28b59-122">Syntax</span></span>            | [<span data-ttu-id="28b59-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="28b59-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="28b59-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="28b59-124">Implementations</span></span>

-   [<span data-ttu-id="28b59-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28b59-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28b59-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28b59-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28b59-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="28b59-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="28b59-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28b59-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28b59-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28b59-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28b59-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28b59-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28b59-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28b59-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28b59-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28b59-132">Windows 2000 Server</span></span>



| <span data-ttu-id="28b59-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-133">Entry</span></span> | <span data-ttu-id="28b59-134">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-136">MAPI-Id</span></span>                | <span data-ttu-id="28b59-137">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-137">0x8175</span></span>                          |
| <span data-ttu-id="28b59-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-138">System-Only</span></span>            | <span data-ttu-id="28b59-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-139">False</span></span>                           |
| <span data-ttu-id="28b59-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-140">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-141">False</span></span>                           |
| <span data-ttu-id="28b59-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-142">Is Indexed</span></span>             | <span data-ttu-id="28b59-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-143">False</span></span>                           |
| <span data-ttu-id="28b59-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-144">In Global Catalog</span></span>      | <span data-ttu-id="28b59-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-145">False</span></span>                           |
| <span data-ttu-id="28b59-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-150">Search-Flags</span></span>           | <span data-ttu-id="28b59-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-151">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-152">System-Flags</span></span>           | <span data-ttu-id="28b59-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-153">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-154">Classes used in</span></span>        | [<span data-ttu-id="28b59-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28b59-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28b59-156">Windows Server 2003</span></span>



| <span data-ttu-id="28b59-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-157">Entry</span></span> | <span data-ttu-id="28b59-158">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-159">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-160">MAPI-Id</span></span>                | <span data-ttu-id="28b59-161">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-161">0x8175</span></span>                          |
| <span data-ttu-id="28b59-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-162">System-Only</span></span>            | <span data-ttu-id="28b59-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-163">False</span></span>                           |
| <span data-ttu-id="28b59-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-164">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-165">False</span></span>                           |
| <span data-ttu-id="28b59-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-166">Is Indexed</span></span>             | <span data-ttu-id="28b59-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-167">False</span></span>                           |
| <span data-ttu-id="28b59-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-168">In Global Catalog</span></span>      | <span data-ttu-id="28b59-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-169">False</span></span>                           |
| <span data-ttu-id="28b59-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-174">Search-Flags</span></span>           | <span data-ttu-id="28b59-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-175">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-176">System-Flags</span></span>           | <span data-ttu-id="28b59-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-177">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-178">Classes used in</span></span>        | [<span data-ttu-id="28b59-179">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="28b59-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="28b59-180">ADAM</span></span>



| <span data-ttu-id="28b59-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-181">Entry</span></span> | <span data-ttu-id="28b59-182">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-183">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-184">MAPI-Id</span></span>                | <span data-ttu-id="28b59-185">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-185">0x8175</span></span>                          |
| <span data-ttu-id="28b59-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-186">System-Only</span></span>            | <span data-ttu-id="28b59-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-187">False</span></span>                           |
| <span data-ttu-id="28b59-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-188">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-189">False</span></span>                           |
| <span data-ttu-id="28b59-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-190">Is Indexed</span></span>             | <span data-ttu-id="28b59-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-191">False</span></span>                           |
| <span data-ttu-id="28b59-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-192">In Global Catalog</span></span>      | <span data-ttu-id="28b59-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-193">False</span></span>                           |
| <span data-ttu-id="28b59-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-198">Search-Flags</span></span>           | <span data-ttu-id="28b59-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-199">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-200">System-Flags</span></span>           | <span data-ttu-id="28b59-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-201">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-202">Classes used in</span></span>        | [<span data-ttu-id="28b59-203">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28b59-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28b59-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28b59-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-205">Entry</span></span> | <span data-ttu-id="28b59-206">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-207">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-208">MAPI-Id</span></span>                | <span data-ttu-id="28b59-209">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-209">0x8175</span></span>                          |
| <span data-ttu-id="28b59-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-210">System-Only</span></span>            | <span data-ttu-id="28b59-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-211">False</span></span>                           |
| <span data-ttu-id="28b59-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-212">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-213">False</span></span>                           |
| <span data-ttu-id="28b59-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-214">Is Indexed</span></span>             | <span data-ttu-id="28b59-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-215">False</span></span>                           |
| <span data-ttu-id="28b59-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-216">In Global Catalog</span></span>      | <span data-ttu-id="28b59-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-217">False</span></span>                           |
| <span data-ttu-id="28b59-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-222">Search-Flags</span></span>           | <span data-ttu-id="28b59-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-223">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-224">System-Flags</span></span>           | <span data-ttu-id="28b59-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-225">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-226">Classes used in</span></span>        | [<span data-ttu-id="28b59-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28b59-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28b59-228">Windows Server 2008</span></span>



| <span data-ttu-id="28b59-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-229">Entry</span></span> | <span data-ttu-id="28b59-230">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-231">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-232">MAPI-Id</span></span>                | <span data-ttu-id="28b59-233">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-233">0x8175</span></span>                          |
| <span data-ttu-id="28b59-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-234">System-Only</span></span>            | <span data-ttu-id="28b59-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-235">False</span></span>                           |
| <span data-ttu-id="28b59-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-236">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-237">False</span></span>                           |
| <span data-ttu-id="28b59-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-238">Is Indexed</span></span>             | <span data-ttu-id="28b59-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-239">False</span></span>                           |
| <span data-ttu-id="28b59-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-240">In Global Catalog</span></span>      | <span data-ttu-id="28b59-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-241">False</span></span>                           |
| <span data-ttu-id="28b59-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-246">Search-Flags</span></span>           | <span data-ttu-id="28b59-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-247">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-248">System-Flags</span></span>           | <span data-ttu-id="28b59-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-249">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-250">Classes used in</span></span>        | [<span data-ttu-id="28b59-251">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28b59-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28b59-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28b59-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-253">Entry</span></span> | <span data-ttu-id="28b59-254">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-255">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-256">MAPI-Id</span></span>                | <span data-ttu-id="28b59-257">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-257">0x8175</span></span>                          |
| <span data-ttu-id="28b59-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-258">System-Only</span></span>            | <span data-ttu-id="28b59-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-259">False</span></span>                           |
| <span data-ttu-id="28b59-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-260">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-261">False</span></span>                           |
| <span data-ttu-id="28b59-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-262">Is Indexed</span></span>             | <span data-ttu-id="28b59-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-263">False</span></span>                           |
| <span data-ttu-id="28b59-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-264">In Global Catalog</span></span>      | <span data-ttu-id="28b59-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-265">False</span></span>                           |
| <span data-ttu-id="28b59-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-270">Search-Flags</span></span>           | <span data-ttu-id="28b59-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-271">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-272">System-Flags</span></span>           | <span data-ttu-id="28b59-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-273">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-274">Classes used in</span></span>        | [<span data-ttu-id="28b59-275">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28b59-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28b59-276">Windows Server 2012</span></span>



| <span data-ttu-id="28b59-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b59-277">Entry</span></span> | <span data-ttu-id="28b59-278">Значение</span><span class="sxs-lookup"><span data-stu-id="28b59-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="28b59-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b59-279">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="28b59-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b59-280">MAPI-Id</span></span>                | <span data-ttu-id="28b59-281">0x8175</span><span class="sxs-lookup"><span data-stu-id="28b59-281">0x8175</span></span>                          |
| <span data-ttu-id="28b59-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b59-282">System-Only</span></span>            | <span data-ttu-id="28b59-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-283">False</span></span>                           |
| <span data-ttu-id="28b59-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b59-284">Is-Single-Valued</span></span>       | <span data-ttu-id="28b59-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-285">False</span></span>                           |
| <span data-ttu-id="28b59-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b59-286">Is Indexed</span></span>             | <span data-ttu-id="28b59-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-287">False</span></span>                           |
| <span data-ttu-id="28b59-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b59-288">In Global Catalog</span></span>      | <span data-ttu-id="28b59-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b59-289">False</span></span>                           |
| <span data-ttu-id="28b59-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b59-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b59-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b59-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="28b59-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b59-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="28b59-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b59-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="28b59-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-294">Search-Flags</span></span>           | <span data-ttu-id="28b59-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b59-295">0x00000000</span></span>                      |
| <span data-ttu-id="28b59-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b59-296">System-Flags</span></span>           | <span data-ttu-id="28b59-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b59-297">0x00000010</span></span>                      |
| <span data-ttu-id="28b59-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b59-298">Classes used in</span></span>        | [<span data-ttu-id="28b59-299">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="28b59-299">**Top**</span></span>](c-top.md)<br/> |



 

 





