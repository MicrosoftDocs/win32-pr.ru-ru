---
title: Атрибут комментария
description: Комментарии пользователя. Эта строка может быть пустой строкой.
ms.assetid: c57493b3-a42a-49ad-8f8c-0afadbb3ba09
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута комментария
- Схема AD атрибута info
topic_type:
- apiref
api_name:
- Comment
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd84674fce08f75c3162628b32f67a75fb8c026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804307"
---
# <a name="comment-attribute-ad-schema"></a><span data-ttu-id="963b3-106">Атрибут Comment (схема AD)</span><span class="sxs-lookup"><span data-stu-id="963b3-106">Comment attribute (AD Schema)</span></span>

<span data-ttu-id="963b3-107">Комментарии пользователя.</span><span class="sxs-lookup"><span data-stu-id="963b3-107">The user's comments.</span></span> <span data-ttu-id="963b3-108">Эта строка может быть пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="963b3-108">This string can be a null string.</span></span>



| <span data-ttu-id="963b3-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-109">Entry</span></span> | <span data-ttu-id="963b3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-110">Value</span></span> |
|-------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="963b3-111">CN</span><span class="sxs-lookup"><span data-stu-id="963b3-111">CN</span></span>                | <span data-ttu-id="963b3-112">Комментировать</span><span class="sxs-lookup"><span data-stu-id="963b3-112">Comment</span></span>                                                                  |
| <span data-ttu-id="963b3-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="963b3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="963b3-114">сведения</span><span class="sxs-lookup"><span data-stu-id="963b3-114">info</span></span>                                                                     |
| <span data-ttu-id="963b3-115">Размер</span><span class="sxs-lookup"><span data-stu-id="963b3-115">Size</span></span>              | \-                                                                       |
| <span data-ttu-id="963b3-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="963b3-116">Update Privilege</span></span>  | <span data-ttu-id="963b3-117">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="963b3-117">Domain administrator or account owner.</span></span>                                   |
| <span data-ttu-id="963b3-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="963b3-118">Update Frequency</span></span>  | <span data-ttu-id="963b3-119">Каждый раз, когда пользователю или администратору необходимо добавить комментарии к учетной записи.</span><span class="sxs-lookup"><span data-stu-id="963b3-119">Whenever the user or administrator needs to add comments on the account.</span></span> |
| <span data-ttu-id="963b3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-120">Attribute-Id</span></span>      | <span data-ttu-id="963b3-121">1.2.840.113556.1.2.81</span><span class="sxs-lookup"><span data-stu-id="963b3-121">1.2.840.113556.1.2.81</span></span>                                                    |
| <span data-ttu-id="963b3-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="963b3-122">System-Id-Guid</span></span>    | <span data-ttu-id="963b3-123">bf96793e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="963b3-123">bf96793e-0de6-11d0-a285-00aa003049e2</span></span>                                     |
| <span data-ttu-id="963b3-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="963b3-124">Syntax</span></span>            | [<span data-ttu-id="963b3-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="963b3-125">**String(Unicode)**</span></span>](s-string-unicode.md)                              |



## <a name="implementations"></a><span data-ttu-id="963b3-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="963b3-126">Implementations</span></span>

