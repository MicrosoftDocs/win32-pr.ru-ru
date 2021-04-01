---
title: атрибут MS-дов-Лабеледури
description: URI Exchange, за которым следует метка.
ms.assetid: 56b92fb9-0000-4ce4-8319-f3cad2b6f392
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-дов-Лабеледури
- Схема AD атрибута Мсексчлабеледури
topic_type:
- apiref
api_name:
- ms-Exch-LabeledURI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8632f1b4de60aa9ba04de15781d7e34fe0c105e7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989691"
---
# <a name="ms-exch-labeleduri-attribute"></a><span data-ttu-id="8cec9-105">атрибут MS-дов-Лабеледури</span><span class="sxs-lookup"><span data-stu-id="8cec9-105">ms-Exch-LabeledURI attribute</span></span>

<span data-ttu-id="8cec9-106">URI Exchange, за которым следует метка.</span><span class="sxs-lookup"><span data-stu-id="8cec9-106">An Exchange URI followed by a label.</span></span> <span data-ttu-id="8cec9-107">Метка используется для описания ресурса, на который указывает URI, и предназначенного для удобного для восприятия имени.</span><span class="sxs-lookup"><span data-stu-id="8cec9-107">The label is used to describe the resource to which the URI points and is intended as a human-readable name.</span></span>



| <span data-ttu-id="8cec9-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cec9-108">Entry</span></span> | <span data-ttu-id="8cec9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8cec9-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8cec9-110">CN</span><span class="sxs-lookup"><span data-stu-id="8cec9-110">CN</span></span>                | <span data-ttu-id="8cec9-111">MS-дов-Лабеледури</span><span class="sxs-lookup"><span data-stu-id="8cec9-111">ms-Exch-LabeledURI</span></span>                          |
| <span data-ttu-id="8cec9-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8cec9-112">Ldap-Display-Name</span></span> | <span data-ttu-id="8cec9-113">мсексчлабеледури</span><span class="sxs-lookup"><span data-stu-id="8cec9-113">msExchLabeledURI</span></span>                            |
| <span data-ttu-id="8cec9-114">Размер</span><span class="sxs-lookup"><span data-stu-id="8cec9-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="8cec9-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8cec9-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="8cec9-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8cec9-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8cec9-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8cec9-117">Attribute-Id</span></span>      | <span data-ttu-id="8cec9-118">1.2.840.113556.1.2.593</span><span class="sxs-lookup"><span data-stu-id="8cec9-118">1.2.840.113556.1.2.593</span></span>                      |
| <span data-ttu-id="8cec9-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8cec9-119">System-Id-Guid</span></span>    | <span data-ttu-id="8cec9-120">16775820-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8cec9-120">16775820-47f3-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="8cec9-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8cec9-121">Syntax</span></span>            | [<span data-ttu-id="8cec9-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8cec9-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8cec9-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8cec9-123">Implementations</span></span>

