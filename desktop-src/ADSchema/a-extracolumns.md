---
title: Атрибут Extra-Columns
description: Это многозначный атрибут, значения которого состоят из 5 кортежа (имя атрибута), (заголовок столбца), (видимость по умолчанию (0, 1)), (ширина столбца (\ 8211; 1 для автоматической ширины)), 0 (зарезервировано для использования в будущем должно быть равно нулю).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Extra-Columns
- Схема AD атрибута Екстраколумнс
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804433"
---
# <a name="extra-columns-attribute"></a><span data-ttu-id="647f9-105">Атрибут Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="647f9-105">Extra-Columns attribute</span></span>

<span data-ttu-id="647f9-106">Это многозначный атрибут, значения которого состоят из 5 кортежа: (имя атрибута), (заголовок столбца), (видимость по умолчанию (0, 1)), (ширина столбца (1 для автоматической ширины)), 0 (зарезервировано для будущего использования должна быть нулевой).</span><span class="sxs-lookup"><span data-stu-id="647f9-106">This is a multivalued attribute whose values consist of a 5 tuple: (attribute name), (column title), (default visibility (0,1)), (column width ( 1 for auto width)), 0 (reserved for future use must be zero).</span></span> <span data-ttu-id="647f9-107">Это значение используется в консоли "пользователи и компьютеры Active Directory".</span><span class="sxs-lookup"><span data-stu-id="647f9-107">This value is used by the AD Users and Computers console.</span></span>



| <span data-ttu-id="647f9-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="647f9-108">Entry</span></span> | <span data-ttu-id="647f9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="647f9-109">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="647f9-110">CN</span><span class="sxs-lookup"><span data-stu-id="647f9-110">CN</span></span>                | <span data-ttu-id="647f9-111">Extra-Columns</span><span class="sxs-lookup"><span data-stu-id="647f9-111">Extra-Columns</span></span>                                                                                                                                                        |
| <span data-ttu-id="647f9-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="647f9-112">Ldap-Display-Name</span></span> | <span data-ttu-id="647f9-113">екстраколумнс</span><span class="sxs-lookup"><span data-stu-id="647f9-113">extraColumns</span></span>                                                                                                                                                         |
| <span data-ttu-id="647f9-114">Размер</span><span class="sxs-lookup"><span data-stu-id="647f9-114">Size</span></span>              | <span data-ttu-id="647f9-115">Каждое значение будет иметь размер строки из 5 кортежа выше.</span><span class="sxs-lookup"><span data-stu-id="647f9-115">Each value would be the size of the string of the 5 tuple above.</span></span> <span data-ttu-id="647f9-116">По умолчанию для объекта, отображаемого по умолчанию в контейнере ДисплайспеЦифиер, будет отображаться 22 значения.</span><span class="sxs-lookup"><span data-stu-id="647f9-116">By default there will be 22 values on the default-Display object in the DisplaySpecifier container.</span></span> |
| <span data-ttu-id="647f9-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="647f9-117">Update Privilege</span></span>  | <span data-ttu-id="647f9-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="647f9-118">Domain administrator</span></span>                                                                                                                                                 |
| <span data-ttu-id="647f9-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="647f9-119">Update Frequency</span></span>  | <span data-ttu-id="647f9-120">Это будет обновлено только в том случае, если установлена служба Exchange.</span><span class="sxs-lookup"><span data-stu-id="647f9-120">This will only be updated if a service like Exchange is installed.</span></span>                                                                                                   |
| <span data-ttu-id="647f9-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="647f9-121">Attribute-Id</span></span>      | <span data-ttu-id="647f9-122">1.2.840.113556.1.4.1687</span><span class="sxs-lookup"><span data-stu-id="647f9-122">1.2.840.113556.1.4.1687</span></span>                                                                                                                                              |
| <span data-ttu-id="647f9-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="647f9-123">System-Id-Guid</span></span>    | <span data-ttu-id="647f9-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span><span class="sxs-lookup"><span data-stu-id="647f9-124">d24e2846-1dd9-4bcf-99d7-a6227cc86da7</span></span>                                                                                                                                 |
| <span data-ttu-id="647f9-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="647f9-125">Syntax</span></span>            | [<span data-ttu-id="647f9-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="647f9-126">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a><span data-ttu-id="647f9-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="647f9-127">Implementations</span></span>

