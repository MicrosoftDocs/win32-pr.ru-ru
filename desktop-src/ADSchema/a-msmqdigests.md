---
title: Атрибут MSMQ-Digests
description: Массив дайджестов соответствующих сертификатов в атрибуте mSMQ-Sign-Certificates. Они используются для сопоставления дайджеста с сертификатом.
ms.assetid: a9b03edd-1506-4f2d-afe1-7d953977f6fa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MSMQ-Digests
- Схема AD атрибута Мсмкдижестс
topic_type:
- apiref
api_name:
- MSMQ-Digests
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d51c607b1d99af0aed46f259513f4bcf790844
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655398"
---
# <a name="msmq-digests-attribute"></a><span data-ttu-id="4d339-106">Атрибут MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="4d339-106">MSMQ-Digests attribute</span></span>

<span data-ttu-id="4d339-107">Массив дайджестов соответствующих сертификатов в атрибуте mSMQ-Sign-Certificates.</span><span class="sxs-lookup"><span data-stu-id="4d339-107">An array of digests of the corresponding certificates in attribute mSMQ-Sign-Certificates.</span></span> <span data-ttu-id="4d339-108">Они используются для сопоставления дайджеста с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="4d339-108">They are used for mapping a digest into a certificate.</span></span>



| <span data-ttu-id="4d339-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-109">Entry</span></span> | <span data-ttu-id="4d339-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4d339-111">CN</span><span class="sxs-lookup"><span data-stu-id="4d339-111">CN</span></span>                | <span data-ttu-id="4d339-112">MSMQ-Digests</span><span class="sxs-lookup"><span data-stu-id="4d339-112">MSMQ-Digests</span></span>                                          |
| <span data-ttu-id="4d339-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4d339-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4d339-114">мсмкдижестс</span><span class="sxs-lookup"><span data-stu-id="4d339-114">mSMQDigests</span></span>                                           |
| <span data-ttu-id="4d339-115">Размер</span><span class="sxs-lookup"><span data-stu-id="4d339-115">Size</span></span>              | <span data-ttu-id="4d339-116">Каждый дайджест имеет размер 16 байт.</span><span class="sxs-lookup"><span data-stu-id="4d339-116">Each digest is 16 bytes.</span></span>                              |
| <span data-ttu-id="4d339-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4d339-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="4d339-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4d339-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="4d339-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-119">Attribute-Id</span></span>      | <span data-ttu-id="4d339-120">1.2.840.113556.1.4.948</span><span class="sxs-lookup"><span data-stu-id="4d339-120">1.2.840.113556.1.4.948</span></span>                                |
| <span data-ttu-id="4d339-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4d339-121">System-Id-Guid</span></span>    | <span data-ttu-id="4d339-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="4d339-122">9a0dc33c-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="4d339-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d339-123">Syntax</span></span>            | [<span data-ttu-id="4d339-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="4d339-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4d339-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4d339-125">Implementations</span></span>

