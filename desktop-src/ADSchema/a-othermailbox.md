---
title: Атрибут Other-Mailbox
description: Содержит другие дополнительные адреса электронной почты в форме, например ККМАИЛ Бруцекивер.
ms.assetid: c7e49fbc-fb3a-487e-835b-ad2c1481425a
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Other-Mailbox
- Схема AD атрибута Осермаилбокс
topic_type:
- apiref
api_name:
- Other-Mailbox
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d02bb4031da8938fc38bf25562918204089db08
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655322"
---
# <a name="other-mailbox-attribute"></a><span data-ttu-id="cf608-105">Атрибут Other-Mailbox</span><span class="sxs-lookup"><span data-stu-id="cf608-105">Other-Mailbox attribute</span></span>

<span data-ttu-id="cf608-106">Содержит другие дополнительные адреса электронной почты в форме, например ККМАИЛ: Бруцекивер.</span><span class="sxs-lookup"><span data-stu-id="cf608-106">Contains other additional mail addresses in a form such as CCMAIL: BruceKeever.</span></span>



| <span data-ttu-id="cf608-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-107">Entry</span></span> | <span data-ttu-id="cf608-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-108">Value</span></span> |
|-------------------|----------------------------------------------------------|
| <span data-ttu-id="cf608-109">CN</span><span class="sxs-lookup"><span data-stu-id="cf608-109">CN</span></span>                | <span data-ttu-id="cf608-110">Other-Mailbox</span><span class="sxs-lookup"><span data-stu-id="cf608-110">Other-Mailbox</span></span>                                            |
| <span data-ttu-id="cf608-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cf608-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cf608-112">осермаилбокс</span><span class="sxs-lookup"><span data-stu-id="cf608-112">otherMailbox</span></span>                                             |
| <span data-ttu-id="cf608-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cf608-113">Size</span></span>              | \-                                                       |
| <span data-ttu-id="cf608-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cf608-114">Update Privilege</span></span>  | <span data-ttu-id="cf608-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="cf608-115">Domain administrator</span></span>                                     |
| <span data-ttu-id="cf608-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cf608-116">Update Frequency</span></span>  | <span data-ttu-id="cf608-117">Каждый раз, когда пользователю выдается дополнительный адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cf608-117">Each time the user is issued an additional mail address.</span></span> |
| <span data-ttu-id="cf608-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-118">Attribute-Id</span></span>      | <span data-ttu-id="cf608-119">1.2.840.113556.1.4.651</span><span class="sxs-lookup"><span data-stu-id="cf608-119">1.2.840.113556.1.4.651</span></span>                                   |
| <span data-ttu-id="cf608-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cf608-120">System-Id-Guid</span></span>    | <span data-ttu-id="cf608-121">0296c123-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="cf608-121">0296c123-40da-11d1-a9c0-0000f80367c1</span></span>                     |
| <span data-ttu-id="cf608-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf608-122">Syntax</span></span>            | [<span data-ttu-id="cf608-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="cf608-123">**String(Unicode)**</span></span>](s-string-unicode.md)              |



## <a name="implementations"></a><span data-ttu-id="cf608-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cf608-124">Implementations</span></span>

-   [<span data-ttu-id="cf608-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf608-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf608-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf608-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf608-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf608-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf608-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf608-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf608-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf608-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf608-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf608-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf608-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf608-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cf608-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-132">Entry</span></span> | <span data-ttu-id="cf608-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cf608-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf608-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf608-136">System-Only</span></span>            | <span data-ttu-id="cf608-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-137">False</span></span>                                                              |
| <span data-ttu-id="cf608-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf608-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cf608-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-139">False</span></span>                                                              |
| <span data-ttu-id="cf608-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf608-140">Is Indexed</span></span>             | <span data-ttu-id="cf608-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-141">False</span></span>                                                              |
| <span data-ttu-id="cf608-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf608-142">In Global Catalog</span></span>      | <span data-ttu-id="cf608-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-143">False</span></span>                                                              |
| <span data-ttu-id="cf608-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf608-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf608-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf608-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cf608-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf608-146">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf608-147">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-148">Search-Flags</span></span>           | <span data-ttu-id="cf608-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-149">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-150">System-Flags</span></span>           | <span data-ttu-id="cf608-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf608-152">Classes used in</span></span>        | [<span data-ttu-id="cf608-153">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cf608-153">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf608-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf608-154">Windows Server 2003</span></span>



| <span data-ttu-id="cf608-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-155">Entry</span></span> | <span data-ttu-id="cf608-156">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-156">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cf608-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf608-157">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-158">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf608-159">System-Only</span></span>            | <span data-ttu-id="cf608-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-160">False</span></span>                                                              |
| <span data-ttu-id="cf608-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf608-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cf608-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-162">False</span></span>                                                              |
| <span data-ttu-id="cf608-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf608-163">Is Indexed</span></span>             | <span data-ttu-id="cf608-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-164">False</span></span>                                                              |
| <span data-ttu-id="cf608-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf608-165">In Global Catalog</span></span>      | <span data-ttu-id="cf608-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-166">False</span></span>                                                              |
| <span data-ttu-id="cf608-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf608-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf608-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf608-168">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cf608-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf608-169">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf608-170">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-171">Search-Flags</span></span>           | <span data-ttu-id="cf608-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-172">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-173">System-Flags</span></span>           | <span data-ttu-id="cf608-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-174">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf608-175">Classes used in</span></span>        | [<span data-ttu-id="cf608-176">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cf608-176">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf608-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf608-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf608-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-178">Entry</span></span> | <span data-ttu-id="cf608-179">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-179">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cf608-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf608-180">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-181">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf608-182">System-Only</span></span>            | <span data-ttu-id="cf608-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-183">False</span></span>                                                              |
| <span data-ttu-id="cf608-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf608-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cf608-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-185">False</span></span>                                                              |
| <span data-ttu-id="cf608-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf608-186">Is Indexed</span></span>             | <span data-ttu-id="cf608-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-187">False</span></span>                                                              |
| <span data-ttu-id="cf608-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf608-188">In Global Catalog</span></span>      | <span data-ttu-id="cf608-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-189">False</span></span>                                                              |
| <span data-ttu-id="cf608-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf608-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf608-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf608-191">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cf608-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf608-192">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf608-193">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-194">Search-Flags</span></span>           | <span data-ttu-id="cf608-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-195">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-196">System-Flags</span></span>           | <span data-ttu-id="cf608-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-197">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf608-198">Classes used in</span></span>        | [<span data-ttu-id="cf608-199">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cf608-199">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf608-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf608-200">Windows Server 2008</span></span>



| <span data-ttu-id="cf608-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-201">Entry</span></span> | <span data-ttu-id="cf608-202">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-202">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cf608-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf608-203">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-204">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf608-205">System-Only</span></span>            | <span data-ttu-id="cf608-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-206">False</span></span>                                                              |
| <span data-ttu-id="cf608-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf608-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cf608-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-208">False</span></span>                                                              |
| <span data-ttu-id="cf608-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf608-209">Is Indexed</span></span>             | <span data-ttu-id="cf608-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-210">False</span></span>                                                              |
| <span data-ttu-id="cf608-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf608-211">In Global Catalog</span></span>      | <span data-ttu-id="cf608-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-212">False</span></span>                                                              |
| <span data-ttu-id="cf608-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf608-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf608-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf608-214">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cf608-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf608-215">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf608-216">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-217">Search-Flags</span></span>           | <span data-ttu-id="cf608-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-218">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-219">System-Flags</span></span>           | <span data-ttu-id="cf608-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-220">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf608-221">Classes used in</span></span>        | [<span data-ttu-id="cf608-222">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cf608-222">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf608-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf608-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf608-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-224">Entry</span></span> | <span data-ttu-id="cf608-225">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-225">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cf608-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf608-226">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-227">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf608-228">System-Only</span></span>            | <span data-ttu-id="cf608-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-229">False</span></span>                                                              |
| <span data-ttu-id="cf608-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf608-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cf608-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-231">False</span></span>                                                              |
| <span data-ttu-id="cf608-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf608-232">Is Indexed</span></span>             | <span data-ttu-id="cf608-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-233">False</span></span>                                                              |
| <span data-ttu-id="cf608-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf608-234">In Global Catalog</span></span>      | <span data-ttu-id="cf608-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-235">False</span></span>                                                              |
| <span data-ttu-id="cf608-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf608-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf608-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf608-237">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cf608-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf608-238">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf608-239">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-240">Search-Flags</span></span>           | <span data-ttu-id="cf608-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-241">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-242">System-Flags</span></span>           | <span data-ttu-id="cf608-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-243">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf608-244">Classes used in</span></span>        | [<span data-ttu-id="cf608-245">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cf608-245">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf608-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf608-246">Windows Server 2012</span></span>



| <span data-ttu-id="cf608-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf608-247">Entry</span></span> | <span data-ttu-id="cf608-248">Значение</span><span class="sxs-lookup"><span data-stu-id="cf608-248">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="cf608-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf608-249">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf608-250">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="cf608-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf608-251">System-Only</span></span>            | <span data-ttu-id="cf608-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-252">False</span></span>                                                              |
| <span data-ttu-id="cf608-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf608-253">Is-Single-Valued</span></span>       | <span data-ttu-id="cf608-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-254">False</span></span>                                                              |
| <span data-ttu-id="cf608-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf608-255">Is Indexed</span></span>             | <span data-ttu-id="cf608-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-256">False</span></span>                                                              |
| <span data-ttu-id="cf608-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf608-257">In Global Catalog</span></span>      | <span data-ttu-id="cf608-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf608-258">False</span></span>                                                              |
| <span data-ttu-id="cf608-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf608-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf608-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf608-260">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="cf608-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf608-261">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf608-262">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="cf608-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-263">Search-Flags</span></span>           | <span data-ttu-id="cf608-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-264">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf608-265">System-Flags</span></span>           | <span data-ttu-id="cf608-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf608-266">0x00000000</span></span>                                                         |
| <span data-ttu-id="cf608-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf608-267">Classes used in</span></span>        | [<span data-ttu-id="cf608-268">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cf608-268">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





