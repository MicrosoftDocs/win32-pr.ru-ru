---
title: Атрибут "показывать в адресной книге"
description: Этот атрибут используется для указания того, в каких адресных книгах MAPI будет отображаться объект.
ms.assetid: de00da4d-7c04-4d1d-b375-ce3b5eb2f50f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "показывать в адресной книге"
- Схема AD атрибута Шовинаддрессбук
topic_type:
- apiref
api_name:
- Show-In-Address-Book
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44632604c539278c67e9dd46537d8e797e2d70d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493695"
---
# <a name="show-in-address-book-attribute"></a><span data-ttu-id="ca8ca-105">Атрибут "показывать в адресной книге"</span><span class="sxs-lookup"><span data-stu-id="ca8ca-105">Show-In-Address-Book attribute</span></span>

<span data-ttu-id="ca8ca-106">Этот атрибут используется для указания того, в каких адресных книгах MAPI будет отображаться объект.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-106">This attribute is used to indicate in which MAPI address books an object will appear.</span></span> <span data-ttu-id="ca8ca-107">Обычно она поддерживается службой обновления получателей Exchange.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-107">It is usually maintained by the Exchange Recipient Update Service.</span></span>



| <span data-ttu-id="ca8ca-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-108">Entry</span></span> | <span data-ttu-id="ca8ca-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-109">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="ca8ca-110">CN</span><span class="sxs-lookup"><span data-stu-id="ca8ca-110">CN</span></span>                | <span data-ttu-id="ca8ca-111">Отображение в адресной книге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-111">Show-In-Address-Book</span></span>                    |
| <span data-ttu-id="ca8ca-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ca8ca-112">Ldap-Display-Name</span></span> | <span data-ttu-id="ca8ca-113">шовинаддрессбук</span><span class="sxs-lookup"><span data-stu-id="ca8ca-113">showInAddressBook</span></span>                       |
| <span data-ttu-id="ca8ca-114">Размер</span><span class="sxs-lookup"><span data-stu-id="ca8ca-114">Size</span></span>              | \-                                      |
| <span data-ttu-id="ca8ca-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ca8ca-115">Update Privilege</span></span>  | <span data-ttu-id="ca8ca-116">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="ca8ca-116">This is used by the system.</span></span>             |
| <span data-ttu-id="ca8ca-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ca8ca-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="ca8ca-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-118">Attribute-Id</span></span>      | <span data-ttu-id="ca8ca-119">1.2.840.113556.1.4.644</span><span class="sxs-lookup"><span data-stu-id="ca8ca-119">1.2.840.113556.1.4.644</span></span>                  |
| <span data-ttu-id="ca8ca-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ca8ca-120">System-Id-Guid</span></span>    | <span data-ttu-id="ca8ca-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ca8ca-121">3e74f60e-3e73-11d1-a9c0-0000f80367c1</span></span>    |
| <span data-ttu-id="ca8ca-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca8ca-122">Syntax</span></span>            | [<span data-ttu-id="ca8ca-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="ca8ca-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ca8ca-124">Implementations</span></span>

-   [<span data-ttu-id="ca8ca-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ca8ca-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ca8ca-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ca8ca-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ca8ca-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ca8ca-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ca8ca-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ca8ca-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ca8ca-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-132">Entry</span></span> | <span data-ttu-id="ca8ca-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ca8ca-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8ca-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8ca-136">System-Only</span></span>            | <span data-ttu-id="ca8ca-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-137">False</span></span>                                                |
| <span data-ttu-id="ca8ca-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8ca-138">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8ca-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-139">False</span></span>                                                |
| <span data-ttu-id="ca8ca-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8ca-140">Is Indexed</span></span>             | <span data-ttu-id="ca8ca-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-141">False</span></span>                                                |
| <span data-ttu-id="ca8ca-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-142">In Global Catalog</span></span>      | <span data-ttu-id="ca8ca-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-143">False</span></span>                                                |
| <span data-ttu-id="ca8ca-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8ca-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8ca-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ca8ca-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8ca-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8ca-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-148">Search-Flags</span></span>           | <span data-ttu-id="ca8ca-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-149">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-150">System-Flags</span></span>           | <span data-ttu-id="ca8ca-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-151">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8ca-152">Classes used in</span></span>        | [<span data-ttu-id="ca8ca-153">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ca8ca-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ca8ca-154">Windows Server 2003</span></span>



| <span data-ttu-id="ca8ca-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-155">Entry</span></span> | <span data-ttu-id="ca8ca-156">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ca8ca-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8ca-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8ca-159">System-Only</span></span>            | <span data-ttu-id="ca8ca-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-160">False</span></span>                                                |
| <span data-ttu-id="ca8ca-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8ca-161">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8ca-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-162">False</span></span>                                                |
| <span data-ttu-id="ca8ca-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8ca-163">Is Indexed</span></span>             | <span data-ttu-id="ca8ca-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-164">False</span></span>                                                |
| <span data-ttu-id="ca8ca-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-165">In Global Catalog</span></span>      | <span data-ttu-id="ca8ca-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-166">False</span></span>                                                |
| <span data-ttu-id="ca8ca-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8ca-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8ca-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ca8ca-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8ca-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8ca-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-171">Search-Flags</span></span>           | <span data-ttu-id="ca8ca-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-172">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-173">System-Flags</span></span>           | <span data-ttu-id="ca8ca-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-174">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8ca-175">Classes used in</span></span>        | [<span data-ttu-id="ca8ca-176">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-176">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ca8ca-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ca8ca-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ca8ca-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-178">Entry</span></span> | <span data-ttu-id="ca8ca-179">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ca8ca-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8ca-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8ca-182">System-Only</span></span>            | <span data-ttu-id="ca8ca-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-183">False</span></span>                                                |
| <span data-ttu-id="ca8ca-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8ca-184">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8ca-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-185">False</span></span>                                                |
| <span data-ttu-id="ca8ca-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8ca-186">Is Indexed</span></span>             | <span data-ttu-id="ca8ca-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-187">False</span></span>                                                |
| <span data-ttu-id="ca8ca-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-188">In Global Catalog</span></span>      | <span data-ttu-id="ca8ca-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-189">False</span></span>                                                |
| <span data-ttu-id="ca8ca-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8ca-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8ca-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ca8ca-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8ca-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8ca-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-194">Search-Flags</span></span>           | <span data-ttu-id="ca8ca-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-195">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-196">System-Flags</span></span>           | <span data-ttu-id="ca8ca-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-197">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8ca-198">Classes used in</span></span>        | [<span data-ttu-id="ca8ca-199">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-199">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ca8ca-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca8ca-200">Windows Server 2008</span></span>



| <span data-ttu-id="ca8ca-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-201">Entry</span></span> | <span data-ttu-id="ca8ca-202">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ca8ca-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8ca-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8ca-205">System-Only</span></span>            | <span data-ttu-id="ca8ca-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-206">False</span></span>                                                |
| <span data-ttu-id="ca8ca-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8ca-207">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8ca-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-208">False</span></span>                                                |
| <span data-ttu-id="ca8ca-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8ca-209">Is Indexed</span></span>             | <span data-ttu-id="ca8ca-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-210">False</span></span>                                                |
| <span data-ttu-id="ca8ca-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-211">In Global Catalog</span></span>      | <span data-ttu-id="ca8ca-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-212">False</span></span>                                                |
| <span data-ttu-id="ca8ca-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8ca-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8ca-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ca8ca-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8ca-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8ca-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-217">Search-Flags</span></span>           | <span data-ttu-id="ca8ca-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-218">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-219">System-Flags</span></span>           | <span data-ttu-id="ca8ca-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-220">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8ca-221">Classes used in</span></span>        | [<span data-ttu-id="ca8ca-222">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-222">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ca8ca-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ca8ca-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ca8ca-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-224">Entry</span></span> | <span data-ttu-id="ca8ca-225">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ca8ca-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8ca-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8ca-228">System-Only</span></span>            | <span data-ttu-id="ca8ca-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-229">False</span></span>                                                |
| <span data-ttu-id="ca8ca-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8ca-230">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8ca-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-231">False</span></span>                                                |
| <span data-ttu-id="ca8ca-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8ca-232">Is Indexed</span></span>             | <span data-ttu-id="ca8ca-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-233">False</span></span>                                                |
| <span data-ttu-id="ca8ca-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-234">In Global Catalog</span></span>      | <span data-ttu-id="ca8ca-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-235">False</span></span>                                                |
| <span data-ttu-id="ca8ca-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8ca-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8ca-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ca8ca-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8ca-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8ca-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-240">Search-Flags</span></span>           | <span data-ttu-id="ca8ca-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-241">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-242">System-Flags</span></span>           | <span data-ttu-id="ca8ca-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-243">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8ca-244">Classes used in</span></span>        | [<span data-ttu-id="ca8ca-245">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-245">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ca8ca-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca8ca-246">Windows Server 2012</span></span>



| <span data-ttu-id="ca8ca-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="ca8ca-247">Entry</span></span> | <span data-ttu-id="ca8ca-248">Значение</span><span class="sxs-lookup"><span data-stu-id="ca8ca-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="ca8ca-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ca8ca-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ca8ca-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="ca8ca-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="ca8ca-251">System-Only</span></span>            | <span data-ttu-id="ca8ca-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-252">False</span></span>                                                |
| <span data-ttu-id="ca8ca-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ca8ca-253">Is-Single-Valued</span></span>       | <span data-ttu-id="ca8ca-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-254">False</span></span>                                                |
| <span data-ttu-id="ca8ca-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ca8ca-255">Is Indexed</span></span>             | <span data-ttu-id="ca8ca-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-256">False</span></span>                                                |
| <span data-ttu-id="ca8ca-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ca8ca-257">In Global Catalog</span></span>      | <span data-ttu-id="ca8ca-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="ca8ca-258">False</span></span>                                                |
| <span data-ttu-id="ca8ca-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ca8ca-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="ca8ca-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ca8ca-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="ca8ca-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ca8ca-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ca8ca-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="ca8ca-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-263">Search-Flags</span></span>           | <span data-ttu-id="ca8ca-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-264">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ca8ca-265">System-Flags</span></span>           | <span data-ttu-id="ca8ca-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ca8ca-266">0x00000010</span></span>                                           |
| <span data-ttu-id="ca8ca-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ca8ca-267">Classes used in</span></span>        | [<span data-ttu-id="ca8ca-268">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="ca8ca-268">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





