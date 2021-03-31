---
title: Атрибут MSMQ-Sign-Certificates
description: Этот атрибут содержит несколько сертификатов. Пользователь может создать сертификат для каждого компьютера. Для каждого сертификата также сохраняется дайджест.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута MSMQ-Sign-Certificates
- Схема AD атрибута Мсмксигнцертификатес
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893433"
---
# <a name="msmq-sign-certificates-attribute"></a><span data-ttu-id="e9d04-107">Атрибут MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="e9d04-107">MSMQ-Sign-Certificates attribute</span></span>

<span data-ttu-id="e9d04-108">Этот атрибут содержит несколько сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e9d04-108">This attribute contains a number of certificates.</span></span> <span data-ttu-id="e9d04-109">Пользователь может создать сертификат для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="e9d04-109">A user can generate a certificate per computer.</span></span> <span data-ttu-id="e9d04-110">Для каждого сертификата также сохраняется дайджест.</span><span class="sxs-lookup"><span data-stu-id="e9d04-110">For each certificate we also keep a digest.</span></span>



| <span data-ttu-id="e9d04-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-111">Entry</span></span> | <span data-ttu-id="e9d04-112">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-113">CN</span><span class="sxs-lookup"><span data-stu-id="e9d04-113">CN</span></span>                | <span data-ttu-id="e9d04-114">MSMQ-Sign-Certificates</span><span class="sxs-lookup"><span data-stu-id="e9d04-114">MSMQ-Sign-Certificates</span></span>                                                                 |
| <span data-ttu-id="e9d04-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e9d04-115">Ldap-Display-Name</span></span> | <span data-ttu-id="e9d04-116">мсмксигнцертификатес</span><span class="sxs-lookup"><span data-stu-id="e9d04-116">mSMQSignCertificates</span></span>                                                                   |
| <span data-ttu-id="e9d04-117">Размер</span><span class="sxs-lookup"><span data-stu-id="e9d04-117">Size</span></span>              | <span data-ttu-id="e9d04-118">Тип атрибута — большой двоичный объект, размер не ограничен, и данные хранятся в собственном формате.</span><span class="sxs-lookup"><span data-stu-id="e9d04-118">The attribute type is a BLOB, size is not limited, and data is kept in our own format.</span></span> |
| <span data-ttu-id="e9d04-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e9d04-119">Update Privilege</span></span>  | \-                                                                                     |
| <span data-ttu-id="e9d04-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e9d04-120">Update Frequency</span></span>  | \-                                                                                     |
| <span data-ttu-id="e9d04-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-121">Attribute-Id</span></span>      | <span data-ttu-id="e9d04-122">1.2.840.113556.1.4.947</span><span class="sxs-lookup"><span data-stu-id="e9d04-122">1.2.840.113556.1.4.947</span></span>                                                                 |
| <span data-ttu-id="e9d04-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e9d04-123">System-Id-Guid</span></span>    | <span data-ttu-id="e9d04-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="e9d04-124">9a0dc33b-c100-11d1-bbc5-0080c76670c0</span></span>                                                   |
| <span data-ttu-id="e9d04-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9d04-125">Syntax</span></span>            | [<span data-ttu-id="e9d04-126">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="e9d04-126">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                  |



## <a name="implementations"></a><span data-ttu-id="e9d04-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e9d04-127">Implementations</span></span>

-   [<span data-ttu-id="e9d04-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e9d04-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e9d04-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e9d04-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e9d04-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e9d04-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e9d04-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e9d04-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e9d04-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e9d04-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e9d04-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e9d04-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e9d04-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9d04-134">Windows 2000 Server</span></span>



| <span data-ttu-id="e9d04-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-135">Entry</span></span> | <span data-ttu-id="e9d04-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-136">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9d04-137">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-138">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9d04-139">System-Only</span></span>            | <span data-ttu-id="e9d04-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-140">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9d04-141">Is-Single-Valued</span></span>       | <span data-ttu-id="e9d04-142">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-142">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9d04-143">Is Indexed</span></span>             | <span data-ttu-id="e9d04-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-144">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9d04-145">In Global Catalog</span></span>      | <span data-ttu-id="e9d04-146">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-146">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9d04-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9d04-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9d04-148">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="e9d04-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9d04-149">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9d04-150">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-151">Search-Flags</span></span>           | <span data-ttu-id="e9d04-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9d04-152">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="e9d04-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-153">System-Flags</span></span>           | <span data-ttu-id="e9d04-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9d04-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="e9d04-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9d04-155">Classes used in</span></span>        | [<span data-ttu-id="e9d04-156">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="e9d04-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9d04-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e9d04-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e9d04-158">Windows Server 2003</span></span>



| <span data-ttu-id="e9d04-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-159">Entry</span></span> | <span data-ttu-id="e9d04-160">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9d04-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9d04-163">System-Only</span></span>            | <span data-ttu-id="e9d04-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-164">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9d04-165">Is-Single-Valued</span></span>       | <span data-ttu-id="e9d04-166">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-166">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9d04-167">Is Indexed</span></span>             | <span data-ttu-id="e9d04-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-168">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9d04-169">In Global Catalog</span></span>      | <span data-ttu-id="e9d04-170">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-170">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9d04-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9d04-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9d04-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="e9d04-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9d04-173">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9d04-174">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-175">Search-Flags</span></span>           | <span data-ttu-id="e9d04-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9d04-176">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="e9d04-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-177">System-Flags</span></span>           | <span data-ttu-id="e9d04-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9d04-178">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="e9d04-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9d04-179">Classes used in</span></span>        | [<span data-ttu-id="e9d04-180">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-180">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="e9d04-181">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9d04-181">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e9d04-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e9d04-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e9d04-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-183">Entry</span></span> | <span data-ttu-id="e9d04-184">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9d04-185">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-186">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9d04-187">System-Only</span></span>            | <span data-ttu-id="e9d04-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-188">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9d04-189">Is-Single-Valued</span></span>       | <span data-ttu-id="e9d04-190">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-190">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9d04-191">Is Indexed</span></span>             | <span data-ttu-id="e9d04-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-192">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9d04-193">In Global Catalog</span></span>      | <span data-ttu-id="e9d04-194">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-194">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9d04-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9d04-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9d04-196">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="e9d04-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9d04-197">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9d04-198">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-199">Search-Flags</span></span>           | <span data-ttu-id="e9d04-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9d04-200">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="e9d04-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-201">System-Flags</span></span>           | <span data-ttu-id="e9d04-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9d04-202">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="e9d04-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9d04-203">Classes used in</span></span>        | [<span data-ttu-id="e9d04-204">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-204">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="e9d04-205">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9d04-205">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e9d04-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9d04-206">Windows Server 2008</span></span>



| <span data-ttu-id="e9d04-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-207">Entry</span></span> | <span data-ttu-id="e9d04-208">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-208">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9d04-209">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-210">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9d04-211">System-Only</span></span>            | <span data-ttu-id="e9d04-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-212">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9d04-213">Is-Single-Valued</span></span>       | <span data-ttu-id="e9d04-214">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-214">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9d04-215">Is Indexed</span></span>             | <span data-ttu-id="e9d04-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-216">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9d04-217">In Global Catalog</span></span>      | <span data-ttu-id="e9d04-218">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-218">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9d04-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9d04-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9d04-220">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="e9d04-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9d04-221">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9d04-222">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-223">Search-Flags</span></span>           | <span data-ttu-id="e9d04-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9d04-224">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="e9d04-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-225">System-Flags</span></span>           | <span data-ttu-id="e9d04-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9d04-226">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="e9d04-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9d04-227">Classes used in</span></span>        | [<span data-ttu-id="e9d04-228">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-228">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="e9d04-229">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9d04-229">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e9d04-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e9d04-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e9d04-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-231">Entry</span></span> | <span data-ttu-id="e9d04-232">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-232">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9d04-233">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-234">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9d04-235">System-Only</span></span>            | <span data-ttu-id="e9d04-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-236">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9d04-237">Is-Single-Valued</span></span>       | <span data-ttu-id="e9d04-238">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-238">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9d04-239">Is Indexed</span></span>             | <span data-ttu-id="e9d04-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-240">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9d04-241">In Global Catalog</span></span>      | <span data-ttu-id="e9d04-242">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-242">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9d04-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9d04-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9d04-244">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="e9d04-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9d04-245">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9d04-246">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-247">Search-Flags</span></span>           | <span data-ttu-id="e9d04-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9d04-248">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="e9d04-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-249">System-Flags</span></span>           | <span data-ttu-id="e9d04-250">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9d04-250">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="e9d04-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9d04-251">Classes used in</span></span>        | [<span data-ttu-id="e9d04-252">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-252">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="e9d04-253">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="e9d04-253">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e9d04-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9d04-254">Windows Server 2012</span></span>



| <span data-ttu-id="e9d04-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="e9d04-255">Entry</span></span> | <span data-ttu-id="e9d04-256">Значение</span><span class="sxs-lookup"><span data-stu-id="e9d04-256">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9d04-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e9d04-257">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e9d04-258">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="e9d04-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="e9d04-259">System-Only</span></span>            | <span data-ttu-id="e9d04-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-260">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e9d04-261">Is-Single-Valued</span></span>       | <span data-ttu-id="e9d04-262">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-262">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e9d04-263">Is Indexed</span></span>             | <span data-ttu-id="e9d04-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="e9d04-264">False</span></span>                                                                                         |
| <span data-ttu-id="e9d04-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e9d04-265">In Global Catalog</span></span>      | <span data-ttu-id="e9d04-266">True</span><span class="sxs-lookup"><span data-stu-id="e9d04-266">True</span></span>                                                                                          |
| <span data-ttu-id="e9d04-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e9d04-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="e9d04-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e9d04-268">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="e9d04-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e9d04-269">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e9d04-270">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="e9d04-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-271">Search-Flags</span></span>           | <span data-ttu-id="e9d04-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e9d04-272">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="e9d04-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e9d04-273">System-Flags</span></span>           | <span data-ttu-id="e9d04-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e9d04-274">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="e9d04-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e9d04-275">Classes used in</span></span>        | [<span data-ttu-id="e9d04-276">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-276">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="e9d04-277">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="e9d04-277">**User**</span></span>](c-user.md)<br/> |



 

 