-   [<span data-ttu-id="4d339-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4d339-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4d339-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4d339-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4d339-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4d339-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4d339-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4d339-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4d339-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4d339-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4d339-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4d339-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4d339-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d339-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4d339-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-133">Entry</span></span> | <span data-ttu-id="4d339-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d339-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d339-135">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-136">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d339-137">System-Only</span></span>            | <span data-ttu-id="4d339-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-138">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d339-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4d339-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-140">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d339-141">Is Indexed</span></span>             | <span data-ttu-id="4d339-142">True</span><span class="sxs-lookup"><span data-stu-id="4d339-142">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d339-143">In Global Catalog</span></span>      | <span data-ttu-id="4d339-144">True</span><span class="sxs-lookup"><span data-stu-id="4d339-144">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d339-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d339-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d339-146">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4d339-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d339-147">Range-Lower</span></span>            | <span data-ttu-id="4d339-148">16</span><span class="sxs-lookup"><span data-stu-id="4d339-148">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d339-149">Range-Upper</span></span>            | <span data-ttu-id="4d339-150">16</span><span class="sxs-lookup"><span data-stu-id="4d339-150">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-151">Search-Flags</span></span>           | <span data-ttu-id="4d339-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4d339-152">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="4d339-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-153">System-Flags</span></span>           | <span data-ttu-id="4d339-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d339-154">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4d339-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d339-155">Classes used in</span></span>        | [<span data-ttu-id="4d339-156">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-156">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4d339-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4d339-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4d339-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d339-158">Windows Server 2003</span></span>



| <span data-ttu-id="4d339-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-159">Entry</span></span> | <span data-ttu-id="4d339-160">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-160">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d339-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d339-161">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-162">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d339-163">System-Only</span></span>            | <span data-ttu-id="4d339-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-164">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d339-165">Is-Single-Valued</span></span>       | <span data-ttu-id="4d339-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-166">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d339-167">Is Indexed</span></span>             | <span data-ttu-id="4d339-168">True</span><span class="sxs-lookup"><span data-stu-id="4d339-168">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d339-169">In Global Catalog</span></span>      | <span data-ttu-id="4d339-170">True</span><span class="sxs-lookup"><span data-stu-id="4d339-170">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d339-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d339-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d339-172">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4d339-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d339-173">Range-Lower</span></span>            | <span data-ttu-id="4d339-174">16</span><span class="sxs-lookup"><span data-stu-id="4d339-174">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d339-175">Range-Upper</span></span>            | <span data-ttu-id="4d339-176">16</span><span class="sxs-lookup"><span data-stu-id="4d339-176">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-177">Search-Flags</span></span>           | <span data-ttu-id="4d339-178">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4d339-178">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="4d339-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-179">System-Flags</span></span>           | <span data-ttu-id="4d339-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d339-180">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4d339-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d339-181">Classes used in</span></span>        | [<span data-ttu-id="4d339-182">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-182">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4d339-183">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4d339-183">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4d339-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4d339-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4d339-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-185">Entry</span></span> | <span data-ttu-id="4d339-186">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-186">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d339-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d339-187">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-188">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d339-189">System-Only</span></span>            | <span data-ttu-id="4d339-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-190">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d339-191">Is-Single-Valued</span></span>       | <span data-ttu-id="4d339-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-192">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d339-193">Is Indexed</span></span>             | <span data-ttu-id="4d339-194">True</span><span class="sxs-lookup"><span data-stu-id="4d339-194">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d339-195">In Global Catalog</span></span>      | <span data-ttu-id="4d339-196">True</span><span class="sxs-lookup"><span data-stu-id="4d339-196">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d339-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d339-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d339-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4d339-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d339-199">Range-Lower</span></span>            | <span data-ttu-id="4d339-200">16</span><span class="sxs-lookup"><span data-stu-id="4d339-200">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d339-201">Range-Upper</span></span>            | <span data-ttu-id="4d339-202">16</span><span class="sxs-lookup"><span data-stu-id="4d339-202">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-203">Search-Flags</span></span>           | <span data-ttu-id="4d339-204">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4d339-204">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="4d339-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-205">System-Flags</span></span>           | <span data-ttu-id="4d339-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d339-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4d339-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d339-207">Classes used in</span></span>        | [<span data-ttu-id="4d339-208">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-208">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4d339-209">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4d339-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4d339-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d339-210">Windows Server 2008</span></span>



| <span data-ttu-id="4d339-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-211">Entry</span></span> | <span data-ttu-id="4d339-212">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d339-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d339-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-214">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d339-215">System-Only</span></span>            | <span data-ttu-id="4d339-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-216">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d339-217">Is-Single-Valued</span></span>       | <span data-ttu-id="4d339-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-218">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d339-219">Is Indexed</span></span>             | <span data-ttu-id="4d339-220">True</span><span class="sxs-lookup"><span data-stu-id="4d339-220">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d339-221">In Global Catalog</span></span>      | <span data-ttu-id="4d339-222">True</span><span class="sxs-lookup"><span data-stu-id="4d339-222">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d339-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d339-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d339-224">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4d339-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d339-225">Range-Lower</span></span>            | <span data-ttu-id="4d339-226">16</span><span class="sxs-lookup"><span data-stu-id="4d339-226">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d339-227">Range-Upper</span></span>            | <span data-ttu-id="4d339-228">16</span><span class="sxs-lookup"><span data-stu-id="4d339-228">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-229">Search-Flags</span></span>           | <span data-ttu-id="4d339-230">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4d339-230">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="4d339-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-231">System-Flags</span></span>           | <span data-ttu-id="4d339-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d339-232">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4d339-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d339-233">Classes used in</span></span>        | [<span data-ttu-id="4d339-234">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-234">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4d339-235">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4d339-235">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4d339-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4d339-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4d339-237">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-237">Entry</span></span> | <span data-ttu-id="4d339-238">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-238">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d339-239">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d339-239">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-240">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-240">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d339-241">System-Only</span></span>            | <span data-ttu-id="4d339-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-242">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d339-243">Is-Single-Valued</span></span>       | <span data-ttu-id="4d339-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-244">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d339-245">Is Indexed</span></span>             | <span data-ttu-id="4d339-246">True</span><span class="sxs-lookup"><span data-stu-id="4d339-246">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d339-247">In Global Catalog</span></span>      | <span data-ttu-id="4d339-248">True</span><span class="sxs-lookup"><span data-stu-id="4d339-248">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d339-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d339-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d339-250">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4d339-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d339-251">Range-Lower</span></span>            | <span data-ttu-id="4d339-252">16</span><span class="sxs-lookup"><span data-stu-id="4d339-252">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d339-253">Range-Upper</span></span>            | <span data-ttu-id="4d339-254">16</span><span class="sxs-lookup"><span data-stu-id="4d339-254">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-255">Search-Flags</span></span>           | <span data-ttu-id="4d339-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4d339-256">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="4d339-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-257">System-Flags</span></span>           | <span data-ttu-id="4d339-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d339-258">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4d339-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d339-259">Classes used in</span></span>        | [<span data-ttu-id="4d339-260">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-260">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4d339-261">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="4d339-261">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4d339-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d339-262">Windows Server 2012</span></span>



| <span data-ttu-id="4d339-263">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d339-263">Entry</span></span> | <span data-ttu-id="4d339-264">Значение</span><span class="sxs-lookup"><span data-stu-id="4d339-264">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d339-265">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d339-265">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-266">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d339-266">MAPI-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4d339-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d339-267">System-Only</span></span>            | <span data-ttu-id="4d339-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-268">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d339-269">Is-Single-Valued</span></span>       | <span data-ttu-id="4d339-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d339-270">False</span></span>                                                                                         |
| <span data-ttu-id="4d339-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d339-271">Is Indexed</span></span>             | <span data-ttu-id="4d339-272">True</span><span class="sxs-lookup"><span data-stu-id="4d339-272">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d339-273">In Global Catalog</span></span>      | <span data-ttu-id="4d339-274">True</span><span class="sxs-lookup"><span data-stu-id="4d339-274">True</span></span>                                                                                          |
| <span data-ttu-id="4d339-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d339-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d339-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d339-276">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4d339-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d339-277">Range-Lower</span></span>            | <span data-ttu-id="4d339-278">16</span><span class="sxs-lookup"><span data-stu-id="4d339-278">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d339-279">Range-Upper</span></span>            | <span data-ttu-id="4d339-280">16</span><span class="sxs-lookup"><span data-stu-id="4d339-280">16</span></span>                                                                                            |
| <span data-ttu-id="4d339-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-281">Search-Flags</span></span>           | <span data-ttu-id="4d339-282">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4d339-282">0x00000001</span></span>                                                                                    |
| <span data-ttu-id="4d339-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d339-283">System-Flags</span></span>           | <span data-ttu-id="4d339-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4d339-284">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4d339-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d339-285">Classes used in</span></span>        | [<span data-ttu-id="4d339-286">**MSMQ — перенесено — пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-286">**MSMQ-Migrated-User**</span></span>](c-msmqmigrateduser.md)<br/> [<span data-ttu-id="4d339-287">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="4d339-287">**User**</span></span>](c-user.md)<br/> |



 

 





