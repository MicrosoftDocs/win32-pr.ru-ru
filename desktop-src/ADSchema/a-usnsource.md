---
title: Атрибут USN-Source
description: Значение атрибута USN-Changed объекта из удаленного каталога, который реплицирует изменение на локальный сервер.
ms.assetid: b307f84a-3ab1-4bfa-afc2-e74055f2a652
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута USN-Source
- Схема AD атрибута Уснсаурце
topic_type:
- apiref
api_name:
- USN-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0998ffb73fc02511d77440550c8c669b35a98563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416237"
---
# <a name="usn-source-attribute"></a><span data-ttu-id="1abab-105">Атрибут USN-Source</span><span class="sxs-lookup"><span data-stu-id="1abab-105">USN-Source attribute</span></span>

<span data-ttu-id="1abab-106">Значение атрибута [**USN-Changed**](a-usnchanged.md) объекта из удаленного каталога, который реплицирует изменение на локальный сервер.</span><span class="sxs-lookup"><span data-stu-id="1abab-106">Value of the [**USN-Changed**](a-usnchanged.md) attribute of the object from the remote directory that replicated the change to the local server.</span></span>



| <span data-ttu-id="1abab-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-107">Entry</span></span> | <span data-ttu-id="1abab-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-108">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1abab-109">CN</span><span class="sxs-lookup"><span data-stu-id="1abab-109">CN</span></span>                | <span data-ttu-id="1abab-110">USN-Source</span><span class="sxs-lookup"><span data-stu-id="1abab-110">USN-Source</span></span>                                                                                          |
| <span data-ttu-id="1abab-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1abab-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1abab-112">уснсаурце</span><span class="sxs-lookup"><span data-stu-id="1abab-112">uSNSource</span></span>                                                                                           |
| <span data-ttu-id="1abab-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1abab-113">Size</span></span>              | <span data-ttu-id="1abab-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="1abab-114">8 bytes</span></span>                                                                                             |
| <span data-ttu-id="1abab-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1abab-115">Update Privilege</span></span>  | <span data-ttu-id="1abab-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="1abab-116">This value is set by the system.</span></span>                                                                    |
| <span data-ttu-id="1abab-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1abab-117">Update Frequency</span></span>  | <span data-ttu-id="1abab-118">При изменении объекта в удаленном каталоге, который реплицирует изменения в локальный каталог.</span><span class="sxs-lookup"><span data-stu-id="1abab-118">When the object is changed on a remote directory that replicated the change to the local directory.</span></span> |
| <span data-ttu-id="1abab-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-119">Attribute-Id</span></span>      | <span data-ttu-id="1abab-120">1.2.840.113556.1.4.896</span><span class="sxs-lookup"><span data-stu-id="1abab-120">1.2.840.113556.1.4.896</span></span>                                                                              |
| <span data-ttu-id="1abab-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1abab-121">System-Id-Guid</span></span>    | <span data-ttu-id="1abab-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1abab-122">167758ad-47f3-11d1-a9c3-0000f80367c1</span></span>                                                                |
| <span data-ttu-id="1abab-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1abab-123">Syntax</span></span>            | [<span data-ttu-id="1abab-124">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="1abab-124">**Interval**</span></span>](s-interval.md)                                                                      |



## <a name="implementations"></a><span data-ttu-id="1abab-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1abab-125">Implementations</span></span>

