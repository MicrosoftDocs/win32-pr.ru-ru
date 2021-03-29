---
title: Атрибут «администратор» — «свойство-страница»
description: Это многозначный атрибут, значения которого представляют собой число, представляющее порядок добавления страниц, и идентификатор GUID COM-объекта, который реализует страницы свойств с множественным выделением для оснастки "пользователи и компьютеры Active Directory".
ms.assetid: b2b4aafe-ac2d-44b3-80eb-910ba9852bb0
ms.tgt_platform: multiple
keywords:
- Администратор-схема AD для атрибута "многовыборочная выбор-свойство-страница"
- Схема AD атрибута Админмултиселектпропертипажес
topic_type:
- apiref
api_name:
- Admin-Multiselect-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e653568d4f8f6653e4c7dc939c91a7d3cd8b83c6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654989"
---
# <a name="admin-multiselect-property-pages-attribute"></a><span data-ttu-id="0e340-105">Атрибут «администратор» — «свойство-страница»</span><span class="sxs-lookup"><span data-stu-id="0e340-105">Admin-Multiselect-Property-Pages attribute</span></span>

<span data-ttu-id="0e340-106">Это многозначный атрибут, значения которого представляют собой число, представляющее порядок добавления страниц, и идентификатор GUID COM-объекта, который реализует страницы свойств с множественным выделением для оснастки "пользователи и компьютеры Active Directory".</span><span class="sxs-lookup"><span data-stu-id="0e340-106">This is a multivalued attribute whose values are a number that represents the order in which the pages are added and a GUID of a COM object that implements multi-select property pages for the AD Users and Computers snap-in.</span></span>



