---
title: Пек-Key-изменение-атрибут Interval
description: Интервал изменения ключа шифрования пароля.
ms.assetid: 2031feda-3f5d-4c76-bb45-42157fd5cb84
ms.tgt_platform: multiple
keywords:
- Пек — схема AD атрибута Interval
- Схема AD атрибута Пеккэйчанжеинтервал
topic_type:
- apiref
api_name:
- Pek-Key-Change-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2259bdd4dfee24bbccfeafa6d5bb06490c24c25c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655091"
---
# <a name="pek-key-change-interval-attribute"></a><span data-ttu-id="4b8a9-105">Пек-Key-изменение-атрибут Interval</span><span class="sxs-lookup"><span data-stu-id="4b8a9-105">Pek-Key-Change-Interval attribute</span></span>

<span data-ttu-id="4b8a9-106">Интервал изменения ключа шифрования пароля.</span><span class="sxs-lookup"><span data-stu-id="4b8a9-106">Password encryption key change interval.</span></span>



| <span data-ttu-id="4b8a9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-107">Entry</span></span> | <span data-ttu-id="4b8a9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4b8a9-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b8a9-109">CN</span></span>                | <span data-ttu-id="4b8a9-110">Пек — изменение интервала</span><span class="sxs-lookup"><span data-stu-id="4b8a9-110">Pek-Key-Change-Interval</span></span>              |
| <span data-ttu-id="4b8a9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4b8a9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b8a9-112">пеккэйчанжеинтервал</span><span class="sxs-lookup"><span data-stu-id="4b8a9-112">pekKeyChangeInterval</span></span>                 |
| <span data-ttu-id="4b8a9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4b8a9-113">Size</span></span>              | <span data-ttu-id="4b8a9-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="4b8a9-114">8 bytes</span></span>                              |
| <span data-ttu-id="4b8a9-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4b8a9-115">Update Privilege</span></span>  | <span data-ttu-id="4b8a9-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="4b8a9-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="4b8a9-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4b8a9-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4b8a9-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-118">Attribute-Id</span></span>      | <span data-ttu-id="4b8a9-119">1.2.840.113556.1.4.866</span><span class="sxs-lookup"><span data-stu-id="4b8a9-119">1.2.840.113556.1.4.866</span></span>               |
| <span data-ttu-id="4b8a9-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4b8a9-120">System-Id-Guid</span></span>    | <span data-ttu-id="4b8a9-121">07383084-91df-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="4b8a9-121">07383084-91df-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="4b8a9-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b8a9-122">Syntax</span></span>            | [<span data-ttu-id="4b8a9-123">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-123">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="4b8a9-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4b8a9-124">Implementations</span></span>

-   [<span data-ttu-id="4b8a9-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b8a9-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b8a9-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b8a9-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b8a9-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b8a9-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b8a9-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b8a9-131">Windows 2000 Server</span></span>



| <span data-ttu-id="4b8a9-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-132">Entry</span></span> | <span data-ttu-id="4b8a9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b8a9-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8a9-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8a9-136">System-Only</span></span>            | <span data-ttu-id="4b8a9-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-137">False</span></span>                                        |
| <span data-ttu-id="4b8a9-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8a9-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8a9-139">True</span><span class="sxs-lookup"><span data-stu-id="4b8a9-139">True</span></span>                                         |
| <span data-ttu-id="4b8a9-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8a9-140">Is Indexed</span></span>             | <span data-ttu-id="4b8a9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-141">False</span></span>                                        |
| <span data-ttu-id="4b8a9-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8a9-142">In Global Catalog</span></span>      | <span data-ttu-id="4b8a9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-143">False</span></span>                                        |
| <span data-ttu-id="4b8a9-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8a9-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8a9-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8a9-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b8a9-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8a9-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8a9-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-148">Search-Flags</span></span>           | <span data-ttu-id="4b8a9-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8a9-149">0x00000000</span></span>                                   |
| <span data-ttu-id="4b8a9-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-150">System-Flags</span></span>           | <span data-ttu-id="4b8a9-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8a9-151">0x00000010</span></span>                                   |
| <span data-ttu-id="4b8a9-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8a9-152">Classes used in</span></span>        | [<span data-ttu-id="4b8a9-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b8a9-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b8a9-154">Windows Server 2003</span></span>



| <span data-ttu-id="4b8a9-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-155">Entry</span></span> | <span data-ttu-id="4b8a9-156">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b8a9-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8a9-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8a9-159">System-Only</span></span>            | <span data-ttu-id="4b8a9-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-160">False</span></span>                                        |
| <span data-ttu-id="4b8a9-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8a9-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8a9-162">True</span><span class="sxs-lookup"><span data-stu-id="4b8a9-162">True</span></span>                                         |
| <span data-ttu-id="4b8a9-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8a9-163">Is Indexed</span></span>             | <span data-ttu-id="4b8a9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-164">False</span></span>                                        |
| <span data-ttu-id="4b8a9-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8a9-165">In Global Catalog</span></span>      | <span data-ttu-id="4b8a9-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-166">False</span></span>                                        |
| <span data-ttu-id="4b8a9-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8a9-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8a9-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8a9-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b8a9-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8a9-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8a9-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-171">Search-Flags</span></span>           | <span data-ttu-id="4b8a9-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8a9-172">0x00000000</span></span>                                   |
| <span data-ttu-id="4b8a9-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-173">System-Flags</span></span>           | <span data-ttu-id="4b8a9-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8a9-174">0x00000010</span></span>                                   |
| <span data-ttu-id="4b8a9-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8a9-175">Classes used in</span></span>        | [<span data-ttu-id="4b8a9-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b8a9-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b8a9-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b8a9-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-178">Entry</span></span> | <span data-ttu-id="4b8a9-179">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b8a9-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8a9-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8a9-182">System-Only</span></span>            | <span data-ttu-id="4b8a9-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-183">False</span></span>                                        |
| <span data-ttu-id="4b8a9-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8a9-184">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8a9-185">True</span><span class="sxs-lookup"><span data-stu-id="4b8a9-185">True</span></span>                                         |
| <span data-ttu-id="4b8a9-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8a9-186">Is Indexed</span></span>             | <span data-ttu-id="4b8a9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-187">False</span></span>                                        |
| <span data-ttu-id="4b8a9-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8a9-188">In Global Catalog</span></span>      | <span data-ttu-id="4b8a9-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-189">False</span></span>                                        |
| <span data-ttu-id="4b8a9-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8a9-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8a9-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8a9-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b8a9-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8a9-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8a9-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-194">Search-Flags</span></span>           | <span data-ttu-id="4b8a9-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8a9-195">0x00000000</span></span>                                   |
| <span data-ttu-id="4b8a9-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-196">System-Flags</span></span>           | <span data-ttu-id="4b8a9-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8a9-197">0x00000010</span></span>                                   |
| <span data-ttu-id="4b8a9-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8a9-198">Classes used in</span></span>        | [<span data-ttu-id="4b8a9-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b8a9-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b8a9-200">Windows Server 2008</span></span>



| <span data-ttu-id="4b8a9-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-201">Entry</span></span> | <span data-ttu-id="4b8a9-202">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b8a9-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8a9-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8a9-205">System-Only</span></span>            | <span data-ttu-id="4b8a9-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-206">False</span></span>                                        |
| <span data-ttu-id="4b8a9-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8a9-207">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8a9-208">True</span><span class="sxs-lookup"><span data-stu-id="4b8a9-208">True</span></span>                                         |
| <span data-ttu-id="4b8a9-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8a9-209">Is Indexed</span></span>             | <span data-ttu-id="4b8a9-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-210">False</span></span>                                        |
| <span data-ttu-id="4b8a9-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8a9-211">In Global Catalog</span></span>      | <span data-ttu-id="4b8a9-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-212">False</span></span>                                        |
| <span data-ttu-id="4b8a9-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8a9-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8a9-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8a9-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b8a9-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8a9-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8a9-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-217">Search-Flags</span></span>           | <span data-ttu-id="4b8a9-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8a9-218">0x00000000</span></span>                                   |
| <span data-ttu-id="4b8a9-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-219">System-Flags</span></span>           | <span data-ttu-id="4b8a9-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8a9-220">0x00000010</span></span>                                   |
| <span data-ttu-id="4b8a9-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8a9-221">Classes used in</span></span>        | [<span data-ttu-id="4b8a9-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b8a9-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b8a9-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b8a9-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-224">Entry</span></span> | <span data-ttu-id="4b8a9-225">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b8a9-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8a9-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8a9-228">System-Only</span></span>            | <span data-ttu-id="4b8a9-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-229">False</span></span>                                        |
| <span data-ttu-id="4b8a9-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8a9-230">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8a9-231">True</span><span class="sxs-lookup"><span data-stu-id="4b8a9-231">True</span></span>                                         |
| <span data-ttu-id="4b8a9-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8a9-232">Is Indexed</span></span>             | <span data-ttu-id="4b8a9-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-233">False</span></span>                                        |
| <span data-ttu-id="4b8a9-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8a9-234">In Global Catalog</span></span>      | <span data-ttu-id="4b8a9-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-235">False</span></span>                                        |
| <span data-ttu-id="4b8a9-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8a9-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8a9-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8a9-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b8a9-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8a9-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8a9-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-240">Search-Flags</span></span>           | <span data-ttu-id="4b8a9-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8a9-241">0x00000000</span></span>                                   |
| <span data-ttu-id="4b8a9-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-242">System-Flags</span></span>           | <span data-ttu-id="4b8a9-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8a9-243">0x00000010</span></span>                                   |
| <span data-ttu-id="4b8a9-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8a9-244">Classes used in</span></span>        | [<span data-ttu-id="4b8a9-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b8a9-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b8a9-246">Windows Server 2012</span></span>



| <span data-ttu-id="4b8a9-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b8a9-247">Entry</span></span> | <span data-ttu-id="4b8a9-248">Значение</span><span class="sxs-lookup"><span data-stu-id="4b8a9-248">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b8a9-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b8a9-249">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b8a9-250">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b8a9-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b8a9-251">System-Only</span></span>            | <span data-ttu-id="4b8a9-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-252">False</span></span>                                        |
| <span data-ttu-id="4b8a9-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b8a9-253">Is-Single-Valued</span></span>       | <span data-ttu-id="4b8a9-254">True</span><span class="sxs-lookup"><span data-stu-id="4b8a9-254">True</span></span>                                         |
| <span data-ttu-id="4b8a9-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b8a9-255">Is Indexed</span></span>             | <span data-ttu-id="4b8a9-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-256">False</span></span>                                        |
| <span data-ttu-id="4b8a9-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b8a9-257">In Global Catalog</span></span>      | <span data-ttu-id="4b8a9-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b8a9-258">False</span></span>                                        |
| <span data-ttu-id="4b8a9-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b8a9-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b8a9-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b8a9-260">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b8a9-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b8a9-261">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b8a9-262">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b8a9-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-263">Search-Flags</span></span>           | <span data-ttu-id="4b8a9-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b8a9-264">0x00000000</span></span>                                   |
| <span data-ttu-id="4b8a9-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b8a9-265">System-Flags</span></span>           | <span data-ttu-id="4b8a9-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b8a9-266">0x00000010</span></span>                                   |
| <span data-ttu-id="4b8a9-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b8a9-267">Classes used in</span></span>        | [<span data-ttu-id="4b8a9-268">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b8a9-268">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





