---
title: Атрибут "Shell-property-pages"
description: Порядковый номер и идентификатор GUID страниц свойств для управления объектами Active Directory. Доступ к этим страницам свойств можно получить из оболочки Windows. Дополнительные сведения см. в документе расширение пользовательского интерфейса для объектов каталога.
ms.assetid: e0edd91b-bdb6-47aa-9be2-8a23a89adb26
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "Shell-property-pages"
- Схема AD атрибута Шеллпропертипажес
topic_type:
- apiref
api_name:
- Shell-Property-Pages
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: befad2334a754843fa0ae412565db8c82260f7cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138462"
---
# <a name="shell-property-pages-attribute"></a><span data-ttu-id="b6613-107">Атрибут "Shell-property-pages"</span><span class="sxs-lookup"><span data-stu-id="b6613-107">Shell-Property-Pages attribute</span></span>

<span data-ttu-id="b6613-108">Порядковый номер и идентификатор GUID страниц свойств для управления объектами Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b6613-108">The order number and GUID of property pages for managing Active Directory objects.</span></span> <span data-ttu-id="b6613-109">Доступ к этим страницам свойств можно получить из оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="b6613-109">These property pages can be accessed from the Windows shell.</span></span> <span data-ttu-id="b6613-110">Дополнительные сведения см. в документе расширение пользовательского интерфейса для объектов каталога.</span><span class="sxs-lookup"><span data-stu-id="b6613-110">For more information see the document, Extending the User Interface for Directory Objects.</span></span>



