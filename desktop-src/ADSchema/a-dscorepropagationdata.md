---
title: DS-Core-Propagate-атрибут данных
description: Атрибут DS-Core-Propagate-Data предназначен только для внутреннего использования.
ms.assetid: 6483890a-b1ef-4c8d-941d-8f25f722a305
ms.tgt_platform: multiple
keywords:
- DS-Core-распространение — схема AD атрибутов данных
- Схема AD атрибута Дскорепропагатиондата
topic_type:
- apiref
api_name:
- DS-Core-Propagation-Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324e3db3c71d11f47cb0a7afec875b9d129fa2d9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654958"
---
# <a name="ds-core-propagation-data-attribute"></a><span data-ttu-id="dedaa-105">DS-Core-Propagate-атрибут данных</span><span class="sxs-lookup"><span data-stu-id="dedaa-105">DS-Core-Propagation-Data attribute</span></span>

<span data-ttu-id="dedaa-106">Атрибут **DS-Core-Propagate-Data** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="dedaa-106">The **DS-Core-Propagation-Data** attribute is for internal use only.</span></span>



| <span data-ttu-id="dedaa-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-107">Entry</span></span> | <span data-ttu-id="dedaa-108">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-108">Value</span></span> |
|-------------------|---------------------------------------------------------------|
| <span data-ttu-id="dedaa-109">CN</span><span class="sxs-lookup"><span data-stu-id="dedaa-109">CN</span></span>                | <span data-ttu-id="dedaa-110">DS-Core-распространение-данные</span><span class="sxs-lookup"><span data-stu-id="dedaa-110">DS-Core-Propagation-Data</span></span>                                      |
| <span data-ttu-id="dedaa-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="dedaa-111">Ldap-Display-Name</span></span> | <span data-ttu-id="dedaa-112">дскорепропагатиондата</span><span class="sxs-lookup"><span data-stu-id="dedaa-112">dSCorePropagationData</span></span>                                         |
| <span data-ttu-id="dedaa-113">Размер</span><span class="sxs-lookup"><span data-stu-id="dedaa-113">Size</span></span>              | \-                                                            |
| <span data-ttu-id="dedaa-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="dedaa-114">Update Privilege</span></span>  | \-                                                            |
| <span data-ttu-id="dedaa-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="dedaa-115">Update Frequency</span></span>  | \-                                                            |
| <span data-ttu-id="dedaa-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-116">Attribute-Id</span></span>      | <span data-ttu-id="dedaa-117">1.2.840.113556.1.4.1357</span><span class="sxs-lookup"><span data-stu-id="dedaa-117">1.2.840.113556.1.4.1357</span></span>                                       |
| <span data-ttu-id="dedaa-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="dedaa-118">System-Id-Guid</span></span>    | <span data-ttu-id="dedaa-119">d167aa4b-8b08-11d2-9939-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="dedaa-119">d167aa4b-8b08-11d2-9939-0000f87a57d4</span></span>                          |
| <span data-ttu-id="dedaa-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dedaa-120">Syntax</span></span>            | [<span data-ttu-id="dedaa-121">**String(обобщенное_время)**</span><span class="sxs-lookup"><span data-stu-id="dedaa-121">**String(Generalized-Time)**</span></span>](s-string-generalized-time.md) |



## <a name="implementations"></a><span data-ttu-id="dedaa-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="dedaa-122">Implementations</span></span>

