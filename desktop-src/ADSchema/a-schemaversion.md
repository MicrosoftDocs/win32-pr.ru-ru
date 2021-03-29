---
title: Атрибут Schema-Version
description: Номер версии схемы.
ms.assetid: b937d704-cd76-41fc-84df-5ea614b1785d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Schema-Version
- Схема AD атрибута schemaVersion
topic_type:
- apiref
api_name:
- Schema-Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d00ca6ad8626933b39a82b2288f89454225ed47f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493932"
---
# <a name="schema-version-attribute"></a><span data-ttu-id="2b9a1-105">Атрибут Schema-Version</span><span class="sxs-lookup"><span data-stu-id="2b9a1-105">Schema-Version attribute</span></span>

<span data-ttu-id="2b9a1-106">Номер версии схемы.</span><span class="sxs-lookup"><span data-stu-id="2b9a1-106">The version number for the schema.</span></span>



| <span data-ttu-id="2b9a1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-107">Entry</span></span> | <span data-ttu-id="2b9a1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2b9a1-109">CN</span><span class="sxs-lookup"><span data-stu-id="2b9a1-109">CN</span></span>                | <span data-ttu-id="2b9a1-110">Schema-Version</span><span class="sxs-lookup"><span data-stu-id="2b9a1-110">Schema-Version</span></span>                       |
| <span data-ttu-id="2b9a1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2b9a1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2b9a1-112">schemaVersion</span><span class="sxs-lookup"><span data-stu-id="2b9a1-112">schemaVersion</span></span>                        |
| <span data-ttu-id="2b9a1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2b9a1-113">Size</span></span>              | <span data-ttu-id="2b9a1-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="2b9a1-114">4 bytes</span></span>                              |
| <span data-ttu-id="2b9a1-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2b9a1-115">Update Privilege</span></span>  | <span data-ttu-id="2b9a1-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="2b9a1-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="2b9a1-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2b9a1-117">Update Frequency</span></span>  | <span data-ttu-id="2b9a1-118">Каждый раз при освобождении схемы.</span><span class="sxs-lookup"><span data-stu-id="2b9a1-118">Each time the schema is released.</span></span>    |
| <span data-ttu-id="2b9a1-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-119">Attribute-Id</span></span>      | <span data-ttu-id="2b9a1-120">1.2.840.113556.1.2.471</span><span class="sxs-lookup"><span data-stu-id="2b9a1-120">1.2.840.113556.1.2.471</span></span>               |
| <span data-ttu-id="2b9a1-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2b9a1-121">System-Id-Guid</span></span>    | <span data-ttu-id="2b9a1-122">bf967a2c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2b9a1-122">bf967a2c-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="2b9a1-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b9a1-123">Syntax</span></span>            | [<span data-ttu-id="2b9a1-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2b9a1-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2b9a1-125">Implementations</span></span>

