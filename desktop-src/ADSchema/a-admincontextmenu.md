---
title: Административный — атрибут контекстного меню
description: Порядковый номер и идентификатор GUID контекстного меню, которое будет использоваться на экранах администрирования.
ms.assetid: da388bf3-1c44-4d34-b763-e45b784d3c9e
ms.tgt_platform: multiple
keywords:
- Административный контекст-схема AD атрибута
- Схема AD атрибута Админконтекстмену
topic_type:
- apiref
api_name:
- Admin-Context-Menu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 955267bf1e494d6bb0c98b3f5d25832896393ff2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893142"
---
# <a name="admin-context-menu-attribute"></a><span data-ttu-id="d988b-105">Административный — атрибут контекстного меню</span><span class="sxs-lookup"><span data-stu-id="d988b-105">Admin-Context-Menu attribute</span></span>

<span data-ttu-id="d988b-106">Порядковый номер и идентификатор GUID контекстного меню, которое будет использоваться на экранах администрирования.</span><span class="sxs-lookup"><span data-stu-id="d988b-106">The order number and GUID of the context menu to be used on administration screens.</span></span>



| <span data-ttu-id="d988b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-107">Entry</span></span> | <span data-ttu-id="d988b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d988b-109">CN</span><span class="sxs-lookup"><span data-stu-id="d988b-109">CN</span></span>                | <span data-ttu-id="d988b-110">Контекстное меню администратора</span><span class="sxs-lookup"><span data-stu-id="d988b-110">Admin-Context-Menu</span></span>                          |
| <span data-ttu-id="d988b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d988b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="d988b-112">админконтекстмену</span><span class="sxs-lookup"><span data-stu-id="d988b-112">adminContextMenu</span></span>                            |
| <span data-ttu-id="d988b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="d988b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="d988b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d988b-114">Update Privilege</span></span>  | <span data-ttu-id="d988b-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="d988b-115">Domain administrator</span></span>                        |
| <span data-ttu-id="d988b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d988b-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d988b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-117">Attribute-Id</span></span>      | <span data-ttu-id="d988b-118">1.2.840.113556.1.4.614</span><span class="sxs-lookup"><span data-stu-id="d988b-118">1.2.840.113556.1.4.614</span></span>                      |
| <span data-ttu-id="d988b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d988b-119">System-Id-Guid</span></span>    | <span data-ttu-id="d988b-120">553fd038-f32e-11d0-b0bc-00c04fd8dca6</span><span class="sxs-lookup"><span data-stu-id="d988b-120">553fd038-f32e-11d0-b0bc-00c04fd8dca6</span></span>        |
| <span data-ttu-id="d988b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d988b-121">Syntax</span></span>            | [<span data-ttu-id="d988b-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d988b-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d988b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d988b-123">Implementations</span></span>

-   [<span data-ttu-id="d988b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d988b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d988b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d988b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d988b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d988b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d988b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d988b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d988b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d988b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d988b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d988b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d988b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d988b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="d988b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-131">Entry</span></span> | <span data-ttu-id="d988b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-132">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d988b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d988b-133">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-134">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="d988b-135">System-Only</span></span>            | <span data-ttu-id="d988b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-136">False</span></span>                                                      |
| <span data-ttu-id="d988b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d988b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="d988b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-138">False</span></span>                                                      |
| <span data-ttu-id="d988b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d988b-139">Is Indexed</span></span>             | <span data-ttu-id="d988b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-140">False</span></span>                                                      |
| <span data-ttu-id="d988b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d988b-141">In Global Catalog</span></span>      | <span data-ttu-id="d988b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-142">False</span></span>                                                      |
| <span data-ttu-id="d988b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d988b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="d988b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d988b-144">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d988b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d988b-145">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d988b-146">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-147">Search-Flags</span></span>           | <span data-ttu-id="d988b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d988b-148">0x00000000</span></span>                                                 |
| <span data-ttu-id="d988b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-149">System-Flags</span></span>           | <span data-ttu-id="d988b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d988b-150">0x00000010</span></span>                                                 |
| <span data-ttu-id="d988b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d988b-151">Classes used in</span></span>        | [<span data-ttu-id="d988b-152">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="d988b-152">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d988b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d988b-153">Windows Server 2003</span></span>



| <span data-ttu-id="d988b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-154">Entry</span></span> | <span data-ttu-id="d988b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-155">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d988b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d988b-156">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-157">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="d988b-158">System-Only</span></span>            | <span data-ttu-id="d988b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-159">False</span></span>                                                      |
| <span data-ttu-id="d988b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d988b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="d988b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-161">False</span></span>                                                      |
| <span data-ttu-id="d988b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d988b-162">Is Indexed</span></span>             | <span data-ttu-id="d988b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-163">False</span></span>                                                      |
| <span data-ttu-id="d988b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d988b-164">In Global Catalog</span></span>      | <span data-ttu-id="d988b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-165">False</span></span>                                                      |
| <span data-ttu-id="d988b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d988b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="d988b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d988b-167">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d988b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d988b-168">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d988b-169">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-170">Search-Flags</span></span>           | <span data-ttu-id="d988b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d988b-171">0x00000000</span></span>                                                 |
| <span data-ttu-id="d988b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-172">System-Flags</span></span>           | <span data-ttu-id="d988b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d988b-173">0x00000010</span></span>                                                 |
| <span data-ttu-id="d988b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d988b-174">Classes used in</span></span>        | [<span data-ttu-id="d988b-175">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="d988b-175">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d988b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d988b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d988b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-177">Entry</span></span> | <span data-ttu-id="d988b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-178">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d988b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d988b-179">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-180">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d988b-181">System-Only</span></span>            | <span data-ttu-id="d988b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-182">False</span></span>                                                      |
| <span data-ttu-id="d988b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d988b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d988b-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-184">False</span></span>                                                      |
| <span data-ttu-id="d988b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d988b-185">Is Indexed</span></span>             | <span data-ttu-id="d988b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-186">False</span></span>                                                      |
| <span data-ttu-id="d988b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d988b-187">In Global Catalog</span></span>      | <span data-ttu-id="d988b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-188">False</span></span>                                                      |
| <span data-ttu-id="d988b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d988b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d988b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d988b-190">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d988b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d988b-191">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d988b-192">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-193">Search-Flags</span></span>           | <span data-ttu-id="d988b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d988b-194">0x00000000</span></span>                                                 |
| <span data-ttu-id="d988b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-195">System-Flags</span></span>           | <span data-ttu-id="d988b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d988b-196">0x00000010</span></span>                                                 |
| <span data-ttu-id="d988b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d988b-197">Classes used in</span></span>        | [<span data-ttu-id="d988b-198">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="d988b-198">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d988b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d988b-199">Windows Server 2008</span></span>



| <span data-ttu-id="d988b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-200">Entry</span></span> | <span data-ttu-id="d988b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-201">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d988b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d988b-202">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-203">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="d988b-204">System-Only</span></span>            | <span data-ttu-id="d988b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-205">False</span></span>                                                      |
| <span data-ttu-id="d988b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d988b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="d988b-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-207">False</span></span>                                                      |
| <span data-ttu-id="d988b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d988b-208">Is Indexed</span></span>             | <span data-ttu-id="d988b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-209">False</span></span>                                                      |
| <span data-ttu-id="d988b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d988b-210">In Global Catalog</span></span>      | <span data-ttu-id="d988b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-211">False</span></span>                                                      |
| <span data-ttu-id="d988b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d988b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="d988b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d988b-213">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d988b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d988b-214">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d988b-215">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-216">Search-Flags</span></span>           | <span data-ttu-id="d988b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d988b-217">0x00000000</span></span>                                                 |
| <span data-ttu-id="d988b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-218">System-Flags</span></span>           | <span data-ttu-id="d988b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d988b-219">0x00000010</span></span>                                                 |
| <span data-ttu-id="d988b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d988b-220">Classes used in</span></span>        | [<span data-ttu-id="d988b-221">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="d988b-221">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d988b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d988b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d988b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-223">Entry</span></span> | <span data-ttu-id="d988b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-224">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d988b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d988b-225">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-226">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="d988b-227">System-Only</span></span>            | <span data-ttu-id="d988b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-228">False</span></span>                                                      |
| <span data-ttu-id="d988b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d988b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="d988b-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-230">False</span></span>                                                      |
| <span data-ttu-id="d988b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d988b-231">Is Indexed</span></span>             | <span data-ttu-id="d988b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-232">False</span></span>                                                      |
| <span data-ttu-id="d988b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d988b-233">In Global Catalog</span></span>      | <span data-ttu-id="d988b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-234">False</span></span>                                                      |
| <span data-ttu-id="d988b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d988b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="d988b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d988b-236">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d988b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d988b-237">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d988b-238">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-239">Search-Flags</span></span>           | <span data-ttu-id="d988b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d988b-240">0x00000000</span></span>                                                 |
| <span data-ttu-id="d988b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-241">System-Flags</span></span>           | <span data-ttu-id="d988b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d988b-242">0x00000010</span></span>                                                 |
| <span data-ttu-id="d988b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d988b-243">Classes used in</span></span>        | [<span data-ttu-id="d988b-244">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="d988b-244">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d988b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d988b-245">Windows Server 2012</span></span>



| <span data-ttu-id="d988b-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="d988b-246">Entry</span></span> | <span data-ttu-id="d988b-247">Значение</span><span class="sxs-lookup"><span data-stu-id="d988b-247">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="d988b-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d988b-248">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d988b-249">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="d988b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d988b-250">System-Only</span></span>            | <span data-ttu-id="d988b-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-251">False</span></span>                                                      |
| <span data-ttu-id="d988b-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d988b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d988b-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-253">False</span></span>                                                      |
| <span data-ttu-id="d988b-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d988b-254">Is Indexed</span></span>             | <span data-ttu-id="d988b-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-255">False</span></span>                                                      |
| <span data-ttu-id="d988b-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d988b-256">In Global Catalog</span></span>      | <span data-ttu-id="d988b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="d988b-257">False</span></span>                                                      |
| <span data-ttu-id="d988b-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d988b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d988b-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d988b-259">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="d988b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d988b-260">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d988b-261">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="d988b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-262">Search-Flags</span></span>           | <span data-ttu-id="d988b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d988b-263">0x00000000</span></span>                                                 |
| <span data-ttu-id="d988b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d988b-264">System-Flags</span></span>           | <span data-ttu-id="d988b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d988b-265">0x00000010</span></span>                                                 |
| <span data-ttu-id="d988b-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d988b-266">Classes used in</span></span>        | [<span data-ttu-id="d988b-267">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="d988b-267">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





