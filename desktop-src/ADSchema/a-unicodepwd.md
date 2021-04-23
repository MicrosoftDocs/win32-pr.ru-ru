---
title: Атрибут Unicode-Pwd
description: Пароль пользователя в одностороннего формата Windows NT (OWF). Windows 2000 использует Windows NT OWF. Это свойство используется только операционной системой. Обратите внимание, что невозможно получить открытый пароль обратно из формы OWF пароля.
ms.assetid: 07b29a0c-aff2-4abd-8ca8-95f1ce5b566b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Unicode-Pwd
- Схема объявления атрибута unicodePwd
topic_type:
- apiref
api_name:
- Unicode-Pwd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d00a1df180b7a30b56bdf198a78edc77cc99755
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138747"
---
# <a name="unicode-pwd-attribute"></a><span data-ttu-id="bfa7e-108">Атрибут Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="bfa7e-108">Unicode-Pwd attribute</span></span>

<span data-ttu-id="bfa7e-109">Пароль пользователя в одностороннего формата Windows NT (OWF).</span><span class="sxs-lookup"><span data-stu-id="bfa7e-109">The password of the user in Windows NT one-way format (OWF).</span></span> <span data-ttu-id="bfa7e-110">Windows 2000 использует Windows NT OWF.</span><span class="sxs-lookup"><span data-stu-id="bfa7e-110">Windows 2000 uses the Windows NT OWF.</span></span> <span data-ttu-id="bfa7e-111">Это свойство используется только операционной системой.</span><span class="sxs-lookup"><span data-stu-id="bfa7e-111">This property is used only by the operating system.</span></span> <span data-ttu-id="bfa7e-112">Обратите внимание, что невозможно получить открытый пароль обратно из формы OWF пароля.</span><span class="sxs-lookup"><span data-stu-id="bfa7e-112">Note that you cannot derive the clear password back from the OWF form of the password.</span></span>



| <span data-ttu-id="bfa7e-113">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-113">Entry</span></span> | <span data-ttu-id="bfa7e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="bfa7e-115">CN</span><span class="sxs-lookup"><span data-stu-id="bfa7e-115">CN</span></span>                | <span data-ttu-id="bfa7e-116">Unicode-Pwd</span><span class="sxs-lookup"><span data-stu-id="bfa7e-116">Unicode-Pwd</span></span>                                                                  |
| <span data-ttu-id="bfa7e-117">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bfa7e-117">Ldap-Display-Name</span></span> | <span data-ttu-id="bfa7e-118">unicodePwd</span><span class="sxs-lookup"><span data-stu-id="bfa7e-118">unicodePwd</span></span>                                                                   |
| <span data-ttu-id="bfa7e-119">Размер</span><span class="sxs-lookup"><span data-stu-id="bfa7e-119">Size</span></span>              | \-                                                                           |
| <span data-ttu-id="bfa7e-120">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bfa7e-120">Update Privilege</span></span>  | <span data-ttu-id="bfa7e-121">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="bfa7e-121">Domain administrator or account owner.</span></span>                                       |
| <span data-ttu-id="bfa7e-122">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bfa7e-122">Update Frequency</span></span>  | <span data-ttu-id="bfa7e-123">При создании записи пользователя и при необходимости изменения пароля.</span><span class="sxs-lookup"><span data-stu-id="bfa7e-123">When the user's record is created and whenever the password needs to change.</span></span> |
| <span data-ttu-id="bfa7e-124">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-124">Attribute-Id</span></span>      | <span data-ttu-id="bfa7e-125">1.2.840.113556.1.4.90</span><span class="sxs-lookup"><span data-stu-id="bfa7e-125">1.2.840.113556.1.4.90</span></span>                                                        |
| <span data-ttu-id="bfa7e-126">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bfa7e-126">System-Id-Guid</span></span>    | <span data-ttu-id="bfa7e-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bfa7e-127">bf9679e1-0de6-11d0-a285-00aa003049e2</span></span>                                         |
| <span data-ttu-id="bfa7e-128">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfa7e-128">Syntax</span></span>            | [<span data-ttu-id="bfa7e-129">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-129">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                        |



## <a name="implementations"></a><span data-ttu-id="bfa7e-130">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bfa7e-130">Implementations</span></span>

