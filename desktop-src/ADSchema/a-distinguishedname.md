---
title: Атрибут obj-расп-Name
description: То же, что и различающееся имя объекта. Используется Exchange.
ms.assetid: 0dc2855c-2707-49d8-80e6-27f163a59bc8
ms.tgt_platform: multiple
keywords:
- Obj-распространитель-схема AD атрибута
- Схема AD атрибута distinguishedName
topic_type:
- apiref
api_name:
- Obj-Dist-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42cd118f38de78546b7b792bca3c8c9ef6d229cb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893034"
---
# <a name="obj-dist-name-attribute"></a><span data-ttu-id="afaab-106">Атрибут obj-расп-Name</span><span class="sxs-lookup"><span data-stu-id="afaab-106">Obj-Dist-Name attribute</span></span>

<span data-ttu-id="afaab-107">То же, что и различающееся имя объекта.</span><span class="sxs-lookup"><span data-stu-id="afaab-107">Same as the Distinguished Name for an object.</span></span> <span data-ttu-id="afaab-108">Используется Exchange.</span><span class="sxs-lookup"><span data-stu-id="afaab-108">Used by Exchange.</span></span>



| <span data-ttu-id="afaab-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-109">Entry</span></span> | <span data-ttu-id="afaab-110">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="afaab-111">CN</span><span class="sxs-lookup"><span data-stu-id="afaab-111">CN</span></span>                | <span data-ttu-id="afaab-112">Obj-расп-имя</span><span class="sxs-lookup"><span data-stu-id="afaab-112">Obj-Dist-Name</span></span>                           |
| <span data-ttu-id="afaab-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="afaab-113">Ldap-Display-Name</span></span> | <span data-ttu-id="afaab-114">distinguishedName</span><span class="sxs-lookup"><span data-stu-id="afaab-114">distinguishedName</span></span>                       |
| <span data-ttu-id="afaab-115">Размер</span><span class="sxs-lookup"><span data-stu-id="afaab-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="afaab-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="afaab-116">Update Privilege</span></span>  | <span data-ttu-id="afaab-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="afaab-117">This value is set by the system.</span></span>        |
| <span data-ttu-id="afaab-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="afaab-118">Update Frequency</span></span>  | <span data-ttu-id="afaab-119">При каждом создании или перемещении объекта.</span><span class="sxs-lookup"><span data-stu-id="afaab-119">Whenever an object is created or moved.</span></span> |
| <span data-ttu-id="afaab-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-120">Attribute-Id</span></span>      | <span data-ttu-id="afaab-121">2.5.4.49</span><span class="sxs-lookup"><span data-stu-id="afaab-121">2.5.4.49</span></span>                                |
| <span data-ttu-id="afaab-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="afaab-122">System-Id-Guid</span></span>    | <span data-ttu-id="afaab-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="afaab-123">bf9679e4-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="afaab-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afaab-124">Syntax</span></span>            | [<span data-ttu-id="afaab-125">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="afaab-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="afaab-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="afaab-126">Implementations</span></span>

-   [<span data-ttu-id="afaab-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="afaab-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="afaab-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="afaab-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="afaab-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="afaab-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="afaab-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="afaab-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="afaab-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="afaab-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="afaab-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="afaab-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="afaab-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="afaab-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="afaab-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afaab-134">Windows 2000 Server</span></span>



| <span data-ttu-id="afaab-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-135">Entry</span></span> | <span data-ttu-id="afaab-136">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-138">MAPI-Id</span></span>                | <span data-ttu-id="afaab-139">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-139">0x803C</span></span>                          |
| <span data-ttu-id="afaab-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-140">System-Only</span></span>            | <span data-ttu-id="afaab-141">True</span><span class="sxs-lookup"><span data-stu-id="afaab-141">True</span></span>                            |
| <span data-ttu-id="afaab-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-142">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-143">True</span><span class="sxs-lookup"><span data-stu-id="afaab-143">True</span></span>                            |
| <span data-ttu-id="afaab-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-144">Is Indexed</span></span>             | <span data-ttu-id="afaab-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-145">False</span></span>                           |
| <span data-ttu-id="afaab-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-146">In Global Catalog</span></span>      | <span data-ttu-id="afaab-147">True</span><span class="sxs-lookup"><span data-stu-id="afaab-147">True</span></span>                            |
| <span data-ttu-id="afaab-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-150">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-151">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-152">Search-Flags</span></span>           | <span data-ttu-id="afaab-153">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-153">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-154">System-Flags</span></span>           | <span data-ttu-id="afaab-155">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-155">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-156">Classes used in</span></span>        | [<span data-ttu-id="afaab-157">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="afaab-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afaab-158">Windows Server 2003</span></span>



| <span data-ttu-id="afaab-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-159">Entry</span></span> | <span data-ttu-id="afaab-160">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-160">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-161">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-162">MAPI-Id</span></span>                | <span data-ttu-id="afaab-163">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-163">0x803C</span></span>                          |
| <span data-ttu-id="afaab-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-164">System-Only</span></span>            | <span data-ttu-id="afaab-165">True</span><span class="sxs-lookup"><span data-stu-id="afaab-165">True</span></span>                            |
| <span data-ttu-id="afaab-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-166">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-167">True</span><span class="sxs-lookup"><span data-stu-id="afaab-167">True</span></span>                            |
| <span data-ttu-id="afaab-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-168">Is Indexed</span></span>             | <span data-ttu-id="afaab-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-169">False</span></span>                           |
| <span data-ttu-id="afaab-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-170">In Global Catalog</span></span>      | <span data-ttu-id="afaab-171">True</span><span class="sxs-lookup"><span data-stu-id="afaab-171">True</span></span>                            |
| <span data-ttu-id="afaab-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-173">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-174">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-175">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-176">Search-Flags</span></span>           | <span data-ttu-id="afaab-177">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-177">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-178">System-Flags</span></span>           | <span data-ttu-id="afaab-179">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-179">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-180">Classes used in</span></span>        | [<span data-ttu-id="afaab-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="afaab-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="afaab-182">ADAM</span></span>



| <span data-ttu-id="afaab-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-183">Entry</span></span> | <span data-ttu-id="afaab-184">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-184">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-185">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-186">MAPI-Id</span></span>                | <span data-ttu-id="afaab-187">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-187">0x803C</span></span>                          |
| <span data-ttu-id="afaab-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-188">System-Only</span></span>            | <span data-ttu-id="afaab-189">True</span><span class="sxs-lookup"><span data-stu-id="afaab-189">True</span></span>                            |
| <span data-ttu-id="afaab-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-190">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-191">True</span><span class="sxs-lookup"><span data-stu-id="afaab-191">True</span></span>                            |
| <span data-ttu-id="afaab-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-192">Is Indexed</span></span>             | <span data-ttu-id="afaab-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-193">False</span></span>                           |
| <span data-ttu-id="afaab-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-194">In Global Catalog</span></span>      | <span data-ttu-id="afaab-195">True</span><span class="sxs-lookup"><span data-stu-id="afaab-195">True</span></span>                            |
| <span data-ttu-id="afaab-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-197">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-198">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-199">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-200">Search-Flags</span></span>           | <span data-ttu-id="afaab-201">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-201">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-202">System-Flags</span></span>           | <span data-ttu-id="afaab-203">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-203">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-204">Classes used in</span></span>        | [<span data-ttu-id="afaab-205">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="afaab-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="afaab-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="afaab-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-207">Entry</span></span> | <span data-ttu-id="afaab-208">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-208">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-209">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-210">MAPI-Id</span></span>                | <span data-ttu-id="afaab-211">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-211">0x803C</span></span>                          |
| <span data-ttu-id="afaab-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-212">System-Only</span></span>            | <span data-ttu-id="afaab-213">True</span><span class="sxs-lookup"><span data-stu-id="afaab-213">True</span></span>                            |
| <span data-ttu-id="afaab-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-214">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-215">True</span><span class="sxs-lookup"><span data-stu-id="afaab-215">True</span></span>                            |
| <span data-ttu-id="afaab-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-216">Is Indexed</span></span>             | <span data-ttu-id="afaab-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-217">False</span></span>                           |
| <span data-ttu-id="afaab-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-218">In Global Catalog</span></span>      | <span data-ttu-id="afaab-219">True</span><span class="sxs-lookup"><span data-stu-id="afaab-219">True</span></span>                            |
| <span data-ttu-id="afaab-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-221">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-222">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-223">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-224">Search-Flags</span></span>           | <span data-ttu-id="afaab-225">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-225">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-226">System-Flags</span></span>           | <span data-ttu-id="afaab-227">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-227">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-228">Classes used in</span></span>        | [<span data-ttu-id="afaab-229">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="afaab-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afaab-230">Windows Server 2008</span></span>



| <span data-ttu-id="afaab-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-231">Entry</span></span> | <span data-ttu-id="afaab-232">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-232">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-233">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-234">MAPI-Id</span></span>                | <span data-ttu-id="afaab-235">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-235">0x803C</span></span>                          |
| <span data-ttu-id="afaab-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-236">System-Only</span></span>            | <span data-ttu-id="afaab-237">True</span><span class="sxs-lookup"><span data-stu-id="afaab-237">True</span></span>                            |
| <span data-ttu-id="afaab-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-238">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-239">True</span><span class="sxs-lookup"><span data-stu-id="afaab-239">True</span></span>                            |
| <span data-ttu-id="afaab-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-240">Is Indexed</span></span>             | <span data-ttu-id="afaab-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-241">False</span></span>                           |
| <span data-ttu-id="afaab-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-242">In Global Catalog</span></span>      | <span data-ttu-id="afaab-243">True</span><span class="sxs-lookup"><span data-stu-id="afaab-243">True</span></span>                            |
| <span data-ttu-id="afaab-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-245">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-246">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-247">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-248">Search-Flags</span></span>           | <span data-ttu-id="afaab-249">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-249">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-250">System-Flags</span></span>           | <span data-ttu-id="afaab-251">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-251">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-252">Classes used in</span></span>        | [<span data-ttu-id="afaab-253">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="afaab-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afaab-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="afaab-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-255">Entry</span></span> | <span data-ttu-id="afaab-256">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-256">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-257">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-258">MAPI-Id</span></span>                | <span data-ttu-id="afaab-259">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-259">0x803C</span></span>                          |
| <span data-ttu-id="afaab-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-260">System-Only</span></span>            | <span data-ttu-id="afaab-261">True</span><span class="sxs-lookup"><span data-stu-id="afaab-261">True</span></span>                            |
| <span data-ttu-id="afaab-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-262">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-263">True</span><span class="sxs-lookup"><span data-stu-id="afaab-263">True</span></span>                            |
| <span data-ttu-id="afaab-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-264">Is Indexed</span></span>             | <span data-ttu-id="afaab-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-265">False</span></span>                           |
| <span data-ttu-id="afaab-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-266">In Global Catalog</span></span>      | <span data-ttu-id="afaab-267">True</span><span class="sxs-lookup"><span data-stu-id="afaab-267">True</span></span>                            |
| <span data-ttu-id="afaab-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-269">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-270">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-271">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-272">Search-Flags</span></span>           | <span data-ttu-id="afaab-273">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-273">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-274">System-Flags</span></span>           | <span data-ttu-id="afaab-275">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-275">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-276">Classes used in</span></span>        | [<span data-ttu-id="afaab-277">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="afaab-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="afaab-278">Windows Server 2012</span></span>



| <span data-ttu-id="afaab-279">Ввод</span><span class="sxs-lookup"><span data-stu-id="afaab-279">Entry</span></span> | <span data-ttu-id="afaab-280">Значение</span><span class="sxs-lookup"><span data-stu-id="afaab-280">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="afaab-281">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="afaab-281">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="afaab-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="afaab-282">MAPI-Id</span></span>                | <span data-ttu-id="afaab-283">0x803C</span><span class="sxs-lookup"><span data-stu-id="afaab-283">0x803C</span></span>                          |
| <span data-ttu-id="afaab-284">System-Only</span><span class="sxs-lookup"><span data-stu-id="afaab-284">System-Only</span></span>            | <span data-ttu-id="afaab-285">True</span><span class="sxs-lookup"><span data-stu-id="afaab-285">True</span></span>                            |
| <span data-ttu-id="afaab-286">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="afaab-286">Is-Single-Valued</span></span>       | <span data-ttu-id="afaab-287">True</span><span class="sxs-lookup"><span data-stu-id="afaab-287">True</span></span>                            |
| <span data-ttu-id="afaab-288">Индексируется</span><span class="sxs-lookup"><span data-stu-id="afaab-288">Is Indexed</span></span>             | <span data-ttu-id="afaab-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="afaab-289">False</span></span>                           |
| <span data-ttu-id="afaab-290">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="afaab-290">In Global Catalog</span></span>      | <span data-ttu-id="afaab-291">True</span><span class="sxs-lookup"><span data-stu-id="afaab-291">True</span></span>                            |
| <span data-ttu-id="afaab-292">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="afaab-292">NT-Security-Descriptor</span></span> | <span data-ttu-id="afaab-293">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="afaab-293">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="afaab-294">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="afaab-294">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="afaab-295">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="afaab-295">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="afaab-296">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-296">Search-Flags</span></span>           | <span data-ttu-id="afaab-297">0x00000008</span><span class="sxs-lookup"><span data-stu-id="afaab-297">0x00000008</span></span>                      |
| <span data-ttu-id="afaab-298">System-Flags</span><span class="sxs-lookup"><span data-stu-id="afaab-298">System-Flags</span></span>           | <span data-ttu-id="afaab-299">0x00000013</span><span class="sxs-lookup"><span data-stu-id="afaab-299">0x00000013</span></span>                      |
| <span data-ttu-id="afaab-300">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="afaab-300">Classes used in</span></span>        | [<span data-ttu-id="afaab-301">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="afaab-301">**Top**</span></span>](c-top.md)<br/> |



 

 





