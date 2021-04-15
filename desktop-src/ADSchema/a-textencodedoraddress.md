---
title: Атрибут с текстовым кодированием или адресом
description: Этот атрибут используется для поддержки адресов X. 400 в текстовом формате.
ms.assetid: 90ec82c5-08c4-44e3-90d8-a0a7a6d5f7b8
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута с кодировкой текста или адреса
- Схема AD атрибута Текстенкодедораддресс
topic_type:
- apiref
api_name:
- Text-Encoded-OR-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc5123f75c4ca628671816e7e5a27c56ee2c6c8a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655043"
---
# <a name="text-encoded-or-address-attribute"></a><span data-ttu-id="af929-105">Атрибут с текстовым кодированием или адресом</span><span class="sxs-lookup"><span data-stu-id="af929-105">Text-Encoded-OR-Address attribute</span></span>

<span data-ttu-id="af929-106">Этот атрибут используется для поддержки адресов X. 400 в текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="af929-106">This attribute is used to support X.400 addresses in a text format.</span></span>



| <span data-ttu-id="af929-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-107">Entry</span></span> | <span data-ttu-id="af929-108">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="af929-109">CN</span><span class="sxs-lookup"><span data-stu-id="af929-109">CN</span></span>                | <span data-ttu-id="af929-110">С текстовым кодированием или адресом</span><span class="sxs-lookup"><span data-stu-id="af929-110">Text-Encoded-OR-Address</span></span>                     |
| <span data-ttu-id="af929-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="af929-111">Ldap-Display-Name</span></span> | <span data-ttu-id="af929-112">текстенкодедораддресс</span><span class="sxs-lookup"><span data-stu-id="af929-112">textEncodedORAddress</span></span>                        |
| <span data-ttu-id="af929-113">Размер</span><span class="sxs-lookup"><span data-stu-id="af929-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="af929-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="af929-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="af929-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="af929-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="af929-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="af929-116">Attribute-Id</span></span>      | <span data-ttu-id="af929-117">0.9.2342.19200300.100.1.2</span><span class="sxs-lookup"><span data-stu-id="af929-117">0.9.2342.19200300.100.1.2</span></span>                   |
| <span data-ttu-id="af929-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="af929-118">System-Id-Guid</span></span>    | <span data-ttu-id="af929-119">a8df7489-c5ea-11d1-bbcb-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="af929-119">a8df7489-c5ea-11d1-bbcb-0080c76670c0</span></span>        |
| <span data-ttu-id="af929-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af929-120">Syntax</span></span>            | [<span data-ttu-id="af929-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="af929-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="af929-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="af929-122">Implementations</span></span>

-   [<span data-ttu-id="af929-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="af929-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="af929-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="af929-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="af929-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="af929-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="af929-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="af929-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="af929-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="af929-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="af929-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="af929-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="af929-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af929-129">Windows 2000 Server</span></span>



| <span data-ttu-id="af929-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-130">Entry</span></span> | <span data-ttu-id="af929-131">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="af929-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af929-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="af929-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af929-133">MAPI-Id</span></span>                | <span data-ttu-id="af929-134">0x8C81</span><span class="sxs-lookup"><span data-stu-id="af929-134">0x8C81</span></span>                                               |
| <span data-ttu-id="af929-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="af929-135">System-Only</span></span>            | <span data-ttu-id="af929-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-136">False</span></span>                                                |
| <span data-ttu-id="af929-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af929-137">Is-Single-Valued</span></span>       | <span data-ttu-id="af929-138">True</span><span class="sxs-lookup"><span data-stu-id="af929-138">True</span></span>                                                 |
| <span data-ttu-id="af929-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af929-139">Is Indexed</span></span>             | <span data-ttu-id="af929-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-140">False</span></span>                                                |
| <span data-ttu-id="af929-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af929-141">In Global Catalog</span></span>      | <span data-ttu-id="af929-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-142">False</span></span>                                                |
| <span data-ttu-id="af929-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af929-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="af929-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af929-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="af929-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af929-145">Range-Lower</span></span>            | <span data-ttu-id="af929-146">1</span><span class="sxs-lookup"><span data-stu-id="af929-146">1</span></span>                                                    |
| <span data-ttu-id="af929-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af929-147">Range-Upper</span></span>            | <span data-ttu-id="af929-148">1024</span><span class="sxs-lookup"><span data-stu-id="af929-148">1024</span></span>                                                 |
| <span data-ttu-id="af929-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-149">Search-Flags</span></span>           | <span data-ttu-id="af929-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-150">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-151">System-Flags</span></span>           | <span data-ttu-id="af929-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-152">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af929-153">Classes used in</span></span>        | [<span data-ttu-id="af929-154">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="af929-154">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="af929-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af929-155">Windows Server 2003</span></span>



| <span data-ttu-id="af929-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-156">Entry</span></span> | <span data-ttu-id="af929-157">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="af929-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af929-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="af929-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af929-159">MAPI-Id</span></span>                | <span data-ttu-id="af929-160">0x8C81</span><span class="sxs-lookup"><span data-stu-id="af929-160">0x8C81</span></span>                                               |
| <span data-ttu-id="af929-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="af929-161">System-Only</span></span>            | <span data-ttu-id="af929-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-162">False</span></span>                                                |
| <span data-ttu-id="af929-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af929-163">Is-Single-Valued</span></span>       | <span data-ttu-id="af929-164">True</span><span class="sxs-lookup"><span data-stu-id="af929-164">True</span></span>                                                 |
| <span data-ttu-id="af929-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af929-165">Is Indexed</span></span>             | <span data-ttu-id="af929-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-166">False</span></span>                                                |
| <span data-ttu-id="af929-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af929-167">In Global Catalog</span></span>      | <span data-ttu-id="af929-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-168">False</span></span>                                                |
| <span data-ttu-id="af929-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af929-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="af929-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af929-170">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="af929-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af929-171">Range-Lower</span></span>            | <span data-ttu-id="af929-172">1</span><span class="sxs-lookup"><span data-stu-id="af929-172">1</span></span>                                                    |
| <span data-ttu-id="af929-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af929-173">Range-Upper</span></span>            | <span data-ttu-id="af929-174">1024</span><span class="sxs-lookup"><span data-stu-id="af929-174">1024</span></span>                                                 |
| <span data-ttu-id="af929-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-175">Search-Flags</span></span>           | <span data-ttu-id="af929-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-176">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-177">System-Flags</span></span>           | <span data-ttu-id="af929-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-178">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af929-179">Classes used in</span></span>        | [<span data-ttu-id="af929-180">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="af929-180">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="af929-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="af929-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="af929-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-182">Entry</span></span> | <span data-ttu-id="af929-183">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-183">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="af929-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af929-184">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="af929-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af929-185">MAPI-Id</span></span>                | <span data-ttu-id="af929-186">0x8C81</span><span class="sxs-lookup"><span data-stu-id="af929-186">0x8C81</span></span>                                               |
| <span data-ttu-id="af929-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="af929-187">System-Only</span></span>            | <span data-ttu-id="af929-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-188">False</span></span>                                                |
| <span data-ttu-id="af929-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af929-189">Is-Single-Valued</span></span>       | <span data-ttu-id="af929-190">True</span><span class="sxs-lookup"><span data-stu-id="af929-190">True</span></span>                                                 |
| <span data-ttu-id="af929-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af929-191">Is Indexed</span></span>             | <span data-ttu-id="af929-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-192">False</span></span>                                                |
| <span data-ttu-id="af929-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af929-193">In Global Catalog</span></span>      | <span data-ttu-id="af929-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-194">False</span></span>                                                |
| <span data-ttu-id="af929-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af929-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="af929-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af929-196">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="af929-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af929-197">Range-Lower</span></span>            | <span data-ttu-id="af929-198">1</span><span class="sxs-lookup"><span data-stu-id="af929-198">1</span></span>                                                    |
| <span data-ttu-id="af929-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af929-199">Range-Upper</span></span>            | <span data-ttu-id="af929-200">1024</span><span class="sxs-lookup"><span data-stu-id="af929-200">1024</span></span>                                                 |
| <span data-ttu-id="af929-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-201">Search-Flags</span></span>           | <span data-ttu-id="af929-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-202">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-203">System-Flags</span></span>           | <span data-ttu-id="af929-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-204">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af929-205">Classes used in</span></span>        | [<span data-ttu-id="af929-206">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="af929-206">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="af929-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af929-207">Windows Server 2008</span></span>



| <span data-ttu-id="af929-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-208">Entry</span></span> | <span data-ttu-id="af929-209">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-209">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="af929-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af929-210">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="af929-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af929-211">MAPI-Id</span></span>                | <span data-ttu-id="af929-212">0x8C81</span><span class="sxs-lookup"><span data-stu-id="af929-212">0x8C81</span></span>                                               |
| <span data-ttu-id="af929-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="af929-213">System-Only</span></span>            | <span data-ttu-id="af929-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-214">False</span></span>                                                |
| <span data-ttu-id="af929-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af929-215">Is-Single-Valued</span></span>       | <span data-ttu-id="af929-216">True</span><span class="sxs-lookup"><span data-stu-id="af929-216">True</span></span>                                                 |
| <span data-ttu-id="af929-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af929-217">Is Indexed</span></span>             | <span data-ttu-id="af929-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-218">False</span></span>                                                |
| <span data-ttu-id="af929-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af929-219">In Global Catalog</span></span>      | <span data-ttu-id="af929-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-220">False</span></span>                                                |
| <span data-ttu-id="af929-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af929-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="af929-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af929-222">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="af929-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af929-223">Range-Lower</span></span>            | <span data-ttu-id="af929-224">1</span><span class="sxs-lookup"><span data-stu-id="af929-224">1</span></span>                                                    |
| <span data-ttu-id="af929-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af929-225">Range-Upper</span></span>            | <span data-ttu-id="af929-226">1024</span><span class="sxs-lookup"><span data-stu-id="af929-226">1024</span></span>                                                 |
| <span data-ttu-id="af929-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-227">Search-Flags</span></span>           | <span data-ttu-id="af929-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-228">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-229">System-Flags</span></span>           | <span data-ttu-id="af929-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-230">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af929-231">Classes used in</span></span>        | [<span data-ttu-id="af929-232">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="af929-232">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="af929-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="af929-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="af929-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-234">Entry</span></span> | <span data-ttu-id="af929-235">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-235">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="af929-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af929-236">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="af929-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af929-237">MAPI-Id</span></span>                | <span data-ttu-id="af929-238">0x8C81</span><span class="sxs-lookup"><span data-stu-id="af929-238">0x8C81</span></span>                                               |
| <span data-ttu-id="af929-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="af929-239">System-Only</span></span>            | <span data-ttu-id="af929-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-240">False</span></span>                                                |
| <span data-ttu-id="af929-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af929-241">Is-Single-Valued</span></span>       | <span data-ttu-id="af929-242">True</span><span class="sxs-lookup"><span data-stu-id="af929-242">True</span></span>                                                 |
| <span data-ttu-id="af929-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af929-243">Is Indexed</span></span>             | <span data-ttu-id="af929-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-244">False</span></span>                                                |
| <span data-ttu-id="af929-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af929-245">In Global Catalog</span></span>      | <span data-ttu-id="af929-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-246">False</span></span>                                                |
| <span data-ttu-id="af929-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af929-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="af929-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af929-248">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="af929-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af929-249">Range-Lower</span></span>            | <span data-ttu-id="af929-250">1</span><span class="sxs-lookup"><span data-stu-id="af929-250">1</span></span>                                                    |
| <span data-ttu-id="af929-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af929-251">Range-Upper</span></span>            | <span data-ttu-id="af929-252">1024</span><span class="sxs-lookup"><span data-stu-id="af929-252">1024</span></span>                                                 |
| <span data-ttu-id="af929-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-253">Search-Flags</span></span>           | <span data-ttu-id="af929-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-254">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-255">System-Flags</span></span>           | <span data-ttu-id="af929-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-256">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af929-257">Classes used in</span></span>        | [<span data-ttu-id="af929-258">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="af929-258">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="af929-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af929-259">Windows Server 2012</span></span>



| <span data-ttu-id="af929-260">Ввод</span><span class="sxs-lookup"><span data-stu-id="af929-260">Entry</span></span> | <span data-ttu-id="af929-261">Значение</span><span class="sxs-lookup"><span data-stu-id="af929-261">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="af929-262">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="af929-262">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="af929-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="af929-263">MAPI-Id</span></span>                | <span data-ttu-id="af929-264">0x8C81</span><span class="sxs-lookup"><span data-stu-id="af929-264">0x8C81</span></span>                                               |
| <span data-ttu-id="af929-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="af929-265">System-Only</span></span>            | <span data-ttu-id="af929-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-266">False</span></span>                                                |
| <span data-ttu-id="af929-267">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="af929-267">Is-Single-Valued</span></span>       | <span data-ttu-id="af929-268">True</span><span class="sxs-lookup"><span data-stu-id="af929-268">True</span></span>                                                 |
| <span data-ttu-id="af929-269">Индексируется</span><span class="sxs-lookup"><span data-stu-id="af929-269">Is Indexed</span></span>             | <span data-ttu-id="af929-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-270">False</span></span>                                                |
| <span data-ttu-id="af929-271">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="af929-271">In Global Catalog</span></span>      | <span data-ttu-id="af929-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="af929-272">False</span></span>                                                |
| <span data-ttu-id="af929-273">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="af929-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="af929-274">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="af929-274">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="af929-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="af929-275">Range-Lower</span></span>            | <span data-ttu-id="af929-276">1</span><span class="sxs-lookup"><span data-stu-id="af929-276">1</span></span>                                                    |
| <span data-ttu-id="af929-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="af929-277">Range-Upper</span></span>            | <span data-ttu-id="af929-278">1024</span><span class="sxs-lookup"><span data-stu-id="af929-278">1024</span></span>                                                 |
| <span data-ttu-id="af929-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-279">Search-Flags</span></span>           | <span data-ttu-id="af929-280">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-280">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="af929-281">System-Flags</span></span>           | <span data-ttu-id="af929-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af929-282">0x00000000</span></span>                                           |
| <span data-ttu-id="af929-283">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="af929-283">Classes used in</span></span>        | [<span data-ttu-id="af929-284">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="af929-284">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





