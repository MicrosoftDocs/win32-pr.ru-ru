---
title: WWW — атрибут главной страницы
description: Веб-страница, которая является первичной целевой страницей веб-сайта.
ms.assetid: 5dbc571d-3032-4eee-ab2d-9f6f0273a472
ms.tgt_platform: multiple
keywords:
- WWW-Главная — схема AD атрибута Active Page
- Схема AD атрибута Вввхомепаже
topic_type:
- apiref
api_name:
- WWW-Home-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 360240cebe5c8d02054307718de0bcaee47cec4e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989745"
---
# <a name="www-home-page-attribute"></a><span data-ttu-id="8709b-105">WWW — атрибут главной страницы</span><span class="sxs-lookup"><span data-stu-id="8709b-105">WWW-Home-Page attribute</span></span>

<span data-ttu-id="8709b-106">Веб-страница, которая является первичной целевой страницей веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="8709b-106">A web page that is the primary landing page of a website.</span></span>



| <span data-ttu-id="8709b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-107">Entry</span></span> | <span data-ttu-id="8709b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8709b-109">CN</span><span class="sxs-lookup"><span data-stu-id="8709b-109">CN</span></span>                | <span data-ttu-id="8709b-110">WWW — Главная страница</span><span class="sxs-lookup"><span data-stu-id="8709b-110">WWW-Home-Page</span></span>                                                               |
| <span data-ttu-id="8709b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8709b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8709b-112">wWWHomePage</span><span class="sxs-lookup"><span data-stu-id="8709b-112">wWWHomePage</span></span>                                                                 |
| <span data-ttu-id="8709b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8709b-113">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="8709b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8709b-114">Update Privilege</span></span>  | <span data-ttu-id="8709b-115">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8709b-115">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="8709b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8709b-116">Update Frequency</span></span>  | <span data-ttu-id="8709b-117">Когда создается запись пользователя и каждый раз, когда необходимо изменить веб-страницу.</span><span class="sxs-lookup"><span data-stu-id="8709b-117">When the user's record is created and whenever the webpage needs to change.</span></span> |
| <span data-ttu-id="8709b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-118">Attribute-Id</span></span>      | <span data-ttu-id="8709b-119">1.2.840.113556.1.2.464</span><span class="sxs-lookup"><span data-stu-id="8709b-119">1.2.840.113556.1.2.464</span></span>                                                      |
| <span data-ttu-id="8709b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8709b-120">System-Id-Guid</span></span>    | <span data-ttu-id="8709b-121">bf967a7a-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8709b-121">bf967a7a-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="8709b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8709b-122">Syntax</span></span>            | [<span data-ttu-id="8709b-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8709b-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="8709b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8709b-124">Implementations</span></span>