| <span data-ttu-id="b6613-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-111">Entry</span></span> | <span data-ttu-id="b6613-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-112">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="b6613-113">CN</span><span class="sxs-lookup"><span data-stu-id="b6613-113">CN</span></span>                | <span data-ttu-id="b6613-114">Свойства оболочки — страницы</span><span class="sxs-lookup"><span data-stu-id="b6613-114">Shell-Property-Pages</span></span>                           |
| <span data-ttu-id="b6613-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b6613-115">Ldap-Display-Name</span></span> | <span data-ttu-id="b6613-116">шеллпропертипажес</span><span class="sxs-lookup"><span data-stu-id="b6613-116">shellPropertyPages</span></span>                             |
| <span data-ttu-id="b6613-117">Размер</span><span class="sxs-lookup"><span data-stu-id="b6613-117">Size</span></span>              | \-                                             |
| <span data-ttu-id="b6613-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b6613-118">Update Privilege</span></span>  | <span data-ttu-id="b6613-119">Администратор домена или разработчик приложения.</span><span class="sxs-lookup"><span data-stu-id="b6613-119">Domain administrator or application developer.</span></span> |
| <span data-ttu-id="b6613-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b6613-120">Update Frequency</span></span>  | <span data-ttu-id="b6613-121">При добавлении или удалении страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="b6613-121">Whenever a property page is added or removed.</span></span>  |
| <span data-ttu-id="b6613-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-122">Attribute-Id</span></span>      | <span data-ttu-id="b6613-123">1.2.840.113556.1.4.563</span><span class="sxs-lookup"><span data-stu-id="b6613-123">1.2.840.113556.1.4.563</span></span>                         |
| <span data-ttu-id="b6613-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b6613-124">System-Id-Guid</span></span>    | <span data-ttu-id="b6613-125">52458039-ca6a-11D0-аффф-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b6613-125">52458039-ca6a-11d0-afff-0000f80367c1</span></span>           |
| <span data-ttu-id="b6613-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6613-126">Syntax</span></span>            | [<span data-ttu-id="b6613-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="b6613-127">**String(Unicode)**</span></span>](s-string-unicode.md)    |



## <a name="implementations"></a><span data-ttu-id="b6613-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b6613-128">Implementations</span></span>

-   [<span data-ttu-id="b6613-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b6613-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b6613-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b6613-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b6613-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b6613-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b6613-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b6613-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b6613-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b6613-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b6613-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b6613-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b6613-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b6613-135">Windows 2000 Server</span></span>



| <span data-ttu-id="b6613-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-136">Entry</span></span> | <span data-ttu-id="b6613-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-137">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b6613-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b6613-138">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-139">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6613-140">System-Only</span></span>            | <span data-ttu-id="b6613-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-141">False</span></span>                                                      |
| <span data-ttu-id="b6613-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b6613-142">Is-Single-Valued</span></span>       | <span data-ttu-id="b6613-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-143">False</span></span>                                                      |
| <span data-ttu-id="b6613-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b6613-144">Is Indexed</span></span>             | <span data-ttu-id="b6613-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-145">False</span></span>                                                      |
| <span data-ttu-id="b6613-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b6613-146">In Global Catalog</span></span>      | <span data-ttu-id="b6613-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-147">False</span></span>                                                      |
| <span data-ttu-id="b6613-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b6613-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6613-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6613-149">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b6613-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6613-150">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6613-151">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-152">Search-Flags</span></span>           | <span data-ttu-id="b6613-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6613-153">0x00000000</span></span>                                                 |
| <span data-ttu-id="b6613-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-154">System-Flags</span></span>           | <span data-ttu-id="b6613-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6613-155">0x00000010</span></span>                                                 |
| <span data-ttu-id="b6613-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b6613-156">Classes used in</span></span>        | [<span data-ttu-id="b6613-157">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="b6613-157">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b6613-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6613-158">Windows Server 2003</span></span>



| <span data-ttu-id="b6613-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-159">Entry</span></span> | <span data-ttu-id="b6613-160">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-160">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b6613-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b6613-161">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-162">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6613-163">System-Only</span></span>            | <span data-ttu-id="b6613-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-164">False</span></span>                                                      |
| <span data-ttu-id="b6613-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b6613-165">Is-Single-Valued</span></span>       | <span data-ttu-id="b6613-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-166">False</span></span>                                                      |
| <span data-ttu-id="b6613-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b6613-167">Is Indexed</span></span>             | <span data-ttu-id="b6613-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-168">False</span></span>                                                      |
| <span data-ttu-id="b6613-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b6613-169">In Global Catalog</span></span>      | <span data-ttu-id="b6613-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-170">False</span></span>                                                      |
| <span data-ttu-id="b6613-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b6613-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6613-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6613-172">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b6613-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6613-173">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6613-174">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-175">Search-Flags</span></span>           | <span data-ttu-id="b6613-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6613-176">0x00000000</span></span>                                                 |
| <span data-ttu-id="b6613-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-177">System-Flags</span></span>           | <span data-ttu-id="b6613-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6613-178">0x00000010</span></span>                                                 |
| <span data-ttu-id="b6613-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b6613-179">Classes used in</span></span>        | [<span data-ttu-id="b6613-180">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="b6613-180">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b6613-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b6613-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b6613-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-182">Entry</span></span> | <span data-ttu-id="b6613-183">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-183">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b6613-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b6613-184">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-185">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6613-186">System-Only</span></span>            | <span data-ttu-id="b6613-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-187">False</span></span>                                                      |
| <span data-ttu-id="b6613-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b6613-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b6613-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-189">False</span></span>                                                      |
| <span data-ttu-id="b6613-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b6613-190">Is Indexed</span></span>             | <span data-ttu-id="b6613-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-191">False</span></span>                                                      |
| <span data-ttu-id="b6613-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b6613-192">In Global Catalog</span></span>      | <span data-ttu-id="b6613-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-193">False</span></span>                                                      |
| <span data-ttu-id="b6613-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b6613-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6613-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6613-195">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b6613-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6613-196">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6613-197">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-198">Search-Flags</span></span>           | <span data-ttu-id="b6613-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6613-199">0x00000000</span></span>                                                 |
| <span data-ttu-id="b6613-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-200">System-Flags</span></span>           | <span data-ttu-id="b6613-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6613-201">0x00000010</span></span>                                                 |
| <span data-ttu-id="b6613-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b6613-202">Classes used in</span></span>        | [<span data-ttu-id="b6613-203">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="b6613-203">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b6613-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6613-204">Windows Server 2008</span></span>



| <span data-ttu-id="b6613-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-205">Entry</span></span> | <span data-ttu-id="b6613-206">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-206">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b6613-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b6613-207">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-208">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6613-209">System-Only</span></span>            | <span data-ttu-id="b6613-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-210">False</span></span>                                                      |
| <span data-ttu-id="b6613-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b6613-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b6613-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-212">False</span></span>                                                      |
| <span data-ttu-id="b6613-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b6613-213">Is Indexed</span></span>             | <span data-ttu-id="b6613-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-214">False</span></span>                                                      |
| <span data-ttu-id="b6613-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b6613-215">In Global Catalog</span></span>      | <span data-ttu-id="b6613-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-216">False</span></span>                                                      |
| <span data-ttu-id="b6613-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b6613-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6613-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6613-218">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b6613-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6613-219">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6613-220">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-221">Search-Flags</span></span>           | <span data-ttu-id="b6613-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6613-222">0x00000000</span></span>                                                 |
| <span data-ttu-id="b6613-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-223">System-Flags</span></span>           | <span data-ttu-id="b6613-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6613-224">0x00000010</span></span>                                                 |
| <span data-ttu-id="b6613-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b6613-225">Classes used in</span></span>        | [<span data-ttu-id="b6613-226">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="b6613-226">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b6613-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b6613-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b6613-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-228">Entry</span></span> | <span data-ttu-id="b6613-229">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-229">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b6613-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b6613-230">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-231">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6613-232">System-Only</span></span>            | <span data-ttu-id="b6613-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-233">False</span></span>                                                      |
| <span data-ttu-id="b6613-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b6613-234">Is-Single-Valued</span></span>       | <span data-ttu-id="b6613-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-235">False</span></span>                                                      |
| <span data-ttu-id="b6613-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b6613-236">Is Indexed</span></span>             | <span data-ttu-id="b6613-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-237">False</span></span>                                                      |
| <span data-ttu-id="b6613-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b6613-238">In Global Catalog</span></span>      | <span data-ttu-id="b6613-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-239">False</span></span>                                                      |
| <span data-ttu-id="b6613-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b6613-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6613-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6613-241">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b6613-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6613-242">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6613-243">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-244">Search-Flags</span></span>           | <span data-ttu-id="b6613-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6613-245">0x00000000</span></span>                                                 |
| <span data-ttu-id="b6613-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-246">System-Flags</span></span>           | <span data-ttu-id="b6613-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6613-247">0x00000010</span></span>                                                 |
| <span data-ttu-id="b6613-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b6613-248">Classes used in</span></span>        | [<span data-ttu-id="b6613-249">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="b6613-249">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b6613-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b6613-250">Windows Server 2012</span></span>



| <span data-ttu-id="b6613-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="b6613-251">Entry</span></span> | <span data-ttu-id="b6613-252">Значение</span><span class="sxs-lookup"><span data-stu-id="b6613-252">Value</span></span> |
|------------------------|------------------------------------------------------------|
| <span data-ttu-id="b6613-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b6613-253">Link-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b6613-254">MAPI-Id</span></span>                | \-                                                         |
| <span data-ttu-id="b6613-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="b6613-255">System-Only</span></span>            | <span data-ttu-id="b6613-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-256">False</span></span>                                                      |
| <span data-ttu-id="b6613-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b6613-257">Is-Single-Valued</span></span>       | <span data-ttu-id="b6613-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-258">False</span></span>                                                      |
| <span data-ttu-id="b6613-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b6613-259">Is Indexed</span></span>             | <span data-ttu-id="b6613-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-260">False</span></span>                                                      |
| <span data-ttu-id="b6613-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b6613-261">In Global Catalog</span></span>      | <span data-ttu-id="b6613-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="b6613-262">False</span></span>                                                      |
| <span data-ttu-id="b6613-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b6613-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="b6613-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b6613-264">O:BAG:BAD:S:</span></span>                                               |
| <span data-ttu-id="b6613-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b6613-265">Range-Lower</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b6613-266">Range-Upper</span></span>            | \-                                                         |
| <span data-ttu-id="b6613-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-267">Search-Flags</span></span>           | <span data-ttu-id="b6613-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b6613-268">0x00000000</span></span>                                                 |
| <span data-ttu-id="b6613-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b6613-269">System-Flags</span></span>           | <span data-ttu-id="b6613-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b6613-270">0x00000010</span></span>                                                 |
| <span data-ttu-id="b6613-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b6613-271">Classes used in</span></span>        | [<span data-ttu-id="b6613-272">**Описатель вывода**</span><span class="sxs-lookup"><span data-stu-id="b6613-272">**Display-Specifier**</span></span>](c-displayspecifier.md)<br/> |



 

 