-   [<span data-ttu-id="647f9-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="647f9-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="647f9-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="647f9-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="647f9-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="647f9-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="647f9-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="647f9-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="647f9-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="647f9-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="647f9-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="647f9-133">Windows Server 2003</span></span>



| <span data-ttu-id="647f9-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="647f9-134">Entry</span></span> | <span data-ttu-id="647f9-135">Значение</span><span class="sxs-lookup"><span data-stu-id="647f9-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="647f9-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="647f9-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="647f9-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="647f9-138">System-Only</span></span>            | <span data-ttu-id="647f9-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-139">False</span></span>                                                      |
| <span data-ttu-id="647f9-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="647f9-140">Is-Single-Valued</span></span>       | <span data-ttu-id="647f9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-141">False</span></span>                                                      |
| <span data-ttu-id="647f9-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="647f9-142">Is Indexed</span></span>             | <span data-ttu-id="647f9-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-143">False</span></span>                                                      |
| <span data-ttu-id="647f9-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="647f9-144">In Global Catalog</span></span>      | <span data-ttu-id="647f9-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-145">False</span></span>                                                      |
| <span data-ttu-id="647f9-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="647f9-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="647f9-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="647f9-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="647f9-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="647f9-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="647f9-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-150">Search-Flags</span></span>           | <span data-ttu-id="647f9-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="647f9-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="647f9-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-152">System-Flags</span></span>           | <span data-ttu-id="647f9-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="647f9-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="647f9-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="647f9-154">Classes used in</span></span>        | [<span data-ttu-id="647f9-155">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="647f9-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="647f9-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="647f9-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="647f9-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="647f9-157">Entry</span></span> | <span data-ttu-id="647f9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="647f9-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="647f9-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="647f9-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="647f9-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="647f9-161">System-Only</span></span>            | <span data-ttu-id="647f9-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-162">False</span></span>                                                      |
| <span data-ttu-id="647f9-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="647f9-163">Is-Single-Valued</span></span>       | <span data-ttu-id="647f9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-164">False</span></span>                                                      |
| <span data-ttu-id="647f9-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="647f9-165">Is Indexed</span></span>             | <span data-ttu-id="647f9-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-166">False</span></span>                                                      |
| <span data-ttu-id="647f9-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="647f9-167">In Global Catalog</span></span>      | <span data-ttu-id="647f9-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-168">False</span></span>                                                      |
| <span data-ttu-id="647f9-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="647f9-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="647f9-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="647f9-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="647f9-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="647f9-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="647f9-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-173">Search-Flags</span></span>           | <span data-ttu-id="647f9-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="647f9-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="647f9-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-175">System-Flags</span></span>           | <span data-ttu-id="647f9-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="647f9-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="647f9-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="647f9-177">Classes used in</span></span>        | [<span data-ttu-id="647f9-178">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="647f9-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="647f9-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="647f9-179">Windows Server 2008</span></span>



| <span data-ttu-id="647f9-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="647f9-180">Entry</span></span> | <span data-ttu-id="647f9-181">Значение</span><span class="sxs-lookup"><span data-stu-id="647f9-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="647f9-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="647f9-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="647f9-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="647f9-184">System-Only</span></span>            | <span data-ttu-id="647f9-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-185">False</span></span>                                                      |
| <span data-ttu-id="647f9-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="647f9-186">Is-Single-Valued</span></span>       | <span data-ttu-id="647f9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-187">False</span></span>                                                      |
| <span data-ttu-id="647f9-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="647f9-188">Is Indexed</span></span>             | <span data-ttu-id="647f9-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-189">False</span></span>                                                      |
| <span data-ttu-id="647f9-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="647f9-190">In Global Catalog</span></span>      | <span data-ttu-id="647f9-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-191">False</span></span>                                                      |
| <span data-ttu-id="647f9-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="647f9-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="647f9-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="647f9-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="647f9-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="647f9-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="647f9-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-196">Search-Flags</span></span>           | <span data-ttu-id="647f9-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="647f9-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="647f9-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-198">System-Flags</span></span>           | <span data-ttu-id="647f9-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="647f9-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="647f9-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="647f9-200">Classes used in</span></span>        | [<span data-ttu-id="647f9-201">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="647f9-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="647f9-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="647f9-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="647f9-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="647f9-203">Entry</span></span> | <span data-ttu-id="647f9-204">Значение</span><span class="sxs-lookup"><span data-stu-id="647f9-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="647f9-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="647f9-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="647f9-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="647f9-207">System-Only</span></span>            | <span data-ttu-id="647f9-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-208">False</span></span>                                                      |
| <span data-ttu-id="647f9-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="647f9-209">Is-Single-Valued</span></span>       | <span data-ttu-id="647f9-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-210">False</span></span>                                                      |
| <span data-ttu-id="647f9-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="647f9-211">Is Indexed</span></span>             | <span data-ttu-id="647f9-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-212">False</span></span>                                                      |
| <span data-ttu-id="647f9-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="647f9-213">In Global Catalog</span></span>      | <span data-ttu-id="647f9-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-214">False</span></span>                                                      |
| <span data-ttu-id="647f9-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="647f9-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="647f9-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="647f9-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="647f9-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="647f9-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="647f9-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-219">Search-Flags</span></span>           | <span data-ttu-id="647f9-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="647f9-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="647f9-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-221">System-Flags</span></span>           | <span data-ttu-id="647f9-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="647f9-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="647f9-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="647f9-223">Classes used in</span></span>        | [<span data-ttu-id="647f9-224">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="647f9-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="647f9-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="647f9-225">Windows Server 2012</span></span>



| <span data-ttu-id="647f9-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="647f9-226">Entry</span></span> | <span data-ttu-id="647f9-227">Значение</span><span class="sxs-lookup"><span data-stu-id="647f9-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="647f9-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="647f9-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="647f9-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="647f9-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="647f9-230">System-Only</span></span>            | <span data-ttu-id="647f9-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-231">False</span></span>                                                      |
| <span data-ttu-id="647f9-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="647f9-232">Is-Single-Valued</span></span>       | <span data-ttu-id="647f9-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-233">False</span></span>                                                      |
| <span data-ttu-id="647f9-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="647f9-234">Is Indexed</span></span>             | <span data-ttu-id="647f9-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-235">False</span></span>                                                      |
| <span data-ttu-id="647f9-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="647f9-236">In Global Catalog</span></span>      | <span data-ttu-id="647f9-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="647f9-237">False</span></span>                                                      |
| <span data-ttu-id="647f9-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="647f9-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="647f9-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="647f9-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="647f9-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="647f9-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="647f9-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="647f9-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-242">Search-Flags</span></span>           | <span data-ttu-id="647f9-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="647f9-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="647f9-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="647f9-244">System-Flags</span></span>           | <span data-ttu-id="647f9-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="647f9-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="647f9-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="647f9-246">Classes used in</span></span>        | [<span data-ttu-id="647f9-247">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="647f9-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