-   [<span data-ttu-id="8709b-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8709b-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8709b-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8709b-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8709b-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8709b-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8709b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8709b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8709b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8709b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8709b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8709b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8709b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8709b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8709b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8709b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="8709b-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-133">Entry</span></span> | <span data-ttu-id="8709b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-135">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-136">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-137">System-Only</span></span>            | <span data-ttu-id="8709b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-138">False</span></span>                           |
| <span data-ttu-id="8709b-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-140">True</span><span class="sxs-lookup"><span data-stu-id="8709b-140">True</span></span>                            |
| <span data-ttu-id="8709b-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-141">Is Indexed</span></span>             | <span data-ttu-id="8709b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-142">False</span></span>                           |
| <span data-ttu-id="8709b-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-143">In Global Catalog</span></span>      | <span data-ttu-id="8709b-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-144">False</span></span>                           |
| <span data-ttu-id="8709b-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-147">Range-Lower</span></span>            | <span data-ttu-id="8709b-148">1</span><span class="sxs-lookup"><span data-stu-id="8709b-148">1</span></span>                               |
| <span data-ttu-id="8709b-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-149">Range-Upper</span></span>            | <span data-ttu-id="8709b-150">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-150">2048</span></span>                            |
| <span data-ttu-id="8709b-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-151">Search-Flags</span></span>           | <span data-ttu-id="8709b-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-152">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-153">System-Flags</span></span>           | <span data-ttu-id="8709b-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-154">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-155">Classes used in</span></span>        | [<span data-ttu-id="8709b-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8709b-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8709b-157">Windows Server 2003</span></span>



| <span data-ttu-id="8709b-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-158">Entry</span></span> | <span data-ttu-id="8709b-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-162">System-Only</span></span>            | <span data-ttu-id="8709b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-163">False</span></span>                           |
| <span data-ttu-id="8709b-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-164">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-165">True</span><span class="sxs-lookup"><span data-stu-id="8709b-165">True</span></span>                            |
| <span data-ttu-id="8709b-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-166">Is Indexed</span></span>             | <span data-ttu-id="8709b-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-167">False</span></span>                           |
| <span data-ttu-id="8709b-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-168">In Global Catalog</span></span>      | <span data-ttu-id="8709b-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-169">False</span></span>                           |
| <span data-ttu-id="8709b-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-172">Range-Lower</span></span>            | <span data-ttu-id="8709b-173">1</span><span class="sxs-lookup"><span data-stu-id="8709b-173">1</span></span>                               |
| <span data-ttu-id="8709b-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-174">Range-Upper</span></span>            | <span data-ttu-id="8709b-175">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-175">2048</span></span>                            |
| <span data-ttu-id="8709b-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-176">Search-Flags</span></span>           | <span data-ttu-id="8709b-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-177">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-178">System-Flags</span></span>           | <span data-ttu-id="8709b-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-179">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-180">Classes used in</span></span>        | [<span data-ttu-id="8709b-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8709b-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="8709b-182">ADAM</span></span>



| <span data-ttu-id="8709b-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-183">Entry</span></span> | <span data-ttu-id="8709b-184">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-186">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-187">System-Only</span></span>            | <span data-ttu-id="8709b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-188">False</span></span>                           |
| <span data-ttu-id="8709b-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-190">True</span><span class="sxs-lookup"><span data-stu-id="8709b-190">True</span></span>                            |
| <span data-ttu-id="8709b-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-191">Is Indexed</span></span>             | <span data-ttu-id="8709b-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-192">False</span></span>                           |
| <span data-ttu-id="8709b-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-193">In Global Catalog</span></span>      | <span data-ttu-id="8709b-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-194">False</span></span>                           |
| <span data-ttu-id="8709b-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-197">Range-Lower</span></span>            | <span data-ttu-id="8709b-198">1</span><span class="sxs-lookup"><span data-stu-id="8709b-198">1</span></span>                               |
| <span data-ttu-id="8709b-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-199">Range-Upper</span></span>            | <span data-ttu-id="8709b-200">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-200">2048</span></span>                            |
| <span data-ttu-id="8709b-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-201">Search-Flags</span></span>           | <span data-ttu-id="8709b-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-202">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-203">System-Flags</span></span>           | <span data-ttu-id="8709b-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-204">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-205">Classes used in</span></span>        | [<span data-ttu-id="8709b-206">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-206">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8709b-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8709b-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8709b-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-208">Entry</span></span> | <span data-ttu-id="8709b-209">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-209">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-210">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-211">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-212">System-Only</span></span>            | <span data-ttu-id="8709b-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-213">False</span></span>                           |
| <span data-ttu-id="8709b-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-214">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-215">True</span><span class="sxs-lookup"><span data-stu-id="8709b-215">True</span></span>                            |
| <span data-ttu-id="8709b-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-216">Is Indexed</span></span>             | <span data-ttu-id="8709b-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-217">False</span></span>                           |
| <span data-ttu-id="8709b-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-218">In Global Catalog</span></span>      | <span data-ttu-id="8709b-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-219">False</span></span>                           |
| <span data-ttu-id="8709b-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-222">Range-Lower</span></span>            | <span data-ttu-id="8709b-223">1</span><span class="sxs-lookup"><span data-stu-id="8709b-223">1</span></span>                               |
| <span data-ttu-id="8709b-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-224">Range-Upper</span></span>            | <span data-ttu-id="8709b-225">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-225">2048</span></span>                            |
| <span data-ttu-id="8709b-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-226">Search-Flags</span></span>           | <span data-ttu-id="8709b-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-227">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-228">System-Flags</span></span>           | <span data-ttu-id="8709b-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-229">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-230">Classes used in</span></span>        | [<span data-ttu-id="8709b-231">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-231">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8709b-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8709b-232">Windows Server 2008</span></span>



| <span data-ttu-id="8709b-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-233">Entry</span></span> | <span data-ttu-id="8709b-234">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-234">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-235">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-236">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-237">System-Only</span></span>            | <span data-ttu-id="8709b-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-238">False</span></span>                           |
| <span data-ttu-id="8709b-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-239">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-240">True</span><span class="sxs-lookup"><span data-stu-id="8709b-240">True</span></span>                            |
| <span data-ttu-id="8709b-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-241">Is Indexed</span></span>             | <span data-ttu-id="8709b-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-242">False</span></span>                           |
| <span data-ttu-id="8709b-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-243">In Global Catalog</span></span>      | <span data-ttu-id="8709b-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-244">False</span></span>                           |
| <span data-ttu-id="8709b-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-246">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-247">Range-Lower</span></span>            | <span data-ttu-id="8709b-248">1</span><span class="sxs-lookup"><span data-stu-id="8709b-248">1</span></span>                               |
| <span data-ttu-id="8709b-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-249">Range-Upper</span></span>            | <span data-ttu-id="8709b-250">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-250">2048</span></span>                            |
| <span data-ttu-id="8709b-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-251">Search-Flags</span></span>           | <span data-ttu-id="8709b-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-252">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-253">System-Flags</span></span>           | <span data-ttu-id="8709b-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-254">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-255">Classes used in</span></span>        | [<span data-ttu-id="8709b-256">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-256">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8709b-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8709b-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8709b-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-258">Entry</span></span> | <span data-ttu-id="8709b-259">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-259">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-260">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-261">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-262">System-Only</span></span>            | <span data-ttu-id="8709b-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-263">False</span></span>                           |
| <span data-ttu-id="8709b-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-264">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-265">True</span><span class="sxs-lookup"><span data-stu-id="8709b-265">True</span></span>                            |
| <span data-ttu-id="8709b-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-266">Is Indexed</span></span>             | <span data-ttu-id="8709b-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-267">False</span></span>                           |
| <span data-ttu-id="8709b-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-268">In Global Catalog</span></span>      | <span data-ttu-id="8709b-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-269">False</span></span>                           |
| <span data-ttu-id="8709b-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-271">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-272">Range-Lower</span></span>            | <span data-ttu-id="8709b-273">1</span><span class="sxs-lookup"><span data-stu-id="8709b-273">1</span></span>                               |
| <span data-ttu-id="8709b-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-274">Range-Upper</span></span>            | <span data-ttu-id="8709b-275">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-275">2048</span></span>                            |
| <span data-ttu-id="8709b-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-276">Search-Flags</span></span>           | <span data-ttu-id="8709b-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-277">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-278">System-Flags</span></span>           | <span data-ttu-id="8709b-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-279">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-280">Classes used in</span></span>        | [<span data-ttu-id="8709b-281">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-281">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8709b-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8709b-282">Windows Server 2012</span></span>



| <span data-ttu-id="8709b-283">Ввод</span><span class="sxs-lookup"><span data-stu-id="8709b-283">Entry</span></span> | <span data-ttu-id="8709b-284">Значение</span><span class="sxs-lookup"><span data-stu-id="8709b-284">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="8709b-285">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8709b-285">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8709b-286">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="8709b-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="8709b-287">System-Only</span></span>            | <span data-ttu-id="8709b-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-288">False</span></span>                           |
| <span data-ttu-id="8709b-289">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8709b-289">Is-Single-Valued</span></span>       | <span data-ttu-id="8709b-290">True</span><span class="sxs-lookup"><span data-stu-id="8709b-290">True</span></span>                            |
| <span data-ttu-id="8709b-291">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8709b-291">Is Indexed</span></span>             | <span data-ttu-id="8709b-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-292">False</span></span>                           |
| <span data-ttu-id="8709b-293">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8709b-293">In Global Catalog</span></span>      | <span data-ttu-id="8709b-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="8709b-294">False</span></span>                           |
| <span data-ttu-id="8709b-295">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8709b-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="8709b-296">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8709b-296">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="8709b-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8709b-297">Range-Lower</span></span>            | <span data-ttu-id="8709b-298">1</span><span class="sxs-lookup"><span data-stu-id="8709b-298">1</span></span>                               |
| <span data-ttu-id="8709b-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8709b-299">Range-Upper</span></span>            | <span data-ttu-id="8709b-300">2048</span><span class="sxs-lookup"><span data-stu-id="8709b-300">2048</span></span>                            |
| <span data-ttu-id="8709b-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-301">Search-Flags</span></span>           | <span data-ttu-id="8709b-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8709b-302">0x00000000</span></span>                      |
| <span data-ttu-id="8709b-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8709b-303">System-Flags</span></span>           | <span data-ttu-id="8709b-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8709b-304">0x00000010</span></span>                      |
| <span data-ttu-id="8709b-305">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8709b-305">Classes used in</span></span>        | [<span data-ttu-id="8709b-306">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="8709b-306">**Top**</span></span>](c-top.md)<br/> |



 

 





