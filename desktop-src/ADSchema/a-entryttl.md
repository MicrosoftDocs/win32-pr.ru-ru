---
title: Атрибут "Entry-TTL"
description: Этот рабочий атрибут поддерживается сервером и, по-видимому, присутствует в каждой динамической записи.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута TTL для входа
- Схема AD атрибута Ентриттл
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2dd5e38b22731fee7f957ee8f817537e32c645
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493533"
---
# <a name="entry-ttl-attribute"></a><span data-ttu-id="c0197-105">Атрибут "Entry-TTL"</span><span class="sxs-lookup"><span data-stu-id="c0197-105">Entry-TTL attribute</span></span>

<span data-ttu-id="c0197-106">Этот рабочий атрибут поддерживается сервером и, по-видимому, присутствует в каждой динамической записи.</span><span class="sxs-lookup"><span data-stu-id="c0197-106">This operational attribute is maintained by the server and appears to be present in every dynamic entry.</span></span> <span data-ttu-id="c0197-107">Атрибут отсутствует, если запись не содержит класс объекта dynamicObject.</span><span class="sxs-lookup"><span data-stu-id="c0197-107">The attribute is not present when the entry does not contain the dynamicObject object class.</span></span> <span data-ttu-id="c0197-108">Значение этого атрибута — это время в секундах, в течение которого запись будет продолжать существовать, прежде чем выводить из каталога.</span><span class="sxs-lookup"><span data-stu-id="c0197-108">The value of this attribute is the time, in seconds, that the entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="c0197-109">При отсутствии промежуточных операций обновления значения, возвращаемые путем считывания атрибута в двух последовательных операциях поиска, гарантированно будут невозрастающими.</span><span class="sxs-lookup"><span data-stu-id="c0197-109">In the absence of intervening "refresh" operations, the values returned by reading the attribute in two successive searches are guaranteed to be nonincreasing.</span></span> <span data-ttu-id="c0197-110">Наименьшее допустимое значение равно 0, что означает, что запись может исчезнуть без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="c0197-110">The smallest permissible value is 0, indicating that the entry may disappear without warning.</span></span> <span data-ttu-id="c0197-111">Атрибут помечен как "без изменения пользователя", так как он может быть изменен только с помощью операции обновления.</span><span class="sxs-lookup"><span data-stu-id="c0197-111">The attribute is marked NO-USER-MODIFICATION because it may only be changed by using the refresh operation.</span></span>



| <span data-ttu-id="c0197-112">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-112">Entry</span></span> | <span data-ttu-id="c0197-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-113">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c0197-114">CN</span><span class="sxs-lookup"><span data-stu-id="c0197-114">CN</span></span>                | <span data-ttu-id="c0197-115">Срок жизни записи</span><span class="sxs-lookup"><span data-stu-id="c0197-115">Entry-TTL</span></span>                                   |
| <span data-ttu-id="c0197-116">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c0197-116">Ldap-Display-Name</span></span> | <span data-ttu-id="c0197-117">ентриттл</span><span class="sxs-lookup"><span data-stu-id="c0197-117">entryTTL</span></span>                                    |
| <span data-ttu-id="c0197-118">Размер</span><span class="sxs-lookup"><span data-stu-id="c0197-118">Size</span></span>              | <span data-ttu-id="c0197-119">4 байта.</span><span class="sxs-lookup"><span data-stu-id="c0197-119">4 bytes.</span></span> <span data-ttu-id="c0197-120">Максимальное значение = 1 год, по умолчанию — 1 день.</span><span class="sxs-lookup"><span data-stu-id="c0197-120">Maximum = 1 year, default = 1 day.</span></span> |
| <span data-ttu-id="c0197-121">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c0197-121">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="c0197-122">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c0197-122">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c0197-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-123">Attribute-Id</span></span>      | <span data-ttu-id="c0197-124">1.3.6.1.4.1.1466.101.119.3</span><span class="sxs-lookup"><span data-stu-id="c0197-124">1.3.6.1.4.1.1466.101.119.3</span></span>                  |
| <span data-ttu-id="c0197-125">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c0197-125">System-Id-Guid</span></span>    | <span data-ttu-id="c0197-126">d213decc-d81a-4384-AAC2-dcfcfd631cf8</span><span class="sxs-lookup"><span data-stu-id="c0197-126">d213decc-d81a-4384-aac2-dcfcfd631cf8</span></span>        |
| <span data-ttu-id="c0197-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0197-127">Syntax</span></span>            | [<span data-ttu-id="c0197-128">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="c0197-128">**Enumeration**</span></span>](s-enumeration.md)        |



