---
title: Атрибут Reps-From
description: Выводит список серверов, на которых каталог будет принимать изменения для определенного контекста именования.
ms.assetid: 2e18410b-d383-4838-aeaf-dd479be5f44d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Reps-From
- Схема AD атрибута Репсфром
topic_type:
- apiref
api_name:
- Reps-From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc6981b71b6ec251eb27af0e7570fe1558d1ff20
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655069"
---
# <a name="reps-from-attribute"></a><span data-ttu-id="b8cdb-105">Атрибут Reps-From</span><span class="sxs-lookup"><span data-stu-id="b8cdb-105">Reps-From attribute</span></span>

<span data-ttu-id="b8cdb-106">Выводит список серверов, на которых каталог будет принимать изменения для определенного контекста именования.</span><span class="sxs-lookup"><span data-stu-id="b8cdb-106">Lists the servers from which the directory will accept changes for the defined naming context.</span></span>



| <span data-ttu-id="b8cdb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-107">Entry</span></span> | <span data-ttu-id="b8cdb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b8cdb-109">CN</span><span class="sxs-lookup"><span data-stu-id="b8cdb-109">CN</span></span>                | <span data-ttu-id="b8cdb-110">Reps-From</span><span class="sxs-lookup"><span data-stu-id="b8cdb-110">Reps-From</span></span>                                             |
| <span data-ttu-id="b8cdb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b8cdb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b8cdb-112">репсфром</span><span class="sxs-lookup"><span data-stu-id="b8cdb-112">repsFrom</span></span>                                              |
| <span data-ttu-id="b8cdb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b8cdb-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b8cdb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b8cdb-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b8cdb-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b8cdb-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b8cdb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-116">Attribute-Id</span></span>      | <span data-ttu-id="b8cdb-117">1.2.840.113556.1.2.91</span><span class="sxs-lookup"><span data-stu-id="b8cdb-117">1.2.840.113556.1.2.91</span></span>                                 |
| <span data-ttu-id="b8cdb-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b8cdb-118">System-Id-Guid</span></span>    | <span data-ttu-id="b8cdb-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="b8cdb-119">bf967a1d-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="b8cdb-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8cdb-120">Syntax</span></span>            | [<span data-ttu-id="b8cdb-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b8cdb-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b8cdb-122">Implementations</span></span>

