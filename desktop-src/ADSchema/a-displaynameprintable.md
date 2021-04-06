---
title: Отображаемое имя — атрибут, поддерживающий печать
description: Отображаемое имя для печати объекта.
ms.assetid: e8e5ff25-66dd-4c74-9571-9ec765d6d1af
ms.tgt_platform: multiple
keywords:
- Отображаемое имя — схема AD атрибута, поддерживающая печать
- Схема AD атрибута Дисплайнамепринтабле
topic_type:
- apiref
api_name:
- Display-Name-Printable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eff05c2279f026e3a94b707b522509b4801ff27
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893922"
---
# <a name="display-name-printable-attribute"></a><span data-ttu-id="bf706-105">Отображаемое имя — атрибут, поддерживающий печать</span><span class="sxs-lookup"><span data-stu-id="bf706-105">Display-Name-Printable attribute</span></span>

<span data-ttu-id="bf706-106">Отображаемое имя для печати объекта.</span><span class="sxs-lookup"><span data-stu-id="bf706-106">The printable display name for an object.</span></span> <span data-ttu-id="bf706-107">Отображаемое имя для печати обычно представляет собой сочетание имени, отчество и фамилии пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf706-107">The printable display name is usually the combination of the user's first name, middle initial, and last name.</span></span>



| <span data-ttu-id="bf706-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-108">Entry</span></span> | <span data-ttu-id="bf706-109">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-109">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="bf706-110">CN</span><span class="sxs-lookup"><span data-stu-id="bf706-110">CN</span></span>                | <span data-ttu-id="bf706-111">Отображаемое имя — печатаемое</span><span class="sxs-lookup"><span data-stu-id="bf706-111">Display-Name-Printable</span></span>                 |
| <span data-ttu-id="bf706-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bf706-112">Ldap-Display-Name</span></span> | <span data-ttu-id="bf706-113">дисплайнамепринтабле</span><span class="sxs-lookup"><span data-stu-id="bf706-113">displayNamePrintable</span></span>                   |
| <span data-ttu-id="bf706-114">Размер</span><span class="sxs-lookup"><span data-stu-id="bf706-114">Size</span></span>              | \-                                     |
| <span data-ttu-id="bf706-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bf706-115">Update Privilege</span></span>  | <span data-ttu-id="bf706-116">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="bf706-116">Domain administrator or account owner.</span></span> |
| <span data-ttu-id="bf706-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bf706-117">Update Frequency</span></span>  | \-                                     |
| <span data-ttu-id="bf706-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-118">Attribute-Id</span></span>      | <span data-ttu-id="bf706-119">1.2.840.113556.1.2.353</span><span class="sxs-lookup"><span data-stu-id="bf706-119">1.2.840.113556.1.2.353</span></span>                 |
| <span data-ttu-id="bf706-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bf706-120">System-Id-Guid</span></span>    | <span data-ttu-id="bf706-121">bf967954-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bf706-121">bf967954-0de6-11d0-a285-00aa003049e2</span></span>   |
| <span data-ttu-id="bf706-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf706-122">Syntax</span></span>            | [<span data-ttu-id="bf706-123">**String(IA5)**</span><span class="sxs-lookup"><span data-stu-id="bf706-123">**String(IA5)**</span></span>](s-string-ia5.md)    |



## <a name="implementations"></a><span data-ttu-id="bf706-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bf706-124">Implementations</span></span>

