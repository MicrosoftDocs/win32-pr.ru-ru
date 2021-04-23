---
title: Атрибут Object-Version
description: Это можно использовать для хранения номера версии объекта.
ms.assetid: 1aa8520b-c640-4ea2-9230-f28154bf69b0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Object-Version
- Схема AD атрибута Обжектверсион
topic_type:
- apiref
api_name:
- Object-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f038f6286db575f4141c2e306086bb9a8faac71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655326"
---
# <a name="object-version-attribute"></a><span data-ttu-id="b9f4f-105">Атрибут Object-Version</span><span class="sxs-lookup"><span data-stu-id="b9f4f-105">Object-Version attribute</span></span>

<span data-ttu-id="b9f4f-106">Это можно использовать для хранения номера версии объекта.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-106">This can be used to store a version number for the object.</span></span>



| <span data-ttu-id="b9f4f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-107">Entry</span></span> | <span data-ttu-id="b9f4f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-108">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="b9f4f-109">CN</span><span class="sxs-lookup"><span data-stu-id="b9f4f-109">CN</span></span>                | <span data-ttu-id="b9f4f-110">Object-Version</span><span class="sxs-lookup"><span data-stu-id="b9f4f-110">Object-Version</span></span>                                                 |
| <span data-ttu-id="b9f4f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b9f4f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b9f4f-112">обжектверсион</span><span class="sxs-lookup"><span data-stu-id="b9f4f-112">objectVersion</span></span>                                                  |
| <span data-ttu-id="b9f4f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b9f4f-113">Size</span></span>              | <span data-ttu-id="b9f4f-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="b9f4f-114">4 bytes</span></span>                                                        |
| <span data-ttu-id="b9f4f-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b9f4f-115">Update Privilege</span></span>  | <span data-ttu-id="b9f4f-116">Это значение задается конструктором объекта.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-116">The designer of the object would set this value.</span></span>               |
| <span data-ttu-id="b9f4f-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b9f4f-117">Update Frequency</span></span>  | <span data-ttu-id="b9f4f-118">Это значение должно увеличиваться каждый раз при изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="b9f4f-118">This value should be incremented each time the object changes.</span></span> |
| <span data-ttu-id="b9f4f-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-119">Attribute-Id</span></span>      | <span data-ttu-id="b9f4f-120">1.2.840.113556.1.2.76</span><span class="sxs-lookup"><span data-stu-id="b9f4f-120">1.2.840.113556.1.2.76</span></span>                                          |
| <span data-ttu-id="b9f4f-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b9f4f-121">System-Id-Guid</span></span>    | <span data-ttu-id="b9f4f-122">16775848-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b9f4f-122">16775848-47f3-11d1-a9c3-0000f80367c1</span></span>                           |
| <span data-ttu-id="b9f4f-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9f4f-123">Syntax</span></span>            | [<span data-ttu-id="b9f4f-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-124">**Enumeration**</span></span>](s-enumeration.md)                           |



## <a name="implementations"></a><span data-ttu-id="b9f4f-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b9f4f-125">Implementations</span></span>

