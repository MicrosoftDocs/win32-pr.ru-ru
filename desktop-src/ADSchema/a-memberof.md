---
title: Атрибут является членом списка рассылки
description: Различающееся имя групп, к которым принадлежит этот объект.
ms.assetid: 28fe1991-291b-4531-aec2-b1a1910be464
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута является членом группы рассылки
- Схема AD атрибута memberOf
topic_type:
- apiref
api_name:
- Is-Member-Of-DL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad522fcba256e0965057a9f8a8505e99a3fdbdeb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654911"
---
# <a name="is-member-of-dl-attribute"></a><span data-ttu-id="36a6a-105">Атрибут является членом списка рассылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-105">Is-Member-Of-DL attribute</span></span>

<span data-ttu-id="36a6a-106">Различающееся имя групп, к которым принадлежит этот объект.</span><span class="sxs-lookup"><span data-stu-id="36a6a-106">The distinguished name of the groups to which this object belongs.</span></span>



| <span data-ttu-id="36a6a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-107">Entry</span></span> | <span data-ttu-id="36a6a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="36a6a-109">CN</span><span class="sxs-lookup"><span data-stu-id="36a6a-109">CN</span></span>                | <span data-ttu-id="36a6a-110">Входит в состав списка рассылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-110">Is-Member-Of-DL</span></span>                         |
| <span data-ttu-id="36a6a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="36a6a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36a6a-112">memberOf</span><span class="sxs-lookup"><span data-stu-id="36a6a-112">memberOf</span></span>                                |
| <span data-ttu-id="36a6a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="36a6a-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="36a6a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="36a6a-114">Update Privilege</span></span>  | <span data-ttu-id="36a6a-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="36a6a-115">Domain administrator</span></span>                    |
| <span data-ttu-id="36a6a-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="36a6a-116">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="36a6a-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-117">Attribute-Id</span></span>      | <span data-ttu-id="36a6a-118">1.2.840.113556.1.2.102</span><span class="sxs-lookup"><span data-stu-id="36a6a-118">1.2.840.113556.1.2.102</span></span>                  |
| <span data-ttu-id="36a6a-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="36a6a-119">System-Id-Guid</span></span>    | <span data-ttu-id="36a6a-120">bf967991-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="36a6a-120">bf967991-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="36a6a-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36a6a-121">Syntax</span></span>            | [<span data-ttu-id="36a6a-122">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="36a6a-122">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="36a6a-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="36a6a-123">Implementations</span></span>

