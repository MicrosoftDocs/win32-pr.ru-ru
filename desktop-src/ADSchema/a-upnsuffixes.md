---
title: Атрибут UPN-Suffixes
description: Список суффиксов имени участника-пользователя для домена.
ms.assetid: ad861d2d-b643-468c-a346-36ad6a828359
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута UPN-Suffixes
- Схема AD атрибута Упнсуффиксес
topic_type:
- apiref
api_name:
- UPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4aa5fb9398478e4b91fb8f36b8cf96a244935fd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893622"
---
# <a name="upn-suffixes-attribute"></a><span data-ttu-id="c229d-105">Атрибут UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="c229d-105">UPN-Suffixes attribute</span></span>

<span data-ttu-id="c229d-106">Список суффиксов имени участника-пользователя для домена.</span><span class="sxs-lookup"><span data-stu-id="c229d-106">The list of User-Principal-Name suffixes for a domain.</span></span>



| <span data-ttu-id="c229d-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-107">Entry</span></span> | <span data-ttu-id="c229d-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="c229d-109">CN</span><span class="sxs-lookup"><span data-stu-id="c229d-109">CN</span></span>                | <span data-ttu-id="c229d-110">UPN-Suffixes</span><span class="sxs-lookup"><span data-stu-id="c229d-110">UPN-Suffixes</span></span>                                |
| <span data-ttu-id="c229d-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c229d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c229d-112">упнсуффиксес</span><span class="sxs-lookup"><span data-stu-id="c229d-112">uPNSuffixes</span></span>                                 |
| <span data-ttu-id="c229d-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c229d-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="c229d-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c229d-114">Update Privilege</span></span>  | <span data-ttu-id="c229d-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="c229d-115">Domain Administrator</span></span>                        |
| <span data-ttu-id="c229d-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c229d-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="c229d-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-117">Attribute-Id</span></span>      | <span data-ttu-id="c229d-118">1.2.840.113556.1.4.890</span><span class="sxs-lookup"><span data-stu-id="c229d-118">1.2.840.113556.1.4.890</span></span>                      |
| <span data-ttu-id="c229d-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c229d-119">System-Id-Guid</span></span>    | <span data-ttu-id="c229d-120">032160bf-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c229d-120">032160bf-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="c229d-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c229d-121">Syntax</span></span>            | [<span data-ttu-id="c229d-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c229d-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="c229d-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c229d-123">Implementations</span></span>

