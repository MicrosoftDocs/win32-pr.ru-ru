---
title: Атрибут расширенного атрибута-info
description: Многозначное свойство, содержащее строки, представляющие дополнительные сведения для каждого атрибута.
ms.assetid: 38f87907-a328-473f-bc9c-f3573bc05af5
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута расширенного атрибута--info
- Схема AD атрибута Екстендедаттрибутеинфо
topic_type:
- apiref
api_name:
- Extended-Attribute-Info
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2c5e1498716dfbac2a1c539f7c9a5bfb48fb41
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416228"
---
# <a name="extended-attribute-info-attribute"></a><span data-ttu-id="2d74b-105">Атрибут расширенного атрибута-info</span><span class="sxs-lookup"><span data-stu-id="2d74b-105">Extended-Attribute-Info attribute</span></span>

<span data-ttu-id="2d74b-106">Многозначное свойство, содержащее строки, представляющие дополнительные сведения для каждого атрибута.</span><span class="sxs-lookup"><span data-stu-id="2d74b-106">A multi-valued property that contains strings that represent additional information for each attribute.</span></span>



| <span data-ttu-id="2d74b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-107">Entry</span></span> | <span data-ttu-id="2d74b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-109">CN</span><span class="sxs-lookup"><span data-stu-id="2d74b-109">CN</span></span>                | <span data-ttu-id="2d74b-110">Расширенный атрибут-сведения</span><span class="sxs-lookup"><span data-stu-id="2d74b-110">Extended-Attribute-Info</span></span>                     |
| <span data-ttu-id="2d74b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2d74b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2d74b-112">екстендедаттрибутеинфо</span><span class="sxs-lookup"><span data-stu-id="2d74b-112">extendedAttributeInfo</span></span>                       |
| <span data-ttu-id="2d74b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2d74b-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2d74b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2d74b-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="2d74b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2d74b-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2d74b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-116">Attribute-Id</span></span>      | <span data-ttu-id="2d74b-117">1.2.840.113556.1.4.909</span><span class="sxs-lookup"><span data-stu-id="2d74b-117">1.2.840.113556.1.4.909</span></span>                      |
| <span data-ttu-id="2d74b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2d74b-118">System-Id-Guid</span></span>    | <span data-ttu-id="2d74b-119">9a7ad947-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="2d74b-119">9a7ad947-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="2d74b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d74b-120">Syntax</span></span>            | [<span data-ttu-id="2d74b-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2d74b-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2d74b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2d74b-122">Implementations</span></span>

-   [<span data-ttu-id="2d74b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2d74b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2d74b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2d74b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2d74b-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2d74b-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2d74b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2d74b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2d74b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2d74b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2d74b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2d74b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2d74b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d74b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2d74b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2d74b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2d74b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-131">Entry</span></span> | <span data-ttu-id="2d74b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-132">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-133">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-134">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-135">System-Only</span></span>            | <span data-ttu-id="2d74b-136">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-136">True</span></span>                                        |
| <span data-ttu-id="2d74b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-138">False</span></span>                                       |
| <span data-ttu-id="2d74b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-139">Is Indexed</span></span>             | <span data-ttu-id="2d74b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-140">False</span></span>                                       |
| <span data-ttu-id="2d74b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-141">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-142">False</span></span>                                       |
| <span data-ttu-id="2d74b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-144">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-145">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-146">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-147">Search-Flags</span></span>           | <span data-ttu-id="2d74b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-148">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-149">System-Flags</span></span>           | <span data-ttu-id="2d74b-150">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-150">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-151">Classes used in</span></span>        | [<span data-ttu-id="2d74b-152">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-152">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2d74b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2d74b-153">Windows Server 2003</span></span>



| <span data-ttu-id="2d74b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-154">Entry</span></span> | <span data-ttu-id="2d74b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-155">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-156">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-157">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-158">System-Only</span></span>            | <span data-ttu-id="2d74b-159">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-159">True</span></span>                                        |
| <span data-ttu-id="2d74b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-161">False</span></span>                                       |
| <span data-ttu-id="2d74b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-162">Is Indexed</span></span>             | <span data-ttu-id="2d74b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-163">False</span></span>                                       |
| <span data-ttu-id="2d74b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-164">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-165">False</span></span>                                       |
| <span data-ttu-id="2d74b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-167">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-168">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-169">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-170">Search-Flags</span></span>           | <span data-ttu-id="2d74b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-171">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-172">System-Flags</span></span>           | <span data-ttu-id="2d74b-173">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-173">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-174">Classes used in</span></span>        | [<span data-ttu-id="2d74b-175">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-175">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2d74b-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="2d74b-176">ADAM</span></span>



| <span data-ttu-id="2d74b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-177">Entry</span></span> | <span data-ttu-id="2d74b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-178">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-179">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-180">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-181">System-Only</span></span>            | <span data-ttu-id="2d74b-182">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-182">True</span></span>                                        |
| <span data-ttu-id="2d74b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-184">False</span></span>                                       |
| <span data-ttu-id="2d74b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-185">Is Indexed</span></span>             | <span data-ttu-id="2d74b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-186">False</span></span>                                       |
| <span data-ttu-id="2d74b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-187">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-188">False</span></span>                                       |
| <span data-ttu-id="2d74b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-190">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-191">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-192">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-193">Search-Flags</span></span>           | <span data-ttu-id="2d74b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-194">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-195">System-Flags</span></span>           | <span data-ttu-id="2d74b-196">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-196">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-197">Classes used in</span></span>        | [<span data-ttu-id="2d74b-198">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-198">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2d74b-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2d74b-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2d74b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-200">Entry</span></span> | <span data-ttu-id="2d74b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-201">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-202">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-203">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-204">System-Only</span></span>            | <span data-ttu-id="2d74b-205">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-205">True</span></span>                                        |
| <span data-ttu-id="2d74b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-207">False</span></span>                                       |
| <span data-ttu-id="2d74b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-208">Is Indexed</span></span>             | <span data-ttu-id="2d74b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-209">False</span></span>                                       |
| <span data-ttu-id="2d74b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-210">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-211">False</span></span>                                       |
| <span data-ttu-id="2d74b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-213">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-214">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-215">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-216">Search-Flags</span></span>           | <span data-ttu-id="2d74b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-217">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-218">System-Flags</span></span>           | <span data-ttu-id="2d74b-219">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-219">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-220">Classes used in</span></span>        | [<span data-ttu-id="2d74b-221">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-221">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2d74b-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d74b-222">Windows Server 2008</span></span>



| <span data-ttu-id="2d74b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-223">Entry</span></span> | <span data-ttu-id="2d74b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-224">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-225">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-226">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-227">System-Only</span></span>            | <span data-ttu-id="2d74b-228">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-228">True</span></span>                                        |
| <span data-ttu-id="2d74b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-230">False</span></span>                                       |
| <span data-ttu-id="2d74b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-231">Is Indexed</span></span>             | <span data-ttu-id="2d74b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-232">False</span></span>                                       |
| <span data-ttu-id="2d74b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-233">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-234">False</span></span>                                       |
| <span data-ttu-id="2d74b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-236">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-237">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-238">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-239">Search-Flags</span></span>           | <span data-ttu-id="2d74b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-240">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-241">System-Flags</span></span>           | <span data-ttu-id="2d74b-242">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-242">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-243">Classes used in</span></span>        | [<span data-ttu-id="2d74b-244">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-244">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2d74b-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2d74b-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2d74b-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-246">Entry</span></span> | <span data-ttu-id="2d74b-247">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-247">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-248">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-249">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-250">System-Only</span></span>            | <span data-ttu-id="2d74b-251">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-251">True</span></span>                                        |
| <span data-ttu-id="2d74b-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-253">False</span></span>                                       |
| <span data-ttu-id="2d74b-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-254">Is Indexed</span></span>             | <span data-ttu-id="2d74b-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-255">False</span></span>                                       |
| <span data-ttu-id="2d74b-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-256">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-257">False</span></span>                                       |
| <span data-ttu-id="2d74b-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-259">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-260">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-261">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-262">Search-Flags</span></span>           | <span data-ttu-id="2d74b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-263">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-264">System-Flags</span></span>           | <span data-ttu-id="2d74b-265">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-265">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-266">Classes used in</span></span>        | [<span data-ttu-id="2d74b-267">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-267">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2d74b-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d74b-268">Windows Server 2012</span></span>



| <span data-ttu-id="2d74b-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d74b-269">Entry</span></span> | <span data-ttu-id="2d74b-270">Значение</span><span class="sxs-lookup"><span data-stu-id="2d74b-270">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2d74b-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d74b-271">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d74b-272">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="2d74b-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d74b-273">System-Only</span></span>            | <span data-ttu-id="2d74b-274">True</span><span class="sxs-lookup"><span data-stu-id="2d74b-274">True</span></span>                                        |
| <span data-ttu-id="2d74b-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d74b-275">Is-Single-Valued</span></span>       | <span data-ttu-id="2d74b-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-276">False</span></span>                                       |
| <span data-ttu-id="2d74b-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d74b-277">Is Indexed</span></span>             | <span data-ttu-id="2d74b-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-278">False</span></span>                                       |
| <span data-ttu-id="2d74b-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d74b-279">In Global Catalog</span></span>      | <span data-ttu-id="2d74b-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d74b-280">False</span></span>                                       |
| <span data-ttu-id="2d74b-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d74b-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d74b-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d74b-282">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2d74b-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d74b-283">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d74b-284">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2d74b-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-285">Search-Flags</span></span>           | <span data-ttu-id="2d74b-286">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d74b-286">0x00000000</span></span>                                  |
| <span data-ttu-id="2d74b-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d74b-287">System-Flags</span></span>           | <span data-ttu-id="2d74b-288">0x08000014</span><span class="sxs-lookup"><span data-stu-id="2d74b-288">0x08000014</span></span>                                  |
| <span data-ttu-id="2d74b-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d74b-289">Classes used in</span></span>        | [<span data-ttu-id="2d74b-290">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="2d74b-290">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





