---
title: Атрибут "admin" — "property-pages"
description: Порядковый номер и идентификатор GUID страниц свойств для объекта, отображаемого на экранах администрирования Active Directory. Дополнительные сведения см. в документе расширение пользовательского интерфейса для объектов каталога.
ms.assetid: 70455768-11e0-4d12-ad44-4b3115aa1594
ms.tgt_platform: multiple
keywords:
- Атрибут AD для атрибута "admin-Pages"
- Схема AD атрибута Админпропертипажес
topic_type:
- apiref
api_name:
- Admin-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4e3814662cc8acf1a987cb92a1b9579cc43a4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655544"
---
# <a name="admin-property-pages-attribute"></a><span data-ttu-id="14c1c-106">Атрибут "admin" — "property-pages"</span><span class="sxs-lookup"><span data-stu-id="14c1c-106">Admin-Property-Pages attribute</span></span>

<span data-ttu-id="14c1c-107">Порядковый номер и идентификатор GUID страниц свойств для объекта, отображаемого на экранах администрирования Active Directory.</span><span class="sxs-lookup"><span data-stu-id="14c1c-107">The order number and GUID of the property pages for an object to be displayed on Active Directory administration screens.</span></span> <span data-ttu-id="14c1c-108">Дополнительные сведения см. в документе расширение пользовательского интерфейса для объектов каталога.</span><span class="sxs-lookup"><span data-stu-id="14c1c-108">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="14c1c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-109">Entry</span></span> | <span data-ttu-id="14c1c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-110">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="14c1c-111">CN</span><span class="sxs-lookup"><span data-stu-id="14c1c-111">CN</span></span>                | <span data-ttu-id="14c1c-112">Свойства администрирования — страницы</span><span class="sxs-lookup"><span data-stu-id="14c1c-112">Admin-Property-Pages</span></span>                           |
| <span data-ttu-id="14c1c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="14c1c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="14c1c-114">админпропертипажес</span><span class="sxs-lookup"><span data-stu-id="14c1c-114">adminPropertyPages</span></span>                             |
| <span data-ttu-id="14c1c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="14c1c-115">Size</span></span>              | \-                                             |
| <span data-ttu-id="14c1c-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="14c1c-116">Update Privilege</span></span>  | <span data-ttu-id="14c1c-117">Администратор домена или разработчик приложения.</span><span class="sxs-lookup"><span data-stu-id="14c1c-117">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="14c1c-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="14c1c-118">Update Frequency</span></span>  | <span data-ttu-id="14c1c-119">При добавлении или удалении страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="14c1c-119">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="14c1c-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-120">Attribute-Id</span></span>      | <span data-ttu-id="14c1c-121">1.2.840.113556.1.4.562</span><span class="sxs-lookup"><span data-stu-id="14c1c-121">1.2.840.113556.1.4.562</span></span>                         |
| <span data-ttu-id="14c1c-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="14c1c-122">System-Id-Guid</span></span>    | <span data-ttu-id="14c1c-123">52458038-ca6a-11D0-аффф-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="14c1c-123">52458038-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="14c1c-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14c1c-124">Syntax</span></span>            | [<span data-ttu-id="14c1c-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="14c1c-125">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="14c1c-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="14c1c-126">Implementations</span></span>

