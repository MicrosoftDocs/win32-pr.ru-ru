---
title: Атрибут MSMQ-Recipient-FormatName
description: Используется в качестве имени формата получателя в классе MSMQ-Custom-получател.
ms.assetid: 26ee4cec-4e69-412e-914b-437f2f4cd88e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибутов MSMQ-Recipient-FormatName
- Схема AD атрибутов msMQ-Recipient-FormatName
topic_type:
- apiref
api_name:
- MSMQ-Recipient-FormatName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57fbeee49ddf0c734212bc91926e5c848a9e8d1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138918"
---
# <a name="msmq-recipient-formatname-attribute"></a><span data-ttu-id="74b56-105">Атрибут MSMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="74b56-105">MSMQ-Recipient-FormatName attribute</span></span>

<span data-ttu-id="74b56-106">Используется в качестве имени формата получателя в классе MSMQ-Custom-получател.</span><span class="sxs-lookup"><span data-stu-id="74b56-106">Used as the recipient format name in the MSMQ-Custom-Recipient class.</span></span>



| <span data-ttu-id="74b56-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="74b56-107">Entry</span></span> | <span data-ttu-id="74b56-108">Значение</span><span class="sxs-lookup"><span data-stu-id="74b56-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="74b56-109">CN</span><span class="sxs-lookup"><span data-stu-id="74b56-109">CN</span></span>                | <span data-ttu-id="74b56-110">MSMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="74b56-110">MSMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="74b56-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="74b56-111">Ldap-Display-Name</span></span> | <span data-ttu-id="74b56-112">msMQ-Recipient-FormatName</span><span class="sxs-lookup"><span data-stu-id="74b56-112">msMQ-Recipient-FormatName</span></span>                   |
| <span data-ttu-id="74b56-113">Размер</span><span class="sxs-lookup"><span data-stu-id="74b56-113">Size</span></span>              | <span data-ttu-id="74b56-114">от 1 до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="74b56-114">1 to 255 characters.</span></span>                        |
| <span data-ttu-id="74b56-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="74b56-115">Update Privilege</span></span>  | <span data-ttu-id="74b56-116">Владелец очереди.</span><span class="sxs-lookup"><span data-stu-id="74b56-116">The queue owner.</span></span>                            |
| <span data-ttu-id="74b56-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="74b56-117">Update Frequency</span></span>  | <span data-ttu-id="74b56-118">Только после перемещения внешней очереди.</span><span class="sxs-lookup"><span data-stu-id="74b56-118">Only after the external queue was moved.</span></span>    |
| <span data-ttu-id="74b56-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74b56-119">Attribute-Id</span></span>      | <span data-ttu-id="74b56-120">1.2.840.113556.1.4.1695</span><span class="sxs-lookup"><span data-stu-id="74b56-120">1.2.840.113556.1.4.1695</span></span>                     |
| <span data-ttu-id="74b56-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="74b56-121">System-Id-Guid</span></span>    | <span data-ttu-id="74b56-122">3bfe6748-b544-485a-b067-1b310c4334bf</span><span class="sxs-lookup"><span data-stu-id="74b56-122">3bfe6748-b544-485a-b067-1b310c4334bf</span></span>        |
| <span data-ttu-id="74b56-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74b56-123">Syntax</span></span>            | [<span data-ttu-id="74b56-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="74b56-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="74b56-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="74b56-125">Implementations</span></span>

-   [<span data-ttu-id="74b56-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="74b56-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="74b56-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="74b56-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="74b56-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="74b56-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="74b56-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="74b56-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="74b56-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74b56-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="74b56-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74b56-131">Windows Server 2003</span></span>



| <span data-ttu-id="74b56-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="74b56-132">Entry</span></span> | <span data-ttu-id="74b56-133">Значение</span><span class="sxs-lookup"><span data-stu-id="74b56-133">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="74b56-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74b56-134">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b56-135">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b56-136">System-Only</span></span>            | <span data-ttu-id="74b56-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-137">False</span></span>                                                               |
| <span data-ttu-id="74b56-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74b56-138">Is-Single-Valued</span></span>       | <span data-ttu-id="74b56-139">True</span><span class="sxs-lookup"><span data-stu-id="74b56-139">True</span></span>                                                                |
| <span data-ttu-id="74b56-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74b56-140">Is Indexed</span></span>             | <span data-ttu-id="74b56-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-141">False</span></span>                                                               |
| <span data-ttu-id="74b56-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74b56-142">In Global Catalog</span></span>      | <span data-ttu-id="74b56-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-143">False</span></span>                                                               |
| <span data-ttu-id="74b56-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74b56-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b56-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74b56-145">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="74b56-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b56-146">Range-Lower</span></span>            | <span data-ttu-id="74b56-147">1</span><span class="sxs-lookup"><span data-stu-id="74b56-147">1</span></span>                                                                   |
| <span data-ttu-id="74b56-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b56-148">Range-Upper</span></span>            | <span data-ttu-id="74b56-149">255</span><span class="sxs-lookup"><span data-stu-id="74b56-149">255</span></span>                                                                 |
| <span data-ttu-id="74b56-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-150">Search-Flags</span></span>           | <span data-ttu-id="74b56-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b56-151">0x00000000</span></span>                                                          |
| <span data-ttu-id="74b56-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-152">System-Flags</span></span>           | <span data-ttu-id="74b56-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b56-153">0x00000010</span></span>                                                          |
| <span data-ttu-id="74b56-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74b56-154">Classes used in</span></span>        | [<span data-ttu-id="74b56-155">**MSMQ-Custom-получател**</span><span class="sxs-lookup"><span data-stu-id="74b56-155">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="74b56-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="74b56-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="74b56-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="74b56-157">Entry</span></span> | <span data-ttu-id="74b56-158">Значение</span><span class="sxs-lookup"><span data-stu-id="74b56-158">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="74b56-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74b56-159">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b56-160">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b56-161">System-Only</span></span>            | <span data-ttu-id="74b56-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-162">False</span></span>                                                               |
| <span data-ttu-id="74b56-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74b56-163">Is-Single-Valued</span></span>       | <span data-ttu-id="74b56-164">True</span><span class="sxs-lookup"><span data-stu-id="74b56-164">True</span></span>                                                                |
| <span data-ttu-id="74b56-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74b56-165">Is Indexed</span></span>             | <span data-ttu-id="74b56-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-166">False</span></span>                                                               |
| <span data-ttu-id="74b56-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74b56-167">In Global Catalog</span></span>      | <span data-ttu-id="74b56-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-168">False</span></span>                                                               |
| <span data-ttu-id="74b56-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74b56-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b56-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74b56-170">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="74b56-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b56-171">Range-Lower</span></span>            | <span data-ttu-id="74b56-172">1</span><span class="sxs-lookup"><span data-stu-id="74b56-172">1</span></span>                                                                   |
| <span data-ttu-id="74b56-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b56-173">Range-Upper</span></span>            | <span data-ttu-id="74b56-174">255</span><span class="sxs-lookup"><span data-stu-id="74b56-174">255</span></span>                                                                 |
| <span data-ttu-id="74b56-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-175">Search-Flags</span></span>           | <span data-ttu-id="74b56-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b56-176">0x00000000</span></span>                                                          |
| <span data-ttu-id="74b56-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-177">System-Flags</span></span>           | <span data-ttu-id="74b56-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b56-178">0x00000010</span></span>                                                          |
| <span data-ttu-id="74b56-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74b56-179">Classes used in</span></span>        | [<span data-ttu-id="74b56-180">**MSMQ-Custom-получател**</span><span class="sxs-lookup"><span data-stu-id="74b56-180">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="74b56-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74b56-181">Windows Server 2008</span></span>



| <span data-ttu-id="74b56-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="74b56-182">Entry</span></span> | <span data-ttu-id="74b56-183">Значение</span><span class="sxs-lookup"><span data-stu-id="74b56-183">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="74b56-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74b56-184">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b56-185">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b56-186">System-Only</span></span>            | <span data-ttu-id="74b56-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-187">False</span></span>                                                               |
| <span data-ttu-id="74b56-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74b56-188">Is-Single-Valued</span></span>       | <span data-ttu-id="74b56-189">True</span><span class="sxs-lookup"><span data-stu-id="74b56-189">True</span></span>                                                                |
| <span data-ttu-id="74b56-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74b56-190">Is Indexed</span></span>             | <span data-ttu-id="74b56-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-191">False</span></span>                                                               |
| <span data-ttu-id="74b56-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74b56-192">In Global Catalog</span></span>      | <span data-ttu-id="74b56-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-193">False</span></span>                                                               |
| <span data-ttu-id="74b56-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74b56-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b56-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74b56-195">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="74b56-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b56-196">Range-Lower</span></span>            | <span data-ttu-id="74b56-197">1</span><span class="sxs-lookup"><span data-stu-id="74b56-197">1</span></span>                                                                   |
| <span data-ttu-id="74b56-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b56-198">Range-Upper</span></span>            | <span data-ttu-id="74b56-199">255</span><span class="sxs-lookup"><span data-stu-id="74b56-199">255</span></span>                                                                 |
| <span data-ttu-id="74b56-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-200">Search-Flags</span></span>           | <span data-ttu-id="74b56-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b56-201">0x00000000</span></span>                                                          |
| <span data-ttu-id="74b56-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-202">System-Flags</span></span>           | <span data-ttu-id="74b56-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b56-203">0x00000010</span></span>                                                          |
| <span data-ttu-id="74b56-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74b56-204">Classes used in</span></span>        | [<span data-ttu-id="74b56-205">**MSMQ-Custom-получател**</span><span class="sxs-lookup"><span data-stu-id="74b56-205">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="74b56-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="74b56-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="74b56-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="74b56-207">Entry</span></span> | <span data-ttu-id="74b56-208">Значение</span><span class="sxs-lookup"><span data-stu-id="74b56-208">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="74b56-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74b56-209">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b56-210">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b56-211">System-Only</span></span>            | <span data-ttu-id="74b56-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-212">False</span></span>                                                               |
| <span data-ttu-id="74b56-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74b56-213">Is-Single-Valued</span></span>       | <span data-ttu-id="74b56-214">True</span><span class="sxs-lookup"><span data-stu-id="74b56-214">True</span></span>                                                                |
| <span data-ttu-id="74b56-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74b56-215">Is Indexed</span></span>             | <span data-ttu-id="74b56-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-216">False</span></span>                                                               |
| <span data-ttu-id="74b56-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74b56-217">In Global Catalog</span></span>      | <span data-ttu-id="74b56-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-218">False</span></span>                                                               |
| <span data-ttu-id="74b56-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74b56-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b56-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74b56-220">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="74b56-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b56-221">Range-Lower</span></span>            | <span data-ttu-id="74b56-222">1</span><span class="sxs-lookup"><span data-stu-id="74b56-222">1</span></span>                                                                   |
| <span data-ttu-id="74b56-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b56-223">Range-Upper</span></span>            | <span data-ttu-id="74b56-224">255</span><span class="sxs-lookup"><span data-stu-id="74b56-224">255</span></span>                                                                 |
| <span data-ttu-id="74b56-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-225">Search-Flags</span></span>           | <span data-ttu-id="74b56-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b56-226">0x00000000</span></span>                                                          |
| <span data-ttu-id="74b56-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-227">System-Flags</span></span>           | <span data-ttu-id="74b56-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b56-228">0x00000010</span></span>                                                          |
| <span data-ttu-id="74b56-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74b56-229">Classes used in</span></span>        | [<span data-ttu-id="74b56-230">**MSMQ-Custom-получател**</span><span class="sxs-lookup"><span data-stu-id="74b56-230">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="74b56-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74b56-231">Windows Server 2012</span></span>



| <span data-ttu-id="74b56-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="74b56-232">Entry</span></span> | <span data-ttu-id="74b56-233">Значение</span><span class="sxs-lookup"><span data-stu-id="74b56-233">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="74b56-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="74b56-234">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74b56-235">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="74b56-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="74b56-236">System-Only</span></span>            | <span data-ttu-id="74b56-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-237">False</span></span>                                                               |
| <span data-ttu-id="74b56-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="74b56-238">Is-Single-Valued</span></span>       | <span data-ttu-id="74b56-239">True</span><span class="sxs-lookup"><span data-stu-id="74b56-239">True</span></span>                                                                |
| <span data-ttu-id="74b56-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="74b56-240">Is Indexed</span></span>             | <span data-ttu-id="74b56-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-241">False</span></span>                                                               |
| <span data-ttu-id="74b56-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="74b56-242">In Global Catalog</span></span>      | <span data-ttu-id="74b56-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="74b56-243">False</span></span>                                                               |
| <span data-ttu-id="74b56-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="74b56-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="74b56-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74b56-245">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="74b56-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74b56-246">Range-Lower</span></span>            | <span data-ttu-id="74b56-247">1</span><span class="sxs-lookup"><span data-stu-id="74b56-247">1</span></span>                                                                   |
| <span data-ttu-id="74b56-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74b56-248">Range-Upper</span></span>            | <span data-ttu-id="74b56-249">255</span><span class="sxs-lookup"><span data-stu-id="74b56-249">255</span></span>                                                                 |
| <span data-ttu-id="74b56-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-250">Search-Flags</span></span>           | <span data-ttu-id="74b56-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="74b56-251">0x00000000</span></span>                                                          |
| <span data-ttu-id="74b56-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74b56-252">System-Flags</span></span>           | <span data-ttu-id="74b56-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74b56-253">0x00000010</span></span>                                                          |
| <span data-ttu-id="74b56-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="74b56-254">Classes used in</span></span>        | [<span data-ttu-id="74b56-255">**MSMQ-Custom-получател**</span><span class="sxs-lookup"><span data-stu-id="74b56-255">**MSMQ-Custom-Recipient**</span></span>](c-msmq-custom-recipient.md)<br/> |



 

 