-   [<span data-ttu-id="dedaa-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="dedaa-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="dedaa-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="dedaa-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="dedaa-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="dedaa-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="dedaa-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="dedaa-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="dedaa-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="dedaa-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="dedaa-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="dedaa-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="dedaa-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="dedaa-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="dedaa-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dedaa-130">Windows 2000 Server</span></span>



| <span data-ttu-id="dedaa-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-131">Entry</span></span> | <span data-ttu-id="dedaa-132">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-132">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-133">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-134">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-135">System-Only</span></span>            | <span data-ttu-id="dedaa-136">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-136">True</span></span>                            |
| <span data-ttu-id="dedaa-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-137">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-138">False</span></span>                           |
| <span data-ttu-id="dedaa-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-139">Is Indexed</span></span>             | <span data-ttu-id="dedaa-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-140">False</span></span>                           |
| <span data-ttu-id="dedaa-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-141">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-142">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-142">True</span></span>                            |
| <span data-ttu-id="dedaa-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-144">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-145">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-146">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-147">Search-Flags</span></span>           | <span data-ttu-id="dedaa-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-148">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-149">System-Flags</span></span>           | <span data-ttu-id="dedaa-150">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-150">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-151">Classes used in</span></span>        | [<span data-ttu-id="dedaa-152">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-152">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="dedaa-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dedaa-153">Windows Server 2003</span></span>



| <span data-ttu-id="dedaa-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-154">Entry</span></span> | <span data-ttu-id="dedaa-155">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-155">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-156">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-157">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-158">System-Only</span></span>            | <span data-ttu-id="dedaa-159">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-159">True</span></span>                            |
| <span data-ttu-id="dedaa-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-160">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-161">False</span></span>                           |
| <span data-ttu-id="dedaa-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-162">Is Indexed</span></span>             | <span data-ttu-id="dedaa-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-163">False</span></span>                           |
| <span data-ttu-id="dedaa-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-164">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-165">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-165">True</span></span>                            |
| <span data-ttu-id="dedaa-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-167">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-168">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-169">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-170">Search-Flags</span></span>           | <span data-ttu-id="dedaa-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-171">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-172">System-Flags</span></span>           | <span data-ttu-id="dedaa-173">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-173">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-174">Classes used in</span></span>        | [<span data-ttu-id="dedaa-175">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-175">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="dedaa-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="dedaa-176">ADAM</span></span>



| <span data-ttu-id="dedaa-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-177">Entry</span></span> | <span data-ttu-id="dedaa-178">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-178">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-179">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-180">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-181">System-Only</span></span>            | <span data-ttu-id="dedaa-182">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-182">True</span></span>                            |
| <span data-ttu-id="dedaa-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-183">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-184">False</span></span>                           |
| <span data-ttu-id="dedaa-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-185">Is Indexed</span></span>             | <span data-ttu-id="dedaa-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-186">False</span></span>                           |
| <span data-ttu-id="dedaa-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-187">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-188">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-188">True</span></span>                            |
| <span data-ttu-id="dedaa-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-190">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-191">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-192">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-193">Search-Flags</span></span>           | <span data-ttu-id="dedaa-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-194">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-195">System-Flags</span></span>           | <span data-ttu-id="dedaa-196">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-196">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-197">Classes used in</span></span>        | [<span data-ttu-id="dedaa-198">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-198">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="dedaa-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="dedaa-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="dedaa-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-200">Entry</span></span> | <span data-ttu-id="dedaa-201">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-201">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-202">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-203">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-204">System-Only</span></span>            | <span data-ttu-id="dedaa-205">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-205">True</span></span>                            |
| <span data-ttu-id="dedaa-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-206">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-207">False</span></span>                           |
| <span data-ttu-id="dedaa-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-208">Is Indexed</span></span>             | <span data-ttu-id="dedaa-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-209">False</span></span>                           |
| <span data-ttu-id="dedaa-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-210">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-211">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-211">True</span></span>                            |
| <span data-ttu-id="dedaa-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-213">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-214">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-215">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-216">Search-Flags</span></span>           | <span data-ttu-id="dedaa-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-217">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-218">System-Flags</span></span>           | <span data-ttu-id="dedaa-219">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-219">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-220">Classes used in</span></span>        | [<span data-ttu-id="dedaa-221">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-221">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="dedaa-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dedaa-222">Windows Server 2008</span></span>



| <span data-ttu-id="dedaa-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-223">Entry</span></span> | <span data-ttu-id="dedaa-224">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-224">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-225">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-226">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-227">System-Only</span></span>            | <span data-ttu-id="dedaa-228">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-228">True</span></span>                            |
| <span data-ttu-id="dedaa-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-229">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-230">False</span></span>                           |
| <span data-ttu-id="dedaa-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-231">Is Indexed</span></span>             | <span data-ttu-id="dedaa-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-232">False</span></span>                           |
| <span data-ttu-id="dedaa-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-233">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-234">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-234">True</span></span>                            |
| <span data-ttu-id="dedaa-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-239">Search-Flags</span></span>           | <span data-ttu-id="dedaa-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-240">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-241">System-Flags</span></span>           | <span data-ttu-id="dedaa-242">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-242">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-243">Classes used in</span></span>        | [<span data-ttu-id="dedaa-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="dedaa-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dedaa-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="dedaa-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-246">Entry</span></span> | <span data-ttu-id="dedaa-247">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-250">System-Only</span></span>            | <span data-ttu-id="dedaa-251">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-251">True</span></span>                            |
| <span data-ttu-id="dedaa-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-252">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-253">False</span></span>                           |
| <span data-ttu-id="dedaa-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-254">Is Indexed</span></span>             | <span data-ttu-id="dedaa-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-255">False</span></span>                           |
| <span data-ttu-id="dedaa-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-256">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-257">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-257">True</span></span>                            |
| <span data-ttu-id="dedaa-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-260">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-261">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-262">Search-Flags</span></span>           | <span data-ttu-id="dedaa-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-263">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-264">System-Flags</span></span>           | <span data-ttu-id="dedaa-265">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-265">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-266">Classes used in</span></span>        | [<span data-ttu-id="dedaa-267">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-267">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="dedaa-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dedaa-268">Windows Server 2012</span></span>



| <span data-ttu-id="dedaa-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="dedaa-269">Entry</span></span> | <span data-ttu-id="dedaa-270">Значение</span><span class="sxs-lookup"><span data-stu-id="dedaa-270">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="dedaa-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="dedaa-271">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="dedaa-272">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="dedaa-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="dedaa-273">System-Only</span></span>            | <span data-ttu-id="dedaa-274">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-274">True</span></span>                            |
| <span data-ttu-id="dedaa-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="dedaa-275">Is-Single-Valued</span></span>       | <span data-ttu-id="dedaa-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-276">False</span></span>                           |
| <span data-ttu-id="dedaa-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="dedaa-277">Is Indexed</span></span>             | <span data-ttu-id="dedaa-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="dedaa-278">False</span></span>                           |
| <span data-ttu-id="dedaa-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="dedaa-279">In Global Catalog</span></span>      | <span data-ttu-id="dedaa-280">True</span><span class="sxs-lookup"><span data-stu-id="dedaa-280">True</span></span>                            |
| <span data-ttu-id="dedaa-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="dedaa-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="dedaa-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="dedaa-282">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="dedaa-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="dedaa-283">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="dedaa-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="dedaa-284">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="dedaa-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-285">Search-Flags</span></span>           | <span data-ttu-id="dedaa-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="dedaa-286">0x00000000</span></span>                      |
| <span data-ttu-id="dedaa-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="dedaa-287">System-Flags</span></span>           | <span data-ttu-id="dedaa-288">0x00000013</span><span class="sxs-lookup"><span data-stu-id="dedaa-288">0x00000013</span></span>                      |
| <span data-ttu-id="dedaa-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="dedaa-289">Classes used in</span></span>        | [<span data-ttu-id="dedaa-290">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="dedaa-290">**Top**</span></span>](c-top.md)<br/> |



 

 





