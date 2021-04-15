---
title: Атрибут "является критически важным" — "системный объект"
description: Если значение — TRUE, то объект, на котором размещен этот атрибут, должен быть реплицирован во время установки новой реплики.
ms.assetid: 736c8b25-0f82-4b3c-a4fc-4643cd71474e
ms.tgt_platform: multiple
keywords:
- Является критически важным — схема AD атрибута системного объекта
- Схема AD атрибута Искритикалсистемобжект
topic_type:
- apiref
api_name:
- Is-Critical-System-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6030da908fe96a4bea5267872e8bae928a6555e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493509"
---
# <a name="is-critical-system-object-attribute"></a><span data-ttu-id="63da4-105">Атрибут "является критически важным" — "системный объект"</span><span class="sxs-lookup"><span data-stu-id="63da4-105">Is-Critical-System-Object attribute</span></span>

<span data-ttu-id="63da4-106">Если **значение — true**, то объект, на котором размещен этот атрибут, должен быть реплицирован во время установки новой реплики.</span><span class="sxs-lookup"><span data-stu-id="63da4-106">If **TRUE**, the object hosting this attribute must be replicated during installation of a new replica.</span></span>



| <span data-ttu-id="63da4-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-107">Entry</span></span> | <span data-ttu-id="63da4-108">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="63da4-109">CN</span><span class="sxs-lookup"><span data-stu-id="63da4-109">CN</span></span>                | <span data-ttu-id="63da4-110">Является критически важным — системный объект</span><span class="sxs-lookup"><span data-stu-id="63da4-110">Is-Critical-System-Object</span></span>            |
| <span data-ttu-id="63da4-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="63da4-111">Ldap-Display-Name</span></span> | <span data-ttu-id="63da4-112">искритикалсистемобжект</span><span class="sxs-lookup"><span data-stu-id="63da4-112">isCriticalSystemObject</span></span>               |
| <span data-ttu-id="63da4-113">Размер</span><span class="sxs-lookup"><span data-stu-id="63da4-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="63da4-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="63da4-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="63da4-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="63da4-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="63da4-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-116">Attribute-Id</span></span>      | <span data-ttu-id="63da4-117">1.2.840.113556.1.4.868</span><span class="sxs-lookup"><span data-stu-id="63da4-117">1.2.840.113556.1.4.868</span></span>               |
| <span data-ttu-id="63da4-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="63da4-118">System-Id-Guid</span></span>    | <span data-ttu-id="63da4-119">00fbf30d-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="63da4-119">00fbf30d-91fe-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="63da4-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63da4-120">Syntax</span></span>            | [<span data-ttu-id="63da4-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="63da4-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="63da4-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="63da4-122">Implementations</span></span>

