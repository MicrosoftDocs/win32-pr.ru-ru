---
title: Атрибут Code-Page
description: Указывает кодовую страницу для выбранного языка пользователя. Это значение не используется в Windows 2000.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Code-Page
- Схема AD атрибута кодовой страницы
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c3e9858ba387b98d5556c6010490c024be836b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804451"
---
# <a name="code-page-attribute"></a><span data-ttu-id="87f1f-106">Атрибут Code-Page</span><span class="sxs-lookup"><span data-stu-id="87f1f-106">Code-Page attribute</span></span>

<span data-ttu-id="87f1f-107">Указывает кодовую страницу для выбранного языка пользователя.</span><span class="sxs-lookup"><span data-stu-id="87f1f-107">Specifies the code page for the user's language of choice.</span></span> <span data-ttu-id="87f1f-108">Это значение не используется в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="87f1f-108">This value is not used by Windows 2000.</span></span>



| <span data-ttu-id="87f1f-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-109">Entry</span></span> | <span data-ttu-id="87f1f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="87f1f-111">CN</span><span class="sxs-lookup"><span data-stu-id="87f1f-111">CN</span></span>                | <span data-ttu-id="87f1f-112">Code-Page</span><span class="sxs-lookup"><span data-stu-id="87f1f-112">Code-Page</span></span>                                             |
| <span data-ttu-id="87f1f-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="87f1f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="87f1f-114">Страница</span><span class="sxs-lookup"><span data-stu-id="87f1f-114">codePage</span></span>                                              |
| <span data-ttu-id="87f1f-115">Размер</span><span class="sxs-lookup"><span data-stu-id="87f1f-115">Size</span></span>              | <span data-ttu-id="87f1f-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="87f1f-116">4 bytes</span></span>                                               |
| <span data-ttu-id="87f1f-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="87f1f-117">Update Privilege</span></span>  | <span data-ttu-id="87f1f-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="87f1f-118">Domain administrator</span></span>                                  |
| <span data-ttu-id="87f1f-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="87f1f-119">Update Frequency</span></span>  | <span data-ttu-id="87f1f-120">Когда пользователь хочет изменить язык по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87f1f-120">When the user desires to change the default language.</span></span> |
| <span data-ttu-id="87f1f-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-121">Attribute-Id</span></span>      | <span data-ttu-id="87f1f-122">1.2.840.113556.1.4.16</span><span class="sxs-lookup"><span data-stu-id="87f1f-122">1.2.840.113556.1.4.16</span></span>                                 |
| <span data-ttu-id="87f1f-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="87f1f-123">System-Id-Guid</span></span>    | <span data-ttu-id="87f1f-124">bf967938-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="87f1f-124">bf967938-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="87f1f-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87f1f-125">Syntax</span></span>            | [<span data-ttu-id="87f1f-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="87f1f-126">**Enumeration**</span></span>](s-enumeration.md)                  |



## <a name="implementations"></a><span data-ttu-id="87f1f-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="87f1f-127">Implementations</span></span>