| <span data-ttu-id="0e340-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="0e340-107">Entry</span></span> | <span data-ttu-id="0e340-108">Значение</span><span class="sxs-lookup"><span data-stu-id="0e340-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e340-109">CN</span><span class="sxs-lookup"><span data-stu-id="0e340-109">CN</span></span>                | <span data-ttu-id="0e340-110">Администрирование — Многовыборочные страницы свойств</span><span class="sxs-lookup"><span data-stu-id="0e340-110">Admin-Multiselect-Property-Pages</span></span>                                                                                                            |
| <span data-ttu-id="0e340-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0e340-111">Ldap-Display-Name</span></span> | <span data-ttu-id="0e340-112">админмултиселектпропертипажес</span><span class="sxs-lookup"><span data-stu-id="0e340-112">adminMultiselectPropertyPages</span></span>                                                                                                               |
| <span data-ttu-id="0e340-113">Размер</span><span class="sxs-lookup"><span data-stu-id="0e340-113">Size</span></span>              | <span data-ttu-id="0e340-114">40 байт</span><span class="sxs-lookup"><span data-stu-id="0e340-114">40 bytes</span></span>                                                                                                                                    |
| <span data-ttu-id="0e340-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0e340-115">Update Privilege</span></span>  | <span data-ttu-id="0e340-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="0e340-116">Domain administrator</span></span>                                                                                                                        |
| <span data-ttu-id="0e340-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0e340-117">Update Frequency</span></span>  | <span data-ttu-id="0e340-118">Обновление будет выполнено только в том случае, если установлена служба Exchange или сервер терминалов, реализующая собственные страницы свойств с множественным выделением.</span><span class="sxs-lookup"><span data-stu-id="0e340-118">This will only be updated if a service like Exchange or Terminal Server is installed that implements their own multi-select property pages.</span></span> |
| <span data-ttu-id="0e340-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0e340-119">Attribute-Id</span></span>      | <span data-ttu-id="0e340-120">1.2.840.113556.1.4.1690</span><span class="sxs-lookup"><span data-stu-id="0e340-120">1.2.840.113556.1.4.1690</span></span>                                                                                                                     |
| <span data-ttu-id="0e340-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0e340-121">System-Id-Guid</span></span>    | <span data-ttu-id="0e340-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span><span class="sxs-lookup"><span data-stu-id="0e340-122">18f9b67d-5ac6-4b3b-97db-d0a406afb7ba</span></span>                                                                                                        |
| <span data-ttu-id="0e340-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e340-123">Syntax</span></span>            | [<span data-ttu-id="0e340-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="0e340-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                                                 |



## <a name="implementations"></a><span data-ttu-id="0e340-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0e340-125">Implementations</span></span>

-   [<span data-ttu-id="0e340-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0e340-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0e340-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0e340-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0e340-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0e340-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0e340-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0e340-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0e340-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0e340-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="0e340-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0e340-131">Windows Server 2003</span></span>



| <span data-ttu-id="0e340-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="0e340-132">Entry</span></span> | <span data-ttu-id="0e340-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0e340-133">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e340-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0e340-134">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e340-135">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e340-136">System-Only</span></span>            | <span data-ttu-id="0e340-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-137">False</span></span>                                                      |
| <span data-ttu-id="0e340-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0e340-138">Is-Single-Valued</span></span>       | <span data-ttu-id="0e340-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-139">False</span></span>                                                      |
| <span data-ttu-id="0e340-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0e340-140">Is Indexed</span></span>             | <span data-ttu-id="0e340-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-141">False</span></span>                                                      |
| <span data-ttu-id="0e340-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0e340-142">In Global Catalog</span></span>      | <span data-ttu-id="0e340-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-143">False</span></span>                                                      |
| <span data-ttu-id="0e340-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0e340-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e340-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0e340-145">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0e340-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e340-146">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e340-147">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-148">Search-Flags</span></span>           | <span data-ttu-id="0e340-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e340-149">0x00000000</span></span>                                                 |
| <span data-ttu-id="0e340-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-150">System-Flags</span></span>           | <span data-ttu-id="0e340-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e340-151">0x00000010</span></span>                                                 |
| <span data-ttu-id="0e340-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0e340-152">Classes used in</span></span>        | [<span data-ttu-id="0e340-153">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="0e340-153">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0e340-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0e340-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0e340-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="0e340-155">Entry</span></span> | <span data-ttu-id="0e340-156">Значение</span><span class="sxs-lookup"><span data-stu-id="0e340-156">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e340-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0e340-157">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e340-158">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e340-159">System-Only</span></span>            | <span data-ttu-id="0e340-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-160">False</span></span>                                                      |
| <span data-ttu-id="0e340-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0e340-161">Is-Single-Valued</span></span>       | <span data-ttu-id="0e340-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-162">False</span></span>                                                      |
| <span data-ttu-id="0e340-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0e340-163">Is Indexed</span></span>             | <span data-ttu-id="0e340-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-164">False</span></span>                                                      |
| <span data-ttu-id="0e340-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0e340-165">In Global Catalog</span></span>      | <span data-ttu-id="0e340-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-166">False</span></span>                                                      |
| <span data-ttu-id="0e340-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0e340-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e340-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0e340-168">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0e340-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e340-169">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e340-170">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-171">Search-Flags</span></span>           | <span data-ttu-id="0e340-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e340-172">0x00000000</span></span>                                                 |
| <span data-ttu-id="0e340-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-173">System-Flags</span></span>           | <span data-ttu-id="0e340-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e340-174">0x00000010</span></span>                                                 |
| <span data-ttu-id="0e340-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0e340-175">Classes used in</span></span>        | [<span data-ttu-id="0e340-176">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="0e340-176">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0e340-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e340-177">Windows Server 2008</span></span>



| <span data-ttu-id="0e340-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="0e340-178">Entry</span></span> | <span data-ttu-id="0e340-179">Значение</span><span class="sxs-lookup"><span data-stu-id="0e340-179">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e340-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0e340-180">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e340-181">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e340-182">System-Only</span></span>            | <span data-ttu-id="0e340-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-183">False</span></span>                                                      |
| <span data-ttu-id="0e340-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0e340-184">Is-Single-Valued</span></span>       | <span data-ttu-id="0e340-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-185">False</span></span>                                                      |
| <span data-ttu-id="0e340-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0e340-186">Is Indexed</span></span>             | <span data-ttu-id="0e340-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-187">False</span></span>                                                      |
| <span data-ttu-id="0e340-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0e340-188">In Global Catalog</span></span>      | <span data-ttu-id="0e340-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-189">False</span></span>                                                      |
| <span data-ttu-id="0e340-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0e340-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e340-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0e340-191">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0e340-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e340-192">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e340-193">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-194">Search-Flags</span></span>           | <span data-ttu-id="0e340-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e340-195">0x00000000</span></span>                                                 |
| <span data-ttu-id="0e340-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-196">System-Flags</span></span>           | <span data-ttu-id="0e340-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e340-197">0x00000010</span></span>                                                 |
| <span data-ttu-id="0e340-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0e340-198">Classes used in</span></span>        | [<span data-ttu-id="0e340-199">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="0e340-199">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0e340-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0e340-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0e340-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="0e340-201">Entry</span></span> | <span data-ttu-id="0e340-202">Значение</span><span class="sxs-lookup"><span data-stu-id="0e340-202">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e340-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0e340-203">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e340-204">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e340-205">System-Only</span></span>            | <span data-ttu-id="0e340-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-206">False</span></span>                                                      |
| <span data-ttu-id="0e340-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0e340-207">Is-Single-Valued</span></span>       | <span data-ttu-id="0e340-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-208">False</span></span>                                                      |
| <span data-ttu-id="0e340-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0e340-209">Is Indexed</span></span>             | <span data-ttu-id="0e340-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-210">False</span></span>                                                      |
| <span data-ttu-id="0e340-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0e340-211">In Global Catalog</span></span>      | <span data-ttu-id="0e340-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-212">False</span></span>                                                      |
| <span data-ttu-id="0e340-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0e340-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e340-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0e340-214">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0e340-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e340-215">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e340-216">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-217">Search-Flags</span></span>           | <span data-ttu-id="0e340-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e340-218">0x00000000</span></span>                                                 |
| <span data-ttu-id="0e340-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-219">System-Flags</span></span>           | <span data-ttu-id="0e340-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e340-220">0x00000010</span></span>                                                 |
| <span data-ttu-id="0e340-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0e340-221">Classes used in</span></span>        | [<span data-ttu-id="0e340-222">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="0e340-222">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0e340-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e340-223">Windows Server 2012</span></span>



| <span data-ttu-id="0e340-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="0e340-224">Entry</span></span> | <span data-ttu-id="0e340-225">Значение</span><span class="sxs-lookup"><span data-stu-id="0e340-225">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e340-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0e340-226">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0e340-227">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="0e340-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="0e340-228">System-Only</span></span>            | <span data-ttu-id="0e340-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-229">False</span></span>                                                      |
| <span data-ttu-id="0e340-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0e340-230">Is-Single-Valued</span></span>       | <span data-ttu-id="0e340-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-231">False</span></span>                                                      |
| <span data-ttu-id="0e340-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0e340-232">Is Indexed</span></span>             | <span data-ttu-id="0e340-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-233">False</span></span>                                                      |
| <span data-ttu-id="0e340-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0e340-234">In Global Catalog</span></span>      | <span data-ttu-id="0e340-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="0e340-235">False</span></span>                                                      |
| <span data-ttu-id="0e340-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0e340-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="0e340-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0e340-237">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="0e340-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0e340-238">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0e340-239">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="0e340-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-240">Search-Flags</span></span>           | <span data-ttu-id="0e340-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0e340-241">0x00000000</span></span>                                                 |
| <span data-ttu-id="0e340-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0e340-242">System-Flags</span></span>           | <span data-ttu-id="0e340-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0e340-243">0x00000010</span></span>                                                 |
| <span data-ttu-id="0e340-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0e340-244">Classes used in</span></span>        | [<span data-ttu-id="0e340-245">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="0e340-245">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