-   [<span data-ttu-id="b8cdb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b8cdb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b8cdb-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b8cdb-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b8cdb-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b8cdb-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b8cdb-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b8cdb-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8cdb-130">Windows 2000 Server</span></span>



| <span data-ttu-id="b8cdb-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-131">Entry</span></span> | <span data-ttu-id="b8cdb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-135">System-Only</span></span>            | <span data-ttu-id="b8cdb-136">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-136">True</span></span>                            |
| <span data-ttu-id="b8cdb-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-138">False</span></span>                           |
| <span data-ttu-id="b8cdb-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-139">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-140">False</span></span>                           |
| <span data-ttu-id="b8cdb-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-141">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-142">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-142">True</span></span>                            |
| <span data-ttu-id="b8cdb-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-147">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-148">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-149">System-Flags</span></span>           | <span data-ttu-id="b8cdb-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-150">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-151">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b8cdb-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b8cdb-153">Windows Server 2003</span></span>



| <span data-ttu-id="b8cdb-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-154">Entry</span></span> | <span data-ttu-id="b8cdb-155">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-158">System-Only</span></span>            | <span data-ttu-id="b8cdb-159">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-159">True</span></span>                            |
| <span data-ttu-id="b8cdb-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-160">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-161">False</span></span>                           |
| <span data-ttu-id="b8cdb-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-162">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-163">False</span></span>                           |
| <span data-ttu-id="b8cdb-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-164">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-165">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-165">True</span></span>                            |
| <span data-ttu-id="b8cdb-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-170">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-171">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-172">System-Flags</span></span>           | <span data-ttu-id="b8cdb-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-173">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-174">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b8cdb-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="b8cdb-176">ADAM</span></span>



| <span data-ttu-id="b8cdb-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-177">Entry</span></span> | <span data-ttu-id="b8cdb-178">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-181">System-Only</span></span>            | <span data-ttu-id="b8cdb-182">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-182">True</span></span>                            |
| <span data-ttu-id="b8cdb-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-183">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-184">False</span></span>                           |
| <span data-ttu-id="b8cdb-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-185">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-186">False</span></span>                           |
| <span data-ttu-id="b8cdb-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-187">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-188">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-188">True</span></span>                            |
| <span data-ttu-id="b8cdb-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-193">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-194">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-195">System-Flags</span></span>           | <span data-ttu-id="b8cdb-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-196">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-197">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b8cdb-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b8cdb-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b8cdb-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-200">Entry</span></span> | <span data-ttu-id="b8cdb-201">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-204">System-Only</span></span>            | <span data-ttu-id="b8cdb-205">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-205">True</span></span>                            |
| <span data-ttu-id="b8cdb-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-206">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-207">False</span></span>                           |
| <span data-ttu-id="b8cdb-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-208">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-209">False</span></span>                           |
| <span data-ttu-id="b8cdb-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-210">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-211">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-211">True</span></span>                            |
| <span data-ttu-id="b8cdb-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-216">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-217">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-218">System-Flags</span></span>           | <span data-ttu-id="b8cdb-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-219">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-220">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b8cdb-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8cdb-222">Windows Server 2008</span></span>



| <span data-ttu-id="b8cdb-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-223">Entry</span></span> | <span data-ttu-id="b8cdb-224">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-227">System-Only</span></span>            | <span data-ttu-id="b8cdb-228">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-228">True</span></span>                            |
| <span data-ttu-id="b8cdb-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-229">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-230">False</span></span>                           |
| <span data-ttu-id="b8cdb-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-231">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-232">False</span></span>                           |
| <span data-ttu-id="b8cdb-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-233">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-234">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-234">True</span></span>                            |
| <span data-ttu-id="b8cdb-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-239">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-240">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-241">System-Flags</span></span>           | <span data-ttu-id="b8cdb-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-242">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-243">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b8cdb-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8cdb-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b8cdb-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-246">Entry</span></span> | <span data-ttu-id="b8cdb-247">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-250">System-Only</span></span>            | <span data-ttu-id="b8cdb-251">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-251">True</span></span>                            |
| <span data-ttu-id="b8cdb-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-252">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-253">False</span></span>                           |
| <span data-ttu-id="b8cdb-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-254">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-255">False</span></span>                           |
| <span data-ttu-id="b8cdb-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-256">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-257">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-257">True</span></span>                            |
| <span data-ttu-id="b8cdb-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-262">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-263">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-264">System-Flags</span></span>           | <span data-ttu-id="b8cdb-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-265">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-266">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b8cdb-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8cdb-268">Windows Server 2012</span></span>



| <span data-ttu-id="b8cdb-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="b8cdb-269">Entry</span></span> | <span data-ttu-id="b8cdb-270">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cdb-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b8cdb-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b8cdb-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b8cdb-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b8cdb-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="b8cdb-273">System-Only</span></span>            | <span data-ttu-id="b8cdb-274">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-274">True</span></span>                            |
| <span data-ttu-id="b8cdb-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b8cdb-275">Is-Single-Valued</span></span>       | <span data-ttu-id="b8cdb-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-276">False</span></span>                           |
| <span data-ttu-id="b8cdb-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b8cdb-277">Is Indexed</span></span>             | <span data-ttu-id="b8cdb-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="b8cdb-278">False</span></span>                           |
| <span data-ttu-id="b8cdb-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b8cdb-279">In Global Catalog</span></span>      | <span data-ttu-id="b8cdb-280">True</span><span class="sxs-lookup"><span data-stu-id="b8cdb-280">True</span></span>                            |
| <span data-ttu-id="b8cdb-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b8cdb-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="b8cdb-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b8cdb-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b8cdb-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b8cdb-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b8cdb-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b8cdb-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-285">Search-Flags</span></span>           | <span data-ttu-id="b8cdb-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b8cdb-286">0x00000000</span></span>                      |
| <span data-ttu-id="b8cdb-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b8cdb-287">System-Flags</span></span>           | <span data-ttu-id="b8cdb-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="b8cdb-288">0x00000013</span></span>                      |
| <span data-ttu-id="b8cdb-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b8cdb-289">Classes used in</span></span>        | [<span data-ttu-id="b8cdb-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b8cdb-290">**Top**</span></span>](c-top.md)<br/> |



 

 