-   [<span data-ttu-id="b9f4f-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b9f4f-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b9f4f-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b9f4f-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b9f4f-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b9f4f-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b9f4f-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b9f4f-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b9f4f-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b9f4f-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-134">Entry</span></span> | <span data-ttu-id="b9f4f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-137">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-138">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-138">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-139">System-Only</span></span>            | <span data-ttu-id="b9f4f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-140">False</span></span>                           |
| <span data-ttu-id="b9f4f-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-142">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-142">True</span></span>                            |
| <span data-ttu-id="b9f4f-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-143">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-144">False</span></span>                           |
| <span data-ttu-id="b9f4f-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-145">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-146">False</span></span>                           |
| <span data-ttu-id="b9f4f-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-151">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-152">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-153">System-Flags</span></span>           | <span data-ttu-id="b9f4f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-154">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-155">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b9f4f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b9f4f-157">Windows Server 2003</span></span>



| <span data-ttu-id="b9f4f-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-158">Entry</span></span> | <span data-ttu-id="b9f4f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-161">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-162">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-162">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-163">System-Only</span></span>            | <span data-ttu-id="b9f4f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-164">False</span></span>                           |
| <span data-ttu-id="b9f4f-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-166">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-166">True</span></span>                            |
| <span data-ttu-id="b9f4f-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-167">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-168">False</span></span>                           |
| <span data-ttu-id="b9f4f-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-169">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-170">False</span></span>                           |
| <span data-ttu-id="b9f4f-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-175">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-176">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-177">System-Flags</span></span>           | <span data-ttu-id="b9f4f-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-178">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-179">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-180">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b9f4f-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="b9f4f-181">ADAM</span></span>



| <span data-ttu-id="b9f4f-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-182">Entry</span></span> | <span data-ttu-id="b9f4f-183">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-185">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-186">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-186">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-187">System-Only</span></span>            | <span data-ttu-id="b9f4f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-188">False</span></span>                           |
| <span data-ttu-id="b9f4f-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-190">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-190">True</span></span>                            |
| <span data-ttu-id="b9f4f-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-191">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-192">False</span></span>                           |
| <span data-ttu-id="b9f4f-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-193">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-194">False</span></span>                           |
| <span data-ttu-id="b9f4f-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-199">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-200">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-201">System-Flags</span></span>           | <span data-ttu-id="b9f4f-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-202">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-203">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b9f4f-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b9f4f-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b9f4f-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-206">Entry</span></span> | <span data-ttu-id="b9f4f-207">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-209">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-210">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-210">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-211">System-Only</span></span>            | <span data-ttu-id="b9f4f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-212">False</span></span>                           |
| <span data-ttu-id="b9f4f-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-214">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-214">True</span></span>                            |
| <span data-ttu-id="b9f4f-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-215">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-216">False</span></span>                           |
| <span data-ttu-id="b9f4f-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-217">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-218">False</span></span>                           |
| <span data-ttu-id="b9f4f-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-223">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-224">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-225">System-Flags</span></span>           | <span data-ttu-id="b9f4f-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-226">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-227">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b9f4f-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9f4f-229">Windows Server 2008</span></span>



| <span data-ttu-id="b9f4f-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-230">Entry</span></span> | <span data-ttu-id="b9f4f-231">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-233">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-234">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-234">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-235">System-Only</span></span>            | <span data-ttu-id="b9f4f-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-236">False</span></span>                           |
| <span data-ttu-id="b9f4f-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-238">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-238">True</span></span>                            |
| <span data-ttu-id="b9f4f-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-239">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-240">False</span></span>                           |
| <span data-ttu-id="b9f4f-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-241">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-242">False</span></span>                           |
| <span data-ttu-id="b9f4f-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-247">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-248">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-249">System-Flags</span></span>           | <span data-ttu-id="b9f4f-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-250">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-251">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-252">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b9f4f-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9f4f-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b9f4f-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-254">Entry</span></span> | <span data-ttu-id="b9f4f-255">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-257">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-258">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-258">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-259">System-Only</span></span>            | <span data-ttu-id="b9f4f-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-260">False</span></span>                           |
| <span data-ttu-id="b9f4f-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-262">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-262">True</span></span>                            |
| <span data-ttu-id="b9f4f-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-263">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-264">False</span></span>                           |
| <span data-ttu-id="b9f4f-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-265">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-266">False</span></span>                           |
| <span data-ttu-id="b9f4f-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-271">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-272">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-273">System-Flags</span></span>           | <span data-ttu-id="b9f4f-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-274">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-275">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-276">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b9f4f-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b9f4f-277">Windows Server 2012</span></span>



| <span data-ttu-id="b9f4f-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="b9f4f-278">Entry</span></span> | <span data-ttu-id="b9f4f-279">Значение</span><span class="sxs-lookup"><span data-stu-id="b9f4f-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b9f4f-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b9f4f-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b9f4f-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b9f4f-281">MAPI-Id</span></span>                | <span data-ttu-id="b9f4f-282">0x80F7</span><span class="sxs-lookup"><span data-stu-id="b9f4f-282">0x80F7</span></span>                          |
| <span data-ttu-id="b9f4f-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="b9f4f-283">System-Only</span></span>            | <span data-ttu-id="b9f4f-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-284">False</span></span>                           |
| <span data-ttu-id="b9f4f-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b9f4f-285">Is-Single-Valued</span></span>       | <span data-ttu-id="b9f4f-286">True</span><span class="sxs-lookup"><span data-stu-id="b9f4f-286">True</span></span>                            |
| <span data-ttu-id="b9f4f-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b9f4f-287">Is Indexed</span></span>             | <span data-ttu-id="b9f4f-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-288">False</span></span>                           |
| <span data-ttu-id="b9f4f-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b9f4f-289">In Global Catalog</span></span>      | <span data-ttu-id="b9f4f-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="b9f4f-290">False</span></span>                           |
| <span data-ttu-id="b9f4f-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b9f4f-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="b9f4f-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b9f4f-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b9f4f-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b9f4f-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b9f4f-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b9f4f-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-295">Search-Flags</span></span>           | <span data-ttu-id="b9f4f-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b9f4f-296">0x00000000</span></span>                      |
| <span data-ttu-id="b9f4f-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b9f4f-297">System-Flags</span></span>           | <span data-ttu-id="b9f4f-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b9f4f-298">0x00000010</span></span>                      |
| <span data-ttu-id="b9f4f-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b9f4f-299">Classes used in</span></span>        | [<span data-ttu-id="b9f4f-300">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b9f4f-300">**Top**</span></span>](c-top.md)<br/> |



 

 