-   [<span data-ttu-id="8cec9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8cec9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8cec9-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8cec9-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8cec9-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8cec9-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8cec9-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8cec9-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8cec9-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8cec9-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8cec9-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8cec9-129">Windows Server 2003</span></span>



| <span data-ttu-id="8cec9-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cec9-130">Entry</span></span> | <span data-ttu-id="8cec9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8cec9-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8cec9-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cec9-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8cec9-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cec9-133">MAPI-Id</span></span>                | <span data-ttu-id="8cec9-134">0x921</span><span class="sxs-lookup"><span data-stu-id="8cec9-134">0x921</span></span>                                                |
| <span data-ttu-id="8cec9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cec9-135">System-Only</span></span>            | <span data-ttu-id="8cec9-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-136">False</span></span>                                                |
| <span data-ttu-id="8cec9-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cec9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8cec9-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-138">False</span></span>                                                |
| <span data-ttu-id="8cec9-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cec9-139">Is Indexed</span></span>             | <span data-ttu-id="8cec9-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-140">False</span></span>                                                |
| <span data-ttu-id="8cec9-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cec9-141">In Global Catalog</span></span>      | <span data-ttu-id="8cec9-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-142">False</span></span>                                                |
| <span data-ttu-id="8cec9-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cec9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cec9-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cec9-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8cec9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cec9-145">Range-Lower</span></span>            | <span data-ttu-id="8cec9-146">1</span><span class="sxs-lookup"><span data-stu-id="8cec9-146">1</span></span>                                                    |
| <span data-ttu-id="8cec9-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cec9-147">Range-Upper</span></span>            | <span data-ttu-id="8cec9-148">1024</span><span class="sxs-lookup"><span data-stu-id="8cec9-148">1024</span></span>                                                 |
| <span data-ttu-id="8cec9-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-149">Search-Flags</span></span>           | <span data-ttu-id="8cec9-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-150">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-151">System-Flags</span></span>           | <span data-ttu-id="8cec9-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-152">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cec9-153">Classes used in</span></span>        | [<span data-ttu-id="8cec9-154">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="8cec9-154">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8cec9-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8cec9-155">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8cec9-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cec9-156">Entry</span></span> | <span data-ttu-id="8cec9-157">Значение</span><span class="sxs-lookup"><span data-stu-id="8cec9-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8cec9-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cec9-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8cec9-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cec9-159">MAPI-Id</span></span>                | <span data-ttu-id="8cec9-160">0x921</span><span class="sxs-lookup"><span data-stu-id="8cec9-160">0x921</span></span>                                                |
| <span data-ttu-id="8cec9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cec9-161">System-Only</span></span>            | <span data-ttu-id="8cec9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-162">False</span></span>                                                |
| <span data-ttu-id="8cec9-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cec9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8cec9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-164">False</span></span>                                                |
| <span data-ttu-id="8cec9-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cec9-165">Is Indexed</span></span>             | <span data-ttu-id="8cec9-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-166">False</span></span>                                                |
| <span data-ttu-id="8cec9-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cec9-167">In Global Catalog</span></span>      | <span data-ttu-id="8cec9-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-168">False</span></span>                                                |
| <span data-ttu-id="8cec9-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cec9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cec9-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cec9-170">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8cec9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cec9-171">Range-Lower</span></span>            | <span data-ttu-id="8cec9-172">1</span><span class="sxs-lookup"><span data-stu-id="8cec9-172">1</span></span>                                                    |
| <span data-ttu-id="8cec9-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cec9-173">Range-Upper</span></span>            | <span data-ttu-id="8cec9-174">1024</span><span class="sxs-lookup"><span data-stu-id="8cec9-174">1024</span></span>                                                 |
| <span data-ttu-id="8cec9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-175">Search-Flags</span></span>           | <span data-ttu-id="8cec9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-176">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-177">System-Flags</span></span>           | <span data-ttu-id="8cec9-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-178">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cec9-179">Classes used in</span></span>        | [<span data-ttu-id="8cec9-180">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="8cec9-180">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8cec9-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cec9-181">Windows Server 2008</span></span>



| <span data-ttu-id="8cec9-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cec9-182">Entry</span></span> | <span data-ttu-id="8cec9-183">Значение</span><span class="sxs-lookup"><span data-stu-id="8cec9-183">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8cec9-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cec9-184">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8cec9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cec9-185">MAPI-Id</span></span>                | <span data-ttu-id="8cec9-186">0x921</span><span class="sxs-lookup"><span data-stu-id="8cec9-186">0x921</span></span>                                                |
| <span data-ttu-id="8cec9-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cec9-187">System-Only</span></span>            | <span data-ttu-id="8cec9-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-188">False</span></span>                                                |
| <span data-ttu-id="8cec9-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cec9-189">Is-Single-Valued</span></span>       | <span data-ttu-id="8cec9-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-190">False</span></span>                                                |
| <span data-ttu-id="8cec9-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cec9-191">Is Indexed</span></span>             | <span data-ttu-id="8cec9-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-192">False</span></span>                                                |
| <span data-ttu-id="8cec9-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cec9-193">In Global Catalog</span></span>      | <span data-ttu-id="8cec9-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-194">False</span></span>                                                |
| <span data-ttu-id="8cec9-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cec9-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cec9-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cec9-196">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8cec9-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cec9-197">Range-Lower</span></span>            | <span data-ttu-id="8cec9-198">1</span><span class="sxs-lookup"><span data-stu-id="8cec9-198">1</span></span>                                                    |
| <span data-ttu-id="8cec9-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cec9-199">Range-Upper</span></span>            | <span data-ttu-id="8cec9-200">1024</span><span class="sxs-lookup"><span data-stu-id="8cec9-200">1024</span></span>                                                 |
| <span data-ttu-id="8cec9-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-201">Search-Flags</span></span>           | <span data-ttu-id="8cec9-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-202">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-203">System-Flags</span></span>           | <span data-ttu-id="8cec9-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-204">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cec9-205">Classes used in</span></span>        | [<span data-ttu-id="8cec9-206">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="8cec9-206">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8cec9-207">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8cec9-207">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8cec9-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cec9-208">Entry</span></span> | <span data-ttu-id="8cec9-209">Значение</span><span class="sxs-lookup"><span data-stu-id="8cec9-209">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8cec9-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cec9-210">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8cec9-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cec9-211">MAPI-Id</span></span>                | <span data-ttu-id="8cec9-212">0x921</span><span class="sxs-lookup"><span data-stu-id="8cec9-212">0x921</span></span>                                                |
| <span data-ttu-id="8cec9-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cec9-213">System-Only</span></span>            | <span data-ttu-id="8cec9-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-214">False</span></span>                                                |
| <span data-ttu-id="8cec9-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cec9-215">Is-Single-Valued</span></span>       | <span data-ttu-id="8cec9-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-216">False</span></span>                                                |
| <span data-ttu-id="8cec9-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cec9-217">Is Indexed</span></span>             | <span data-ttu-id="8cec9-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-218">False</span></span>                                                |
| <span data-ttu-id="8cec9-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cec9-219">In Global Catalog</span></span>      | <span data-ttu-id="8cec9-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-220">False</span></span>                                                |
| <span data-ttu-id="8cec9-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cec9-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cec9-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cec9-222">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8cec9-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cec9-223">Range-Lower</span></span>            | <span data-ttu-id="8cec9-224">1</span><span class="sxs-lookup"><span data-stu-id="8cec9-224">1</span></span>                                                    |
| <span data-ttu-id="8cec9-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cec9-225">Range-Upper</span></span>            | <span data-ttu-id="8cec9-226">1024</span><span class="sxs-lookup"><span data-stu-id="8cec9-226">1024</span></span>                                                 |
| <span data-ttu-id="8cec9-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-227">Search-Flags</span></span>           | <span data-ttu-id="8cec9-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-228">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-229">System-Flags</span></span>           | <span data-ttu-id="8cec9-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-230">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cec9-231">Classes used in</span></span>        | [<span data-ttu-id="8cec9-232">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="8cec9-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8cec9-233">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cec9-233">Windows Server 2012</span></span>



| <span data-ttu-id="8cec9-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="8cec9-234">Entry</span></span> | <span data-ttu-id="8cec9-235">Значение</span><span class="sxs-lookup"><span data-stu-id="8cec9-235">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8cec9-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8cec9-236">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8cec9-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8cec9-237">MAPI-Id</span></span>                | <span data-ttu-id="8cec9-238">0x921</span><span class="sxs-lookup"><span data-stu-id="8cec9-238">0x921</span></span>                                                |
| <span data-ttu-id="8cec9-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="8cec9-239">System-Only</span></span>            | <span data-ttu-id="8cec9-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-240">False</span></span>                                                |
| <span data-ttu-id="8cec9-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8cec9-241">Is-Single-Valued</span></span>       | <span data-ttu-id="8cec9-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-242">False</span></span>                                                |
| <span data-ttu-id="8cec9-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8cec9-243">Is Indexed</span></span>             | <span data-ttu-id="8cec9-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-244">False</span></span>                                                |
| <span data-ttu-id="8cec9-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8cec9-245">In Global Catalog</span></span>      | <span data-ttu-id="8cec9-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="8cec9-246">False</span></span>                                                |
| <span data-ttu-id="8cec9-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8cec9-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="8cec9-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8cec9-248">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8cec9-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8cec9-249">Range-Lower</span></span>            | <span data-ttu-id="8cec9-250">1</span><span class="sxs-lookup"><span data-stu-id="8cec9-250">1</span></span>                                                    |
| <span data-ttu-id="8cec9-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8cec9-251">Range-Upper</span></span>            | <span data-ttu-id="8cec9-252">1024</span><span class="sxs-lookup"><span data-stu-id="8cec9-252">1024</span></span>                                                 |
| <span data-ttu-id="8cec9-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-253">Search-Flags</span></span>           | <span data-ttu-id="8cec9-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-254">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8cec9-255">System-Flags</span></span>           | <span data-ttu-id="8cec9-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8cec9-256">0x00000000</span></span>                                           |
| <span data-ttu-id="8cec9-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8cec9-257">Classes used in</span></span>        | [<span data-ttu-id="8cec9-258">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="8cec9-258">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