-   [<span data-ttu-id="36a6a-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="36a6a-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="36a6a-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="36a6a-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="36a6a-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="36a6a-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="36a6a-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="36a6a-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="36a6a-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36a6a-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36a6a-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36a6a-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36a6a-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36a6a-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="36a6a-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36a6a-131">Windows 2000 Server</span></span>



| <span data-ttu-id="36a6a-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-132">Entry</span></span> | <span data-ttu-id="36a6a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-134">Link-Id</span></span>                | <span data-ttu-id="36a6a-135">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-135">3</span></span>                               |
| <span data-ttu-id="36a6a-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-136">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-137">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-137">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-138">System-Only</span></span>            | <span data-ttu-id="36a6a-139">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-139">True</span></span>                            |
| <span data-ttu-id="36a6a-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-140">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-141">False</span></span>                           |
| <span data-ttu-id="36a6a-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-142">Is Indexed</span></span>             | <span data-ttu-id="36a6a-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-143">False</span></span>                           |
| <span data-ttu-id="36a6a-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-144">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-145">False</span></span>                           |
| <span data-ttu-id="36a6a-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-150">Search-Flags</span></span>           | <span data-ttu-id="36a6a-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-151">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-152">System-Flags</span></span>           | <span data-ttu-id="36a6a-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-153">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-154">Classes used in</span></span>        | [<span data-ttu-id="36a6a-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="36a6a-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36a6a-156">Windows Server 2003</span></span>



| <span data-ttu-id="36a6a-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-157">Entry</span></span> | <span data-ttu-id="36a6a-158">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-159">Link-Id</span></span>                | <span data-ttu-id="36a6a-160">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-160">3</span></span>                               |
| <span data-ttu-id="36a6a-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-161">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-162">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-162">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-163">System-Only</span></span>            | <span data-ttu-id="36a6a-164">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-164">True</span></span>                            |
| <span data-ttu-id="36a6a-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-165">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-166">False</span></span>                           |
| <span data-ttu-id="36a6a-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-167">Is Indexed</span></span>             | <span data-ttu-id="36a6a-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-168">False</span></span>                           |
| <span data-ttu-id="36a6a-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-169">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-170">False</span></span>                           |
| <span data-ttu-id="36a6a-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-175">Search-Flags</span></span>           | <span data-ttu-id="36a6a-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-176">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-177">System-Flags</span></span>           | <span data-ttu-id="36a6a-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-178">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-179">Classes used in</span></span>        | [<span data-ttu-id="36a6a-180">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="36a6a-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="36a6a-181">ADAM</span></span>



| <span data-ttu-id="36a6a-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-182">Entry</span></span> | <span data-ttu-id="36a6a-183">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-184">Link-Id</span></span>                | <span data-ttu-id="36a6a-185">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-185">3</span></span>                               |
| <span data-ttu-id="36a6a-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-186">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-187">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-187">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-188">System-Only</span></span>            | <span data-ttu-id="36a6a-189">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-189">True</span></span>                            |
| <span data-ttu-id="36a6a-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-190">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-191">False</span></span>                           |
| <span data-ttu-id="36a6a-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-192">Is Indexed</span></span>             | <span data-ttu-id="36a6a-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-193">False</span></span>                           |
| <span data-ttu-id="36a6a-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-194">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-195">False</span></span>                           |
| <span data-ttu-id="36a6a-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-200">Search-Flags</span></span>           | <span data-ttu-id="36a6a-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-201">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-202">System-Flags</span></span>           | <span data-ttu-id="36a6a-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-203">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-204">Classes used in</span></span>        | [<span data-ttu-id="36a6a-205">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="36a6a-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="36a6a-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="36a6a-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-207">Entry</span></span> | <span data-ttu-id="36a6a-208">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-209">Link-Id</span></span>                | <span data-ttu-id="36a6a-210">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-210">3</span></span>                               |
| <span data-ttu-id="36a6a-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-211">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-212">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-212">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-213">System-Only</span></span>            | <span data-ttu-id="36a6a-214">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-214">True</span></span>                            |
| <span data-ttu-id="36a6a-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-215">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-216">False</span></span>                           |
| <span data-ttu-id="36a6a-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-217">Is Indexed</span></span>             | <span data-ttu-id="36a6a-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-218">False</span></span>                           |
| <span data-ttu-id="36a6a-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-219">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-220">False</span></span>                           |
| <span data-ttu-id="36a6a-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-222">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-223">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-224">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-225">Search-Flags</span></span>           | <span data-ttu-id="36a6a-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-226">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-227">System-Flags</span></span>           | <span data-ttu-id="36a6a-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-228">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-229">Classes used in</span></span>        | [<span data-ttu-id="36a6a-230">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-230">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="36a6a-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36a6a-231">Windows Server 2008</span></span>



| <span data-ttu-id="36a6a-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-232">Entry</span></span> | <span data-ttu-id="36a6a-233">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-233">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-234">Link-Id</span></span>                | <span data-ttu-id="36a6a-235">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-235">3</span></span>                               |
| <span data-ttu-id="36a6a-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-236">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-237">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-237">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-238">System-Only</span></span>            | <span data-ttu-id="36a6a-239">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-239">True</span></span>                            |
| <span data-ttu-id="36a6a-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-240">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-241">False</span></span>                           |
| <span data-ttu-id="36a6a-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-242">Is Indexed</span></span>             | <span data-ttu-id="36a6a-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-243">False</span></span>                           |
| <span data-ttu-id="36a6a-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-244">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-245">False</span></span>                           |
| <span data-ttu-id="36a6a-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-247">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-248">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-249">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-250">Search-Flags</span></span>           | <span data-ttu-id="36a6a-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-251">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-252">System-Flags</span></span>           | <span data-ttu-id="36a6a-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-253">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-254">Classes used in</span></span>        | [<span data-ttu-id="36a6a-255">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-255">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36a6a-256">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36a6a-256">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36a6a-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-257">Entry</span></span> | <span data-ttu-id="36a6a-258">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-258">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-259">Link-Id</span></span>                | <span data-ttu-id="36a6a-260">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-260">3</span></span>                               |
| <span data-ttu-id="36a6a-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-261">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-262">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-262">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-263">System-Only</span></span>            | <span data-ttu-id="36a6a-264">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-264">True</span></span>                            |
| <span data-ttu-id="36a6a-265">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-265">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-266">False</span></span>                           |
| <span data-ttu-id="36a6a-267">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-267">Is Indexed</span></span>             | <span data-ttu-id="36a6a-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-268">False</span></span>                           |
| <span data-ttu-id="36a6a-269">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-269">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-270">False</span></span>                           |
| <span data-ttu-id="36a6a-271">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-272">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-272">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-273">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-274">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-275">Search-Flags</span></span>           | <span data-ttu-id="36a6a-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-276">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-277">System-Flags</span></span>           | <span data-ttu-id="36a6a-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-278">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-279">Classes used in</span></span>        | [<span data-ttu-id="36a6a-280">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-280">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36a6a-281">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36a6a-281">Windows Server 2012</span></span>



| <span data-ttu-id="36a6a-282">Ввод</span><span class="sxs-lookup"><span data-stu-id="36a6a-282">Entry</span></span> | <span data-ttu-id="36a6a-283">Значение</span><span class="sxs-lookup"><span data-stu-id="36a6a-283">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="36a6a-284">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36a6a-284">Link-Id</span></span>                | <span data-ttu-id="36a6a-285">3</span><span class="sxs-lookup"><span data-stu-id="36a6a-285">3</span></span>                               |
| <span data-ttu-id="36a6a-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36a6a-286">MAPI-Id</span></span>                | <span data-ttu-id="36a6a-287">0x8008</span><span class="sxs-lookup"><span data-stu-id="36a6a-287">0x8008</span></span>                          |
| <span data-ttu-id="36a6a-288">System-Only</span><span class="sxs-lookup"><span data-stu-id="36a6a-288">System-Only</span></span>            | <span data-ttu-id="36a6a-289">True</span><span class="sxs-lookup"><span data-stu-id="36a6a-289">True</span></span>                            |
| <span data-ttu-id="36a6a-290">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36a6a-290">Is-Single-Valued</span></span>       | <span data-ttu-id="36a6a-291">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-291">False</span></span>                           |
| <span data-ttu-id="36a6a-292">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36a6a-292">Is Indexed</span></span>             | <span data-ttu-id="36a6a-293">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-293">False</span></span>                           |
| <span data-ttu-id="36a6a-294">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36a6a-294">In Global Catalog</span></span>      | <span data-ttu-id="36a6a-295">Неверно</span><span class="sxs-lookup"><span data-stu-id="36a6a-295">False</span></span>                           |
| <span data-ttu-id="36a6a-296">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36a6a-296">NT-Security-Descriptor</span></span> | <span data-ttu-id="36a6a-297">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36a6a-297">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="36a6a-298">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36a6a-298">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="36a6a-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36a6a-299">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="36a6a-300">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-300">Search-Flags</span></span>           | <span data-ttu-id="36a6a-301">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-301">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-302">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36a6a-302">System-Flags</span></span>           | <span data-ttu-id="36a6a-303">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36a6a-303">0x00000010</span></span>                      |
| <span data-ttu-id="36a6a-304">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36a6a-304">Classes used in</span></span>        | [<span data-ttu-id="36a6a-305">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="36a6a-305">**Top**</span></span>](c-top.md)<br/> |



 

 





