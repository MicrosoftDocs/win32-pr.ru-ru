---
title: Атрибут DIT-Content-Rules
description: Это указывает допустимое содержимое записей определенного класса структурного объекта с помощью идентификации необязательного набора вспомогательных классов объектов, обязательных, необязательных и исключенных атрибутов.
ms.assetid: 75550f5c-efbf-4cd9-8619-a69d2b462f13
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута DIT-Content-Rules
- Схема AD атрибута Дитконтентрулес
topic_type:
- apiref
api_name:
- DIT-Content-Rules
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399529237cb7a9f2c4bf1803255f546184ad47f3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139042"
---
# <a name="dit-content-rules-attribute"></a><span data-ttu-id="b57dd-105">Атрибут DIT-Content-Rules</span><span class="sxs-lookup"><span data-stu-id="b57dd-105">DIT-Content-Rules attribute</span></span>

<span data-ttu-id="b57dd-106">Это указывает допустимое содержимое записей определенного класса структурного объекта с помощью идентификации необязательного набора вспомогательных классов объектов, обязательных, необязательных и исключенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b57dd-106">This specifies the permissible content of entries of a particular structural object class by using the identification of an optional set of auxiliary object classes, and mandatory, optional, and precluded attributes.</span></span> <span data-ttu-id="b57dd-107">Коллективные атрибуты включены в правила DIT-Content-Rules, как определено в RFC 2251.</span><span class="sxs-lookup"><span data-stu-id="b57dd-107">Collective attributes are included in DIT-Content-Rules as defined in RFC 2251.</span></span>