-   [<span data-ttu-id="bfa7e-131">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-131">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bfa7e-132">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-132">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bfa7e-133">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-133">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="bfa7e-134">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-134">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bfa7e-135">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-135">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bfa7e-136">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-136">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bfa7e-137">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-137">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bfa7e-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bfa7e-138">Windows 2000 Server</span></span>



| <span data-ttu-id="bfa7e-139">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-139">Entry</span></span> | <span data-ttu-id="bfa7e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-140">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfa7e-141">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-141">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-142">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-142">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-143">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-143">System-Only</span></span>            | <span data-ttu-id="bfa7e-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-144">False</span></span>                             |
| <span data-ttu-id="bfa7e-145">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-145">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-146">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-146">True</span></span>                              |
| <span data-ttu-id="bfa7e-147">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-147">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-148">False</span></span>                             |
| <span data-ttu-id="bfa7e-149">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-149">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-150">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-150">False</span></span>                             |
| <span data-ttu-id="bfa7e-151">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-151">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-152">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-152">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfa7e-153">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-153">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-154">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-155">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-155">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-156">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-156">0x00000000</span></span>                        |
| <span data-ttu-id="bfa7e-157">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-157">System-Flags</span></span>           | <span data-ttu-id="bfa7e-158">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-158">0x00000010</span></span>                        |
| <span data-ttu-id="bfa7e-159">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-159">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-160">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-160">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bfa7e-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfa7e-161">Windows Server 2003</span></span>



| <span data-ttu-id="bfa7e-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-162">Entry</span></span> | <span data-ttu-id="bfa7e-163">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-163">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfa7e-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-164">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-165">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-166">System-Only</span></span>            | <span data-ttu-id="bfa7e-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-167">False</span></span>                             |
| <span data-ttu-id="bfa7e-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-168">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-169">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-169">True</span></span>                              |
| <span data-ttu-id="bfa7e-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-170">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-171">False</span></span>                             |
| <span data-ttu-id="bfa7e-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-172">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-173">False</span></span>                             |
| <span data-ttu-id="bfa7e-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-175">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfa7e-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-176">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-177">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-178">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-179">0x00000000</span></span>                        |
| <span data-ttu-id="bfa7e-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-180">System-Flags</span></span>           | <span data-ttu-id="bfa7e-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-181">0x00000010</span></span>                        |
| <span data-ttu-id="bfa7e-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-182">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-183">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-183">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="bfa7e-184">ADAM</span><span class="sxs-lookup"><span data-stu-id="bfa7e-184">ADAM</span></span>



| <span data-ttu-id="bfa7e-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-185">Entry</span></span> | <span data-ttu-id="bfa7e-186">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-186">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="bfa7e-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-187">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bfa7e-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-188">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="bfa7e-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-189">System-Only</span></span>            | <span data-ttu-id="bfa7e-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-190">False</span></span>                                                             |
| <span data-ttu-id="bfa7e-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-191">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-192">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-192">True</span></span>                                                              |
| <span data-ttu-id="bfa7e-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-193">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-194">False</span></span>                                                             |
| <span data-ttu-id="bfa7e-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-195">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-196">False</span></span>                                                             |
| <span data-ttu-id="bfa7e-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-198">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="bfa7e-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-199">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="bfa7e-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-200">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="bfa7e-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-201">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-202">0x00000000</span></span>                                                        |
| <span data-ttu-id="bfa7e-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-203">System-Flags</span></span>           | <span data-ttu-id="bfa7e-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-204">0x00000010</span></span>                                                        |
| <span data-ttu-id="bfa7e-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-205">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-206">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-206">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bfa7e-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bfa7e-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bfa7e-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-208">Entry</span></span> | <span data-ttu-id="bfa7e-209">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-209">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfa7e-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-210">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-211">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-212">System-Only</span></span>            | <span data-ttu-id="bfa7e-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-213">False</span></span>                             |
| <span data-ttu-id="bfa7e-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-214">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-215">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-215">True</span></span>                              |
| <span data-ttu-id="bfa7e-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-216">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-217">False</span></span>                             |
| <span data-ttu-id="bfa7e-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-218">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-219">False</span></span>                             |
| <span data-ttu-id="bfa7e-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-221">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfa7e-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-222">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-223">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-224">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-225">0x00000000</span></span>                        |
| <span data-ttu-id="bfa7e-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-226">System-Flags</span></span>           | <span data-ttu-id="bfa7e-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-227">0x00000010</span></span>                        |
| <span data-ttu-id="bfa7e-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-228">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-229">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bfa7e-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfa7e-230">Windows Server 2008</span></span>



| <span data-ttu-id="bfa7e-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-231">Entry</span></span> | <span data-ttu-id="bfa7e-232">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-232">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfa7e-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-233">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-234">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-235">System-Only</span></span>            | <span data-ttu-id="bfa7e-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-236">False</span></span>                             |
| <span data-ttu-id="bfa7e-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-237">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-238">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-238">True</span></span>                              |
| <span data-ttu-id="bfa7e-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-239">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-240">False</span></span>                             |
| <span data-ttu-id="bfa7e-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-241">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-242">False</span></span>                             |
| <span data-ttu-id="bfa7e-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-244">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfa7e-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-245">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-246">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-247">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-248">0x00000000</span></span>                        |
| <span data-ttu-id="bfa7e-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-249">System-Flags</span></span>           | <span data-ttu-id="bfa7e-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-250">0x00000010</span></span>                        |
| <span data-ttu-id="bfa7e-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-251">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-252">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-252">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bfa7e-253">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfa7e-253">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bfa7e-254">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-254">Entry</span></span> | <span data-ttu-id="bfa7e-255">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-255">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfa7e-256">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-256">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-257">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-258">System-Only</span></span>            | <span data-ttu-id="bfa7e-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-259">False</span></span>                             |
| <span data-ttu-id="bfa7e-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-260">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-261">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-261">True</span></span>                              |
| <span data-ttu-id="bfa7e-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-262">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-263">False</span></span>                             |
| <span data-ttu-id="bfa7e-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-264">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-265">False</span></span>                             |
| <span data-ttu-id="bfa7e-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-267">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfa7e-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-268">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-269">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-270">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-271">0x00000000</span></span>                        |
| <span data-ttu-id="bfa7e-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-272">System-Flags</span></span>           | <span data-ttu-id="bfa7e-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-273">0x00000010</span></span>                        |
| <span data-ttu-id="bfa7e-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-274">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-275">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-275">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bfa7e-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfa7e-276">Windows Server 2012</span></span>



| <span data-ttu-id="bfa7e-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfa7e-277">Entry</span></span> | <span data-ttu-id="bfa7e-278">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa7e-278">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfa7e-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfa7e-279">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-280">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfa7e-280">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfa7e-281">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfa7e-281">System-Only</span></span>            | <span data-ttu-id="bfa7e-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-282">False</span></span>                             |
| <span data-ttu-id="bfa7e-283">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfa7e-283">Is-Single-Valued</span></span>       | <span data-ttu-id="bfa7e-284">True</span><span class="sxs-lookup"><span data-stu-id="bfa7e-284">True</span></span>                              |
| <span data-ttu-id="bfa7e-285">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfa7e-285">Is Indexed</span></span>             | <span data-ttu-id="bfa7e-286">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-286">False</span></span>                             |
| <span data-ttu-id="bfa7e-287">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfa7e-287">In Global Catalog</span></span>      | <span data-ttu-id="bfa7e-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfa7e-288">False</span></span>                             |
| <span data-ttu-id="bfa7e-289">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfa7e-289">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfa7e-290">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfa7e-290">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfa7e-291">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfa7e-291">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-292">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfa7e-292">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="bfa7e-293">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-293">Search-Flags</span></span>           | <span data-ttu-id="bfa7e-294">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfa7e-294">0x00000000</span></span>                        |
| <span data-ttu-id="bfa7e-295">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfa7e-295">System-Flags</span></span>           | <span data-ttu-id="bfa7e-296">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfa7e-296">0x00000010</span></span>                        |
| <span data-ttu-id="bfa7e-297">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfa7e-297">Classes used in</span></span>        | [<span data-ttu-id="bfa7e-298">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="bfa7e-298">**User**</span></span>](c-user.md)<br/> |



 

 





