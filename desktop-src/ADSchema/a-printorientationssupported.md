---
title: Print — ориентация — поддерживаемый атрибут
description: Поворот страницы для альбомной печати.
ms.assetid: a3e910f1-452e-4b85-8ede-50b7274475a0
ms.tgt_platform: multiple
keywords:
- Ориентация на печать — схема Active Directory, поддерживаемая атрибутом
- Схема AD атрибута Принториентатионссуппортед
topic_type:
- apiref
api_name:
- Print-Orientations-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49888caa713de7dd12616dcb9932e52b15b2a454
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655081"
---
# <a name="print-orientations-supported-attribute"></a><span data-ttu-id="231f7-105">Print — ориентация — поддерживаемый атрибут</span><span class="sxs-lookup"><span data-stu-id="231f7-105">Print-Orientations-Supported attribute</span></span>

<span data-ttu-id="231f7-106">Поворот страницы для альбомной печати.</span><span class="sxs-lookup"><span data-stu-id="231f7-106">The page rotation for landscape printing.</span></span>



| <span data-ttu-id="231f7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-107">Entry</span></span> | <span data-ttu-id="231f7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-108">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="231f7-109">CN</span><span class="sxs-lookup"><span data-stu-id="231f7-109">CN</span></span>                | <span data-ttu-id="231f7-110">Ориентация на печать — поддерживается</span><span class="sxs-lookup"><span data-stu-id="231f7-110">Print-Orientations-Supported</span></span>                                |
| <span data-ttu-id="231f7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="231f7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="231f7-112">принториентатионссуппортед</span><span class="sxs-lookup"><span data-stu-id="231f7-112">printOrientationsSupported</span></span>                                  |
| <span data-ttu-id="231f7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="231f7-113">Size</span></span>              | <span data-ttu-id="231f7-114">4 байта.</span><span class="sxs-lookup"><span data-stu-id="231f7-114">4 bytes.</span></span> <span data-ttu-id="231f7-115">Возможные значения: 0, 90, 270 и 0 = нет альбомной ориентации.</span><span class="sxs-lookup"><span data-stu-id="231f7-115">Possible values: 0, 90, 270, and 0 = no landscape.</span></span> |
| <span data-ttu-id="231f7-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="231f7-116">Update Privilege</span></span>  | \-                                                          |
| <span data-ttu-id="231f7-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="231f7-117">Update Frequency</span></span>  | \-                                                          |
| <span data-ttu-id="231f7-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-118">Attribute-Id</span></span>      | <span data-ttu-id="231f7-119">1.2.840.113556.1.4.240</span><span class="sxs-lookup"><span data-stu-id="231f7-119">1.2.840.113556.1.4.240</span></span>                                      |
| <span data-ttu-id="231f7-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="231f7-120">System-Id-Guid</span></span>    | <span data-ttu-id="231f7-121">281416d0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="231f7-121">281416d0-1968-11d0-a28f-00aa003049e2</span></span>                        |
| <span data-ttu-id="231f7-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="231f7-122">Syntax</span></span>            | [<span data-ttu-id="231f7-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="231f7-123">**String(Unicode)**</span></span>](s-string-unicode.md)                 |



## <a name="implementations"></a><span data-ttu-id="231f7-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="231f7-124">Implementations</span></span>

