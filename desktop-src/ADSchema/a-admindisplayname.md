---
title: Атрибут "admin-Name"
description: Имя, отображаемое на экранах администратора.
ms.assetid: a4395f7f-3665-48c8-ac1a-68ab9a03d762
ms.tgt_platform: multiple
keywords:
- Администратор-отображаемое имя-схема атрибута AD
- Схема AD атрибута Админдисплайнаме
topic_type:
- apiref
api_name:
- Admin-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02f8e84e0c6779e8a1a7dc25eff285cd4b13b5d8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494118"
---
# <a name="admin-display-name-attribute"></a><span data-ttu-id="65d4d-105">Атрибут "admin-Name"</span><span class="sxs-lookup"><span data-stu-id="65d4d-105">Admin-Display-Name attribute</span></span>

<span data-ttu-id="65d4d-106">Имя, отображаемое на экранах администратора.</span><span class="sxs-lookup"><span data-stu-id="65d4d-106">The name to be displayed on admin screens.</span></span>



| <span data-ttu-id="65d4d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-107">Entry</span></span> | <span data-ttu-id="65d4d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="65d4d-109">CN</span><span class="sxs-lookup"><span data-stu-id="65d4d-109">CN</span></span>                | <span data-ttu-id="65d4d-110">Имя администратора-отображение</span><span class="sxs-lookup"><span data-stu-id="65d4d-110">Admin-Display-Name</span></span>                          |
| <span data-ttu-id="65d4d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="65d4d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="65d4d-112">adminDisplayName</span><span class="sxs-lookup"><span data-stu-id="65d4d-112">adminDisplayName</span></span>                            |
| <span data-ttu-id="65d4d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="65d4d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="65d4d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="65d4d-114">Update Privilege</span></span>  | <span data-ttu-id="65d4d-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="65d4d-115">Domain administrator</span></span>                        |
| <span data-ttu-id="65d4d-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="65d4d-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="65d4d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-117">Attribute-Id</span></span>      | <span data-ttu-id="65d4d-118">1.2.840.113556.1.2.194</span><span class="sxs-lookup"><span data-stu-id="65d4d-118">1.2.840.113556.1.2.194</span></span>                      |
| <span data-ttu-id="65d4d-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="65d4d-119">System-Id-Guid</span></span>    | <span data-ttu-id="65d4d-120">bf96791a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="65d4d-120">bf96791a-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="65d4d-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65d4d-121">Syntax</span></span>            | [<span data-ttu-id="65d4d-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="65d4d-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="65d4d-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="65d4d-123">Implementations</span></span>