-   [<span data-ttu-id="63da4-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="63da4-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="63da4-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="63da4-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="63da4-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="63da4-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="63da4-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="63da4-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="63da4-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="63da4-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="63da4-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="63da4-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="63da4-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="63da4-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="63da4-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="63da4-130">Windows 2000 Server</span></span>



| <span data-ttu-id="63da4-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-131">Entry</span></span> | <span data-ttu-id="63da4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-135">System-Only</span></span>            | <span data-ttu-id="63da4-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-136">False</span></span>                           |
| <span data-ttu-id="63da4-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-137">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-138">True</span><span class="sxs-lookup"><span data-stu-id="63da4-138">True</span></span>                            |
| <span data-ttu-id="63da4-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-139">Is Indexed</span></span>             | <span data-ttu-id="63da4-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-140">False</span></span>                           |
| <span data-ttu-id="63da4-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-141">In Global Catalog</span></span>      | <span data-ttu-id="63da4-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-142">False</span></span>                           |
| <span data-ttu-id="63da4-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-147">Search-Flags</span></span>           | <span data-ttu-id="63da4-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-148">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-149">System-Flags</span></span>           | <span data-ttu-id="63da4-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-150">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-151">Classes used in</span></span>        | [<span data-ttu-id="63da4-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="63da4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="63da4-153">Windows Server 2003</span></span>



| <span data-ttu-id="63da4-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-154">Entry</span></span> | <span data-ttu-id="63da4-155">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-158">System-Only</span></span>            | <span data-ttu-id="63da4-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-159">False</span></span>                           |
| <span data-ttu-id="63da4-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-160">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-161">True</span><span class="sxs-lookup"><span data-stu-id="63da4-161">True</span></span>                            |
| <span data-ttu-id="63da4-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-162">Is Indexed</span></span>             | <span data-ttu-id="63da4-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-163">False</span></span>                           |
| <span data-ttu-id="63da4-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-164">In Global Catalog</span></span>      | <span data-ttu-id="63da4-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-165">False</span></span>                           |
| <span data-ttu-id="63da4-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-170">Search-Flags</span></span>           | <span data-ttu-id="63da4-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-171">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-172">System-Flags</span></span>           | <span data-ttu-id="63da4-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-173">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-174">Classes used in</span></span>        | [<span data-ttu-id="63da4-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="63da4-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="63da4-176">ADAM</span></span>



| <span data-ttu-id="63da4-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-177">Entry</span></span> | <span data-ttu-id="63da4-178">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-181">System-Only</span></span>            | <span data-ttu-id="63da4-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-182">False</span></span>                           |
| <span data-ttu-id="63da4-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-183">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-184">True</span><span class="sxs-lookup"><span data-stu-id="63da4-184">True</span></span>                            |
| <span data-ttu-id="63da4-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-185">Is Indexed</span></span>             | <span data-ttu-id="63da4-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-186">False</span></span>                           |
| <span data-ttu-id="63da4-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-187">In Global Catalog</span></span>      | <span data-ttu-id="63da4-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-188">False</span></span>                           |
| <span data-ttu-id="63da4-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-193">Search-Flags</span></span>           | <span data-ttu-id="63da4-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-194">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-195">System-Flags</span></span>           | <span data-ttu-id="63da4-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-196">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-197">Classes used in</span></span>        | [<span data-ttu-id="63da4-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="63da4-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="63da4-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="63da4-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-200">Entry</span></span> | <span data-ttu-id="63da4-201">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-204">System-Only</span></span>            | <span data-ttu-id="63da4-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-205">False</span></span>                           |
| <span data-ttu-id="63da4-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-206">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-207">True</span><span class="sxs-lookup"><span data-stu-id="63da4-207">True</span></span>                            |
| <span data-ttu-id="63da4-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-208">Is Indexed</span></span>             | <span data-ttu-id="63da4-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-209">False</span></span>                           |
| <span data-ttu-id="63da4-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-210">In Global Catalog</span></span>      | <span data-ttu-id="63da4-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-211">False</span></span>                           |
| <span data-ttu-id="63da4-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-216">Search-Flags</span></span>           | <span data-ttu-id="63da4-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-217">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-218">System-Flags</span></span>           | <span data-ttu-id="63da4-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-219">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-220">Classes used in</span></span>        | [<span data-ttu-id="63da4-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="63da4-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63da4-222">Windows Server 2008</span></span>



| <span data-ttu-id="63da4-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-223">Entry</span></span> | <span data-ttu-id="63da4-224">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-227">System-Only</span></span>            | <span data-ttu-id="63da4-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-228">False</span></span>                           |
| <span data-ttu-id="63da4-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-229">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-230">True</span><span class="sxs-lookup"><span data-stu-id="63da4-230">True</span></span>                            |
| <span data-ttu-id="63da4-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-231">Is Indexed</span></span>             | <span data-ttu-id="63da4-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-232">False</span></span>                           |
| <span data-ttu-id="63da4-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-233">In Global Catalog</span></span>      | <span data-ttu-id="63da4-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-234">False</span></span>                           |
| <span data-ttu-id="63da4-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-239">Search-Flags</span></span>           | <span data-ttu-id="63da4-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-240">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-241">System-Flags</span></span>           | <span data-ttu-id="63da4-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-242">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-243">Classes used in</span></span>        | [<span data-ttu-id="63da4-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="63da4-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="63da4-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="63da4-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-246">Entry</span></span> | <span data-ttu-id="63da4-247">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-250">System-Only</span></span>            | <span data-ttu-id="63da4-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-251">False</span></span>                           |
| <span data-ttu-id="63da4-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-252">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-253">True</span><span class="sxs-lookup"><span data-stu-id="63da4-253">True</span></span>                            |
| <span data-ttu-id="63da4-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-254">Is Indexed</span></span>             | <span data-ttu-id="63da4-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-255">False</span></span>                           |
| <span data-ttu-id="63da4-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-256">In Global Catalog</span></span>      | <span data-ttu-id="63da4-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-257">False</span></span>                           |
| <span data-ttu-id="63da4-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-262">Search-Flags</span></span>           | <span data-ttu-id="63da4-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-263">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-264">System-Flags</span></span>           | <span data-ttu-id="63da4-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-265">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-266">Classes used in</span></span>        | [<span data-ttu-id="63da4-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="63da4-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63da4-268">Windows Server 2012</span></span>



| <span data-ttu-id="63da4-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="63da4-269">Entry</span></span> | <span data-ttu-id="63da4-270">Значение</span><span class="sxs-lookup"><span data-stu-id="63da4-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="63da4-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="63da4-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="63da4-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="63da4-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="63da4-273">System-Only</span></span>            | <span data-ttu-id="63da4-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-274">False</span></span>                           |
| <span data-ttu-id="63da4-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="63da4-275">Is-Single-Valued</span></span>       | <span data-ttu-id="63da4-276">True</span><span class="sxs-lookup"><span data-stu-id="63da4-276">True</span></span>                            |
| <span data-ttu-id="63da4-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="63da4-277">Is Indexed</span></span>             | <span data-ttu-id="63da4-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-278">False</span></span>                           |
| <span data-ttu-id="63da4-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="63da4-279">In Global Catalog</span></span>      | <span data-ttu-id="63da4-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="63da4-280">False</span></span>                           |
| <span data-ttu-id="63da4-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="63da4-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="63da4-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="63da4-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="63da4-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="63da4-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="63da4-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="63da4-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="63da4-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-285">Search-Flags</span></span>           | <span data-ttu-id="63da4-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="63da4-286">0x00000000</span></span>                      |
| <span data-ttu-id="63da4-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="63da4-287">System-Flags</span></span>           | <span data-ttu-id="63da4-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="63da4-288">0x00000010</span></span>                      |
| <span data-ttu-id="63da4-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="63da4-289">Classes used in</span></span>        | [<span data-ttu-id="63da4-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="63da4-290">**Top**</span></span>](c-top.md)<br/> |



 

 





