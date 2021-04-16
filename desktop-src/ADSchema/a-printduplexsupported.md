---
title: Print — поддерживаемый атрибут
description: Указывает тип дуплексной поддержки принтера.
ms.assetid: c7d3e3f1-d6a1-41b7-a54d-c932a00b2a68
ms.tgt_platform: multiple
keywords:
- Print-схема AD атрибутов, поддерживаемая в режиме дуплекса
- Схема AD атрибута Принтдуплекссуппортед
topic_type:
- apiref
api_name:
- Print-Duplex-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027b5af8d2c2bc8ece810a00c17060608b7824c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655086"
---
# <a name="print-duplex-supported-attribute"></a><span data-ttu-id="75f45-105">Print — поддерживаемый атрибут</span><span class="sxs-lookup"><span data-stu-id="75f45-105">Print-Duplex-Supported attribute</span></span>

<span data-ttu-id="75f45-106">Указывает тип дуплексной поддержки принтера.</span><span class="sxs-lookup"><span data-stu-id="75f45-106">Indicates the type of duplex support a printer has.</span></span>



| <span data-ttu-id="75f45-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-107">Entry</span></span> | <span data-ttu-id="75f45-108">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="75f45-109">CN</span><span class="sxs-lookup"><span data-stu-id="75f45-109">CN</span></span>                | <span data-ttu-id="75f45-110">Печать — дуплексная — поддерживается</span><span class="sxs-lookup"><span data-stu-id="75f45-110">Print-Duplex-Supported</span></span>                                |
| <span data-ttu-id="75f45-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="75f45-111">Ldap-Display-Name</span></span> | <span data-ttu-id="75f45-112">printDuplexSupported</span><span class="sxs-lookup"><span data-stu-id="75f45-112">printDuplexSupported</span></span>                                  |
| <span data-ttu-id="75f45-113">Размер</span><span class="sxs-lookup"><span data-stu-id="75f45-113">Size</span></span>              | <span data-ttu-id="75f45-114">4 байта.</span><span class="sxs-lookup"><span data-stu-id="75f45-114">4 bytes.</span></span> <span data-ttu-id="75f45-115">Поддержка дуплекса = 2.</span><span class="sxs-lookup"><span data-stu-id="75f45-115">Duplex supported = 2.</span></span> <span data-ttu-id="75f45-116">Симплексная = 1 или 0.</span><span class="sxs-lookup"><span data-stu-id="75f45-116">Simplex only = 1 or 0.</span></span> |
| <span data-ttu-id="75f45-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="75f45-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="75f45-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="75f45-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="75f45-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-119">Attribute-Id</span></span>      | <span data-ttu-id="75f45-120">1.2.840.113556.1.4.1311</span><span class="sxs-lookup"><span data-stu-id="75f45-120">1.2.840.113556.1.4.1311</span></span>                               |
| <span data-ttu-id="75f45-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="75f45-121">System-Id-Guid</span></span>    | <span data-ttu-id="75f45-122">281416cc-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="75f45-122">281416cc-1968-11d0-a28f-00aa003049e2</span></span>                  |
| <span data-ttu-id="75f45-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75f45-123">Syntax</span></span>            | [<span data-ttu-id="75f45-124">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="75f45-124">**Boolean**</span></span>](s-boolean.md)                          |



## <a name="implementations"></a><span data-ttu-id="75f45-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="75f45-125">Implementations</span></span>

