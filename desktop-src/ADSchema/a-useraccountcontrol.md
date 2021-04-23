---
title: Атрибут управления учетной записью пользователя
description: Флаги, управляющие поведением учетной записи пользователя.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута управления учетной записью пользователя
- Схема AD атрибута userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138742"
---
# <a name="user-account-control-attribute"></a><span data-ttu-id="c53eb-105">Атрибут управления учетной записью пользователя</span><span class="sxs-lookup"><span data-stu-id="c53eb-105">User-Account-Control attribute</span></span>

<span data-ttu-id="c53eb-106">Флаги, управляющие поведением учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="c53eb-106">Flags that control the behavior of the user account.</span></span>



| <span data-ttu-id="c53eb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-107">Entry</span></span> | <span data-ttu-id="c53eb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="c53eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="c53eb-109">CN</span></span>                | <span data-ttu-id="c53eb-110">Управление учетными записями пользователей</span><span class="sxs-lookup"><span data-stu-id="c53eb-110">User-Account-Control</span></span>                  |
| <span data-ttu-id="c53eb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c53eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c53eb-112">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="c53eb-112">userAccountControl</span></span>                    |
| <span data-ttu-id="c53eb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c53eb-113">Size</span></span>              | <span data-ttu-id="c53eb-114">4 байта.</span><span class="sxs-lookup"><span data-stu-id="c53eb-114">4 bytes.</span></span>                              |
| <span data-ttu-id="c53eb-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c53eb-115">Update Privilege</span></span>  | <span data-ttu-id="c53eb-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c53eb-116">This value is set by the system.</span></span>      |
| <span data-ttu-id="c53eb-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c53eb-117">Update Frequency</span></span>  | <span data-ttu-id="c53eb-118">При каждом изменении политики учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c53eb-118">Each time the account policy changes.</span></span> |
| <span data-ttu-id="c53eb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-119">Attribute-Id</span></span>      | <span data-ttu-id="c53eb-120">1.2.840.113556.1.4.8</span><span class="sxs-lookup"><span data-stu-id="c53eb-120">1.2.840.113556.1.4.8</span></span>                  |
| <span data-ttu-id="c53eb-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c53eb-121">System-Id-Guid</span></span>    | <span data-ttu-id="c53eb-122">bf967a68-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c53eb-122">bf967a68-0de6-11d0-a285-00aa003049e2</span></span>  |
| <span data-ttu-id="c53eb-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c53eb-123">Syntax</span></span>            | [<span data-ttu-id="c53eb-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="c53eb-124">**Enumeration**</span></span>](s-enumeration.md)  |



## <a name="implementations"></a><span data-ttu-id="c53eb-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c53eb-125">Implementations</span></span>

-   [<span data-ttu-id="c53eb-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c53eb-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c53eb-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c53eb-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c53eb-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c53eb-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c53eb-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c53eb-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c53eb-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c53eb-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c53eb-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c53eb-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c53eb-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c53eb-132">Windows 2000 Server</span></span>



| <span data-ttu-id="c53eb-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-133">Entry</span></span> | <span data-ttu-id="c53eb-134">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-134">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c53eb-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c53eb-135">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-136">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="c53eb-137">System-Only</span></span>            | <span data-ttu-id="c53eb-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="c53eb-138">False</span></span>                             |
| <span data-ttu-id="c53eb-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c53eb-139">Is-Single-Valued</span></span>       | <span data-ttu-id="c53eb-140">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-140">True</span></span>                              |
| <span data-ttu-id="c53eb-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c53eb-141">Is Indexed</span></span>             | <span data-ttu-id="c53eb-142">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-142">True</span></span>                              |
| <span data-ttu-id="c53eb-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c53eb-143">In Global Catalog</span></span>      | <span data-ttu-id="c53eb-144">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-144">True</span></span>                              |
| <span data-ttu-id="c53eb-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c53eb-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="c53eb-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c53eb-146">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c53eb-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c53eb-147">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c53eb-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c53eb-148">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c53eb-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-149">Search-Flags</span></span>           | <span data-ttu-id="c53eb-150">0x00000019</span><span class="sxs-lookup"><span data-stu-id="c53eb-150">0x00000019</span></span>                        |
| <span data-ttu-id="c53eb-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-151">System-Flags</span></span>           | <span data-ttu-id="c53eb-152">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c53eb-152">0x00000012</span></span>                        |
| <span data-ttu-id="c53eb-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c53eb-153">Classes used in</span></span>        | [<span data-ttu-id="c53eb-154">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="c53eb-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c53eb-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c53eb-155">Windows Server 2003</span></span>



| <span data-ttu-id="c53eb-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-156">Entry</span></span> | <span data-ttu-id="c53eb-157">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-157">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c53eb-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c53eb-158">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-159">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c53eb-160">System-Only</span></span>            | <span data-ttu-id="c53eb-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="c53eb-161">False</span></span>                             |
| <span data-ttu-id="c53eb-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c53eb-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c53eb-163">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-163">True</span></span>                              |
| <span data-ttu-id="c53eb-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c53eb-164">Is Indexed</span></span>             | <span data-ttu-id="c53eb-165">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-165">True</span></span>                              |
| <span data-ttu-id="c53eb-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c53eb-166">In Global Catalog</span></span>      | <span data-ttu-id="c53eb-167">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-167">True</span></span>                              |
| <span data-ttu-id="c53eb-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c53eb-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c53eb-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c53eb-169">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c53eb-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c53eb-170">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c53eb-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c53eb-171">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c53eb-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-172">Search-Flags</span></span>           | <span data-ttu-id="c53eb-173">0x00000019</span><span class="sxs-lookup"><span data-stu-id="c53eb-173">0x00000019</span></span>                        |
| <span data-ttu-id="c53eb-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-174">System-Flags</span></span>           | <span data-ttu-id="c53eb-175">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c53eb-175">0x00000012</span></span>                        |
| <span data-ttu-id="c53eb-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c53eb-176">Classes used in</span></span>        | [<span data-ttu-id="c53eb-177">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="c53eb-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c53eb-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c53eb-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c53eb-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-179">Entry</span></span> | <span data-ttu-id="c53eb-180">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c53eb-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c53eb-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="c53eb-183">System-Only</span></span>            | <span data-ttu-id="c53eb-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="c53eb-184">False</span></span>                             |
| <span data-ttu-id="c53eb-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c53eb-185">Is-Single-Valued</span></span>       | <span data-ttu-id="c53eb-186">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-186">True</span></span>                              |
| <span data-ttu-id="c53eb-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c53eb-187">Is Indexed</span></span>             | <span data-ttu-id="c53eb-188">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-188">True</span></span>                              |
| <span data-ttu-id="c53eb-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c53eb-189">In Global Catalog</span></span>      | <span data-ttu-id="c53eb-190">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-190">True</span></span>                              |
| <span data-ttu-id="c53eb-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c53eb-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="c53eb-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c53eb-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c53eb-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c53eb-193">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c53eb-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c53eb-194">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c53eb-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-195">Search-Flags</span></span>           | <span data-ttu-id="c53eb-196">0x00000019</span><span class="sxs-lookup"><span data-stu-id="c53eb-196">0x00000019</span></span>                        |
| <span data-ttu-id="c53eb-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-197">System-Flags</span></span>           | <span data-ttu-id="c53eb-198">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c53eb-198">0x00000012</span></span>                        |
| <span data-ttu-id="c53eb-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c53eb-199">Classes used in</span></span>        | [<span data-ttu-id="c53eb-200">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="c53eb-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c53eb-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c53eb-201">Windows Server 2008</span></span>



| <span data-ttu-id="c53eb-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-202">Entry</span></span> | <span data-ttu-id="c53eb-203">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-203">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c53eb-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c53eb-204">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-205">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="c53eb-206">System-Only</span></span>            | <span data-ttu-id="c53eb-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="c53eb-207">False</span></span>                             |
| <span data-ttu-id="c53eb-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c53eb-208">Is-Single-Valued</span></span>       | <span data-ttu-id="c53eb-209">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-209">True</span></span>                              |
| <span data-ttu-id="c53eb-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c53eb-210">Is Indexed</span></span>             | <span data-ttu-id="c53eb-211">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-211">True</span></span>                              |
| <span data-ttu-id="c53eb-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c53eb-212">In Global Catalog</span></span>      | <span data-ttu-id="c53eb-213">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-213">True</span></span>                              |
| <span data-ttu-id="c53eb-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c53eb-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="c53eb-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c53eb-215">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c53eb-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c53eb-216">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c53eb-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c53eb-217">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c53eb-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-218">Search-Flags</span></span>           | <span data-ttu-id="c53eb-219">0x00000019</span><span class="sxs-lookup"><span data-stu-id="c53eb-219">0x00000019</span></span>                        |
| <span data-ttu-id="c53eb-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-220">System-Flags</span></span>           | <span data-ttu-id="c53eb-221">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c53eb-221">0x00000012</span></span>                        |
| <span data-ttu-id="c53eb-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c53eb-222">Classes used in</span></span>        | [<span data-ttu-id="c53eb-223">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="c53eb-223">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c53eb-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c53eb-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c53eb-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-225">Entry</span></span> | <span data-ttu-id="c53eb-226">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-226">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c53eb-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c53eb-227">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-228">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="c53eb-229">System-Only</span></span>            | <span data-ttu-id="c53eb-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="c53eb-230">False</span></span>                             |
| <span data-ttu-id="c53eb-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c53eb-231">Is-Single-Valued</span></span>       | <span data-ttu-id="c53eb-232">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-232">True</span></span>                              |
| <span data-ttu-id="c53eb-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c53eb-233">Is Indexed</span></span>             | <span data-ttu-id="c53eb-234">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-234">True</span></span>                              |
| <span data-ttu-id="c53eb-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c53eb-235">In Global Catalog</span></span>      | <span data-ttu-id="c53eb-236">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-236">True</span></span>                              |
| <span data-ttu-id="c53eb-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c53eb-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="c53eb-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c53eb-238">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c53eb-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c53eb-239">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c53eb-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c53eb-240">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c53eb-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-241">Search-Flags</span></span>           | <span data-ttu-id="c53eb-242">0x00000019</span><span class="sxs-lookup"><span data-stu-id="c53eb-242">0x00000019</span></span>                        |
| <span data-ttu-id="c53eb-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-243">System-Flags</span></span>           | <span data-ttu-id="c53eb-244">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c53eb-244">0x00000012</span></span>                        |
| <span data-ttu-id="c53eb-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c53eb-245">Classes used in</span></span>        | [<span data-ttu-id="c53eb-246">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="c53eb-246">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c53eb-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c53eb-247">Windows Server 2012</span></span>



| <span data-ttu-id="c53eb-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="c53eb-248">Entry</span></span> | <span data-ttu-id="c53eb-249">Значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-249">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="c53eb-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c53eb-250">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c53eb-251">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="c53eb-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="c53eb-252">System-Only</span></span>            | <span data-ttu-id="c53eb-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="c53eb-253">False</span></span>                             |
| <span data-ttu-id="c53eb-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c53eb-254">Is-Single-Valued</span></span>       | <span data-ttu-id="c53eb-255">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-255">True</span></span>                              |
| <span data-ttu-id="c53eb-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c53eb-256">Is Indexed</span></span>             | <span data-ttu-id="c53eb-257">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-257">True</span></span>                              |
| <span data-ttu-id="c53eb-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c53eb-258">In Global Catalog</span></span>      | <span data-ttu-id="c53eb-259">True</span><span class="sxs-lookup"><span data-stu-id="c53eb-259">True</span></span>                              |
| <span data-ttu-id="c53eb-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c53eb-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="c53eb-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c53eb-261">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="c53eb-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c53eb-262">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="c53eb-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c53eb-263">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="c53eb-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-264">Search-Flags</span></span>           | <span data-ttu-id="c53eb-265">0x00000019</span><span class="sxs-lookup"><span data-stu-id="c53eb-265">0x00000019</span></span>                        |
| <span data-ttu-id="c53eb-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c53eb-266">System-Flags</span></span>           | <span data-ttu-id="c53eb-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="c53eb-267">0x00000012</span></span>                        |
| <span data-ttu-id="c53eb-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c53eb-268">Classes used in</span></span>        | [<span data-ttu-id="c53eb-269">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="c53eb-269">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c53eb-270">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c53eb-270">Remarks</span></span>

<span data-ttu-id="c53eb-271">Значение этого атрибута может быть равно нулю или быть сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c53eb-271">This attribute value can be zero or a combination of one or more of the following values.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c53eb-272">Шестнадцатеричное значение</span><span class="sxs-lookup"><span data-stu-id="c53eb-272">Hexadecimal value</span></span></th>
<th><span data-ttu-id="c53eb-273">Идентификатор (определяется в iAds. h)</span><span class="sxs-lookup"><span data-stu-id="c53eb-273">Identifier (defined in iads.h)</span></span></th>
<th><span data-ttu-id="c53eb-274">Описание</span><span class="sxs-lookup"><span data-stu-id="c53eb-274">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c53eb-275">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c53eb-275">0x00000001</span></span></td>
<td><span data-ttu-id="c53eb-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-276"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-277">Выполняется сценарий входа.</span><span class="sxs-lookup"><span data-stu-id="c53eb-277">The logon script is executed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-278">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c53eb-278">0x00000002</span></span></td>
<td><span data-ttu-id="c53eb-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-279"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-280">Учетная запись пользователя отключена.</span><span class="sxs-lookup"><span data-stu-id="c53eb-280">The user account is disabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-281">0x00000008</span><span class="sxs-lookup"><span data-stu-id="c53eb-281">0x00000008</span></span></td>
<td><span data-ttu-id="c53eb-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-282"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-283">Требуется корневой каталог.</span><span class="sxs-lookup"><span data-stu-id="c53eb-283">The home directory is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c53eb-284">0x00000010</span></span></td>
<td><span data-ttu-id="c53eb-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-285"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-286">Учетная запись в данный момент заблокирована.</span><span class="sxs-lookup"><span data-stu-id="c53eb-286">The account is currently locked out.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-287">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c53eb-287">0x00000020</span></span></td>
<td><span data-ttu-id="c53eb-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-288"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-289">Пароль не требуется.</span><span class="sxs-lookup"><span data-stu-id="c53eb-289">No password is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-290">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c53eb-290">0x00000040</span></span></td>
<td><span data-ttu-id="c53eb-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-291"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-292">Пользователь не может изменить пароль.</span><span class="sxs-lookup"><span data-stu-id="c53eb-292">The user cannot change the password.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c53eb-293">Вы не можете назначить параметры разрешений PASSWD_CANT_CHANGE путем непосредственного изменения атрибута UserAccountControl.</span><span class="sxs-lookup"><span data-stu-id="c53eb-293">You cannot assign the permission settings of PASSWD_CANT_CHANGE by directly modifying the UserAccountControl attribute.</span></span> <span data-ttu-id="c53eb-294">Дополнительные сведения и пример кода, демонстрирующий, как запретить пользователю изменять пароль, см. в разделе <a href="/windows/desktop/ADSI/user-cannot-change-password">пользователь не может изменить пароль</a>.</span><span class="sxs-lookup"><span data-stu-id="c53eb-294">For more information and a code example that shows how to prevent a user from changing the password, see <a href="/windows/desktop/ADSI/user-cannot-change-password">User Cannot Change Password</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="c53eb-295">:</span><span class="sxs-lookup"><span data-stu-id="c53eb-295">:</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-296">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c53eb-296">0x00000080</span></span></td>
<td><span data-ttu-id="c53eb-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-297"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-298">Пользователь может отправить зашифрованный пароль.</span><span class="sxs-lookup"><span data-stu-id="c53eb-298">The user can send an encrypted password.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-299">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c53eb-299">0x00000100</span></span></td>
<td><span data-ttu-id="c53eb-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-300"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-301">Это учетная запись для пользователей, Первичная учетная запись которых находится в другом домене.</span><span class="sxs-lookup"><span data-stu-id="c53eb-301">This is an account for users whose primary account is in another domain.</span></span> <span data-ttu-id="c53eb-302">Эта учетная запись предоставляет пользователю доступ к этому домену, но не к домену, который доверяет данному домену.</span><span class="sxs-lookup"><span data-stu-id="c53eb-302">This account provides user access to this domain, but not to any domain that trusts this domain.</span></span> <span data-ttu-id="c53eb-303">Также называется учетной записью локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="c53eb-303">Also known as a local user account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-304">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c53eb-304">0x00000200</span></span></td>
<td><span data-ttu-id="c53eb-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-305"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-306">Это тип учетной записи по умолчанию, представляющий обычного пользователя.</span><span class="sxs-lookup"><span data-stu-id="c53eb-306">This is a default account type that represents a typical user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-307">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c53eb-307">0x00000800</span></span></td>
<td><span data-ttu-id="c53eb-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-308"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-309">Это позволяет доверять учетной записи для системного домена, который доверяет другим доменам.</span><span class="sxs-lookup"><span data-stu-id="c53eb-309">This is a permit to trust account for a system domain that trusts other domains.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-310">0x00001000</span><span class="sxs-lookup"><span data-stu-id="c53eb-310">0x00001000</span></span></td>
<td><span data-ttu-id="c53eb-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-311"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-312">Это учетная запись компьютера для компьютера, который является членом этого домена.</span><span class="sxs-lookup"><span data-stu-id="c53eb-312">This is a computer account for a computer that is a member of this domain.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-313">0x00002000</span><span class="sxs-lookup"><span data-stu-id="c53eb-313">0x00002000</span></span></td>
<td><span data-ttu-id="c53eb-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-314"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-315">Это учетная запись компьютера для системного контроллера домена резервного копирования, который является членом этого домена.</span><span class="sxs-lookup"><span data-stu-id="c53eb-315">This is a computer account for a system backup domain controller that is a member of this domain.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-316">0x00004000</span><span class="sxs-lookup"><span data-stu-id="c53eb-316">0x00004000</span></span></td>
<td><span data-ttu-id="c53eb-317">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c53eb-317">N/A</span></span></td>
<td><span data-ttu-id="c53eb-318">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c53eb-318">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-319">0x00008000</span><span class="sxs-lookup"><span data-stu-id="c53eb-319">0x00008000</span></span></td>
<td><span data-ttu-id="c53eb-320">Н/Д</span><span class="sxs-lookup"><span data-stu-id="c53eb-320">N/A</span></span></td>
<td><span data-ttu-id="c53eb-321">Не используется.</span><span class="sxs-lookup"><span data-stu-id="c53eb-321">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-322">0x00010000</span><span class="sxs-lookup"><span data-stu-id="c53eb-322">0x00010000</span></span></td>
<td><span data-ttu-id="c53eb-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-323"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-324">Срок действия пароля для этой учетной записи никогда не истечет.</span><span class="sxs-lookup"><span data-stu-id="c53eb-324">The password for this account will never expire.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-325">0x00020000</span><span class="sxs-lookup"><span data-stu-id="c53eb-325">0x00020000</span></span></td>
<td><span data-ttu-id="c53eb-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-326"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-327">Это учетная запись MNS.</span><span class="sxs-lookup"><span data-stu-id="c53eb-327">This is an MNS logon account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-328">0x00040000</span><span class="sxs-lookup"><span data-stu-id="c53eb-328">0x00040000</span></span></td>
<td><span data-ttu-id="c53eb-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-329"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-330">Пользователь должен войти в систему с помощью смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="c53eb-330">The user must log on using a smart card.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-331">0x00080000</span><span class="sxs-lookup"><span data-stu-id="c53eb-331">0x00080000</span></span></td>
<td><span data-ttu-id="c53eb-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-332"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-333">Учетная запись службы (учетная запись пользователя или компьютера), под которой выполняется служба, является доверенной для делегирования Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c53eb-333">The service account (user or computer account), under which a service runs, is trusted for Kerberos delegation.</span></span> <span data-ttu-id="c53eb-334">Любая такая служба может олицетворять клиента, запрашивающего службу.</span><span class="sxs-lookup"><span data-stu-id="c53eb-334">Any such service can impersonate a client requesting the service.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-335">0x00100000</span><span class="sxs-lookup"><span data-stu-id="c53eb-335">0x00100000</span></span></td>
<td><span data-ttu-id="c53eb-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-336"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-337">Контекст безопасности пользователя не будет делегирован службе, даже если учетная запись службы настроена как доверенная для делегирования Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c53eb-337">The security context of the user will not be delegated to a service even if the service account is set as trusted for Kerberos delegation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-338">0x00200000</span><span class="sxs-lookup"><span data-stu-id="c53eb-338">0x00200000</span></span></td>
<td><span data-ttu-id="c53eb-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-339"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-340">Ограничьте этот субъект для использования только типов шифрования DES для ключей.</span><span class="sxs-lookup"><span data-stu-id="c53eb-340">Restrict this principal to use only Data Encryption Standard (DES) encryption types for keys.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-341">0x00400000</span><span class="sxs-lookup"><span data-stu-id="c53eb-341">0x00400000</span></span></td>
<td><span data-ttu-id="c53eb-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-342"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-343">Для входа в эту учетную запись не требуется предварительная проверка подлинности Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c53eb-343">This account does not require Kerberos pre-authentication for logon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c53eb-344">0x00800000</span><span class="sxs-lookup"><span data-stu-id="c53eb-344">0x00800000</span></span></td>
<td><span data-ttu-id="c53eb-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-345"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-346">Срок действия пароля пользователя истек.</span><span class="sxs-lookup"><span data-stu-id="c53eb-346">The user password has expired.</span></span> <span data-ttu-id="c53eb-347">Этот флаг создается системой с использованием данных из атрибута <a href="a-pwdlastset.md"><strong>PWD-Last-Set</strong></a> и политики домена.</span><span class="sxs-lookup"><span data-stu-id="c53eb-347">This flag is created by the system using data from the <a href="a-pwdlastset.md"><strong>Pwd-Last-Set</strong></a> attribute and the domain policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c53eb-348">0x01000000</span><span class="sxs-lookup"><span data-stu-id="c53eb-348">0x01000000</span></span></td>
<td><span data-ttu-id="c53eb-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="c53eb-349"><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></span></span></td>
<td><span data-ttu-id="c53eb-350">Учетная запись включена для делегирования.</span><span class="sxs-lookup"><span data-stu-id="c53eb-350">The account is enabled for delegation.</span></span> <span data-ttu-id="c53eb-351">Это чувствительный к безопасности параметр. учетные записи с включенным параметром должны быть строго контролируемыми.</span><span class="sxs-lookup"><span data-stu-id="c53eb-351">This is a security-sensitive setting; accounts with this option enabled should be strictly controlled.</span></span> <span data-ttu-id="c53eb-352">Этот параметр позволяет службе, работающей под учетной записью, предположить удостоверение клиента и проходить проверку подлинности от имени этого пользователя на других удаленных серверах в сети.</span><span class="sxs-lookup"><span data-stu-id="c53eb-352">This setting enables a service running under the account to assume a client identity and authenticate as that user to other remote servers on the network.</span></span></td>
</tr>
</tbody>
</table>



 