-   [<span data-ttu-id="2b9a1-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b9a1-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b9a1-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2b9a1-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b9a1-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b9a1-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b9a1-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b9a1-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b9a1-133">Windows 2000 Server</span></span>



| <span data-ttu-id="2b9a1-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-134">Entry</span></span> | <span data-ttu-id="2b9a1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-137">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-138">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-138">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-139">System-Only</span></span>            | <span data-ttu-id="2b9a1-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-140">False</span></span>                                       |
| <span data-ttu-id="2b9a1-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-141">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-142">False</span></span>                                       |
| <span data-ttu-id="2b9a1-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-143">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-144">False</span></span>                                       |
| <span data-ttu-id="2b9a1-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-145">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-146">False</span></span>                                       |
| <span data-ttu-id="2b9a1-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-148">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-149">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-150">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-151">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-152">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-153">System-Flags</span></span>           | <span data-ttu-id="2b9a1-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-154">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-155">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-156">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-156">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b9a1-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b9a1-157">Windows Server 2003</span></span>



| <span data-ttu-id="2b9a1-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-158">Entry</span></span> | <span data-ttu-id="2b9a1-159">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-159">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-160">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-161">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-162">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-162">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-163">System-Only</span></span>            | <span data-ttu-id="2b9a1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-164">False</span></span>                                       |
| <span data-ttu-id="2b9a1-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-165">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-166">False</span></span>                                       |
| <span data-ttu-id="2b9a1-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-167">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-168">False</span></span>                                       |
| <span data-ttu-id="2b9a1-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-169">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-170">False</span></span>                                       |
| <span data-ttu-id="2b9a1-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-172">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-173">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-174">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-175">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-176">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-177">System-Flags</span></span>           | <span data-ttu-id="2b9a1-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-178">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-179">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-180">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-180">**Container**</span></span>](c-container.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2b9a1-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="2b9a1-181">ADAM</span></span>



| <span data-ttu-id="2b9a1-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-182">Entry</span></span> | <span data-ttu-id="2b9a1-183">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-183">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-184">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-185">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-186">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-186">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-187">System-Only</span></span>            | <span data-ttu-id="2b9a1-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-188">False</span></span>                                       |
| <span data-ttu-id="2b9a1-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-189">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-190">False</span></span>                                       |
| <span data-ttu-id="2b9a1-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-191">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-192">False</span></span>                                       |
| <span data-ttu-id="2b9a1-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-193">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-194">False</span></span>                                       |
| <span data-ttu-id="2b9a1-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-196">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-197">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-198">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-199">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-200">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-201">System-Flags</span></span>           | <span data-ttu-id="2b9a1-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-202">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-203">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-204">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-204">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b9a1-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b9a1-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b9a1-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-206">Entry</span></span> | <span data-ttu-id="2b9a1-207">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-207">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-208">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-209">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-210">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-210">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-211">System-Only</span></span>            | <span data-ttu-id="2b9a1-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-212">False</span></span>                                       |
| <span data-ttu-id="2b9a1-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-213">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-214">False</span></span>                                       |
| <span data-ttu-id="2b9a1-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-215">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-216">False</span></span>                                       |
| <span data-ttu-id="2b9a1-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-217">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-218">False</span></span>                                       |
| <span data-ttu-id="2b9a1-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-220">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-221">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-222">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-223">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-224">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-225">System-Flags</span></span>           | <span data-ttu-id="2b9a1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-226">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-227">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-228">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-228">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b9a1-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b9a1-229">Windows Server 2008</span></span>



| <span data-ttu-id="2b9a1-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-230">Entry</span></span> | <span data-ttu-id="2b9a1-231">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-231">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-232">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-233">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-234">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-234">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-235">System-Only</span></span>            | <span data-ttu-id="2b9a1-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-236">False</span></span>                                       |
| <span data-ttu-id="2b9a1-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-237">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-238">False</span></span>                                       |
| <span data-ttu-id="2b9a1-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-239">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-240">False</span></span>                                       |
| <span data-ttu-id="2b9a1-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-241">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-242">False</span></span>                                       |
| <span data-ttu-id="2b9a1-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-244">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-245">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-246">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-247">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-248">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-249">System-Flags</span></span>           | <span data-ttu-id="2b9a1-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-250">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-251">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-252">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-252">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b9a1-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b9a1-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b9a1-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-254">Entry</span></span> | <span data-ttu-id="2b9a1-255">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-255">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-256">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-257">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-258">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-258">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-259">System-Only</span></span>            | <span data-ttu-id="2b9a1-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-260">False</span></span>                                       |
| <span data-ttu-id="2b9a1-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-262">False</span></span>                                       |
| <span data-ttu-id="2b9a1-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-263">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-264">False</span></span>                                       |
| <span data-ttu-id="2b9a1-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-265">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-266">False</span></span>                                       |
| <span data-ttu-id="2b9a1-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-268">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-269">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-270">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-271">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-272">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-273">System-Flags</span></span>           | <span data-ttu-id="2b9a1-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-274">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-275">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-276">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-276">**Container**</span></span>](c-container.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b9a1-277">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b9a1-277">Windows Server 2012</span></span>



| <span data-ttu-id="2b9a1-278">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b9a1-278">Entry</span></span> | <span data-ttu-id="2b9a1-279">Значение</span><span class="sxs-lookup"><span data-stu-id="2b9a1-279">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="2b9a1-280">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b9a1-280">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="2b9a1-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b9a1-281">MAPI-Id</span></span>                | <span data-ttu-id="2b9a1-282">0x817C</span><span class="sxs-lookup"><span data-stu-id="2b9a1-282">0x817C</span></span>                                      |
| <span data-ttu-id="2b9a1-283">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b9a1-283">System-Only</span></span>            | <span data-ttu-id="2b9a1-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-284">False</span></span>                                       |
| <span data-ttu-id="2b9a1-285">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b9a1-285">Is-Single-Valued</span></span>       | <span data-ttu-id="2b9a1-286">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-286">False</span></span>                                       |
| <span data-ttu-id="2b9a1-287">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b9a1-287">Is Indexed</span></span>             | <span data-ttu-id="2b9a1-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-288">False</span></span>                                       |
| <span data-ttu-id="2b9a1-289">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b9a1-289">In Global Catalog</span></span>      | <span data-ttu-id="2b9a1-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b9a1-290">False</span></span>                                       |
| <span data-ttu-id="2b9a1-291">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b9a1-291">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b9a1-292">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b9a1-292">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="2b9a1-293">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b9a1-293">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-294">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b9a1-294">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="2b9a1-295">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-295">Search-Flags</span></span>           | <span data-ttu-id="2b9a1-296">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b9a1-296">0x00000000</span></span>                                  |
| <span data-ttu-id="2b9a1-297">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b9a1-297">System-Flags</span></span>           | <span data-ttu-id="2b9a1-298">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b9a1-298">0x00000010</span></span>                                  |
| <span data-ttu-id="2b9a1-299">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b9a1-299">Classes used in</span></span>        | [<span data-ttu-id="2b9a1-300">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="2b9a1-300">**Container**</span></span>](c-container.md)<br/> |



 

 