-   [<span data-ttu-id="65d4d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="65d4d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="65d4d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="65d4d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="65d4d-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="65d4d-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="65d4d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="65d4d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="65d4d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="65d4d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="65d4d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="65d4d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="65d4d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="65d4d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="65d4d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="65d4d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="65d4d-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-132">Entry</span></span> | <span data-ttu-id="65d4d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-135">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-136">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-136">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-137">System-Only</span></span>            | <span data-ttu-id="65d4d-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-138">False</span></span>                           |
| <span data-ttu-id="65d4d-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-140">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-140">True</span></span>                            |
| <span data-ttu-id="65d4d-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-141">Is Indexed</span></span>             | <span data-ttu-id="65d4d-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-142">False</span></span>                           |
| <span data-ttu-id="65d4d-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-143">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-144">False</span></span>                           |
| <span data-ttu-id="65d4d-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-147">Range-Lower</span></span>            | <span data-ttu-id="65d4d-148">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-148">1</span></span>                               |
| <span data-ttu-id="65d4d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-149">Range-Upper</span></span>            | <span data-ttu-id="65d4d-150">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-150">256</span></span>                             |
| <span data-ttu-id="65d4d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-151">Search-Flags</span></span>           | <span data-ttu-id="65d4d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-152">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-153">System-Flags</span></span>           | <span data-ttu-id="65d4d-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-154">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-155">Classes used in</span></span>        | [<span data-ttu-id="65d4d-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="65d4d-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="65d4d-157">Windows Server 2003</span></span>



| <span data-ttu-id="65d4d-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-158">Entry</span></span> | <span data-ttu-id="65d4d-159">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-161">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-162">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-162">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-163">System-Only</span></span>            | <span data-ttu-id="65d4d-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-164">False</span></span>                           |
| <span data-ttu-id="65d4d-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-165">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-166">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-166">True</span></span>                            |
| <span data-ttu-id="65d4d-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-167">Is Indexed</span></span>             | <span data-ttu-id="65d4d-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-168">False</span></span>                           |
| <span data-ttu-id="65d4d-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-169">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-170">False</span></span>                           |
| <span data-ttu-id="65d4d-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-173">Range-Lower</span></span>            | <span data-ttu-id="65d4d-174">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-174">1</span></span>                               |
| <span data-ttu-id="65d4d-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-175">Range-Upper</span></span>            | <span data-ttu-id="65d4d-176">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-176">256</span></span>                             |
| <span data-ttu-id="65d4d-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-177">Search-Flags</span></span>           | <span data-ttu-id="65d4d-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-178">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-179">System-Flags</span></span>           | <span data-ttu-id="65d4d-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-180">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-181">Classes used in</span></span>        | [<span data-ttu-id="65d4d-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="65d4d-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="65d4d-183">ADAM</span></span>



| <span data-ttu-id="65d4d-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-184">Entry</span></span> | <span data-ttu-id="65d4d-185">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-187">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-188">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-188">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-189">System-Only</span></span>            | <span data-ttu-id="65d4d-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-190">False</span></span>                           |
| <span data-ttu-id="65d4d-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-191">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-192">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-192">True</span></span>                            |
| <span data-ttu-id="65d4d-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-193">Is Indexed</span></span>             | <span data-ttu-id="65d4d-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-194">False</span></span>                           |
| <span data-ttu-id="65d4d-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-195">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-196">False</span></span>                           |
| <span data-ttu-id="65d4d-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-199">Range-Lower</span></span>            | <span data-ttu-id="65d4d-200">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-200">1</span></span>                               |
| <span data-ttu-id="65d4d-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-201">Range-Upper</span></span>            | <span data-ttu-id="65d4d-202">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-202">256</span></span>                             |
| <span data-ttu-id="65d4d-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-203">Search-Flags</span></span>           | <span data-ttu-id="65d4d-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-204">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-205">System-Flags</span></span>           | <span data-ttu-id="65d4d-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-206">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-207">Classes used in</span></span>        | [<span data-ttu-id="65d4d-208">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="65d4d-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="65d4d-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="65d4d-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-210">Entry</span></span> | <span data-ttu-id="65d4d-211">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-213">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-214">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-214">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-215">System-Only</span></span>            | <span data-ttu-id="65d4d-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-216">False</span></span>                           |
| <span data-ttu-id="65d4d-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-217">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-218">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-218">True</span></span>                            |
| <span data-ttu-id="65d4d-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-219">Is Indexed</span></span>             | <span data-ttu-id="65d4d-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-220">False</span></span>                           |
| <span data-ttu-id="65d4d-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-221">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-222">False</span></span>                           |
| <span data-ttu-id="65d4d-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-225">Range-Lower</span></span>            | <span data-ttu-id="65d4d-226">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-226">1</span></span>                               |
| <span data-ttu-id="65d4d-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-227">Range-Upper</span></span>            | <span data-ttu-id="65d4d-228">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-228">256</span></span>                             |
| <span data-ttu-id="65d4d-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-229">Search-Flags</span></span>           | <span data-ttu-id="65d4d-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-230">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-231">System-Flags</span></span>           | <span data-ttu-id="65d4d-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-232">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-233">Classes used in</span></span>        | [<span data-ttu-id="65d4d-234">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="65d4d-235">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65d4d-235">Windows Server 2008</span></span>



| <span data-ttu-id="65d4d-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-236">Entry</span></span> | <span data-ttu-id="65d4d-237">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-239">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-240">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-240">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-241">System-Only</span></span>            | <span data-ttu-id="65d4d-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-242">False</span></span>                           |
| <span data-ttu-id="65d4d-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-243">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-244">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-244">True</span></span>                            |
| <span data-ttu-id="65d4d-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-245">Is Indexed</span></span>             | <span data-ttu-id="65d4d-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-246">False</span></span>                           |
| <span data-ttu-id="65d4d-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-247">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-248">False</span></span>                           |
| <span data-ttu-id="65d4d-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-251">Range-Lower</span></span>            | <span data-ttu-id="65d4d-252">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-252">1</span></span>                               |
| <span data-ttu-id="65d4d-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-253">Range-Upper</span></span>            | <span data-ttu-id="65d4d-254">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-254">256</span></span>                             |
| <span data-ttu-id="65d4d-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-255">Search-Flags</span></span>           | <span data-ttu-id="65d4d-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-256">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-257">System-Flags</span></span>           | <span data-ttu-id="65d4d-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-258">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-259">Classes used in</span></span>        | [<span data-ttu-id="65d4d-260">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="65d4d-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65d4d-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="65d4d-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-262">Entry</span></span> | <span data-ttu-id="65d4d-263">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-265">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-266">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-266">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-267">System-Only</span></span>            | <span data-ttu-id="65d4d-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-268">False</span></span>                           |
| <span data-ttu-id="65d4d-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-269">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-270">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-270">True</span></span>                            |
| <span data-ttu-id="65d4d-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-271">Is Indexed</span></span>             | <span data-ttu-id="65d4d-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-272">False</span></span>                           |
| <span data-ttu-id="65d4d-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-273">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-274">False</span></span>                           |
| <span data-ttu-id="65d4d-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-277">Range-Lower</span></span>            | <span data-ttu-id="65d4d-278">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-278">1</span></span>                               |
| <span data-ttu-id="65d4d-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-279">Range-Upper</span></span>            | <span data-ttu-id="65d4d-280">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-280">256</span></span>                             |
| <span data-ttu-id="65d4d-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-281">Search-Flags</span></span>           | <span data-ttu-id="65d4d-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-282">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-283">System-Flags</span></span>           | <span data-ttu-id="65d4d-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-284">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-285">Classes used in</span></span>        | [<span data-ttu-id="65d4d-286">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-286">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="65d4d-287">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65d4d-287">Windows Server 2012</span></span>



| <span data-ttu-id="65d4d-288">Ввод</span><span class="sxs-lookup"><span data-stu-id="65d4d-288">Entry</span></span> | <span data-ttu-id="65d4d-289">Значение</span><span class="sxs-lookup"><span data-stu-id="65d4d-289">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="65d4d-290">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="65d4d-290">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="65d4d-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="65d4d-291">MAPI-Id</span></span>                | <span data-ttu-id="65d4d-292">0x804B</span><span class="sxs-lookup"><span data-stu-id="65d4d-292">0x804B</span></span>                          |
| <span data-ttu-id="65d4d-293">System-Only</span><span class="sxs-lookup"><span data-stu-id="65d4d-293">System-Only</span></span>            | <span data-ttu-id="65d4d-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-294">False</span></span>                           |
| <span data-ttu-id="65d4d-295">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="65d4d-295">Is-Single-Valued</span></span>       | <span data-ttu-id="65d4d-296">True</span><span class="sxs-lookup"><span data-stu-id="65d4d-296">True</span></span>                            |
| <span data-ttu-id="65d4d-297">Индексируется</span><span class="sxs-lookup"><span data-stu-id="65d4d-297">Is Indexed</span></span>             | <span data-ttu-id="65d4d-298">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-298">False</span></span>                           |
| <span data-ttu-id="65d4d-299">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="65d4d-299">In Global Catalog</span></span>      | <span data-ttu-id="65d4d-300">Неверно</span><span class="sxs-lookup"><span data-stu-id="65d4d-300">False</span></span>                           |
| <span data-ttu-id="65d4d-301">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="65d4d-301">NT-Security-Descriptor</span></span> | <span data-ttu-id="65d4d-302">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="65d4d-302">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="65d4d-303">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="65d4d-303">Range-Lower</span></span>            | <span data-ttu-id="65d4d-304">1</span><span class="sxs-lookup"><span data-stu-id="65d4d-304">1</span></span>                               |
| <span data-ttu-id="65d4d-305">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="65d4d-305">Range-Upper</span></span>            | <span data-ttu-id="65d4d-306">256</span><span class="sxs-lookup"><span data-stu-id="65d4d-306">256</span></span>                             |
| <span data-ttu-id="65d4d-307">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-307">Search-Flags</span></span>           | <span data-ttu-id="65d4d-308">0x00000000</span><span class="sxs-lookup"><span data-stu-id="65d4d-308">0x00000000</span></span>                      |
| <span data-ttu-id="65d4d-309">System-Flags</span><span class="sxs-lookup"><span data-stu-id="65d4d-309">System-Flags</span></span>           | <span data-ttu-id="65d4d-310">0x00000010</span><span class="sxs-lookup"><span data-stu-id="65d4d-310">0x00000010</span></span>                      |
| <span data-ttu-id="65d4d-311">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="65d4d-311">Classes used in</span></span>        | [<span data-ttu-id="65d4d-312">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="65d4d-312">**Top**</span></span>](c-top.md)<br/> |



 

 





