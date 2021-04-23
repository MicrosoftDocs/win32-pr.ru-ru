---
title: Атрибут MSMQ-Sign-Certificates-MIG
description: В смешанном режиме MSMQ атрибут содержит предыдущее значение Мсмксигнцертификатес. MSMQ поддерживает миграцию из DS MSMQ 1,0 в службы Windows 2000 DS, а смешанный режим задает состояние, в котором некоторые из серверов DS не были обновлены до Windows 2000.
ms.assetid: 0dbc5d97-39e6-4863-a386-541ea2abaadc
ms.tgt_platform: multiple
keywords:
- MSMQ-Sign-Certificates-схема AD атрибута MIG
- Схема AD атрибута Мсмксигнцертификатесмиг
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates-Mig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1916cf98d15da1bd84603a2305543e899d868
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655390"
---
# <a name="msmq-sign-certificates-mig-attribute"></a><span data-ttu-id="129fa-106">Атрибут MSMQ-Sign-Certificates-MIG</span><span class="sxs-lookup"><span data-stu-id="129fa-106">MSMQ-Sign-Certificates-Mig attribute</span></span>

<span data-ttu-id="129fa-107">В смешанном режиме MSMQ атрибут содержит предыдущее значение Мсмксигнцертификатес.</span><span class="sxs-lookup"><span data-stu-id="129fa-107">In MSMQ mixed-mode, the attribute contains the previous value of mSMQSignCertificates.</span></span> <span data-ttu-id="129fa-108">MSMQ поддерживает миграцию из DS MSMQ 1,0 в службы Windows 2000 DS, а смешанный режим задает состояние, в котором некоторые из серверов DS не были обновлены до Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="129fa-108">MSMQ supports migration from the MSMQ 1.0 DS to the Windows 2000 DS, and mixed mode specifies a state in which some of the DS severs were not upgraded to Windows 2000.</span></span>



| <span data-ttu-id="129fa-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-109">Entry</span></span> | <span data-ttu-id="129fa-110">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="129fa-111">CN</span><span class="sxs-lookup"><span data-stu-id="129fa-111">CN</span></span>                | <span data-ttu-id="129fa-112">MSMQ-Sign-Certificates-MIG</span><span class="sxs-lookup"><span data-stu-id="129fa-112">MSMQ-Sign-Certificates-Mig</span></span>                            |
| <span data-ttu-id="129fa-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="129fa-113">Ldap-Display-Name</span></span> | <span data-ttu-id="129fa-114">мсмксигнцертификатесмиг</span><span class="sxs-lookup"><span data-stu-id="129fa-114">mSMQSignCertificatesMig</span></span>                               |
| <span data-ttu-id="129fa-115">Размер</span><span class="sxs-lookup"><span data-stu-id="129fa-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="129fa-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="129fa-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="129fa-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="129fa-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="129fa-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-118">Attribute-Id</span></span>      | <span data-ttu-id="129fa-119">1.2.840.113556.1.4.967</span><span class="sxs-lookup"><span data-stu-id="129fa-119">1.2.840.113556.1.4.967</span></span>                                |
| <span data-ttu-id="129fa-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="129fa-120">System-Id-Guid</span></span>    | <span data-ttu-id="129fa-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="129fa-121">3881b8ea-da3b-11d1-90a5-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="129fa-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="129fa-122">Syntax</span></span>            | [<span data-ttu-id="129fa-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="129fa-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="129fa-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="129fa-124">Implementations</span></span>

