---
title: Атрибут Reps-To
description: Выводит список серверов, которые каталог будет уведомлять об изменениях и серверах, на которые каталог будет отправлять изменения по запросу для определенного контекста именования.
ms.assetid: d7fd5a57-a0e1-4c69-9b9a-1cdad87610b1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Reps-To
- Схема AD атрибута Репсто
topic_type:
- apiref
api_name:
- Reps-To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5c39d19eb12bb801d7ca7fb9b22ed665d59d10
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989775"
---
# <a name="reps-to-attribute"></a><span data-ttu-id="05db4-105">Атрибут Reps-To</span><span class="sxs-lookup"><span data-stu-id="05db4-105">Reps-To attribute</span></span>

<span data-ttu-id="05db4-106">Выводит список серверов, которые каталог будет уведомлять об изменениях и серверах, на которые каталог будет отправлять изменения по запросу для определенного контекста именования.</span><span class="sxs-lookup"><span data-stu-id="05db4-106">Lists the servers that the directory will notify of changes and servers to which the directory will send changes on Request for the defined naming context.</span></span>



| <span data-ttu-id="05db4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-107">Entry</span></span> | <span data-ttu-id="05db4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="05db4-109">CN</span><span class="sxs-lookup"><span data-stu-id="05db4-109">CN</span></span>                | <span data-ttu-id="05db4-110">Reps-To</span><span class="sxs-lookup"><span data-stu-id="05db4-110">Reps-To</span></span>                                               |
| <span data-ttu-id="05db4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="05db4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="05db4-112">репсто</span><span class="sxs-lookup"><span data-stu-id="05db4-112">repsTo</span></span>                                                |
| <span data-ttu-id="05db4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="05db4-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="05db4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="05db4-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="05db4-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="05db4-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="05db4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-116">Attribute-Id</span></span>      | <span data-ttu-id="05db4-117">1.2.840.113556.1.2.83</span><span class="sxs-lookup"><span data-stu-id="05db4-117">1.2.840.113556.1.2.83</span></span>                                 |
| <span data-ttu-id="05db4-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="05db4-118">System-Id-Guid</span></span>    | <span data-ttu-id="05db4-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="05db4-119">bf967a1e-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="05db4-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05db4-120">Syntax</span></span>            | [<span data-ttu-id="05db4-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="05db4-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="05db4-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="05db4-122">Implementations</span></span>

-   [<span data-ttu-id="05db4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="05db4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="05db4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="05db4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="05db4-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="05db4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="05db4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="05db4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="05db4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="05db4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="05db4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="05db4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="05db4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="05db4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="05db4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="05db4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="05db4-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-131">Entry</span></span> | <span data-ttu-id="05db4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-135">System-Only</span></span>            | <span data-ttu-id="05db4-136">True</span><span class="sxs-lookup"><span data-stu-id="05db4-136">True</span></span>                            |
| <span data-ttu-id="05db4-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-138">False</span></span>                           |
| <span data-ttu-id="05db4-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-139">Is Indexed</span></span>             | <span data-ttu-id="05db4-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-140">False</span></span>                           |
| <span data-ttu-id="05db4-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-141">In Global Catalog</span></span>      | <span data-ttu-id="05db4-142">True</span><span class="sxs-lookup"><span data-stu-id="05db4-142">True</span></span>                            |
| <span data-ttu-id="05db4-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-147">Search-Flags</span></span>           | <span data-ttu-id="05db4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-148">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-149">System-Flags</span></span>           | <span data-ttu-id="05db4-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-150">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-151">Classes used in</span></span>        | [<span data-ttu-id="05db4-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="05db4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="05db4-153">Windows Server 2003</span></span>



| <span data-ttu-id="05db4-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-154">Entry</span></span> | <span data-ttu-id="05db4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-158">System-Only</span></span>            | <span data-ttu-id="05db4-159">True</span><span class="sxs-lookup"><span data-stu-id="05db4-159">True</span></span>                            |
| <span data-ttu-id="05db4-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-161">False</span></span>                           |
| <span data-ttu-id="05db4-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-162">Is Indexed</span></span>             | <span data-ttu-id="05db4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-163">False</span></span>                           |
| <span data-ttu-id="05db4-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-164">In Global Catalog</span></span>      | <span data-ttu-id="05db4-165">True</span><span class="sxs-lookup"><span data-stu-id="05db4-165">True</span></span>                            |
| <span data-ttu-id="05db4-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-170">Search-Flags</span></span>           | <span data-ttu-id="05db4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-171">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-172">System-Flags</span></span>           | <span data-ttu-id="05db4-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-173">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-174">Classes used in</span></span>        | [<span data-ttu-id="05db4-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="05db4-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="05db4-176">ADAM</span></span>



| <span data-ttu-id="05db4-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-177">Entry</span></span> | <span data-ttu-id="05db4-178">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-181">System-Only</span></span>            | <span data-ttu-id="05db4-182">True</span><span class="sxs-lookup"><span data-stu-id="05db4-182">True</span></span>                            |
| <span data-ttu-id="05db4-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-184">False</span></span>                           |
| <span data-ttu-id="05db4-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-185">Is Indexed</span></span>             | <span data-ttu-id="05db4-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-186">False</span></span>                           |
| <span data-ttu-id="05db4-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-187">In Global Catalog</span></span>      | <span data-ttu-id="05db4-188">True</span><span class="sxs-lookup"><span data-stu-id="05db4-188">True</span></span>                            |
| <span data-ttu-id="05db4-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-193">Search-Flags</span></span>           | <span data-ttu-id="05db4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-194">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-195">System-Flags</span></span>           | <span data-ttu-id="05db4-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-196">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-197">Classes used in</span></span>        | [<span data-ttu-id="05db4-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="05db4-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="05db4-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="05db4-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-200">Entry</span></span> | <span data-ttu-id="05db4-201">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-204">System-Only</span></span>            | <span data-ttu-id="05db4-205">True</span><span class="sxs-lookup"><span data-stu-id="05db4-205">True</span></span>                            |
| <span data-ttu-id="05db4-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-207">False</span></span>                           |
| <span data-ttu-id="05db4-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-208">Is Indexed</span></span>             | <span data-ttu-id="05db4-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-209">False</span></span>                           |
| <span data-ttu-id="05db4-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-210">In Global Catalog</span></span>      | <span data-ttu-id="05db4-211">True</span><span class="sxs-lookup"><span data-stu-id="05db4-211">True</span></span>                            |
| <span data-ttu-id="05db4-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-216">Search-Flags</span></span>           | <span data-ttu-id="05db4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-217">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-218">System-Flags</span></span>           | <span data-ttu-id="05db4-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-219">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-220">Classes used in</span></span>        | [<span data-ttu-id="05db4-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="05db4-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05db4-222">Windows Server 2008</span></span>



| <span data-ttu-id="05db4-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-223">Entry</span></span> | <span data-ttu-id="05db4-224">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-227">System-Only</span></span>            | <span data-ttu-id="05db4-228">True</span><span class="sxs-lookup"><span data-stu-id="05db4-228">True</span></span>                            |
| <span data-ttu-id="05db4-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-230">False</span></span>                           |
| <span data-ttu-id="05db4-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-231">Is Indexed</span></span>             | <span data-ttu-id="05db4-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-232">False</span></span>                           |
| <span data-ttu-id="05db4-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-233">In Global Catalog</span></span>      | <span data-ttu-id="05db4-234">True</span><span class="sxs-lookup"><span data-stu-id="05db4-234">True</span></span>                            |
| <span data-ttu-id="05db4-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-239">Search-Flags</span></span>           | <span data-ttu-id="05db4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-240">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-241">System-Flags</span></span>           | <span data-ttu-id="05db4-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-242">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-243">Classes used in</span></span>        | [<span data-ttu-id="05db4-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="05db4-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="05db4-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="05db4-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-246">Entry</span></span> | <span data-ttu-id="05db4-247">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-250">System-Only</span></span>            | <span data-ttu-id="05db4-251">True</span><span class="sxs-lookup"><span data-stu-id="05db4-251">True</span></span>                            |
| <span data-ttu-id="05db4-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-253">False</span></span>                           |
| <span data-ttu-id="05db4-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-254">Is Indexed</span></span>             | <span data-ttu-id="05db4-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-255">False</span></span>                           |
| <span data-ttu-id="05db4-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-256">In Global Catalog</span></span>      | <span data-ttu-id="05db4-257">True</span><span class="sxs-lookup"><span data-stu-id="05db4-257">True</span></span>                            |
| <span data-ttu-id="05db4-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-262">Search-Flags</span></span>           | <span data-ttu-id="05db4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-263">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-264">System-Flags</span></span>           | <span data-ttu-id="05db4-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-265">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-266">Classes used in</span></span>        | [<span data-ttu-id="05db4-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="05db4-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="05db4-268">Windows Server 2012</span></span>



| <span data-ttu-id="05db4-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="05db4-269">Entry</span></span> | <span data-ttu-id="05db4-270">Значение</span><span class="sxs-lookup"><span data-stu-id="05db4-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="05db4-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="05db4-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="05db4-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="05db4-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="05db4-273">System-Only</span></span>            | <span data-ttu-id="05db4-274">True</span><span class="sxs-lookup"><span data-stu-id="05db4-274">True</span></span>                            |
| <span data-ttu-id="05db4-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="05db4-275">Is-Single-Valued</span></span>       | <span data-ttu-id="05db4-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-276">False</span></span>                           |
| <span data-ttu-id="05db4-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="05db4-277">Is Indexed</span></span>             | <span data-ttu-id="05db4-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="05db4-278">False</span></span>                           |
| <span data-ttu-id="05db4-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="05db4-279">In Global Catalog</span></span>      | <span data-ttu-id="05db4-280">True</span><span class="sxs-lookup"><span data-stu-id="05db4-280">True</span></span>                            |
| <span data-ttu-id="05db4-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="05db4-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="05db4-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="05db4-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="05db4-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="05db4-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="05db4-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="05db4-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="05db4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-285">Search-Flags</span></span>           | <span data-ttu-id="05db4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="05db4-286">0x00000000</span></span>                      |
| <span data-ttu-id="05db4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="05db4-287">System-Flags</span></span>           | <span data-ttu-id="05db4-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="05db4-288">0x00000013</span></span>                      |
| <span data-ttu-id="05db4-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="05db4-289">Classes used in</span></span>        | [<span data-ttu-id="05db4-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="05db4-290">**Top**</span></span>](c-top.md)<br/> |



 

 