-   [<span data-ttu-id="231f7-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="231f7-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="231f7-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="231f7-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="231f7-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="231f7-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="231f7-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="231f7-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="231f7-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="231f7-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="231f7-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="231f7-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="231f7-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="231f7-131">Windows 2000 Server</span></span>



| <span data-ttu-id="231f7-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-132">Entry</span></span> | <span data-ttu-id="231f7-133">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="231f7-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="231f7-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="231f7-136">System-Only</span></span>            | <span data-ttu-id="231f7-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-137">False</span></span>                                          |
| <span data-ttu-id="231f7-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="231f7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="231f7-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-139">False</span></span>                                          |
| <span data-ttu-id="231f7-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="231f7-140">Is Indexed</span></span>             | <span data-ttu-id="231f7-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-141">False</span></span>                                          |
| <span data-ttu-id="231f7-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="231f7-142">In Global Catalog</span></span>      | <span data-ttu-id="231f7-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-143">False</span></span>                                          |
| <span data-ttu-id="231f7-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="231f7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="231f7-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="231f7-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="231f7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="231f7-146">Range-Lower</span></span>            | <span data-ttu-id="231f7-147">1</span><span class="sxs-lookup"><span data-stu-id="231f7-147">1</span></span>                                              |
| <span data-ttu-id="231f7-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="231f7-148">Range-Upper</span></span>            | <span data-ttu-id="231f7-149">256</span><span class="sxs-lookup"><span data-stu-id="231f7-149">256</span></span>                                            |
| <span data-ttu-id="231f7-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-150">Search-Flags</span></span>           | <span data-ttu-id="231f7-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="231f7-151">0x00000000</span></span>                                     |
| <span data-ttu-id="231f7-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-152">System-Flags</span></span>           | <span data-ttu-id="231f7-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="231f7-153">0x00000010</span></span>                                     |
| <span data-ttu-id="231f7-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="231f7-154">Classes used in</span></span>        | [<span data-ttu-id="231f7-155">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="231f7-155">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="231f7-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="231f7-156">Windows Server 2003</span></span>



| <span data-ttu-id="231f7-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-157">Entry</span></span> | <span data-ttu-id="231f7-158">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-158">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="231f7-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="231f7-159">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-160">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="231f7-161">System-Only</span></span>            | <span data-ttu-id="231f7-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-162">False</span></span>                                          |
| <span data-ttu-id="231f7-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="231f7-163">Is-Single-Valued</span></span>       | <span data-ttu-id="231f7-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-164">False</span></span>                                          |
| <span data-ttu-id="231f7-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="231f7-165">Is Indexed</span></span>             | <span data-ttu-id="231f7-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-166">False</span></span>                                          |
| <span data-ttu-id="231f7-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="231f7-167">In Global Catalog</span></span>      | <span data-ttu-id="231f7-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-168">False</span></span>                                          |
| <span data-ttu-id="231f7-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="231f7-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="231f7-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="231f7-170">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="231f7-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="231f7-171">Range-Lower</span></span>            | <span data-ttu-id="231f7-172">1</span><span class="sxs-lookup"><span data-stu-id="231f7-172">1</span></span>                                              |
| <span data-ttu-id="231f7-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="231f7-173">Range-Upper</span></span>            | <span data-ttu-id="231f7-174">256</span><span class="sxs-lookup"><span data-stu-id="231f7-174">256</span></span>                                            |
| <span data-ttu-id="231f7-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-175">Search-Flags</span></span>           | <span data-ttu-id="231f7-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="231f7-176">0x00000000</span></span>                                     |
| <span data-ttu-id="231f7-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-177">System-Flags</span></span>           | <span data-ttu-id="231f7-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="231f7-178">0x00000010</span></span>                                     |
| <span data-ttu-id="231f7-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="231f7-179">Classes used in</span></span>        | [<span data-ttu-id="231f7-180">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="231f7-180">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="231f7-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="231f7-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="231f7-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-182">Entry</span></span> | <span data-ttu-id="231f7-183">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-183">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="231f7-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="231f7-184">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-185">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="231f7-186">System-Only</span></span>            | <span data-ttu-id="231f7-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-187">False</span></span>                                          |
| <span data-ttu-id="231f7-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="231f7-188">Is-Single-Valued</span></span>       | <span data-ttu-id="231f7-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-189">False</span></span>                                          |
| <span data-ttu-id="231f7-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="231f7-190">Is Indexed</span></span>             | <span data-ttu-id="231f7-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-191">False</span></span>                                          |
| <span data-ttu-id="231f7-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="231f7-192">In Global Catalog</span></span>      | <span data-ttu-id="231f7-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-193">False</span></span>                                          |
| <span data-ttu-id="231f7-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="231f7-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="231f7-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="231f7-195">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="231f7-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="231f7-196">Range-Lower</span></span>            | <span data-ttu-id="231f7-197">1</span><span class="sxs-lookup"><span data-stu-id="231f7-197">1</span></span>                                              |
| <span data-ttu-id="231f7-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="231f7-198">Range-Upper</span></span>            | <span data-ttu-id="231f7-199">256</span><span class="sxs-lookup"><span data-stu-id="231f7-199">256</span></span>                                            |
| <span data-ttu-id="231f7-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-200">Search-Flags</span></span>           | <span data-ttu-id="231f7-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="231f7-201">0x00000000</span></span>                                     |
| <span data-ttu-id="231f7-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-202">System-Flags</span></span>           | <span data-ttu-id="231f7-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="231f7-203">0x00000010</span></span>                                     |
| <span data-ttu-id="231f7-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="231f7-204">Classes used in</span></span>        | [<span data-ttu-id="231f7-205">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="231f7-205">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="231f7-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="231f7-206">Windows Server 2008</span></span>



| <span data-ttu-id="231f7-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-207">Entry</span></span> | <span data-ttu-id="231f7-208">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-208">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="231f7-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="231f7-209">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-210">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="231f7-211">System-Only</span></span>            | <span data-ttu-id="231f7-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-212">False</span></span>                                          |
| <span data-ttu-id="231f7-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="231f7-213">Is-Single-Valued</span></span>       | <span data-ttu-id="231f7-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-214">False</span></span>                                          |
| <span data-ttu-id="231f7-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="231f7-215">Is Indexed</span></span>             | <span data-ttu-id="231f7-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-216">False</span></span>                                          |
| <span data-ttu-id="231f7-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="231f7-217">In Global Catalog</span></span>      | <span data-ttu-id="231f7-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-218">False</span></span>                                          |
| <span data-ttu-id="231f7-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="231f7-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="231f7-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="231f7-220">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="231f7-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="231f7-221">Range-Lower</span></span>            | <span data-ttu-id="231f7-222">1</span><span class="sxs-lookup"><span data-stu-id="231f7-222">1</span></span>                                              |
| <span data-ttu-id="231f7-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="231f7-223">Range-Upper</span></span>            | <span data-ttu-id="231f7-224">256</span><span class="sxs-lookup"><span data-stu-id="231f7-224">256</span></span>                                            |
| <span data-ttu-id="231f7-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-225">Search-Flags</span></span>           | <span data-ttu-id="231f7-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="231f7-226">0x00000000</span></span>                                     |
| <span data-ttu-id="231f7-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-227">System-Flags</span></span>           | <span data-ttu-id="231f7-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="231f7-228">0x00000010</span></span>                                     |
| <span data-ttu-id="231f7-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="231f7-229">Classes used in</span></span>        | [<span data-ttu-id="231f7-230">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="231f7-230">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="231f7-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="231f7-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="231f7-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-232">Entry</span></span> | <span data-ttu-id="231f7-233">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-233">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="231f7-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="231f7-234">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-235">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="231f7-236">System-Only</span></span>            | <span data-ttu-id="231f7-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-237">False</span></span>                                          |
| <span data-ttu-id="231f7-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="231f7-238">Is-Single-Valued</span></span>       | <span data-ttu-id="231f7-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-239">False</span></span>                                          |
| <span data-ttu-id="231f7-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="231f7-240">Is Indexed</span></span>             | <span data-ttu-id="231f7-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-241">False</span></span>                                          |
| <span data-ttu-id="231f7-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="231f7-242">In Global Catalog</span></span>      | <span data-ttu-id="231f7-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-243">False</span></span>                                          |
| <span data-ttu-id="231f7-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="231f7-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="231f7-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="231f7-245">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="231f7-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="231f7-246">Range-Lower</span></span>            | <span data-ttu-id="231f7-247">1</span><span class="sxs-lookup"><span data-stu-id="231f7-247">1</span></span>                                              |
| <span data-ttu-id="231f7-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="231f7-248">Range-Upper</span></span>            | <span data-ttu-id="231f7-249">256</span><span class="sxs-lookup"><span data-stu-id="231f7-249">256</span></span>                                            |
| <span data-ttu-id="231f7-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-250">Search-Flags</span></span>           | <span data-ttu-id="231f7-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="231f7-251">0x00000000</span></span>                                     |
| <span data-ttu-id="231f7-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-252">System-Flags</span></span>           | <span data-ttu-id="231f7-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="231f7-253">0x00000010</span></span>                                     |
| <span data-ttu-id="231f7-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="231f7-254">Classes used in</span></span>        | [<span data-ttu-id="231f7-255">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="231f7-255">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="231f7-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="231f7-256">Windows Server 2012</span></span>



| <span data-ttu-id="231f7-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="231f7-257">Entry</span></span> | <span data-ttu-id="231f7-258">Значение</span><span class="sxs-lookup"><span data-stu-id="231f7-258">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="231f7-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="231f7-259">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="231f7-260">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="231f7-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="231f7-261">System-Only</span></span>            | <span data-ttu-id="231f7-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-262">False</span></span>                                          |
| <span data-ttu-id="231f7-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="231f7-263">Is-Single-Valued</span></span>       | <span data-ttu-id="231f7-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-264">False</span></span>                                          |
| <span data-ttu-id="231f7-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="231f7-265">Is Indexed</span></span>             | <span data-ttu-id="231f7-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-266">False</span></span>                                          |
| <span data-ttu-id="231f7-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="231f7-267">In Global Catalog</span></span>      | <span data-ttu-id="231f7-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="231f7-268">False</span></span>                                          |
| <span data-ttu-id="231f7-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="231f7-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="231f7-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="231f7-270">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="231f7-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="231f7-271">Range-Lower</span></span>            | <span data-ttu-id="231f7-272">1</span><span class="sxs-lookup"><span data-stu-id="231f7-272">1</span></span>                                              |
| <span data-ttu-id="231f7-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="231f7-273">Range-Upper</span></span>            | <span data-ttu-id="231f7-274">256</span><span class="sxs-lookup"><span data-stu-id="231f7-274">256</span></span>                                            |
| <span data-ttu-id="231f7-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-275">Search-Flags</span></span>           | <span data-ttu-id="231f7-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="231f7-276">0x00000000</span></span>                                     |
| <span data-ttu-id="231f7-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="231f7-277">System-Flags</span></span>           | <span data-ttu-id="231f7-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="231f7-278">0x00000010</span></span>                                     |
| <span data-ttu-id="231f7-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="231f7-279">Classes used in</span></span>        | [<span data-ttu-id="231f7-280">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="231f7-280">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