-   [<span data-ttu-id="129fa-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="129fa-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="129fa-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="129fa-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="129fa-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="129fa-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="129fa-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="129fa-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="129fa-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="129fa-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="129fa-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="129fa-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="129fa-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="129fa-131">Windows 2000 Server</span></span>



| <span data-ttu-id="129fa-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-132">Entry</span></span> | <span data-ttu-id="129fa-133">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fa-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="129fa-134">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-135">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="129fa-136">System-Only</span></span>            | <span data-ttu-id="129fa-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-137">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="129fa-138">Is-Single-Valued</span></span>       | <span data-ttu-id="129fa-139">True</span><span class="sxs-lookup"><span data-stu-id="129fa-139">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="129fa-140">Is Indexed</span></span>             | <span data-ttu-id="129fa-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-141">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="129fa-142">In Global Catalog</span></span>      | <span data-ttu-id="129fa-143">True</span><span class="sxs-lookup"><span data-stu-id="129fa-143">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="129fa-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="129fa-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="129fa-145">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="129fa-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129fa-146">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129fa-147">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-148">Search-Flags</span></span>           | <span data-ttu-id="129fa-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129fa-149">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="129fa-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-150">System-Flags</span></span>           | <span data-ttu-id="129fa-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="129fa-151">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="129fa-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="129fa-152">Classes used in</span></span>        | [<span data-ttu-id="129fa-153">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-153">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="129fa-154">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="129fa-154">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="129fa-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="129fa-155">Windows Server 2003</span></span>



| <span data-ttu-id="129fa-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-156">Entry</span></span> | <span data-ttu-id="129fa-157">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-157">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fa-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="129fa-158">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-159">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="129fa-160">System-Only</span></span>            | <span data-ttu-id="129fa-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-161">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="129fa-162">Is-Single-Valued</span></span>       | <span data-ttu-id="129fa-163">True</span><span class="sxs-lookup"><span data-stu-id="129fa-163">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="129fa-164">Is Indexed</span></span>             | <span data-ttu-id="129fa-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-165">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="129fa-166">In Global Catalog</span></span>      | <span data-ttu-id="129fa-167">True</span><span class="sxs-lookup"><span data-stu-id="129fa-167">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="129fa-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="129fa-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="129fa-169">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="129fa-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129fa-170">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129fa-171">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-172">Search-Flags</span></span>           | <span data-ttu-id="129fa-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129fa-173">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="129fa-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-174">System-Flags</span></span>           | <span data-ttu-id="129fa-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="129fa-175">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="129fa-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="129fa-176">Classes used in</span></span>        | [<span data-ttu-id="129fa-177">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-177">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="129fa-178">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="129fa-178">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="129fa-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="129fa-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="129fa-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-180">Entry</span></span> | <span data-ttu-id="129fa-181">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-181">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fa-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="129fa-182">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-183">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="129fa-184">System-Only</span></span>            | <span data-ttu-id="129fa-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-185">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="129fa-186">Is-Single-Valued</span></span>       | <span data-ttu-id="129fa-187">True</span><span class="sxs-lookup"><span data-stu-id="129fa-187">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="129fa-188">Is Indexed</span></span>             | <span data-ttu-id="129fa-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-189">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="129fa-190">In Global Catalog</span></span>      | <span data-ttu-id="129fa-191">True</span><span class="sxs-lookup"><span data-stu-id="129fa-191">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="129fa-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="129fa-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="129fa-193">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="129fa-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129fa-194">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129fa-195">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-196">Search-Flags</span></span>           | <span data-ttu-id="129fa-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129fa-197">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="129fa-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-198">System-Flags</span></span>           | <span data-ttu-id="129fa-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="129fa-199">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="129fa-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="129fa-200">Classes used in</span></span>        | [<span data-ttu-id="129fa-201">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-201">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="129fa-202">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="129fa-202">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="129fa-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="129fa-203">Windows Server 2008</span></span>



| <span data-ttu-id="129fa-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-204">Entry</span></span> | <span data-ttu-id="129fa-205">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-205">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fa-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="129fa-206">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-207">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="129fa-208">System-Only</span></span>            | <span data-ttu-id="129fa-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-209">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="129fa-210">Is-Single-Valued</span></span>       | <span data-ttu-id="129fa-211">True</span><span class="sxs-lookup"><span data-stu-id="129fa-211">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="129fa-212">Is Indexed</span></span>             | <span data-ttu-id="129fa-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-213">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="129fa-214">In Global Catalog</span></span>      | <span data-ttu-id="129fa-215">True</span><span class="sxs-lookup"><span data-stu-id="129fa-215">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="129fa-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="129fa-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="129fa-217">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="129fa-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129fa-218">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129fa-219">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-220">Search-Flags</span></span>           | <span data-ttu-id="129fa-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129fa-221">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="129fa-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-222">System-Flags</span></span>           | <span data-ttu-id="129fa-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="129fa-223">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="129fa-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="129fa-224">Classes used in</span></span>        | [<span data-ttu-id="129fa-225">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-225">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="129fa-226">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="129fa-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="129fa-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="129fa-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="129fa-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-228">Entry</span></span> | <span data-ttu-id="129fa-229">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-229">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fa-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="129fa-230">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-231">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="129fa-232">System-Only</span></span>            | <span data-ttu-id="129fa-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-233">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="129fa-234">Is-Single-Valued</span></span>       | <span data-ttu-id="129fa-235">True</span><span class="sxs-lookup"><span data-stu-id="129fa-235">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="129fa-236">Is Indexed</span></span>             | <span data-ttu-id="129fa-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-237">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="129fa-238">In Global Catalog</span></span>      | <span data-ttu-id="129fa-239">True</span><span class="sxs-lookup"><span data-stu-id="129fa-239">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="129fa-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="129fa-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="129fa-241">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="129fa-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129fa-242">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129fa-243">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-244">Search-Flags</span></span>           | <span data-ttu-id="129fa-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129fa-245">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="129fa-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-246">System-Flags</span></span>           | <span data-ttu-id="129fa-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="129fa-247">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="129fa-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="129fa-248">Classes used in</span></span>        | [<span data-ttu-id="129fa-249">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-249">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="129fa-250">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="129fa-250">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="129fa-251">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="129fa-251">Windows Server 2012</span></span>



| <span data-ttu-id="129fa-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="129fa-252">Entry</span></span> | <span data-ttu-id="129fa-253">Значение</span><span class="sxs-lookup"><span data-stu-id="129fa-253">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="129fa-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="129fa-254">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="129fa-255">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="129fa-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="129fa-256">System-Only</span></span>            | <span data-ttu-id="129fa-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-257">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="129fa-258">Is-Single-Valued</span></span>       | <span data-ttu-id="129fa-259">True</span><span class="sxs-lookup"><span data-stu-id="129fa-259">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="129fa-260">Is Indexed</span></span>             | <span data-ttu-id="129fa-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="129fa-261">False</span></span>                                                                                         |
| <span data-ttu-id="129fa-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="129fa-262">In Global Catalog</span></span>      | <span data-ttu-id="129fa-263">True</span><span class="sxs-lookup"><span data-stu-id="129fa-263">True</span></span>                                                                                          |
| <span data-ttu-id="129fa-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="129fa-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="129fa-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="129fa-265">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="129fa-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="129fa-266">Range-Lower</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="129fa-267">Range-Upper</span></span>            | \-                                                                                            |
| <span data-ttu-id="129fa-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-268">Search-Flags</span></span>           | <span data-ttu-id="129fa-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="129fa-269">0x00000000</span></span>                                                                                    |
| <span data-ttu-id="129fa-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="129fa-270">System-Flags</span></span>           | <span data-ttu-id="129fa-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="129fa-271">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="129fa-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="129fa-272">Classes used in</span></span>        | [<span data-ttu-id="129fa-273">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-273">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="129fa-274">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="129fa-274">**User**</span></span>](c-user.md)<br/> |



 

 