-   [<span data-ttu-id="963b3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="963b3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="963b3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="963b3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="963b3-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="963b3-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="963b3-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="963b3-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="963b3-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="963b3-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="963b3-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="963b3-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="963b3-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="963b3-133">Windows 2000 Server</span></span>



| <span data-ttu-id="963b3-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-134">Entry</span></span> | <span data-ttu-id="963b3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-135">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="963b3-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="963b3-136">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="963b3-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-137">MAPI-Id</span></span>                | <span data-ttu-id="963b3-138">0x3004</span><span class="sxs-lookup"><span data-stu-id="963b3-138">0x3004</span></span>                                               |
| <span data-ttu-id="963b3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="963b3-139">System-Only</span></span>            | <span data-ttu-id="963b3-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-140">False</span></span>                                                |
| <span data-ttu-id="963b3-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="963b3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="963b3-142">True</span><span class="sxs-lookup"><span data-stu-id="963b3-142">True</span></span>                                                 |
| <span data-ttu-id="963b3-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="963b3-143">Is Indexed</span></span>             | <span data-ttu-id="963b3-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-144">False</span></span>                                                |
| <span data-ttu-id="963b3-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="963b3-145">In Global Catalog</span></span>      | <span data-ttu-id="963b3-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-146">False</span></span>                                                |
| <span data-ttu-id="963b3-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="963b3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="963b3-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="963b3-148">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="963b3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="963b3-149">Range-Lower</span></span>            | <span data-ttu-id="963b3-150">1</span><span class="sxs-lookup"><span data-stu-id="963b3-150">1</span></span>                                                    |
| <span data-ttu-id="963b3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="963b3-151">Range-Upper</span></span>            | <span data-ttu-id="963b3-152">1024</span><span class="sxs-lookup"><span data-stu-id="963b3-152">1024</span></span>                                                 |
| <span data-ttu-id="963b3-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-153">Search-Flags</span></span>           | <span data-ttu-id="963b3-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="963b3-154">0x00000000</span></span>                                           |
| <span data-ttu-id="963b3-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-155">System-Flags</span></span>           | <span data-ttu-id="963b3-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="963b3-156">0x00000010</span></span>                                           |
| <span data-ttu-id="963b3-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="963b3-157">Classes used in</span></span>        | [<span data-ttu-id="963b3-158">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="963b3-158">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="963b3-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="963b3-159">Windows Server 2003</span></span>



| <span data-ttu-id="963b3-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-160">Entry</span></span> | <span data-ttu-id="963b3-161">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-161">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="963b3-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="963b3-162">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="963b3-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-163">MAPI-Id</span></span>                | <span data-ttu-id="963b3-164">0x3004</span><span class="sxs-lookup"><span data-stu-id="963b3-164">0x3004</span></span>                                               |
| <span data-ttu-id="963b3-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="963b3-165">System-Only</span></span>            | <span data-ttu-id="963b3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-166">False</span></span>                                                |
| <span data-ttu-id="963b3-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="963b3-167">Is-Single-Valued</span></span>       | <span data-ttu-id="963b3-168">True</span><span class="sxs-lookup"><span data-stu-id="963b3-168">True</span></span>                                                 |
| <span data-ttu-id="963b3-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="963b3-169">Is Indexed</span></span>             | <span data-ttu-id="963b3-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-170">False</span></span>                                                |
| <span data-ttu-id="963b3-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="963b3-171">In Global Catalog</span></span>      | <span data-ttu-id="963b3-172">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-172">False</span></span>                                                |
| <span data-ttu-id="963b3-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="963b3-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="963b3-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="963b3-174">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="963b3-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="963b3-175">Range-Lower</span></span>            | <span data-ttu-id="963b3-176">1</span><span class="sxs-lookup"><span data-stu-id="963b3-176">1</span></span>                                                    |
| <span data-ttu-id="963b3-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="963b3-177">Range-Upper</span></span>            | <span data-ttu-id="963b3-178">1024</span><span class="sxs-lookup"><span data-stu-id="963b3-178">1024</span></span>                                                 |
| <span data-ttu-id="963b3-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-179">Search-Flags</span></span>           | <span data-ttu-id="963b3-180">0x00000000</span><span class="sxs-lookup"><span data-stu-id="963b3-180">0x00000000</span></span>                                           |
| <span data-ttu-id="963b3-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-181">System-Flags</span></span>           | <span data-ttu-id="963b3-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="963b3-182">0x00000010</span></span>                                           |
| <span data-ttu-id="963b3-183">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="963b3-183">Classes used in</span></span>        | [<span data-ttu-id="963b3-184">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="963b3-184">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="963b3-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="963b3-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="963b3-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-186">Entry</span></span> | <span data-ttu-id="963b3-187">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-187">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="963b3-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="963b3-188">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="963b3-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-189">MAPI-Id</span></span>                | <span data-ttu-id="963b3-190">0x3004</span><span class="sxs-lookup"><span data-stu-id="963b3-190">0x3004</span></span>                                               |
| <span data-ttu-id="963b3-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="963b3-191">System-Only</span></span>            | <span data-ttu-id="963b3-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-192">False</span></span>                                                |
| <span data-ttu-id="963b3-193">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="963b3-193">Is-Single-Valued</span></span>       | <span data-ttu-id="963b3-194">True</span><span class="sxs-lookup"><span data-stu-id="963b3-194">True</span></span>                                                 |
| <span data-ttu-id="963b3-195">Индексируется</span><span class="sxs-lookup"><span data-stu-id="963b3-195">Is Indexed</span></span>             | <span data-ttu-id="963b3-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-196">False</span></span>                                                |
| <span data-ttu-id="963b3-197">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="963b3-197">In Global Catalog</span></span>      | <span data-ttu-id="963b3-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-198">False</span></span>                                                |
| <span data-ttu-id="963b3-199">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="963b3-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="963b3-200">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="963b3-200">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="963b3-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="963b3-201">Range-Lower</span></span>            | <span data-ttu-id="963b3-202">1</span><span class="sxs-lookup"><span data-stu-id="963b3-202">1</span></span>                                                    |
| <span data-ttu-id="963b3-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="963b3-203">Range-Upper</span></span>            | <span data-ttu-id="963b3-204">1024</span><span class="sxs-lookup"><span data-stu-id="963b3-204">1024</span></span>                                                 |
| <span data-ttu-id="963b3-205">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-205">Search-Flags</span></span>           | <span data-ttu-id="963b3-206">0x00000000</span><span class="sxs-lookup"><span data-stu-id="963b3-206">0x00000000</span></span>                                           |
| <span data-ttu-id="963b3-207">System-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-207">System-Flags</span></span>           | <span data-ttu-id="963b3-208">0x00000010</span><span class="sxs-lookup"><span data-stu-id="963b3-208">0x00000010</span></span>                                           |
| <span data-ttu-id="963b3-209">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="963b3-209">Classes used in</span></span>        | [<span data-ttu-id="963b3-210">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="963b3-210">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="963b3-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="963b3-211">Windows Server 2008</span></span>



| <span data-ttu-id="963b3-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-212">Entry</span></span> | <span data-ttu-id="963b3-213">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-213">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="963b3-214">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="963b3-214">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="963b3-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-215">MAPI-Id</span></span>                | <span data-ttu-id="963b3-216">0x3004</span><span class="sxs-lookup"><span data-stu-id="963b3-216">0x3004</span></span>                                               |
| <span data-ttu-id="963b3-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="963b3-217">System-Only</span></span>            | <span data-ttu-id="963b3-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-218">False</span></span>                                                |
| <span data-ttu-id="963b3-219">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="963b3-219">Is-Single-Valued</span></span>       | <span data-ttu-id="963b3-220">True</span><span class="sxs-lookup"><span data-stu-id="963b3-220">True</span></span>                                                 |
| <span data-ttu-id="963b3-221">Индексируется</span><span class="sxs-lookup"><span data-stu-id="963b3-221">Is Indexed</span></span>             | <span data-ttu-id="963b3-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-222">False</span></span>                                                |
| <span data-ttu-id="963b3-223">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="963b3-223">In Global Catalog</span></span>      | <span data-ttu-id="963b3-224">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-224">False</span></span>                                                |
| <span data-ttu-id="963b3-225">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="963b3-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="963b3-226">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="963b3-226">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="963b3-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="963b3-227">Range-Lower</span></span>            | <span data-ttu-id="963b3-228">1</span><span class="sxs-lookup"><span data-stu-id="963b3-228">1</span></span>                                                    |
| <span data-ttu-id="963b3-229">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="963b3-229">Range-Upper</span></span>            | <span data-ttu-id="963b3-230">1024</span><span class="sxs-lookup"><span data-stu-id="963b3-230">1024</span></span>                                                 |
| <span data-ttu-id="963b3-231">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-231">Search-Flags</span></span>           | <span data-ttu-id="963b3-232">0x00000000</span><span class="sxs-lookup"><span data-stu-id="963b3-232">0x00000000</span></span>                                           |
| <span data-ttu-id="963b3-233">System-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-233">System-Flags</span></span>           | <span data-ttu-id="963b3-234">0x00000010</span><span class="sxs-lookup"><span data-stu-id="963b3-234">0x00000010</span></span>                                           |
| <span data-ttu-id="963b3-235">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="963b3-235">Classes used in</span></span>        | [<span data-ttu-id="963b3-236">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="963b3-236">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="963b3-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="963b3-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="963b3-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-238">Entry</span></span> | <span data-ttu-id="963b3-239">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-239">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="963b3-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="963b3-240">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="963b3-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-241">MAPI-Id</span></span>                | <span data-ttu-id="963b3-242">0x3004</span><span class="sxs-lookup"><span data-stu-id="963b3-242">0x3004</span></span>                                               |
| <span data-ttu-id="963b3-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="963b3-243">System-Only</span></span>            | <span data-ttu-id="963b3-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-244">False</span></span>                                                |
| <span data-ttu-id="963b3-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="963b3-245">Is-Single-Valued</span></span>       | <span data-ttu-id="963b3-246">True</span><span class="sxs-lookup"><span data-stu-id="963b3-246">True</span></span>                                                 |
| <span data-ttu-id="963b3-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="963b3-247">Is Indexed</span></span>             | <span data-ttu-id="963b3-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-248">False</span></span>                                                |
| <span data-ttu-id="963b3-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="963b3-249">In Global Catalog</span></span>      | <span data-ttu-id="963b3-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-250">False</span></span>                                                |
| <span data-ttu-id="963b3-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="963b3-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="963b3-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="963b3-252">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="963b3-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="963b3-253">Range-Lower</span></span>            | <span data-ttu-id="963b3-254">1</span><span class="sxs-lookup"><span data-stu-id="963b3-254">1</span></span>                                                    |
| <span data-ttu-id="963b3-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="963b3-255">Range-Upper</span></span>            | <span data-ttu-id="963b3-256">1024</span><span class="sxs-lookup"><span data-stu-id="963b3-256">1024</span></span>                                                 |
| <span data-ttu-id="963b3-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-257">Search-Flags</span></span>           | <span data-ttu-id="963b3-258">0x00000000</span><span class="sxs-lookup"><span data-stu-id="963b3-258">0x00000000</span></span>                                           |
| <span data-ttu-id="963b3-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-259">System-Flags</span></span>           | <span data-ttu-id="963b3-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="963b3-260">0x00000010</span></span>                                           |
| <span data-ttu-id="963b3-261">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="963b3-261">Classes used in</span></span>        | [<span data-ttu-id="963b3-262">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="963b3-262">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="963b3-263">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="963b3-263">Windows Server 2012</span></span>



| <span data-ttu-id="963b3-264">Ввод</span><span class="sxs-lookup"><span data-stu-id="963b3-264">Entry</span></span> | <span data-ttu-id="963b3-265">Значение</span><span class="sxs-lookup"><span data-stu-id="963b3-265">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="963b3-266">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="963b3-266">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="963b3-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="963b3-267">MAPI-Id</span></span>                | <span data-ttu-id="963b3-268">0x3004</span><span class="sxs-lookup"><span data-stu-id="963b3-268">0x3004</span></span>                                               |
| <span data-ttu-id="963b3-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="963b3-269">System-Only</span></span>            | <span data-ttu-id="963b3-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-270">False</span></span>                                                |
| <span data-ttu-id="963b3-271">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="963b3-271">Is-Single-Valued</span></span>       | <span data-ttu-id="963b3-272">True</span><span class="sxs-lookup"><span data-stu-id="963b3-272">True</span></span>                                                 |
| <span data-ttu-id="963b3-273">Индексируется</span><span class="sxs-lookup"><span data-stu-id="963b3-273">Is Indexed</span></span>             | <span data-ttu-id="963b3-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-274">False</span></span>                                                |
| <span data-ttu-id="963b3-275">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="963b3-275">In Global Catalog</span></span>      | <span data-ttu-id="963b3-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="963b3-276">False</span></span>                                                |
| <span data-ttu-id="963b3-277">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="963b3-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="963b3-278">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="963b3-278">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="963b3-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="963b3-279">Range-Lower</span></span>            | <span data-ttu-id="963b3-280">1</span><span class="sxs-lookup"><span data-stu-id="963b3-280">1</span></span>                                                    |
| <span data-ttu-id="963b3-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="963b3-281">Range-Upper</span></span>            | <span data-ttu-id="963b3-282">1024</span><span class="sxs-lookup"><span data-stu-id="963b3-282">1024</span></span>                                                 |
| <span data-ttu-id="963b3-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-283">Search-Flags</span></span>           | <span data-ttu-id="963b3-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="963b3-284">0x00000000</span></span>                                           |
| <span data-ttu-id="963b3-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="963b3-285">System-Flags</span></span>           | <span data-ttu-id="963b3-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="963b3-286">0x00000010</span></span>                                           |
| <span data-ttu-id="963b3-287">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="963b3-287">Classes used in</span></span>        | [<span data-ttu-id="963b3-288">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="963b3-288">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