-   [<span data-ttu-id="1abab-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1abab-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1abab-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1abab-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1abab-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1abab-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1abab-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1abab-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1abab-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1abab-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1abab-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1abab-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1abab-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1abab-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1abab-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1abab-133">Windows 2000 Server</span></span>



| <span data-ttu-id="1abab-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-134">Entry</span></span> | <span data-ttu-id="1abab-135">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-135">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-136">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-137">MAPI-Id</span></span>                | <span data-ttu-id="1abab-138">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-138">0x8157</span></span>                          |
| <span data-ttu-id="1abab-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-139">System-Only</span></span>            | <span data-ttu-id="1abab-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-140">False</span></span>                           |
| <span data-ttu-id="1abab-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-142">True</span><span class="sxs-lookup"><span data-stu-id="1abab-142">True</span></span>                            |
| <span data-ttu-id="1abab-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-143">Is Indexed</span></span>             | <span data-ttu-id="1abab-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-144">False</span></span>                           |
| <span data-ttu-id="1abab-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-145">In Global Catalog</span></span>      | <span data-ttu-id="1abab-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-146">False</span></span>                           |
| <span data-ttu-id="1abab-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-148">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-149">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-150">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-151">Search-Flags</span></span>           | <span data-ttu-id="1abab-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-152">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-153">System-Flags</span></span>           | <span data-ttu-id="1abab-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-154">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-155">Classes used in</span></span>        | [<span data-ttu-id="1abab-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1abab-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1abab-157">Windows Server 2003</span></span>



| <span data-ttu-id="1abab-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-158">Entry</span></span> | <span data-ttu-id="1abab-159">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-161">MAPI-Id</span></span>                | <span data-ttu-id="1abab-162">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-162">0x8157</span></span>                          |
| <span data-ttu-id="1abab-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-163">System-Only</span></span>            | <span data-ttu-id="1abab-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-164">False</span></span>                           |
| <span data-ttu-id="1abab-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-165">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-166">True</span><span class="sxs-lookup"><span data-stu-id="1abab-166">True</span></span>                            |
| <span data-ttu-id="1abab-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-167">Is Indexed</span></span>             | <span data-ttu-id="1abab-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-168">False</span></span>                           |
| <span data-ttu-id="1abab-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-169">In Global Catalog</span></span>      | <span data-ttu-id="1abab-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-170">False</span></span>                           |
| <span data-ttu-id="1abab-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-173">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-174">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-175">Search-Flags</span></span>           | <span data-ttu-id="1abab-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-176">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-177">System-Flags</span></span>           | <span data-ttu-id="1abab-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-178">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-179">Classes used in</span></span>        | [<span data-ttu-id="1abab-180">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-180">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1abab-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="1abab-181">ADAM</span></span>



| <span data-ttu-id="1abab-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-182">Entry</span></span> | <span data-ttu-id="1abab-183">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-183">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-184">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-185">MAPI-Id</span></span>                | <span data-ttu-id="1abab-186">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-186">0x8157</span></span>                          |
| <span data-ttu-id="1abab-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-187">System-Only</span></span>            | <span data-ttu-id="1abab-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-188">False</span></span>                           |
| <span data-ttu-id="1abab-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-190">True</span><span class="sxs-lookup"><span data-stu-id="1abab-190">True</span></span>                            |
| <span data-ttu-id="1abab-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-191">Is Indexed</span></span>             | <span data-ttu-id="1abab-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-192">False</span></span>                           |
| <span data-ttu-id="1abab-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-193">In Global Catalog</span></span>      | <span data-ttu-id="1abab-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-194">False</span></span>                           |
| <span data-ttu-id="1abab-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-196">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-197">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-198">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-199">Search-Flags</span></span>           | <span data-ttu-id="1abab-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-200">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-201">System-Flags</span></span>           | <span data-ttu-id="1abab-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-202">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-203">Classes used in</span></span>        | [<span data-ttu-id="1abab-204">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-204">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1abab-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1abab-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1abab-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-206">Entry</span></span> | <span data-ttu-id="1abab-207">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-207">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-208">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-209">MAPI-Id</span></span>                | <span data-ttu-id="1abab-210">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-210">0x8157</span></span>                          |
| <span data-ttu-id="1abab-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-211">System-Only</span></span>            | <span data-ttu-id="1abab-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-212">False</span></span>                           |
| <span data-ttu-id="1abab-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-213">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-214">True</span><span class="sxs-lookup"><span data-stu-id="1abab-214">True</span></span>                            |
| <span data-ttu-id="1abab-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-215">Is Indexed</span></span>             | <span data-ttu-id="1abab-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-216">False</span></span>                           |
| <span data-ttu-id="1abab-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-217">In Global Catalog</span></span>      | <span data-ttu-id="1abab-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-218">False</span></span>                           |
| <span data-ttu-id="1abab-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-220">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-221">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-222">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-223">Search-Flags</span></span>           | <span data-ttu-id="1abab-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-224">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-225">System-Flags</span></span>           | <span data-ttu-id="1abab-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-226">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-227">Classes used in</span></span>        | [<span data-ttu-id="1abab-228">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-228">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1abab-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1abab-229">Windows Server 2008</span></span>



| <span data-ttu-id="1abab-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-230">Entry</span></span> | <span data-ttu-id="1abab-231">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-231">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-232">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-233">MAPI-Id</span></span>                | <span data-ttu-id="1abab-234">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-234">0x8157</span></span>                          |
| <span data-ttu-id="1abab-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-235">System-Only</span></span>            | <span data-ttu-id="1abab-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-236">False</span></span>                           |
| <span data-ttu-id="1abab-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-237">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-238">True</span><span class="sxs-lookup"><span data-stu-id="1abab-238">True</span></span>                            |
| <span data-ttu-id="1abab-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-239">Is Indexed</span></span>             | <span data-ttu-id="1abab-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-240">False</span></span>                           |
| <span data-ttu-id="1abab-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-241">In Global Catalog</span></span>      | <span data-ttu-id="1abab-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-242">False</span></span>                           |
| <span data-ttu-id="1abab-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-244">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-245">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-246">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-247">Search-Flags</span></span>           | <span data-ttu-id="1abab-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-248">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-249">System-Flags</span></span>           | <span data-ttu-id="1abab-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-250">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-251">Classes used in</span></span>        | [<span data-ttu-id="1abab-252">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-252">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1abab-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1abab-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1abab-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-254">Entry</span></span> | <span data-ttu-id="1abab-255">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-255">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-256">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-257">MAPI-Id</span></span>                | <span data-ttu-id="1abab-258">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-258">0x8157</span></span>                          |
| <span data-ttu-id="1abab-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-259">System-Only</span></span>            | <span data-ttu-id="1abab-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-260">False</span></span>                           |
| <span data-ttu-id="1abab-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-261">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-262">True</span><span class="sxs-lookup"><span data-stu-id="1abab-262">True</span></span>                            |
| <span data-ttu-id="1abab-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-263">Is Indexed</span></span>             | <span data-ttu-id="1abab-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-264">False</span></span>                           |
| <span data-ttu-id="1abab-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-265">In Global Catalog</span></span>      | <span data-ttu-id="1abab-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-266">False</span></span>                           |
| <span data-ttu-id="1abab-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-268">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-269">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-270">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-271">Search-Flags</span></span>           | <span data-ttu-id="1abab-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-272">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-273">System-Flags</span></span>           | <span data-ttu-id="1abab-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-274">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-275">Classes used in</span></span>        | [<span data-ttu-id="1abab-276">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-276">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1abab-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1abab-277">Windows Server 2012</span></span>



| <span data-ttu-id="1abab-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="1abab-278">Entry</span></span> | <span data-ttu-id="1abab-279">Значение</span><span class="sxs-lookup"><span data-stu-id="1abab-279">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1abab-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1abab-280">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1abab-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1abab-281">MAPI-Id</span></span>                | <span data-ttu-id="1abab-282">0x8157</span><span class="sxs-lookup"><span data-stu-id="1abab-282">0x8157</span></span>                          |
| <span data-ttu-id="1abab-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="1abab-283">System-Only</span></span>            | <span data-ttu-id="1abab-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-284">False</span></span>                           |
| <span data-ttu-id="1abab-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1abab-285">Is-Single-Valued</span></span>       | <span data-ttu-id="1abab-286">True</span><span class="sxs-lookup"><span data-stu-id="1abab-286">True</span></span>                            |
| <span data-ttu-id="1abab-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1abab-287">Is Indexed</span></span>             | <span data-ttu-id="1abab-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-288">False</span></span>                           |
| <span data-ttu-id="1abab-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1abab-289">In Global Catalog</span></span>      | <span data-ttu-id="1abab-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="1abab-290">False</span></span>                           |
| <span data-ttu-id="1abab-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1abab-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="1abab-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1abab-292">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1abab-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1abab-293">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="1abab-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1abab-294">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="1abab-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-295">Search-Flags</span></span>           | <span data-ttu-id="1abab-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1abab-296">0x00000000</span></span>                      |
| <span data-ttu-id="1abab-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1abab-297">System-Flags</span></span>           | <span data-ttu-id="1abab-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1abab-298">0x00000010</span></span>                      |
| <span data-ttu-id="1abab-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1abab-299">Classes used in</span></span>        | [<span data-ttu-id="1abab-300">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="1abab-300">**Top**</span></span>](c-top.md)<br/> |



 

 





