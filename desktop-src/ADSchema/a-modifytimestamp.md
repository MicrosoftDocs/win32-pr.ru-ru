---
title: Атрибут-метка времени изменения
description: Вычисленный атрибут, представляющий дату последнего изменения этого объекта. Это значение не реплицируется.
ms.assetid: ad8fea90-9a78-484d-9549-26d78e87ec44
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута времени изменения
- Схема AD атрибута Модифитиместамп
topic_type:
- apiref
api_name:
- Modify-Time-Stamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c032d19c3bd2bf5a6ee0cfe038e9fa9b184d36
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804403"
---
# <a name="modify-time-stamp-attribute"></a><span data-ttu-id="b4e21-106">Атрибут-метка времени изменения</span><span class="sxs-lookup"><span data-stu-id="b4e21-106">Modify-Time-Stamp attribute</span></span>

<span data-ttu-id="b4e21-107">Вычисленный атрибут, представляющий дату последнего изменения этого объекта.</span><span class="sxs-lookup"><span data-stu-id="b4e21-107">A computed attribute that represents the date when this object was last changed.</span></span> <span data-ttu-id="b4e21-108">Это значение не реплицируется.</span><span class="sxs-lookup"><span data-stu-id="b4e21-108">This value is not replicated.</span></span>



| <span data-ttu-id="b4e21-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-109">Entry</span></span> | <span data-ttu-id="b4e21-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-110">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="b4e21-111">CN</span><span class="sxs-lookup"><span data-stu-id="b4e21-111">CN</span></span>                | <span data-ttu-id="b4e21-112">Метка времени изменения</span><span class="sxs-lookup"><span data-stu-id="b4e21-112">Modify-Time-Stamp</span></span>                                             |
| <span data-ttu-id="b4e21-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b4e21-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b4e21-114">modifyTimeStamp</span><span class="sxs-lookup"><span data-stu-id="b4e21-114">modifyTimeStamp</span></span>                                               |
| <span data-ttu-id="b4e21-115">Размер</span><span class="sxs-lookup"><span data-stu-id="b4e21-115">Size</span></span>              | <span data-ttu-id="b4e21-116">8 байт</span><span class="sxs-lookup"><span data-stu-id="b4e21-116">8 bytes</span></span>                                                       |
| <span data-ttu-id="b4e21-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b4e21-117">Update Privilege</span></span>  | <span data-ttu-id="b4e21-118">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b4e21-118">This value is set by the system.</span></span>                              |
| <span data-ttu-id="b4e21-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b4e21-119">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="b4e21-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-120">Attribute-Id</span></span>      | <span data-ttu-id="b4e21-121">2.5.18.2</span><span class="sxs-lookup"><span data-stu-id="b4e21-121">2.5.18.2</span></span>                                                      |
| <span data-ttu-id="b4e21-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b4e21-122">System-Id-Guid</span></span>    | <span data-ttu-id="b4e21-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b4e21-123">9a7ad94a-ca53-11d1-bbd0-0080c76670c0</span></span>                          |
| <span data-ttu-id="b4e21-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4e21-124">Syntax</span></span>            | [<span data-ttu-id="b4e21-125">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="b4e21-125">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="b4e21-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b4e21-126">Implementations</span></span>

-   [<span data-ttu-id="b4e21-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b4e21-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b4e21-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b4e21-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b4e21-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b4e21-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b4e21-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b4e21-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b4e21-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b4e21-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b4e21-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b4e21-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b4e21-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b4e21-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b4e21-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4e21-134">Windows 2000 Server</span></span>



| <span data-ttu-id="b4e21-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-135">Entry</span></span> | <span data-ttu-id="b4e21-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-137">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-138">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-139">System-Only</span></span>            | <span data-ttu-id="b4e21-140">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-140">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-141">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-142">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-142">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-143">Is Indexed</span></span>             | <span data-ttu-id="b4e21-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-144">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-145">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-146">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-148">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-149">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-150">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-151">Search-Flags</span></span>           | <span data-ttu-id="b4e21-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-152">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-153">System-Flags</span></span>           | <span data-ttu-id="b4e21-154">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-154">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-155">Classes used in</span></span>        | [<span data-ttu-id="b4e21-156">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-156">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-157">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-157">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b4e21-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4e21-158">Windows Server 2003</span></span>



| <span data-ttu-id="b4e21-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-159">Entry</span></span> | <span data-ttu-id="b4e21-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-161">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-162">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-163">System-Only</span></span>            | <span data-ttu-id="b4e21-164">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-164">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-166">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-166">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-167">Is Indexed</span></span>             | <span data-ttu-id="b4e21-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-168">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-169">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-170">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-172">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-173">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-174">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-175">Search-Flags</span></span>           | <span data-ttu-id="b4e21-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-176">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-177">System-Flags</span></span>           | <span data-ttu-id="b4e21-178">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-178">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-179">Classes used in</span></span>        | [<span data-ttu-id="b4e21-180">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-180">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-181">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-181">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b4e21-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="b4e21-182">ADAM</span></span>



| <span data-ttu-id="b4e21-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-183">Entry</span></span> | <span data-ttu-id="b4e21-184">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-185">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-186">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-187">System-Only</span></span>            | <span data-ttu-id="b4e21-188">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-188">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-189">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-190">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-190">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-191">Is Indexed</span></span>             | <span data-ttu-id="b4e21-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-192">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-193">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-194">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-196">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-197">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-198">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-199">Search-Flags</span></span>           | <span data-ttu-id="b4e21-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-200">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-201">System-Flags</span></span>           | <span data-ttu-id="b4e21-202">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-202">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-203">Classes used in</span></span>        | [<span data-ttu-id="b4e21-204">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-204">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-205">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-205">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b4e21-206">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b4e21-206">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b4e21-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-207">Entry</span></span> | <span data-ttu-id="b4e21-208">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-209">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-210">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-211">System-Only</span></span>            | <span data-ttu-id="b4e21-212">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-212">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-213">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-214">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-214">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-215">Is Indexed</span></span>             | <span data-ttu-id="b4e21-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-216">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-217">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-218">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-220">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-221">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-222">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-223">Search-Flags</span></span>           | <span data-ttu-id="b4e21-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-224">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-225">System-Flags</span></span>           | <span data-ttu-id="b4e21-226">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-226">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-227">Classes used in</span></span>        | [<span data-ttu-id="b4e21-228">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-228">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-229">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-229">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b4e21-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4e21-230">Windows Server 2008</span></span>



| <span data-ttu-id="b4e21-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-231">Entry</span></span> | <span data-ttu-id="b4e21-232">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-233">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-234">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-235">System-Only</span></span>            | <span data-ttu-id="b4e21-236">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-236">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-238">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-238">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-239">Is Indexed</span></span>             | <span data-ttu-id="b4e21-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-240">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-241">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-242">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-244">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-245">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-246">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-247">Search-Flags</span></span>           | <span data-ttu-id="b4e21-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-248">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-249">System-Flags</span></span>           | <span data-ttu-id="b4e21-250">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-250">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-251">Classes used in</span></span>        | [<span data-ttu-id="b4e21-252">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-252">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-253">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-253">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b4e21-254">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4e21-254">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b4e21-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-255">Entry</span></span> | <span data-ttu-id="b4e21-256">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-257">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-258">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-259">System-Only</span></span>            | <span data-ttu-id="b4e21-260">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-260">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-262">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-262">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-263">Is Indexed</span></span>             | <span data-ttu-id="b4e21-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-264">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-265">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-266">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-268">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-269">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-270">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-271">Search-Flags</span></span>           | <span data-ttu-id="b4e21-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-272">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-273">System-Flags</span></span>           | <span data-ttu-id="b4e21-274">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-274">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-275">Classes used in</span></span>        | [<span data-ttu-id="b4e21-276">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-276">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-277">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-277">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b4e21-278">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4e21-278">Windows Server 2012</span></span>



| <span data-ttu-id="b4e21-279">Ввод</span><span class="sxs-lookup"><span data-stu-id="b4e21-279">Entry</span></span> | <span data-ttu-id="b4e21-280">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e21-280">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b4e21-281">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b4e21-281">Link-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-282">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b4e21-282">MAPI-Id</span></span>                | \-                                                                          |
| <span data-ttu-id="b4e21-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="b4e21-283">System-Only</span></span>            | <span data-ttu-id="b4e21-284">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-284">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b4e21-285">Is-Single-Valued</span></span>       | <span data-ttu-id="b4e21-286">True</span><span class="sxs-lookup"><span data-stu-id="b4e21-286">True</span></span>                                                                        |
| <span data-ttu-id="b4e21-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b4e21-287">Is Indexed</span></span>             | <span data-ttu-id="b4e21-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-288">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b4e21-289">In Global Catalog</span></span>      | <span data-ttu-id="b4e21-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="b4e21-290">False</span></span>                                                                       |
| <span data-ttu-id="b4e21-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b4e21-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="b4e21-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b4e21-292">O:BAG:BAD:S:</span></span>                                                                |
| <span data-ttu-id="b4e21-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b4e21-293">Range-Lower</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b4e21-294">Range-Upper</span></span>            | \-                                                                          |
| <span data-ttu-id="b4e21-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-295">Search-Flags</span></span>           | <span data-ttu-id="b4e21-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b4e21-296">0x00000000</span></span>                                                                  |
| <span data-ttu-id="b4e21-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b4e21-297">System-Flags</span></span>           | <span data-ttu-id="b4e21-298">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b4e21-298">0x08000014</span></span>                                                                  |
| <span data-ttu-id="b4e21-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b4e21-299">Classes used in</span></span>        | [<span data-ttu-id="b4e21-300">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b4e21-300">**SubSchema**</span></span>](c-subschema.md)<br/> [<span data-ttu-id="b4e21-301">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b4e21-301">**Top**</span></span>](c-top.md)<br/> |



 

 