-   [<span data-ttu-id="87f1f-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="87f1f-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="87f1f-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="87f1f-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="87f1f-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="87f1f-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="87f1f-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="87f1f-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="87f1f-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="87f1f-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="87f1f-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="87f1f-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="87f1f-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="87f1f-134">Windows 2000 Server</span></span>



| <span data-ttu-id="87f1f-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-135">Entry</span></span> | <span data-ttu-id="87f1f-136">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-136">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="87f1f-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="87f1f-137">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-138">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="87f1f-139">System-Only</span></span>            | <span data-ttu-id="87f1f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-140">False</span></span>                             |
| <span data-ttu-id="87f1f-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="87f1f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="87f1f-142">True</span><span class="sxs-lookup"><span data-stu-id="87f1f-142">True</span></span>                              |
| <span data-ttu-id="87f1f-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="87f1f-143">Is Indexed</span></span>             | <span data-ttu-id="87f1f-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-144">False</span></span>                             |
| <span data-ttu-id="87f1f-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="87f1f-145">In Global Catalog</span></span>      | <span data-ttu-id="87f1f-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-146">False</span></span>                             |
| <span data-ttu-id="87f1f-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="87f1f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="87f1f-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87f1f-148">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="87f1f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87f1f-149">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="87f1f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87f1f-150">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="87f1f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-151">Search-Flags</span></span>           | <span data-ttu-id="87f1f-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-152">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-153">System-Flags</span></span>           | <span data-ttu-id="87f1f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-154">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="87f1f-155">Classes used in</span></span>        | [<span data-ttu-id="87f1f-156">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="87f1f-156">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="87f1f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87f1f-157">Windows Server 2003</span></span>



| <span data-ttu-id="87f1f-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-158">Entry</span></span> | <span data-ttu-id="87f1f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-159">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="87f1f-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="87f1f-160">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-161">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="87f1f-162">System-Only</span></span>            | <span data-ttu-id="87f1f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-163">False</span></span>                             |
| <span data-ttu-id="87f1f-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="87f1f-164">Is-Single-Valued</span></span>       | <span data-ttu-id="87f1f-165">True</span><span class="sxs-lookup"><span data-stu-id="87f1f-165">True</span></span>                              |
| <span data-ttu-id="87f1f-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="87f1f-166">Is Indexed</span></span>             | <span data-ttu-id="87f1f-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-167">False</span></span>                             |
| <span data-ttu-id="87f1f-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="87f1f-168">In Global Catalog</span></span>      | <span data-ttu-id="87f1f-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-169">False</span></span>                             |
| <span data-ttu-id="87f1f-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="87f1f-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="87f1f-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87f1f-171">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="87f1f-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87f1f-172">Range-Lower</span></span>            | <span data-ttu-id="87f1f-173">0</span><span class="sxs-lookup"><span data-stu-id="87f1f-173">0</span></span>                                 |
| <span data-ttu-id="87f1f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87f1f-174">Range-Upper</span></span>            | <span data-ttu-id="87f1f-175">65535</span><span class="sxs-lookup"><span data-stu-id="87f1f-175">65535</span></span>                             |
| <span data-ttu-id="87f1f-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-176">Search-Flags</span></span>           | <span data-ttu-id="87f1f-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-177">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-178">System-Flags</span></span>           | <span data-ttu-id="87f1f-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-179">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="87f1f-180">Classes used in</span></span>        | [<span data-ttu-id="87f1f-181">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="87f1f-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="87f1f-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="87f1f-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="87f1f-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-183">Entry</span></span> | <span data-ttu-id="87f1f-184">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-184">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="87f1f-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="87f1f-185">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-186">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="87f1f-187">System-Only</span></span>            | <span data-ttu-id="87f1f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-188">False</span></span>                             |
| <span data-ttu-id="87f1f-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="87f1f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="87f1f-190">True</span><span class="sxs-lookup"><span data-stu-id="87f1f-190">True</span></span>                              |
| <span data-ttu-id="87f1f-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="87f1f-191">Is Indexed</span></span>             | <span data-ttu-id="87f1f-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-192">False</span></span>                             |
| <span data-ttu-id="87f1f-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="87f1f-193">In Global Catalog</span></span>      | <span data-ttu-id="87f1f-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-194">False</span></span>                             |
| <span data-ttu-id="87f1f-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="87f1f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="87f1f-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87f1f-196">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="87f1f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87f1f-197">Range-Lower</span></span>            | <span data-ttu-id="87f1f-198">0</span><span class="sxs-lookup"><span data-stu-id="87f1f-198">0</span></span>                                 |
| <span data-ttu-id="87f1f-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87f1f-199">Range-Upper</span></span>            | <span data-ttu-id="87f1f-200">65535</span><span class="sxs-lookup"><span data-stu-id="87f1f-200">65535</span></span>                             |
| <span data-ttu-id="87f1f-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-201">Search-Flags</span></span>           | <span data-ttu-id="87f1f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-202">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-203">System-Flags</span></span>           | <span data-ttu-id="87f1f-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-204">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="87f1f-205">Classes used in</span></span>        | [<span data-ttu-id="87f1f-206">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="87f1f-206">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="87f1f-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87f1f-207">Windows Server 2008</span></span>



| <span data-ttu-id="87f1f-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-208">Entry</span></span> | <span data-ttu-id="87f1f-209">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="87f1f-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="87f1f-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="87f1f-212">System-Only</span></span>            | <span data-ttu-id="87f1f-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-213">False</span></span>                             |
| <span data-ttu-id="87f1f-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="87f1f-214">Is-Single-Valued</span></span>       | <span data-ttu-id="87f1f-215">True</span><span class="sxs-lookup"><span data-stu-id="87f1f-215">True</span></span>                              |
| <span data-ttu-id="87f1f-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="87f1f-216">Is Indexed</span></span>             | <span data-ttu-id="87f1f-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-217">False</span></span>                             |
| <span data-ttu-id="87f1f-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="87f1f-218">In Global Catalog</span></span>      | <span data-ttu-id="87f1f-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-219">False</span></span>                             |
| <span data-ttu-id="87f1f-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="87f1f-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="87f1f-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87f1f-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="87f1f-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87f1f-222">Range-Lower</span></span>            | <span data-ttu-id="87f1f-223">0</span><span class="sxs-lookup"><span data-stu-id="87f1f-223">0</span></span>                                 |
| <span data-ttu-id="87f1f-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87f1f-224">Range-Upper</span></span>            | <span data-ttu-id="87f1f-225">65535</span><span class="sxs-lookup"><span data-stu-id="87f1f-225">65535</span></span>                             |
| <span data-ttu-id="87f1f-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-226">Search-Flags</span></span>           | <span data-ttu-id="87f1f-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-227">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-228">System-Flags</span></span>           | <span data-ttu-id="87f1f-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-229">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="87f1f-230">Classes used in</span></span>        | [<span data-ttu-id="87f1f-231">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="87f1f-231">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="87f1f-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="87f1f-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="87f1f-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-233">Entry</span></span> | <span data-ttu-id="87f1f-234">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-234">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="87f1f-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="87f1f-235">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-236">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="87f1f-237">System-Only</span></span>            | <span data-ttu-id="87f1f-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-238">False</span></span>                             |
| <span data-ttu-id="87f1f-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="87f1f-239">Is-Single-Valued</span></span>       | <span data-ttu-id="87f1f-240">True</span><span class="sxs-lookup"><span data-stu-id="87f1f-240">True</span></span>                              |
| <span data-ttu-id="87f1f-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="87f1f-241">Is Indexed</span></span>             | <span data-ttu-id="87f1f-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-242">False</span></span>                             |
| <span data-ttu-id="87f1f-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="87f1f-243">In Global Catalog</span></span>      | <span data-ttu-id="87f1f-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-244">False</span></span>                             |
| <span data-ttu-id="87f1f-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="87f1f-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="87f1f-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87f1f-246">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="87f1f-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87f1f-247">Range-Lower</span></span>            | <span data-ttu-id="87f1f-248">0</span><span class="sxs-lookup"><span data-stu-id="87f1f-248">0</span></span>                                 |
| <span data-ttu-id="87f1f-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87f1f-249">Range-Upper</span></span>            | <span data-ttu-id="87f1f-250">65535</span><span class="sxs-lookup"><span data-stu-id="87f1f-250">65535</span></span>                             |
| <span data-ttu-id="87f1f-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-251">Search-Flags</span></span>           | <span data-ttu-id="87f1f-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-252">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-253">System-Flags</span></span>           | <span data-ttu-id="87f1f-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-254">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="87f1f-255">Classes used in</span></span>        | [<span data-ttu-id="87f1f-256">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="87f1f-256">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="87f1f-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87f1f-257">Windows Server 2012</span></span>



| <span data-ttu-id="87f1f-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="87f1f-258">Entry</span></span> | <span data-ttu-id="87f1f-259">Значение</span><span class="sxs-lookup"><span data-stu-id="87f1f-259">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="87f1f-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="87f1f-260">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="87f1f-261">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="87f1f-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="87f1f-262">System-Only</span></span>            | <span data-ttu-id="87f1f-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-263">False</span></span>                             |
| <span data-ttu-id="87f1f-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="87f1f-264">Is-Single-Valued</span></span>       | <span data-ttu-id="87f1f-265">True</span><span class="sxs-lookup"><span data-stu-id="87f1f-265">True</span></span>                              |
| <span data-ttu-id="87f1f-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="87f1f-266">Is Indexed</span></span>             | <span data-ttu-id="87f1f-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-267">False</span></span>                             |
| <span data-ttu-id="87f1f-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="87f1f-268">In Global Catalog</span></span>      | <span data-ttu-id="87f1f-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="87f1f-269">False</span></span>                             |
| <span data-ttu-id="87f1f-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="87f1f-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="87f1f-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="87f1f-271">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="87f1f-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="87f1f-272">Range-Lower</span></span>            | <span data-ttu-id="87f1f-273">0</span><span class="sxs-lookup"><span data-stu-id="87f1f-273">0</span></span>                                 |
| <span data-ttu-id="87f1f-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="87f1f-274">Range-Upper</span></span>            | <span data-ttu-id="87f1f-275">65535</span><span class="sxs-lookup"><span data-stu-id="87f1f-275">65535</span></span>                             |
| <span data-ttu-id="87f1f-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-276">Search-Flags</span></span>           | <span data-ttu-id="87f1f-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-277">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="87f1f-278">System-Flags</span></span>           | <span data-ttu-id="87f1f-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="87f1f-279">0x00000010</span></span>                        |
| <span data-ttu-id="87f1f-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="87f1f-280">Classes used in</span></span>        | [<span data-ttu-id="87f1f-281">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="87f1f-281">**User**</span></span>](c-user.md)<br/> |



 

 