## <a name="implementations"></a><span data-ttu-id="c0197-129">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c0197-129">Implementations</span></span>

-   [<span data-ttu-id="c0197-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c0197-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c0197-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c0197-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c0197-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c0197-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c0197-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c0197-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c0197-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c0197-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c0197-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c0197-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="c0197-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0197-136">Windows Server 2003</span></span>



| <span data-ttu-id="c0197-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-137">Entry</span></span> | <span data-ttu-id="c0197-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-138">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c0197-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0197-139">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-140">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0197-141">System-Only</span></span>            | <span data-ttu-id="c0197-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-142">False</span></span>                                                |
| <span data-ttu-id="c0197-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0197-143">Is-Single-Valued</span></span>       | <span data-ttu-id="c0197-144">True</span><span class="sxs-lookup"><span data-stu-id="c0197-144">True</span></span>                                                 |
| <span data-ttu-id="c0197-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0197-145">Is Indexed</span></span>             | <span data-ttu-id="c0197-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-146">False</span></span>                                                |
| <span data-ttu-id="c0197-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0197-147">In Global Catalog</span></span>      | <span data-ttu-id="c0197-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-148">False</span></span>                                                |
| <span data-ttu-id="c0197-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0197-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0197-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0197-150">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c0197-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0197-151">Range-Lower</span></span>            | <span data-ttu-id="c0197-152">0</span><span class="sxs-lookup"><span data-stu-id="c0197-152">0</span></span>                                                    |
| <span data-ttu-id="c0197-153">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0197-153">Range-Upper</span></span>            | <span data-ttu-id="c0197-154">31557600</span><span class="sxs-lookup"><span data-stu-id="c0197-154">31557600</span></span>                                             |
| <span data-ttu-id="c0197-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-155">Search-Flags</span></span>           | <span data-ttu-id="c0197-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0197-156">0x00000000</span></span>                                           |
| <span data-ttu-id="c0197-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-157">System-Flags</span></span>           | <span data-ttu-id="c0197-158">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c0197-158">0x00000014</span></span>                                           |
| <span data-ttu-id="c0197-159">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0197-159">Classes used in</span></span>        | [<span data-ttu-id="c0197-160">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="c0197-160">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c0197-161">ADAM</span><span class="sxs-lookup"><span data-stu-id="c0197-161">ADAM</span></span>



| <span data-ttu-id="c0197-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-162">Entry</span></span> | <span data-ttu-id="c0197-163">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-163">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c0197-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0197-164">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-165">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0197-166">System-Only</span></span>            | <span data-ttu-id="c0197-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-167">False</span></span>                                                |
| <span data-ttu-id="c0197-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0197-168">Is-Single-Valued</span></span>       | <span data-ttu-id="c0197-169">True</span><span class="sxs-lookup"><span data-stu-id="c0197-169">True</span></span>                                                 |
| <span data-ttu-id="c0197-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0197-170">Is Indexed</span></span>             | <span data-ttu-id="c0197-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-171">False</span></span>                                                |
| <span data-ttu-id="c0197-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0197-172">In Global Catalog</span></span>      | <span data-ttu-id="c0197-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-173">False</span></span>                                                |
| <span data-ttu-id="c0197-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0197-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0197-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0197-175">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c0197-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0197-176">Range-Lower</span></span>            | <span data-ttu-id="c0197-177">0</span><span class="sxs-lookup"><span data-stu-id="c0197-177">0</span></span>                                                    |
| <span data-ttu-id="c0197-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0197-178">Range-Upper</span></span>            | <span data-ttu-id="c0197-179">31557600</span><span class="sxs-lookup"><span data-stu-id="c0197-179">31557600</span></span>                                             |
| <span data-ttu-id="c0197-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-180">Search-Flags</span></span>           | <span data-ttu-id="c0197-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0197-181">0x00000000</span></span>                                           |
| <span data-ttu-id="c0197-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-182">System-Flags</span></span>           | <span data-ttu-id="c0197-183">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c0197-183">0x00000014</span></span>                                           |
| <span data-ttu-id="c0197-184">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0197-184">Classes used in</span></span>        | [<span data-ttu-id="c0197-185">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="c0197-185">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c0197-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c0197-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c0197-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-187">Entry</span></span> | <span data-ttu-id="c0197-188">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-188">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c0197-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0197-189">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-190">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0197-191">System-Only</span></span>            | <span data-ttu-id="c0197-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-192">False</span></span>                                                |
| <span data-ttu-id="c0197-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0197-193">Is-Single-Valued</span></span>       | <span data-ttu-id="c0197-194">True</span><span class="sxs-lookup"><span data-stu-id="c0197-194">True</span></span>                                                 |
| <span data-ttu-id="c0197-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0197-195">Is Indexed</span></span>             | <span data-ttu-id="c0197-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-196">False</span></span>                                                |
| <span data-ttu-id="c0197-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0197-197">In Global Catalog</span></span>      | <span data-ttu-id="c0197-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-198">False</span></span>                                                |
| <span data-ttu-id="c0197-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0197-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0197-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0197-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c0197-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0197-201">Range-Lower</span></span>            | <span data-ttu-id="c0197-202">0</span><span class="sxs-lookup"><span data-stu-id="c0197-202">0</span></span>                                                    |
| <span data-ttu-id="c0197-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0197-203">Range-Upper</span></span>            | <span data-ttu-id="c0197-204">31557600</span><span class="sxs-lookup"><span data-stu-id="c0197-204">31557600</span></span>                                             |
| <span data-ttu-id="c0197-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-205">Search-Flags</span></span>           | <span data-ttu-id="c0197-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0197-206">0x00000000</span></span>                                           |
| <span data-ttu-id="c0197-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-207">System-Flags</span></span>           | <span data-ttu-id="c0197-208">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c0197-208">0x00000014</span></span>                                           |
| <span data-ttu-id="c0197-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0197-209">Classes used in</span></span>        | [<span data-ttu-id="c0197-210">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="c0197-210">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c0197-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0197-211">Windows Server 2008</span></span>



| <span data-ttu-id="c0197-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-212">Entry</span></span> | <span data-ttu-id="c0197-213">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c0197-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0197-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-215">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0197-216">System-Only</span></span>            | <span data-ttu-id="c0197-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-217">False</span></span>                                                |
| <span data-ttu-id="c0197-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0197-218">Is-Single-Valued</span></span>       | <span data-ttu-id="c0197-219">True</span><span class="sxs-lookup"><span data-stu-id="c0197-219">True</span></span>                                                 |
| <span data-ttu-id="c0197-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0197-220">Is Indexed</span></span>             | <span data-ttu-id="c0197-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-221">False</span></span>                                                |
| <span data-ttu-id="c0197-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0197-222">In Global Catalog</span></span>      | <span data-ttu-id="c0197-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-223">False</span></span>                                                |
| <span data-ttu-id="c0197-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0197-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0197-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0197-225">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c0197-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0197-226">Range-Lower</span></span>            | <span data-ttu-id="c0197-227">0</span><span class="sxs-lookup"><span data-stu-id="c0197-227">0</span></span>                                                    |
| <span data-ttu-id="c0197-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0197-228">Range-Upper</span></span>            | <span data-ttu-id="c0197-229">31557600</span><span class="sxs-lookup"><span data-stu-id="c0197-229">31557600</span></span>                                             |
| <span data-ttu-id="c0197-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-230">Search-Flags</span></span>           | <span data-ttu-id="c0197-231">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0197-231">0x00000000</span></span>                                           |
| <span data-ttu-id="c0197-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-232">System-Flags</span></span>           | <span data-ttu-id="c0197-233">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c0197-233">0x00000014</span></span>                                           |
| <span data-ttu-id="c0197-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0197-234">Classes used in</span></span>        | [<span data-ttu-id="c0197-235">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="c0197-235">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c0197-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c0197-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c0197-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-237">Entry</span></span> | <span data-ttu-id="c0197-238">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-238">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c0197-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0197-239">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-240">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0197-241">System-Only</span></span>            | <span data-ttu-id="c0197-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-242">False</span></span>                                                |
| <span data-ttu-id="c0197-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0197-243">Is-Single-Valued</span></span>       | <span data-ttu-id="c0197-244">True</span><span class="sxs-lookup"><span data-stu-id="c0197-244">True</span></span>                                                 |
| <span data-ttu-id="c0197-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0197-245">Is Indexed</span></span>             | <span data-ttu-id="c0197-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-246">False</span></span>                                                |
| <span data-ttu-id="c0197-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0197-247">In Global Catalog</span></span>      | <span data-ttu-id="c0197-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-248">False</span></span>                                                |
| <span data-ttu-id="c0197-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0197-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0197-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0197-250">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c0197-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0197-251">Range-Lower</span></span>            | <span data-ttu-id="c0197-252">0</span><span class="sxs-lookup"><span data-stu-id="c0197-252">0</span></span>                                                    |
| <span data-ttu-id="c0197-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0197-253">Range-Upper</span></span>            | <span data-ttu-id="c0197-254">31557600</span><span class="sxs-lookup"><span data-stu-id="c0197-254">31557600</span></span>                                             |
| <span data-ttu-id="c0197-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-255">Search-Flags</span></span>           | <span data-ttu-id="c0197-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0197-256">0x00000000</span></span>                                           |
| <span data-ttu-id="c0197-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-257">System-Flags</span></span>           | <span data-ttu-id="c0197-258">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c0197-258">0x00000014</span></span>                                           |
| <span data-ttu-id="c0197-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0197-259">Classes used in</span></span>        | [<span data-ttu-id="c0197-260">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="c0197-260">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c0197-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0197-261">Windows Server 2012</span></span>



| <span data-ttu-id="c0197-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="c0197-262">Entry</span></span> | <span data-ttu-id="c0197-263">Значение</span><span class="sxs-lookup"><span data-stu-id="c0197-263">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="c0197-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c0197-264">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c0197-265">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="c0197-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="c0197-266">System-Only</span></span>            | <span data-ttu-id="c0197-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-267">False</span></span>                                                |
| <span data-ttu-id="c0197-268">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c0197-268">Is-Single-Valued</span></span>       | <span data-ttu-id="c0197-269">True</span><span class="sxs-lookup"><span data-stu-id="c0197-269">True</span></span>                                                 |
| <span data-ttu-id="c0197-270">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c0197-270">Is Indexed</span></span>             | <span data-ttu-id="c0197-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-271">False</span></span>                                                |
| <span data-ttu-id="c0197-272">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c0197-272">In Global Catalog</span></span>      | <span data-ttu-id="c0197-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="c0197-273">False</span></span>                                                |
| <span data-ttu-id="c0197-274">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c0197-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="c0197-275">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c0197-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="c0197-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c0197-276">Range-Lower</span></span>            | <span data-ttu-id="c0197-277">0</span><span class="sxs-lookup"><span data-stu-id="c0197-277">0</span></span>                                                    |
| <span data-ttu-id="c0197-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c0197-278">Range-Upper</span></span>            | <span data-ttu-id="c0197-279">31557600</span><span class="sxs-lookup"><span data-stu-id="c0197-279">31557600</span></span>                                             |
| <span data-ttu-id="c0197-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-280">Search-Flags</span></span>           | <span data-ttu-id="c0197-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c0197-281">0x00000000</span></span>                                           |
| <span data-ttu-id="c0197-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c0197-282">System-Flags</span></span>           | <span data-ttu-id="c0197-283">0x00000014</span><span class="sxs-lookup"><span data-stu-id="c0197-283">0x00000014</span></span>                                           |
| <span data-ttu-id="c0197-284">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c0197-284">Classes used in</span></span>        | [<span data-ttu-id="c0197-285">**Динамический объект**</span><span class="sxs-lookup"><span data-stu-id="c0197-285">**Dynamic-Object**</span></span>](c-dynamicobject.md)<br/> |



 

 