-   [<span data-ttu-id="bf706-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bf706-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bf706-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf706-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf706-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf706-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf706-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf706-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf706-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf706-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf706-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf706-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bf706-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf706-131">Windows 2000 Server</span></span>



| <span data-ttu-id="bf706-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-132">Entry</span></span> | <span data-ttu-id="bf706-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-133">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bf706-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf706-134">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bf706-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-135">MAPI-Id</span></span>                | <span data-ttu-id="bf706-136">0x39FF</span><span class="sxs-lookup"><span data-stu-id="bf706-136">0x39FF</span></span>                          |
| <span data-ttu-id="bf706-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf706-137">System-Only</span></span>            | <span data-ttu-id="bf706-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-138">False</span></span>                           |
| <span data-ttu-id="bf706-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf706-139">Is-Single-Valued</span></span>       | <span data-ttu-id="bf706-140">True</span><span class="sxs-lookup"><span data-stu-id="bf706-140">True</span></span>                            |
| <span data-ttu-id="bf706-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf706-141">Is Indexed</span></span>             | <span data-ttu-id="bf706-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-142">False</span></span>                           |
| <span data-ttu-id="bf706-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf706-143">In Global Catalog</span></span>      | <span data-ttu-id="bf706-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-144">False</span></span>                           |
| <span data-ttu-id="bf706-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf706-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf706-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf706-146">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bf706-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf706-147">Range-Lower</span></span>            | <span data-ttu-id="bf706-148">1</span><span class="sxs-lookup"><span data-stu-id="bf706-148">1</span></span>                               |
| <span data-ttu-id="bf706-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf706-149">Range-Upper</span></span>            | <span data-ttu-id="bf706-150">256</span><span class="sxs-lookup"><span data-stu-id="bf706-150">256</span></span>                             |
| <span data-ttu-id="bf706-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-151">Search-Flags</span></span>           | <span data-ttu-id="bf706-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf706-152">0x00000000</span></span>                      |
| <span data-ttu-id="bf706-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-153">System-Flags</span></span>           | <span data-ttu-id="bf706-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf706-154">0x00000010</span></span>                      |
| <span data-ttu-id="bf706-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf706-155">Classes used in</span></span>        | [<span data-ttu-id="bf706-156">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bf706-156">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bf706-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf706-157">Windows Server 2003</span></span>



| <span data-ttu-id="bf706-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-158">Entry</span></span> | <span data-ttu-id="bf706-159">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-159">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bf706-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf706-160">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bf706-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-161">MAPI-Id</span></span>                | <span data-ttu-id="bf706-162">0x39FF</span><span class="sxs-lookup"><span data-stu-id="bf706-162">0x39FF</span></span>                          |
| <span data-ttu-id="bf706-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf706-163">System-Only</span></span>            | <span data-ttu-id="bf706-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-164">False</span></span>                           |
| <span data-ttu-id="bf706-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf706-165">Is-Single-Valued</span></span>       | <span data-ttu-id="bf706-166">True</span><span class="sxs-lookup"><span data-stu-id="bf706-166">True</span></span>                            |
| <span data-ttu-id="bf706-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf706-167">Is Indexed</span></span>             | <span data-ttu-id="bf706-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-168">False</span></span>                           |
| <span data-ttu-id="bf706-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf706-169">In Global Catalog</span></span>      | <span data-ttu-id="bf706-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-170">False</span></span>                           |
| <span data-ttu-id="bf706-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf706-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf706-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf706-172">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bf706-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf706-173">Range-Lower</span></span>            | <span data-ttu-id="bf706-174">1</span><span class="sxs-lookup"><span data-stu-id="bf706-174">1</span></span>                               |
| <span data-ttu-id="bf706-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf706-175">Range-Upper</span></span>            | <span data-ttu-id="bf706-176">256</span><span class="sxs-lookup"><span data-stu-id="bf706-176">256</span></span>                             |
| <span data-ttu-id="bf706-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-177">Search-Flags</span></span>           | <span data-ttu-id="bf706-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf706-178">0x00000000</span></span>                      |
| <span data-ttu-id="bf706-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-179">System-Flags</span></span>           | <span data-ttu-id="bf706-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf706-180">0x00000010</span></span>                      |
| <span data-ttu-id="bf706-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf706-181">Classes used in</span></span>        | [<span data-ttu-id="bf706-182">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bf706-182">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf706-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf706-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf706-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-184">Entry</span></span> | <span data-ttu-id="bf706-185">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-185">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bf706-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf706-186">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bf706-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-187">MAPI-Id</span></span>                | <span data-ttu-id="bf706-188">0x39FF</span><span class="sxs-lookup"><span data-stu-id="bf706-188">0x39FF</span></span>                          |
| <span data-ttu-id="bf706-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf706-189">System-Only</span></span>            | <span data-ttu-id="bf706-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-190">False</span></span>                           |
| <span data-ttu-id="bf706-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf706-191">Is-Single-Valued</span></span>       | <span data-ttu-id="bf706-192">True</span><span class="sxs-lookup"><span data-stu-id="bf706-192">True</span></span>                            |
| <span data-ttu-id="bf706-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf706-193">Is Indexed</span></span>             | <span data-ttu-id="bf706-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-194">False</span></span>                           |
| <span data-ttu-id="bf706-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf706-195">In Global Catalog</span></span>      | <span data-ttu-id="bf706-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-196">False</span></span>                           |
| <span data-ttu-id="bf706-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf706-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf706-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf706-198">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bf706-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf706-199">Range-Lower</span></span>            | <span data-ttu-id="bf706-200">1</span><span class="sxs-lookup"><span data-stu-id="bf706-200">1</span></span>                               |
| <span data-ttu-id="bf706-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf706-201">Range-Upper</span></span>            | <span data-ttu-id="bf706-202">256</span><span class="sxs-lookup"><span data-stu-id="bf706-202">256</span></span>                             |
| <span data-ttu-id="bf706-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-203">Search-Flags</span></span>           | <span data-ttu-id="bf706-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf706-204">0x00000000</span></span>                      |
| <span data-ttu-id="bf706-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-205">System-Flags</span></span>           | <span data-ttu-id="bf706-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf706-206">0x00000010</span></span>                      |
| <span data-ttu-id="bf706-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf706-207">Classes used in</span></span>        | [<span data-ttu-id="bf706-208">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bf706-208">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf706-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf706-209">Windows Server 2008</span></span>



| <span data-ttu-id="bf706-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-210">Entry</span></span> | <span data-ttu-id="bf706-211">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-211">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bf706-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf706-212">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bf706-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-213">MAPI-Id</span></span>                | <span data-ttu-id="bf706-214">0x39FF</span><span class="sxs-lookup"><span data-stu-id="bf706-214">0x39FF</span></span>                          |
| <span data-ttu-id="bf706-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf706-215">System-Only</span></span>            | <span data-ttu-id="bf706-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-216">False</span></span>                           |
| <span data-ttu-id="bf706-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf706-217">Is-Single-Valued</span></span>       | <span data-ttu-id="bf706-218">True</span><span class="sxs-lookup"><span data-stu-id="bf706-218">True</span></span>                            |
| <span data-ttu-id="bf706-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf706-219">Is Indexed</span></span>             | <span data-ttu-id="bf706-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-220">False</span></span>                           |
| <span data-ttu-id="bf706-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf706-221">In Global Catalog</span></span>      | <span data-ttu-id="bf706-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-222">False</span></span>                           |
| <span data-ttu-id="bf706-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf706-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf706-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf706-224">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bf706-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf706-225">Range-Lower</span></span>            | <span data-ttu-id="bf706-226">1</span><span class="sxs-lookup"><span data-stu-id="bf706-226">1</span></span>                               |
| <span data-ttu-id="bf706-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf706-227">Range-Upper</span></span>            | <span data-ttu-id="bf706-228">256</span><span class="sxs-lookup"><span data-stu-id="bf706-228">256</span></span>                             |
| <span data-ttu-id="bf706-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-229">Search-Flags</span></span>           | <span data-ttu-id="bf706-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf706-230">0x00000000</span></span>                      |
| <span data-ttu-id="bf706-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-231">System-Flags</span></span>           | <span data-ttu-id="bf706-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf706-232">0x00000010</span></span>                      |
| <span data-ttu-id="bf706-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf706-233">Classes used in</span></span>        | [<span data-ttu-id="bf706-234">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bf706-234">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf706-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf706-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf706-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-236">Entry</span></span> | <span data-ttu-id="bf706-237">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-237">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bf706-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf706-238">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bf706-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-239">MAPI-Id</span></span>                | <span data-ttu-id="bf706-240">0x39FF</span><span class="sxs-lookup"><span data-stu-id="bf706-240">0x39FF</span></span>                          |
| <span data-ttu-id="bf706-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf706-241">System-Only</span></span>            | <span data-ttu-id="bf706-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-242">False</span></span>                           |
| <span data-ttu-id="bf706-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf706-243">Is-Single-Valued</span></span>       | <span data-ttu-id="bf706-244">True</span><span class="sxs-lookup"><span data-stu-id="bf706-244">True</span></span>                            |
| <span data-ttu-id="bf706-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf706-245">Is Indexed</span></span>             | <span data-ttu-id="bf706-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-246">False</span></span>                           |
| <span data-ttu-id="bf706-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf706-247">In Global Catalog</span></span>      | <span data-ttu-id="bf706-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-248">False</span></span>                           |
| <span data-ttu-id="bf706-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf706-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf706-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf706-250">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bf706-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf706-251">Range-Lower</span></span>            | <span data-ttu-id="bf706-252">1</span><span class="sxs-lookup"><span data-stu-id="bf706-252">1</span></span>                               |
| <span data-ttu-id="bf706-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf706-253">Range-Upper</span></span>            | <span data-ttu-id="bf706-254">256</span><span class="sxs-lookup"><span data-stu-id="bf706-254">256</span></span>                             |
| <span data-ttu-id="bf706-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-255">Search-Flags</span></span>           | <span data-ttu-id="bf706-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf706-256">0x00000000</span></span>                      |
| <span data-ttu-id="bf706-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-257">System-Flags</span></span>           | <span data-ttu-id="bf706-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf706-258">0x00000010</span></span>                      |
| <span data-ttu-id="bf706-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf706-259">Classes used in</span></span>        | [<span data-ttu-id="bf706-260">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bf706-260">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf706-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf706-261">Windows Server 2012</span></span>



| <span data-ttu-id="bf706-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf706-262">Entry</span></span> | <span data-ttu-id="bf706-263">Значение</span><span class="sxs-lookup"><span data-stu-id="bf706-263">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="bf706-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf706-264">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="bf706-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf706-265">MAPI-Id</span></span>                | <span data-ttu-id="bf706-266">0x39FF</span><span class="sxs-lookup"><span data-stu-id="bf706-266">0x39FF</span></span>                          |
| <span data-ttu-id="bf706-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf706-267">System-Only</span></span>            | <span data-ttu-id="bf706-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-268">False</span></span>                           |
| <span data-ttu-id="bf706-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf706-269">Is-Single-Valued</span></span>       | <span data-ttu-id="bf706-270">True</span><span class="sxs-lookup"><span data-stu-id="bf706-270">True</span></span>                            |
| <span data-ttu-id="bf706-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf706-271">Is Indexed</span></span>             | <span data-ttu-id="bf706-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-272">False</span></span>                           |
| <span data-ttu-id="bf706-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf706-273">In Global Catalog</span></span>      | <span data-ttu-id="bf706-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf706-274">False</span></span>                           |
| <span data-ttu-id="bf706-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf706-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf706-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf706-276">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="bf706-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf706-277">Range-Lower</span></span>            | <span data-ttu-id="bf706-278">1</span><span class="sxs-lookup"><span data-stu-id="bf706-278">1</span></span>                               |
| <span data-ttu-id="bf706-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf706-279">Range-Upper</span></span>            | <span data-ttu-id="bf706-280">256</span><span class="sxs-lookup"><span data-stu-id="bf706-280">256</span></span>                             |
| <span data-ttu-id="bf706-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-281">Search-Flags</span></span>           | <span data-ttu-id="bf706-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf706-282">0x00000000</span></span>                      |
| <span data-ttu-id="bf706-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf706-283">System-Flags</span></span>           | <span data-ttu-id="bf706-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf706-284">0x00000010</span></span>                      |
| <span data-ttu-id="bf706-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf706-285">Classes used in</span></span>        | [<span data-ttu-id="bf706-286">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="bf706-286">**Top**</span></span>](c-top.md)<br/> |



 

 





