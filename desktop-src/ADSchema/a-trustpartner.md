---
title: Атрибут Trust-Partner
description: Имя домена, с которым существует доверие.
ms.assetid: 0b7c8e78-614b-46dd-8616-40d75b461639
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Trust-Partner
- Схема AD атрибута Трустпартнер
topic_type:
- apiref
api_name:
- Trust-Partner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201a89e178515b270302b4d8541af64a63ad6813
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138442"
---
# <a name="trust-partner-attribute"></a><span data-ttu-id="819af-105">Атрибут Trust-Partner</span><span class="sxs-lookup"><span data-stu-id="819af-105">Trust-Partner attribute</span></span>

<span data-ttu-id="819af-106">Имя домена, с которым существует доверие.</span><span class="sxs-lookup"><span data-stu-id="819af-106">The name of the domain with which a trust exists.</span></span>



| <span data-ttu-id="819af-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-107">Entry</span></span> | <span data-ttu-id="819af-108">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="819af-109">CN</span><span class="sxs-lookup"><span data-stu-id="819af-109">CN</span></span>                | <span data-ttu-id="819af-110">Trust-Partner</span><span class="sxs-lookup"><span data-stu-id="819af-110">Trust-Partner</span></span>                               |
| <span data-ttu-id="819af-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="819af-111">Ldap-Display-Name</span></span> | <span data-ttu-id="819af-112">трустпартнер</span><span class="sxs-lookup"><span data-stu-id="819af-112">trustPartner</span></span>                                |
| <span data-ttu-id="819af-113">Размер</span><span class="sxs-lookup"><span data-stu-id="819af-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="819af-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="819af-114">Update Privilege</span></span>  | <span data-ttu-id="819af-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="819af-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="819af-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="819af-116">Update Frequency</span></span>  | <span data-ttu-id="819af-117">При создании нового доверия.</span><span class="sxs-lookup"><span data-stu-id="819af-117">When a new trust is created.</span></span>                |
| <span data-ttu-id="819af-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="819af-118">Attribute-Id</span></span>      | <span data-ttu-id="819af-119">1.2.840.113556.1.4.133</span><span class="sxs-lookup"><span data-stu-id="819af-119">1.2.840.113556.1.4.133</span></span>                      |
| <span data-ttu-id="819af-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="819af-120">System-Id-Guid</span></span>    | <span data-ttu-id="819af-121">bf967a5d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="819af-121">bf967a5d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="819af-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="819af-122">Syntax</span></span>            | [<span data-ttu-id="819af-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="819af-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="819af-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="819af-124">Implementations</span></span>

-   [<span data-ttu-id="819af-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="819af-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="819af-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="819af-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="819af-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="819af-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="819af-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="819af-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="819af-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="819af-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="819af-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="819af-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="819af-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="819af-131">Windows 2000 Server</span></span>



| <span data-ttu-id="819af-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-132">Entry</span></span> | <span data-ttu-id="819af-133">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="819af-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="819af-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="819af-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="819af-136">System-Only</span></span>            | <span data-ttu-id="819af-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-137">False</span></span>                                                |
| <span data-ttu-id="819af-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="819af-138">Is-Single-Valued</span></span>       | <span data-ttu-id="819af-139">True</span><span class="sxs-lookup"><span data-stu-id="819af-139">True</span></span>                                                 |
| <span data-ttu-id="819af-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="819af-140">Is Indexed</span></span>             | <span data-ttu-id="819af-141">True</span><span class="sxs-lookup"><span data-stu-id="819af-141">True</span></span>                                                 |
| <span data-ttu-id="819af-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="819af-142">In Global Catalog</span></span>      | <span data-ttu-id="819af-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-143">False</span></span>                                                |
| <span data-ttu-id="819af-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="819af-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="819af-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="819af-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="819af-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="819af-146">Range-Lower</span></span>            | <span data-ttu-id="819af-147">1</span><span class="sxs-lookup"><span data-stu-id="819af-147">1</span></span>                                                    |
| <span data-ttu-id="819af-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="819af-148">Range-Upper</span></span>            | <span data-ttu-id="819af-149">1024</span><span class="sxs-lookup"><span data-stu-id="819af-149">1024</span></span>                                                 |
| <span data-ttu-id="819af-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-150">Search-Flags</span></span>           | <span data-ttu-id="819af-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="819af-151">0x00000001</span></span>                                           |
| <span data-ttu-id="819af-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-152">System-Flags</span></span>           | <span data-ttu-id="819af-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="819af-153">0x00000010</span></span>                                           |
| <span data-ttu-id="819af-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="819af-154">Classes used in</span></span>        | [<span data-ttu-id="819af-155">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="819af-155">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="819af-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="819af-156">Windows Server 2003</span></span>



| <span data-ttu-id="819af-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-157">Entry</span></span> | <span data-ttu-id="819af-158">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-158">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="819af-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="819af-159">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="819af-160">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="819af-161">System-Only</span></span>            | <span data-ttu-id="819af-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-162">False</span></span>                                                |
| <span data-ttu-id="819af-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="819af-163">Is-Single-Valued</span></span>       | <span data-ttu-id="819af-164">True</span><span class="sxs-lookup"><span data-stu-id="819af-164">True</span></span>                                                 |
| <span data-ttu-id="819af-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="819af-165">Is Indexed</span></span>             | <span data-ttu-id="819af-166">True</span><span class="sxs-lookup"><span data-stu-id="819af-166">True</span></span>                                                 |
| <span data-ttu-id="819af-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="819af-167">In Global Catalog</span></span>      | <span data-ttu-id="819af-168">True</span><span class="sxs-lookup"><span data-stu-id="819af-168">True</span></span>                                                 |
| <span data-ttu-id="819af-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="819af-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="819af-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="819af-170">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="819af-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="819af-171">Range-Lower</span></span>            | <span data-ttu-id="819af-172">1</span><span class="sxs-lookup"><span data-stu-id="819af-172">1</span></span>                                                    |
| <span data-ttu-id="819af-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="819af-173">Range-Upper</span></span>            | <span data-ttu-id="819af-174">1024</span><span class="sxs-lookup"><span data-stu-id="819af-174">1024</span></span>                                                 |
| <span data-ttu-id="819af-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-175">Search-Flags</span></span>           | <span data-ttu-id="819af-176">0x00000001</span><span class="sxs-lookup"><span data-stu-id="819af-176">0x00000001</span></span>                                           |
| <span data-ttu-id="819af-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-177">System-Flags</span></span>           | <span data-ttu-id="819af-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="819af-178">0x00000010</span></span>                                           |
| <span data-ttu-id="819af-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="819af-179">Classes used in</span></span>        | [<span data-ttu-id="819af-180">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="819af-180">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="819af-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="819af-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="819af-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-182">Entry</span></span> | <span data-ttu-id="819af-183">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-183">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="819af-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="819af-184">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="819af-185">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="819af-186">System-Only</span></span>            | <span data-ttu-id="819af-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-187">False</span></span>                                                |
| <span data-ttu-id="819af-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="819af-188">Is-Single-Valued</span></span>       | <span data-ttu-id="819af-189">True</span><span class="sxs-lookup"><span data-stu-id="819af-189">True</span></span>                                                 |
| <span data-ttu-id="819af-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="819af-190">Is Indexed</span></span>             | <span data-ttu-id="819af-191">True</span><span class="sxs-lookup"><span data-stu-id="819af-191">True</span></span>                                                 |
| <span data-ttu-id="819af-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="819af-192">In Global Catalog</span></span>      | <span data-ttu-id="819af-193">True</span><span class="sxs-lookup"><span data-stu-id="819af-193">True</span></span>                                                 |
| <span data-ttu-id="819af-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="819af-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="819af-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="819af-195">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="819af-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="819af-196">Range-Lower</span></span>            | <span data-ttu-id="819af-197">1</span><span class="sxs-lookup"><span data-stu-id="819af-197">1</span></span>                                                    |
| <span data-ttu-id="819af-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="819af-198">Range-Upper</span></span>            | <span data-ttu-id="819af-199">1024</span><span class="sxs-lookup"><span data-stu-id="819af-199">1024</span></span>                                                 |
| <span data-ttu-id="819af-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-200">Search-Flags</span></span>           | <span data-ttu-id="819af-201">0x00000001</span><span class="sxs-lookup"><span data-stu-id="819af-201">0x00000001</span></span>                                           |
| <span data-ttu-id="819af-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-202">System-Flags</span></span>           | <span data-ttu-id="819af-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="819af-203">0x00000010</span></span>                                           |
| <span data-ttu-id="819af-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="819af-204">Classes used in</span></span>        | [<span data-ttu-id="819af-205">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="819af-205">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="819af-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="819af-206">Windows Server 2008</span></span>



| <span data-ttu-id="819af-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-207">Entry</span></span> | <span data-ttu-id="819af-208">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-208">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="819af-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="819af-209">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="819af-210">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="819af-211">System-Only</span></span>            | <span data-ttu-id="819af-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-212">False</span></span>                                                |
| <span data-ttu-id="819af-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="819af-213">Is-Single-Valued</span></span>       | <span data-ttu-id="819af-214">True</span><span class="sxs-lookup"><span data-stu-id="819af-214">True</span></span>                                                 |
| <span data-ttu-id="819af-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="819af-215">Is Indexed</span></span>             | <span data-ttu-id="819af-216">True</span><span class="sxs-lookup"><span data-stu-id="819af-216">True</span></span>                                                 |
| <span data-ttu-id="819af-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="819af-217">In Global Catalog</span></span>      | <span data-ttu-id="819af-218">True</span><span class="sxs-lookup"><span data-stu-id="819af-218">True</span></span>                                                 |
| <span data-ttu-id="819af-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="819af-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="819af-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="819af-220">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="819af-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="819af-221">Range-Lower</span></span>            | <span data-ttu-id="819af-222">1</span><span class="sxs-lookup"><span data-stu-id="819af-222">1</span></span>                                                    |
| <span data-ttu-id="819af-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="819af-223">Range-Upper</span></span>            | <span data-ttu-id="819af-224">1024</span><span class="sxs-lookup"><span data-stu-id="819af-224">1024</span></span>                                                 |
| <span data-ttu-id="819af-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-225">Search-Flags</span></span>           | <span data-ttu-id="819af-226">0x00000001</span><span class="sxs-lookup"><span data-stu-id="819af-226">0x00000001</span></span>                                           |
| <span data-ttu-id="819af-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-227">System-Flags</span></span>           | <span data-ttu-id="819af-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="819af-228">0x00000010</span></span>                                           |
| <span data-ttu-id="819af-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="819af-229">Classes used in</span></span>        | [<span data-ttu-id="819af-230">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="819af-230">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="819af-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="819af-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="819af-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-232">Entry</span></span> | <span data-ttu-id="819af-233">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-233">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="819af-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="819af-234">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="819af-235">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="819af-236">System-Only</span></span>            | <span data-ttu-id="819af-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-237">False</span></span>                                                |
| <span data-ttu-id="819af-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="819af-238">Is-Single-Valued</span></span>       | <span data-ttu-id="819af-239">True</span><span class="sxs-lookup"><span data-stu-id="819af-239">True</span></span>                                                 |
| <span data-ttu-id="819af-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="819af-240">Is Indexed</span></span>             | <span data-ttu-id="819af-241">True</span><span class="sxs-lookup"><span data-stu-id="819af-241">True</span></span>                                                 |
| <span data-ttu-id="819af-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="819af-242">In Global Catalog</span></span>      | <span data-ttu-id="819af-243">True</span><span class="sxs-lookup"><span data-stu-id="819af-243">True</span></span>                                                 |
| <span data-ttu-id="819af-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="819af-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="819af-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="819af-245">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="819af-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="819af-246">Range-Lower</span></span>            | <span data-ttu-id="819af-247">1</span><span class="sxs-lookup"><span data-stu-id="819af-247">1</span></span>                                                    |
| <span data-ttu-id="819af-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="819af-248">Range-Upper</span></span>            | <span data-ttu-id="819af-249">1024</span><span class="sxs-lookup"><span data-stu-id="819af-249">1024</span></span>                                                 |
| <span data-ttu-id="819af-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-250">Search-Flags</span></span>           | <span data-ttu-id="819af-251">0x00000001</span><span class="sxs-lookup"><span data-stu-id="819af-251">0x00000001</span></span>                                           |
| <span data-ttu-id="819af-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-252">System-Flags</span></span>           | <span data-ttu-id="819af-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="819af-253">0x00000010</span></span>                                           |
| <span data-ttu-id="819af-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="819af-254">Classes used in</span></span>        | [<span data-ttu-id="819af-255">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="819af-255">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="819af-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="819af-256">Windows Server 2012</span></span>



| <span data-ttu-id="819af-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="819af-257">Entry</span></span> | <span data-ttu-id="819af-258">Значение</span><span class="sxs-lookup"><span data-stu-id="819af-258">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="819af-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="819af-259">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="819af-260">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="819af-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="819af-261">System-Only</span></span>            | <span data-ttu-id="819af-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="819af-262">False</span></span>                                                |
| <span data-ttu-id="819af-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="819af-263">Is-Single-Valued</span></span>       | <span data-ttu-id="819af-264">True</span><span class="sxs-lookup"><span data-stu-id="819af-264">True</span></span>                                                 |
| <span data-ttu-id="819af-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="819af-265">Is Indexed</span></span>             | <span data-ttu-id="819af-266">True</span><span class="sxs-lookup"><span data-stu-id="819af-266">True</span></span>                                                 |
| <span data-ttu-id="819af-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="819af-267">In Global Catalog</span></span>      | <span data-ttu-id="819af-268">True</span><span class="sxs-lookup"><span data-stu-id="819af-268">True</span></span>                                                 |
| <span data-ttu-id="819af-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="819af-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="819af-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="819af-270">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="819af-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="819af-271">Range-Lower</span></span>            | <span data-ttu-id="819af-272">1</span><span class="sxs-lookup"><span data-stu-id="819af-272">1</span></span>                                                    |
| <span data-ttu-id="819af-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="819af-273">Range-Upper</span></span>            | <span data-ttu-id="819af-274">1024</span><span class="sxs-lookup"><span data-stu-id="819af-274">1024</span></span>                                                 |
| <span data-ttu-id="819af-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-275">Search-Flags</span></span>           | <span data-ttu-id="819af-276">0x00000001</span><span class="sxs-lookup"><span data-stu-id="819af-276">0x00000001</span></span>                                           |
| <span data-ttu-id="819af-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="819af-277">System-Flags</span></span>           | <span data-ttu-id="819af-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="819af-278">0x00000010</span></span>                                           |
| <span data-ttu-id="819af-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="819af-279">Classes used in</span></span>        | [<span data-ttu-id="819af-280">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="819af-280">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