-   [<span data-ttu-id="14c1c-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="14c1c-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="14c1c-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="14c1c-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="14c1c-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="14c1c-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="14c1c-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="14c1c-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="14c1c-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14c1c-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="14c1c-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="14c1c-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="14c1c-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="14c1c-133">Windows 2000 Server</span></span>



| <span data-ttu-id="14c1c-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-134">Entry</span></span> | <span data-ttu-id="14c1c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-135">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="14c1c-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14c1c-136">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-137">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="14c1c-138">System-Only</span></span>            | <span data-ttu-id="14c1c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-139">False</span></span>                                                      |
| <span data-ttu-id="14c1c-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14c1c-140">Is-Single-Valued</span></span>       | <span data-ttu-id="14c1c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-141">False</span></span>                                                      |
| <span data-ttu-id="14c1c-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14c1c-142">Is Indexed</span></span>             | <span data-ttu-id="14c1c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-143">False</span></span>                                                      |
| <span data-ttu-id="14c1c-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14c1c-144">In Global Catalog</span></span>      | <span data-ttu-id="14c1c-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-145">False</span></span>                                                      |
| <span data-ttu-id="14c1c-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14c1c-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="14c1c-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14c1c-147">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="14c1c-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14c1c-148">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14c1c-149">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-150">Search-Flags</span></span>           | <span data-ttu-id="14c1c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14c1c-151">0x00000000</span></span>                                                 |
| <span data-ttu-id="14c1c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-152">System-Flags</span></span>           | <span data-ttu-id="14c1c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14c1c-153">0x00000010</span></span>                                                 |
| <span data-ttu-id="14c1c-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14c1c-154">Classes used in</span></span>        | [<span data-ttu-id="14c1c-155">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="14c1c-155">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="14c1c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="14c1c-156">Windows Server 2003</span></span>



| <span data-ttu-id="14c1c-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-157">Entry</span></span> | <span data-ttu-id="14c1c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-158">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="14c1c-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14c1c-159">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-160">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="14c1c-161">System-Only</span></span>            | <span data-ttu-id="14c1c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-162">False</span></span>                                                      |
| <span data-ttu-id="14c1c-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14c1c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="14c1c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-164">False</span></span>                                                      |
| <span data-ttu-id="14c1c-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14c1c-165">Is Indexed</span></span>             | <span data-ttu-id="14c1c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-166">False</span></span>                                                      |
| <span data-ttu-id="14c1c-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14c1c-167">In Global Catalog</span></span>      | <span data-ttu-id="14c1c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-168">False</span></span>                                                      |
| <span data-ttu-id="14c1c-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14c1c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="14c1c-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14c1c-170">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="14c1c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14c1c-171">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14c1c-172">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-173">Search-Flags</span></span>           | <span data-ttu-id="14c1c-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14c1c-174">0x00000000</span></span>                                                 |
| <span data-ttu-id="14c1c-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-175">System-Flags</span></span>           | <span data-ttu-id="14c1c-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14c1c-176">0x00000010</span></span>                                                 |
| <span data-ttu-id="14c1c-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14c1c-177">Classes used in</span></span>        | [<span data-ttu-id="14c1c-178">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="14c1c-178">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="14c1c-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="14c1c-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="14c1c-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-180">Entry</span></span> | <span data-ttu-id="14c1c-181">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-181">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="14c1c-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14c1c-182">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-183">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="14c1c-184">System-Only</span></span>            | <span data-ttu-id="14c1c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-185">False</span></span>                                                      |
| <span data-ttu-id="14c1c-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14c1c-186">Is-Single-Valued</span></span>       | <span data-ttu-id="14c1c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-187">False</span></span>                                                      |
| <span data-ttu-id="14c1c-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14c1c-188">Is Indexed</span></span>             | <span data-ttu-id="14c1c-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-189">False</span></span>                                                      |
| <span data-ttu-id="14c1c-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14c1c-190">In Global Catalog</span></span>      | <span data-ttu-id="14c1c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-191">False</span></span>                                                      |
| <span data-ttu-id="14c1c-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14c1c-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="14c1c-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14c1c-193">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="14c1c-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14c1c-194">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14c1c-195">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-196">Search-Flags</span></span>           | <span data-ttu-id="14c1c-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14c1c-197">0x00000000</span></span>                                                 |
| <span data-ttu-id="14c1c-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-198">System-Flags</span></span>           | <span data-ttu-id="14c1c-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14c1c-199">0x00000010</span></span>                                                 |
| <span data-ttu-id="14c1c-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14c1c-200">Classes used in</span></span>        | [<span data-ttu-id="14c1c-201">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="14c1c-201">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="14c1c-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14c1c-202">Windows Server 2008</span></span>



| <span data-ttu-id="14c1c-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-203">Entry</span></span> | <span data-ttu-id="14c1c-204">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-204">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="14c1c-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14c1c-205">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-206">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="14c1c-207">System-Only</span></span>            | <span data-ttu-id="14c1c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-208">False</span></span>                                                      |
| <span data-ttu-id="14c1c-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14c1c-209">Is-Single-Valued</span></span>       | <span data-ttu-id="14c1c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-210">False</span></span>                                                      |
| <span data-ttu-id="14c1c-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14c1c-211">Is Indexed</span></span>             | <span data-ttu-id="14c1c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-212">False</span></span>                                                      |
| <span data-ttu-id="14c1c-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14c1c-213">In Global Catalog</span></span>      | <span data-ttu-id="14c1c-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-214">False</span></span>                                                      |
| <span data-ttu-id="14c1c-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14c1c-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="14c1c-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14c1c-216">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="14c1c-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14c1c-217">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14c1c-218">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-219">Search-Flags</span></span>           | <span data-ttu-id="14c1c-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14c1c-220">0x00000000</span></span>                                                 |
| <span data-ttu-id="14c1c-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-221">System-Flags</span></span>           | <span data-ttu-id="14c1c-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14c1c-222">0x00000010</span></span>                                                 |
| <span data-ttu-id="14c1c-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14c1c-223">Classes used in</span></span>        | [<span data-ttu-id="14c1c-224">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="14c1c-224">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="14c1c-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14c1c-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="14c1c-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-226">Entry</span></span> | <span data-ttu-id="14c1c-227">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-227">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="14c1c-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14c1c-228">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-229">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="14c1c-230">System-Only</span></span>            | <span data-ttu-id="14c1c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-231">False</span></span>                                                      |
| <span data-ttu-id="14c1c-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14c1c-232">Is-Single-Valued</span></span>       | <span data-ttu-id="14c1c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-233">False</span></span>                                                      |
| <span data-ttu-id="14c1c-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14c1c-234">Is Indexed</span></span>             | <span data-ttu-id="14c1c-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-235">False</span></span>                                                      |
| <span data-ttu-id="14c1c-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14c1c-236">In Global Catalog</span></span>      | <span data-ttu-id="14c1c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-237">False</span></span>                                                      |
| <span data-ttu-id="14c1c-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14c1c-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="14c1c-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14c1c-239">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="14c1c-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14c1c-240">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14c1c-241">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-242">Search-Flags</span></span>           | <span data-ttu-id="14c1c-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14c1c-243">0x00000000</span></span>                                                 |
| <span data-ttu-id="14c1c-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-244">System-Flags</span></span>           | <span data-ttu-id="14c1c-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14c1c-245">0x00000010</span></span>                                                 |
| <span data-ttu-id="14c1c-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14c1c-246">Classes used in</span></span>        | [<span data-ttu-id="14c1c-247">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="14c1c-247">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="14c1c-248">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14c1c-248">Windows Server 2012</span></span>



| <span data-ttu-id="14c1c-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="14c1c-249">Entry</span></span> | <span data-ttu-id="14c1c-250">Значение</span><span class="sxs-lookup"><span data-stu-id="14c1c-250">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="14c1c-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="14c1c-251">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="14c1c-252">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="14c1c-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="14c1c-253">System-Only</span></span>            | <span data-ttu-id="14c1c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-254">False</span></span>                                                      |
| <span data-ttu-id="14c1c-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="14c1c-255">Is-Single-Valued</span></span>       | <span data-ttu-id="14c1c-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-256">False</span></span>                                                      |
| <span data-ttu-id="14c1c-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="14c1c-257">Is Indexed</span></span>             | <span data-ttu-id="14c1c-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-258">False</span></span>                                                      |
| <span data-ttu-id="14c1c-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="14c1c-259">In Global Catalog</span></span>      | <span data-ttu-id="14c1c-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="14c1c-260">False</span></span>                                                      |
| <span data-ttu-id="14c1c-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="14c1c-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="14c1c-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="14c1c-262">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="14c1c-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="14c1c-263">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="14c1c-264">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="14c1c-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-265">Search-Flags</span></span>           | <span data-ttu-id="14c1c-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="14c1c-266">0x00000000</span></span>                                                 |
| <span data-ttu-id="14c1c-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="14c1c-267">System-Flags</span></span>           | <span data-ttu-id="14c1c-268">0x00000010</span><span class="sxs-lookup"><span data-stu-id="14c1c-268">0x00000010</span></span>                                                 |
| <span data-ttu-id="14c1c-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="14c1c-269">Classes used in</span></span>        | [<span data-ttu-id="14c1c-270">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="14c1c-270">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