-   [<span data-ttu-id="75f45-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="75f45-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="75f45-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="75f45-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="75f45-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="75f45-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="75f45-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="75f45-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="75f45-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="75f45-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="75f45-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="75f45-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="75f45-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="75f45-132">Windows 2000 Server</span></span>



| <span data-ttu-id="75f45-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-133">Entry</span></span> | <span data-ttu-id="75f45-134">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="75f45-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="75f45-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="75f45-137">System-Only</span></span>            | <span data-ttu-id="75f45-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-138">False</span></span>                                          |
| <span data-ttu-id="75f45-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="75f45-139">Is-Single-Valued</span></span>       | <span data-ttu-id="75f45-140">True</span><span class="sxs-lookup"><span data-stu-id="75f45-140">True</span></span>                                           |
| <span data-ttu-id="75f45-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="75f45-141">Is Indexed</span></span>             | <span data-ttu-id="75f45-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-142">False</span></span>                                          |
| <span data-ttu-id="75f45-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="75f45-143">In Global Catalog</span></span>      | <span data-ttu-id="75f45-144">True</span><span class="sxs-lookup"><span data-stu-id="75f45-144">True</span></span>                                           |
| <span data-ttu-id="75f45-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="75f45-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="75f45-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75f45-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="75f45-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75f45-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="75f45-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75f45-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="75f45-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-149">Search-Flags</span></span>           | <span data-ttu-id="75f45-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75f45-150">0x00000000</span></span>                                     |
| <span data-ttu-id="75f45-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-151">System-Flags</span></span>           | <span data-ttu-id="75f45-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75f45-152">0x00000010</span></span>                                     |
| <span data-ttu-id="75f45-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="75f45-153">Classes used in</span></span>        | [<span data-ttu-id="75f45-154">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="75f45-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="75f45-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75f45-155">Windows Server 2003</span></span>



| <span data-ttu-id="75f45-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-156">Entry</span></span> | <span data-ttu-id="75f45-157">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="75f45-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="75f45-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="75f45-160">System-Only</span></span>            | <span data-ttu-id="75f45-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-161">False</span></span>                                          |
| <span data-ttu-id="75f45-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="75f45-162">Is-Single-Valued</span></span>       | <span data-ttu-id="75f45-163">True</span><span class="sxs-lookup"><span data-stu-id="75f45-163">True</span></span>                                           |
| <span data-ttu-id="75f45-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="75f45-164">Is Indexed</span></span>             | <span data-ttu-id="75f45-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-165">False</span></span>                                          |
| <span data-ttu-id="75f45-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="75f45-166">In Global Catalog</span></span>      | <span data-ttu-id="75f45-167">True</span><span class="sxs-lookup"><span data-stu-id="75f45-167">True</span></span>                                           |
| <span data-ttu-id="75f45-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="75f45-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="75f45-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75f45-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="75f45-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75f45-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="75f45-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75f45-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="75f45-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-172">Search-Flags</span></span>           | <span data-ttu-id="75f45-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75f45-173">0x00000000</span></span>                                     |
| <span data-ttu-id="75f45-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-174">System-Flags</span></span>           | <span data-ttu-id="75f45-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75f45-175">0x00000010</span></span>                                     |
| <span data-ttu-id="75f45-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="75f45-176">Classes used in</span></span>        | [<span data-ttu-id="75f45-177">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="75f45-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="75f45-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="75f45-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="75f45-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-179">Entry</span></span> | <span data-ttu-id="75f45-180">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="75f45-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="75f45-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="75f45-183">System-Only</span></span>            | <span data-ttu-id="75f45-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-184">False</span></span>                                          |
| <span data-ttu-id="75f45-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="75f45-185">Is-Single-Valued</span></span>       | <span data-ttu-id="75f45-186">True</span><span class="sxs-lookup"><span data-stu-id="75f45-186">True</span></span>                                           |
| <span data-ttu-id="75f45-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="75f45-187">Is Indexed</span></span>             | <span data-ttu-id="75f45-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-188">False</span></span>                                          |
| <span data-ttu-id="75f45-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="75f45-189">In Global Catalog</span></span>      | <span data-ttu-id="75f45-190">True</span><span class="sxs-lookup"><span data-stu-id="75f45-190">True</span></span>                                           |
| <span data-ttu-id="75f45-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="75f45-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="75f45-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75f45-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="75f45-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75f45-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="75f45-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75f45-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="75f45-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-195">Search-Flags</span></span>           | <span data-ttu-id="75f45-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75f45-196">0x00000000</span></span>                                     |
| <span data-ttu-id="75f45-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-197">System-Flags</span></span>           | <span data-ttu-id="75f45-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75f45-198">0x00000010</span></span>                                     |
| <span data-ttu-id="75f45-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="75f45-199">Classes used in</span></span>        | [<span data-ttu-id="75f45-200">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="75f45-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="75f45-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75f45-201">Windows Server 2008</span></span>



| <span data-ttu-id="75f45-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-202">Entry</span></span> | <span data-ttu-id="75f45-203">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="75f45-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="75f45-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="75f45-206">System-Only</span></span>            | <span data-ttu-id="75f45-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-207">False</span></span>                                          |
| <span data-ttu-id="75f45-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="75f45-208">Is-Single-Valued</span></span>       | <span data-ttu-id="75f45-209">True</span><span class="sxs-lookup"><span data-stu-id="75f45-209">True</span></span>                                           |
| <span data-ttu-id="75f45-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="75f45-210">Is Indexed</span></span>             | <span data-ttu-id="75f45-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-211">False</span></span>                                          |
| <span data-ttu-id="75f45-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="75f45-212">In Global Catalog</span></span>      | <span data-ttu-id="75f45-213">True</span><span class="sxs-lookup"><span data-stu-id="75f45-213">True</span></span>                                           |
| <span data-ttu-id="75f45-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="75f45-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="75f45-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75f45-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="75f45-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75f45-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="75f45-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75f45-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="75f45-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-218">Search-Flags</span></span>           | <span data-ttu-id="75f45-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75f45-219">0x00000000</span></span>                                     |
| <span data-ttu-id="75f45-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-220">System-Flags</span></span>           | <span data-ttu-id="75f45-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75f45-221">0x00000010</span></span>                                     |
| <span data-ttu-id="75f45-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="75f45-222">Classes used in</span></span>        | [<span data-ttu-id="75f45-223">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="75f45-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="75f45-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="75f45-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="75f45-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-225">Entry</span></span> | <span data-ttu-id="75f45-226">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="75f45-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="75f45-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="75f45-229">System-Only</span></span>            | <span data-ttu-id="75f45-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-230">False</span></span>                                          |
| <span data-ttu-id="75f45-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="75f45-231">Is-Single-Valued</span></span>       | <span data-ttu-id="75f45-232">True</span><span class="sxs-lookup"><span data-stu-id="75f45-232">True</span></span>                                           |
| <span data-ttu-id="75f45-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="75f45-233">Is Indexed</span></span>             | <span data-ttu-id="75f45-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-234">False</span></span>                                          |
| <span data-ttu-id="75f45-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="75f45-235">In Global Catalog</span></span>      | <span data-ttu-id="75f45-236">True</span><span class="sxs-lookup"><span data-stu-id="75f45-236">True</span></span>                                           |
| <span data-ttu-id="75f45-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="75f45-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="75f45-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75f45-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="75f45-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75f45-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="75f45-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75f45-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="75f45-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-241">Search-Flags</span></span>           | <span data-ttu-id="75f45-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75f45-242">0x00000000</span></span>                                     |
| <span data-ttu-id="75f45-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-243">System-Flags</span></span>           | <span data-ttu-id="75f45-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75f45-244">0x00000010</span></span>                                     |
| <span data-ttu-id="75f45-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="75f45-245">Classes used in</span></span>        | [<span data-ttu-id="75f45-246">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="75f45-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="75f45-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75f45-247">Windows Server 2012</span></span>



| <span data-ttu-id="75f45-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="75f45-248">Entry</span></span> | <span data-ttu-id="75f45-249">Значение</span><span class="sxs-lookup"><span data-stu-id="75f45-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="75f45-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="75f45-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="75f45-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="75f45-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="75f45-252">System-Only</span></span>            | <span data-ttu-id="75f45-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-253">False</span></span>                                          |
| <span data-ttu-id="75f45-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="75f45-254">Is-Single-Valued</span></span>       | <span data-ttu-id="75f45-255">True</span><span class="sxs-lookup"><span data-stu-id="75f45-255">True</span></span>                                           |
| <span data-ttu-id="75f45-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="75f45-256">Is Indexed</span></span>             | <span data-ttu-id="75f45-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="75f45-257">False</span></span>                                          |
| <span data-ttu-id="75f45-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="75f45-258">In Global Catalog</span></span>      | <span data-ttu-id="75f45-259">True</span><span class="sxs-lookup"><span data-stu-id="75f45-259">True</span></span>                                           |
| <span data-ttu-id="75f45-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="75f45-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="75f45-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="75f45-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="75f45-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="75f45-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="75f45-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="75f45-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="75f45-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-264">Search-Flags</span></span>           | <span data-ttu-id="75f45-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="75f45-265">0x00000000</span></span>                                     |
| <span data-ttu-id="75f45-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="75f45-266">System-Flags</span></span>           | <span data-ttu-id="75f45-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="75f45-267">0x00000010</span></span>                                     |
| <span data-ttu-id="75f45-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="75f45-268">Classes used in</span></span>        | [<span data-ttu-id="75f45-269">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="75f45-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