-   [<span data-ttu-id="c229d-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c229d-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c229d-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c229d-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c229d-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c229d-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c229d-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c229d-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c229d-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c229d-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c229d-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c229d-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c229d-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c229d-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c229d-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c229d-131">Windows 2000 Server</span></span>



| <span data-ttu-id="c229d-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-132">Entry</span></span> | <span data-ttu-id="c229d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-133">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-134">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-135">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-136">System-Only</span></span>            | <span data-ttu-id="c229d-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-137">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-138">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-139">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-140">Is Indexed</span></span>             | <span data-ttu-id="c229d-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-141">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-142">In Global Catalog</span></span>      | <span data-ttu-id="c229d-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-143">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-145">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-146">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-147">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-148">Search-Flags</span></span>           | <span data-ttu-id="c229d-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-149">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-150">System-Flags</span></span>           | <span data-ttu-id="c229d-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-151">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-152">Classes used in</span></span>        | [<span data-ttu-id="c229d-153">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-153">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-154">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-154">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c229d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c229d-155">Windows Server 2003</span></span>



| <span data-ttu-id="c229d-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-156">Entry</span></span> | <span data-ttu-id="c229d-157">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-157">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-158">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-159">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-160">System-Only</span></span>            | <span data-ttu-id="c229d-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-161">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-163">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-164">Is Indexed</span></span>             | <span data-ttu-id="c229d-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-165">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-166">In Global Catalog</span></span>      | <span data-ttu-id="c229d-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-167">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-169">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-170">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-171">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-172">Search-Flags</span></span>           | <span data-ttu-id="c229d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-173">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-174">System-Flags</span></span>           | <span data-ttu-id="c229d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-175">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-176">Classes used in</span></span>        | [<span data-ttu-id="c229d-177">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-177">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-178">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-178">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c229d-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="c229d-179">ADAM</span></span>



| <span data-ttu-id="c229d-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-180">Entry</span></span> | <span data-ttu-id="c229d-181">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-181">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-182">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-183">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-184">System-Only</span></span>            | <span data-ttu-id="c229d-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-185">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-187">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-188">Is Indexed</span></span>             | <span data-ttu-id="c229d-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-189">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-190">In Global Catalog</span></span>      | <span data-ttu-id="c229d-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-191">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-193">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-194">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-195">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-196">Search-Flags</span></span>           | <span data-ttu-id="c229d-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-197">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-198">System-Flags</span></span>           | <span data-ttu-id="c229d-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-199">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-200">Classes used in</span></span>        | [<span data-ttu-id="c229d-201">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-201">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-202">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-202">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c229d-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c229d-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c229d-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-204">Entry</span></span> | <span data-ttu-id="c229d-205">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-205">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-206">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-207">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-208">System-Only</span></span>            | <span data-ttu-id="c229d-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-209">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-210">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-211">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-212">Is Indexed</span></span>             | <span data-ttu-id="c229d-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-213">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-214">In Global Catalog</span></span>      | <span data-ttu-id="c229d-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-215">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-217">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-218">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-219">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-220">Search-Flags</span></span>           | <span data-ttu-id="c229d-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-221">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-222">System-Flags</span></span>           | <span data-ttu-id="c229d-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-223">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-224">Classes used in</span></span>        | [<span data-ttu-id="c229d-225">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-225">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-226">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-226">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c229d-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c229d-227">Windows Server 2008</span></span>



| <span data-ttu-id="c229d-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-228">Entry</span></span> | <span data-ttu-id="c229d-229">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-229">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-230">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-231">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-232">System-Only</span></span>            | <span data-ttu-id="c229d-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-233">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-234">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-235">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-236">Is Indexed</span></span>             | <span data-ttu-id="c229d-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-237">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-238">In Global Catalog</span></span>      | <span data-ttu-id="c229d-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-239">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-241">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-242">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-243">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-244">Search-Flags</span></span>           | <span data-ttu-id="c229d-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-245">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-246">System-Flags</span></span>           | <span data-ttu-id="c229d-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-247">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-248">Classes used in</span></span>        | [<span data-ttu-id="c229d-249">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-249">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-250">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-250">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c229d-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c229d-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c229d-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-252">Entry</span></span> | <span data-ttu-id="c229d-253">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-253">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-254">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-255">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-256">System-Only</span></span>            | <span data-ttu-id="c229d-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-257">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-258">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-259">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-260">Is Indexed</span></span>             | <span data-ttu-id="c229d-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-261">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-262">In Global Catalog</span></span>      | <span data-ttu-id="c229d-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-263">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-265">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-266">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-267">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-268">Search-Flags</span></span>           | <span data-ttu-id="c229d-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-269">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-270">System-Flags</span></span>           | <span data-ttu-id="c229d-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-271">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-272">Classes used in</span></span>        | [<span data-ttu-id="c229d-273">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-273">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-274">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-274">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c229d-275">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c229d-275">Windows Server 2012</span></span>



| <span data-ttu-id="c229d-276">Ввод</span><span class="sxs-lookup"><span data-stu-id="c229d-276">Entry</span></span> | <span data-ttu-id="c229d-277">Значение</span><span class="sxs-lookup"><span data-stu-id="c229d-277">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c229d-278">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c229d-278">Link-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-279">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c229d-279">MAPI-Id</span></span>                | \-                                                                                                                           |
| <span data-ttu-id="c229d-280">System-Only</span><span class="sxs-lookup"><span data-stu-id="c229d-280">System-Only</span></span>            | <span data-ttu-id="c229d-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-281">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-282">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c229d-282">Is-Single-Valued</span></span>       | <span data-ttu-id="c229d-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-283">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-284">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c229d-284">Is Indexed</span></span>             | <span data-ttu-id="c229d-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-285">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-286">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c229d-286">In Global Catalog</span></span>      | <span data-ttu-id="c229d-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="c229d-287">False</span></span>                                                                                                                        |
| <span data-ttu-id="c229d-288">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c229d-288">NT-Security-Descriptor</span></span> | <span data-ttu-id="c229d-289">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c229d-289">O:BAG:BAD:S:</span></span>                                                                                                                 |
| <span data-ttu-id="c229d-290">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c229d-290">Range-Lower</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-291">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c229d-291">Range-Upper</span></span>            | \-                                                                                                                           |
| <span data-ttu-id="c229d-292">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-292">Search-Flags</span></span>           | <span data-ttu-id="c229d-293">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c229d-293">0x00000000</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-294">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c229d-294">System-Flags</span></span>           | <span data-ttu-id="c229d-295">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c229d-295">0x00000010</span></span>                                                                                                                   |
| <span data-ttu-id="c229d-296">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c229d-296">Classes used in</span></span>        | [<span data-ttu-id="c229d-297">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="c229d-297">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> [<span data-ttu-id="c229d-298">**Организационная единица**</span><span class="sxs-lookup"><span data-stu-id="c229d-298">**Organizational-Unit**</span></span>](c-organizationalunit.md)<br/> |



 

 