| <span data-ttu-id="b57dd-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-108">Entry</span></span> | <span data-ttu-id="b57dd-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-110">CN</span><span class="sxs-lookup"><span data-stu-id="b57dd-110">CN</span></span>                | <span data-ttu-id="b57dd-111">DIT-Content-правила</span><span class="sxs-lookup"><span data-stu-id="b57dd-111">DIT-Content-Rules</span></span>                           |
| <span data-ttu-id="b57dd-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b57dd-112">Ldap-Display-Name</span></span> | <span data-ttu-id="b57dd-113">дитконтентрулес</span><span class="sxs-lookup"><span data-stu-id="b57dd-113">dITContentRules</span></span>                             |
| <span data-ttu-id="b57dd-114">Размер</span><span class="sxs-lookup"><span data-stu-id="b57dd-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="b57dd-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b57dd-115">Update Privilege</span></span>  | <span data-ttu-id="b57dd-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b57dd-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="b57dd-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b57dd-117">Update Frequency</span></span>  | <span data-ttu-id="b57dd-118">При создании нового класса.</span><span class="sxs-lookup"><span data-stu-id="b57dd-118">Whenever a new class is created.</span></span>            |
| <span data-ttu-id="b57dd-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-119">Attribute-Id</span></span>      | <span data-ttu-id="b57dd-120">2.5.21.2</span><span class="sxs-lookup"><span data-stu-id="b57dd-120">2.5.21.2</span></span>                                    |
| <span data-ttu-id="b57dd-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b57dd-121">System-Id-Guid</span></span>    | <span data-ttu-id="b57dd-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b57dd-122">9a7ad946-ca53-11d1-bbd0-0080c76670c0</span></span>        |
| <span data-ttu-id="b57dd-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b57dd-123">Syntax</span></span>            | [<span data-ttu-id="b57dd-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b57dd-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="b57dd-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b57dd-125">Implementations</span></span>

-   [<span data-ttu-id="b57dd-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b57dd-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b57dd-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b57dd-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b57dd-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b57dd-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b57dd-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b57dd-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b57dd-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b57dd-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b57dd-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b57dd-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b57dd-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b57dd-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b57dd-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b57dd-133">Windows 2000 Server</span></span>



| <span data-ttu-id="b57dd-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-134">Entry</span></span> | <span data-ttu-id="b57dd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-135">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-136">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-137">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-138">System-Only</span></span>            | <span data-ttu-id="b57dd-139">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-139">True</span></span>                                        |
| <span data-ttu-id="b57dd-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-141">False</span></span>                                       |
| <span data-ttu-id="b57dd-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-142">Is Indexed</span></span>             | <span data-ttu-id="b57dd-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-143">False</span></span>                                       |
| <span data-ttu-id="b57dd-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-144">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-145">False</span></span>                                       |
| <span data-ttu-id="b57dd-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-147">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-148">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-149">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-150">Search-Flags</span></span>           | <span data-ttu-id="b57dd-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-151">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-152">System-Flags</span></span>           | <span data-ttu-id="b57dd-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-153">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-154">Classes used in</span></span>        | [<span data-ttu-id="b57dd-155">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-155">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b57dd-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b57dd-156">Windows Server 2003</span></span>



| <span data-ttu-id="b57dd-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-157">Entry</span></span> | <span data-ttu-id="b57dd-158">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-158">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-159">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-160">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-161">System-Only</span></span>            | <span data-ttu-id="b57dd-162">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-162">True</span></span>                                        |
| <span data-ttu-id="b57dd-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-163">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-164">False</span></span>                                       |
| <span data-ttu-id="b57dd-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-165">Is Indexed</span></span>             | <span data-ttu-id="b57dd-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-166">False</span></span>                                       |
| <span data-ttu-id="b57dd-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-167">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-168">False</span></span>                                       |
| <span data-ttu-id="b57dd-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-170">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-171">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-172">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-173">Search-Flags</span></span>           | <span data-ttu-id="b57dd-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-174">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-175">System-Flags</span></span>           | <span data-ttu-id="b57dd-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-176">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-177">Classes used in</span></span>        | [<span data-ttu-id="b57dd-178">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-178">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b57dd-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="b57dd-179">ADAM</span></span>



| <span data-ttu-id="b57dd-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-180">Entry</span></span> | <span data-ttu-id="b57dd-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-181">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-182">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-183">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-184">System-Only</span></span>            | <span data-ttu-id="b57dd-185">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-185">True</span></span>                                        |
| <span data-ttu-id="b57dd-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-187">False</span></span>                                       |
| <span data-ttu-id="b57dd-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-188">Is Indexed</span></span>             | <span data-ttu-id="b57dd-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-189">False</span></span>                                       |
| <span data-ttu-id="b57dd-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-190">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-191">False</span></span>                                       |
| <span data-ttu-id="b57dd-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-193">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-194">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-195">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-196">Search-Flags</span></span>           | <span data-ttu-id="b57dd-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-197">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-198">System-Flags</span></span>           | <span data-ttu-id="b57dd-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-199">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-200">Classes used in</span></span>        | [<span data-ttu-id="b57dd-201">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-201">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b57dd-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b57dd-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b57dd-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-203">Entry</span></span> | <span data-ttu-id="b57dd-204">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-204">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-205">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-206">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-207">System-Only</span></span>            | <span data-ttu-id="b57dd-208">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-208">True</span></span>                                        |
| <span data-ttu-id="b57dd-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-209">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-210">False</span></span>                                       |
| <span data-ttu-id="b57dd-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-211">Is Indexed</span></span>             | <span data-ttu-id="b57dd-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-212">False</span></span>                                       |
| <span data-ttu-id="b57dd-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-213">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-214">False</span></span>                                       |
| <span data-ttu-id="b57dd-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-216">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-217">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-218">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-219">Search-Flags</span></span>           | <span data-ttu-id="b57dd-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-220">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-221">System-Flags</span></span>           | <span data-ttu-id="b57dd-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-222">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-223">Classes used in</span></span>        | [<span data-ttu-id="b57dd-224">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-224">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b57dd-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b57dd-225">Windows Server 2008</span></span>



| <span data-ttu-id="b57dd-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-226">Entry</span></span> | <span data-ttu-id="b57dd-227">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-227">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-228">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-229">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-230">System-Only</span></span>            | <span data-ttu-id="b57dd-231">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-231">True</span></span>                                        |
| <span data-ttu-id="b57dd-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-232">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-233">False</span></span>                                       |
| <span data-ttu-id="b57dd-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-234">Is Indexed</span></span>             | <span data-ttu-id="b57dd-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-235">False</span></span>                                       |
| <span data-ttu-id="b57dd-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-236">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-237">False</span></span>                                       |
| <span data-ttu-id="b57dd-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-239">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-240">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-241">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-242">Search-Flags</span></span>           | <span data-ttu-id="b57dd-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-243">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-244">System-Flags</span></span>           | <span data-ttu-id="b57dd-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-245">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-246">Classes used in</span></span>        | [<span data-ttu-id="b57dd-247">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-247">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b57dd-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b57dd-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b57dd-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-249">Entry</span></span> | <span data-ttu-id="b57dd-250">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-250">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-251">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-252">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-253">System-Only</span></span>            | <span data-ttu-id="b57dd-254">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-254">True</span></span>                                        |
| <span data-ttu-id="b57dd-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-255">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-256">False</span></span>                                       |
| <span data-ttu-id="b57dd-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-257">Is Indexed</span></span>             | <span data-ttu-id="b57dd-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-258">False</span></span>                                       |
| <span data-ttu-id="b57dd-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-259">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-260">False</span></span>                                       |
| <span data-ttu-id="b57dd-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-262">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-263">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-264">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-265">Search-Flags</span></span>           | <span data-ttu-id="b57dd-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-266">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-267">System-Flags</span></span>           | <span data-ttu-id="b57dd-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-268">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-269">Classes used in</span></span>        | [<span data-ttu-id="b57dd-270">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-270">**SubSchema**</span></span>](c-subschema.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b57dd-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b57dd-271">Windows Server 2012</span></span>



| <span data-ttu-id="b57dd-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="b57dd-272">Entry</span></span> | <span data-ttu-id="b57dd-273">Значение</span><span class="sxs-lookup"><span data-stu-id="b57dd-273">Value</span></span> |
|------------------------|---------------------------------------------|
| <span data-ttu-id="b57dd-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b57dd-274">Link-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b57dd-275">MAPI-Id</span></span>                | \-                                          |
| <span data-ttu-id="b57dd-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="b57dd-276">System-Only</span></span>            | <span data-ttu-id="b57dd-277">True</span><span class="sxs-lookup"><span data-stu-id="b57dd-277">True</span></span>                                        |
| <span data-ttu-id="b57dd-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b57dd-278">Is-Single-Valued</span></span>       | <span data-ttu-id="b57dd-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-279">False</span></span>                                       |
| <span data-ttu-id="b57dd-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b57dd-280">Is Indexed</span></span>             | <span data-ttu-id="b57dd-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-281">False</span></span>                                       |
| <span data-ttu-id="b57dd-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b57dd-282">In Global Catalog</span></span>      | <span data-ttu-id="b57dd-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="b57dd-283">False</span></span>                                       |
| <span data-ttu-id="b57dd-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b57dd-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="b57dd-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b57dd-285">O:BAG:BAD:S:</span></span>                                |
| <span data-ttu-id="b57dd-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b57dd-286">Range-Lower</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b57dd-287">Range-Upper</span></span>            | \-                                          |
| <span data-ttu-id="b57dd-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-288">Search-Flags</span></span>           | <span data-ttu-id="b57dd-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b57dd-289">0x00000000</span></span>                                  |
| <span data-ttu-id="b57dd-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b57dd-290">System-Flags</span></span>           | <span data-ttu-id="b57dd-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b57dd-291">0x08000014</span></span>                                  |
| <span data-ttu-id="b57dd-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b57dd-292">Classes used in</span></span>        | [<span data-ttu-id="b57dd-293">**Подсхема**</span><span class="sxs-lookup"><span data-stu-id="b57dd-293">**SubSchema**</span></span>](c-subschema.md)<br/> |



 

 





