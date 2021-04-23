---
title: Атрибут MSMQ-Sign-Key
description: Открытый ключ подписывания компьютера.
ms.assetid: 099cce40-2e6c-409c-bcd3-d38c6b704c0b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active Directory для входа в MSMQ
- Схема AD атрибута Мсмксигнкэй
topic_type:
- apiref
api_name:
- MSMQ-Sign-Key
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60844b6f59c22baa262470af3eca4173f75b6c9d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655143"
---
# <a name="msmq-sign-key-attribute"></a><span data-ttu-id="770ee-105">Атрибут MSMQ-Sign-Key</span><span class="sxs-lookup"><span data-stu-id="770ee-105">MSMQ-Sign-Key attribute</span></span>

<span data-ttu-id="770ee-106">Открытый ключ подписывания компьютера.</span><span class="sxs-lookup"><span data-stu-id="770ee-106">The computer's public signing key.</span></span>



| <span data-ttu-id="770ee-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-107">Entry</span></span> | <span data-ttu-id="770ee-108">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="770ee-109">CN</span><span class="sxs-lookup"><span data-stu-id="770ee-109">CN</span></span>                | <span data-ttu-id="770ee-110">MSMQ-Sign-ключ</span><span class="sxs-lookup"><span data-stu-id="770ee-110">MSMQ-Sign-Key</span></span>                                         |
| <span data-ttu-id="770ee-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="770ee-111">Ldap-Display-Name</span></span> | <span data-ttu-id="770ee-112">мсмксигнкэй</span><span class="sxs-lookup"><span data-stu-id="770ee-112">mSMQSignKey</span></span>                                           |
| <span data-ttu-id="770ee-113">Размер</span><span class="sxs-lookup"><span data-stu-id="770ee-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="770ee-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="770ee-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="770ee-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="770ee-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="770ee-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-116">Attribute-Id</span></span>      | <span data-ttu-id="770ee-117">1.2.840.113556.1.4.937</span><span class="sxs-lookup"><span data-stu-id="770ee-117">1.2.840.113556.1.4.937</span></span>                                |
| <span data-ttu-id="770ee-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="770ee-118">System-Id-Guid</span></span>    | <span data-ttu-id="770ee-119">9a0dc332-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="770ee-119">9a0dc332-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="770ee-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="770ee-120">Syntax</span></span>            | [<span data-ttu-id="770ee-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="770ee-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="770ee-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="770ee-122">Implementations</span></span>

-   [<span data-ttu-id="770ee-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="770ee-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="770ee-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="770ee-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="770ee-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="770ee-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="770ee-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="770ee-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="770ee-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="770ee-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="770ee-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="770ee-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="770ee-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="770ee-129">Windows 2000 Server</span></span>



| <span data-ttu-id="770ee-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-130">Entry</span></span> | <span data-ttu-id="770ee-131">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="770ee-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="770ee-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="770ee-134">System-Only</span></span>            | <span data-ttu-id="770ee-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-135">False</span></span>                                                        |
| <span data-ttu-id="770ee-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="770ee-136">Is-Single-Valued</span></span>       | <span data-ttu-id="770ee-137">True</span><span class="sxs-lookup"><span data-stu-id="770ee-137">True</span></span>                                                         |
| <span data-ttu-id="770ee-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="770ee-138">Is Indexed</span></span>             | <span data-ttu-id="770ee-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-139">False</span></span>                                                        |
| <span data-ttu-id="770ee-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="770ee-140">In Global Catalog</span></span>      | <span data-ttu-id="770ee-141">True</span><span class="sxs-lookup"><span data-stu-id="770ee-141">True</span></span>                                                         |
| <span data-ttu-id="770ee-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="770ee-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="770ee-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="770ee-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="770ee-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="770ee-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="770ee-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-146">Search-Flags</span></span>           | <span data-ttu-id="770ee-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="770ee-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="770ee-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-148">System-Flags</span></span>           | <span data-ttu-id="770ee-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="770ee-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="770ee-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="770ee-150">Classes used in</span></span>        | [<span data-ttu-id="770ee-151">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="770ee-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="770ee-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="770ee-152">Windows Server 2003</span></span>



| <span data-ttu-id="770ee-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-153">Entry</span></span> | <span data-ttu-id="770ee-154">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="770ee-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="770ee-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="770ee-157">System-Only</span></span>            | <span data-ttu-id="770ee-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-158">False</span></span>                                                        |
| <span data-ttu-id="770ee-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="770ee-159">Is-Single-Valued</span></span>       | <span data-ttu-id="770ee-160">True</span><span class="sxs-lookup"><span data-stu-id="770ee-160">True</span></span>                                                         |
| <span data-ttu-id="770ee-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="770ee-161">Is Indexed</span></span>             | <span data-ttu-id="770ee-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-162">False</span></span>                                                        |
| <span data-ttu-id="770ee-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="770ee-163">In Global Catalog</span></span>      | <span data-ttu-id="770ee-164">True</span><span class="sxs-lookup"><span data-stu-id="770ee-164">True</span></span>                                                         |
| <span data-ttu-id="770ee-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="770ee-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="770ee-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="770ee-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="770ee-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="770ee-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="770ee-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-169">Search-Flags</span></span>           | <span data-ttu-id="770ee-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="770ee-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="770ee-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-171">System-Flags</span></span>           | <span data-ttu-id="770ee-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="770ee-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="770ee-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="770ee-173">Classes used in</span></span>        | [<span data-ttu-id="770ee-174">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="770ee-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="770ee-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="770ee-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="770ee-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-176">Entry</span></span> | <span data-ttu-id="770ee-177">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="770ee-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="770ee-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="770ee-180">System-Only</span></span>            | <span data-ttu-id="770ee-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-181">False</span></span>                                                        |
| <span data-ttu-id="770ee-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="770ee-182">Is-Single-Valued</span></span>       | <span data-ttu-id="770ee-183">True</span><span class="sxs-lookup"><span data-stu-id="770ee-183">True</span></span>                                                         |
| <span data-ttu-id="770ee-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="770ee-184">Is Indexed</span></span>             | <span data-ttu-id="770ee-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-185">False</span></span>                                                        |
| <span data-ttu-id="770ee-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="770ee-186">In Global Catalog</span></span>      | <span data-ttu-id="770ee-187">True</span><span class="sxs-lookup"><span data-stu-id="770ee-187">True</span></span>                                                         |
| <span data-ttu-id="770ee-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="770ee-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="770ee-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="770ee-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="770ee-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="770ee-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="770ee-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-192">Search-Flags</span></span>           | <span data-ttu-id="770ee-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="770ee-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="770ee-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-194">System-Flags</span></span>           | <span data-ttu-id="770ee-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="770ee-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="770ee-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="770ee-196">Classes used in</span></span>        | [<span data-ttu-id="770ee-197">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="770ee-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="770ee-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="770ee-198">Windows Server 2008</span></span>



| <span data-ttu-id="770ee-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-199">Entry</span></span> | <span data-ttu-id="770ee-200">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="770ee-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="770ee-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="770ee-203">System-Only</span></span>            | <span data-ttu-id="770ee-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-204">False</span></span>                                                        |
| <span data-ttu-id="770ee-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="770ee-205">Is-Single-Valued</span></span>       | <span data-ttu-id="770ee-206">True</span><span class="sxs-lookup"><span data-stu-id="770ee-206">True</span></span>                                                         |
| <span data-ttu-id="770ee-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="770ee-207">Is Indexed</span></span>             | <span data-ttu-id="770ee-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-208">False</span></span>                                                        |
| <span data-ttu-id="770ee-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="770ee-209">In Global Catalog</span></span>      | <span data-ttu-id="770ee-210">True</span><span class="sxs-lookup"><span data-stu-id="770ee-210">True</span></span>                                                         |
| <span data-ttu-id="770ee-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="770ee-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="770ee-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="770ee-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="770ee-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="770ee-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="770ee-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-215">Search-Flags</span></span>           | <span data-ttu-id="770ee-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="770ee-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="770ee-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-217">System-Flags</span></span>           | <span data-ttu-id="770ee-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="770ee-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="770ee-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="770ee-219">Classes used in</span></span>        | [<span data-ttu-id="770ee-220">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="770ee-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="770ee-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="770ee-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="770ee-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-222">Entry</span></span> | <span data-ttu-id="770ee-223">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="770ee-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="770ee-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="770ee-226">System-Only</span></span>            | <span data-ttu-id="770ee-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-227">False</span></span>                                                        |
| <span data-ttu-id="770ee-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="770ee-228">Is-Single-Valued</span></span>       | <span data-ttu-id="770ee-229">True</span><span class="sxs-lookup"><span data-stu-id="770ee-229">True</span></span>                                                         |
| <span data-ttu-id="770ee-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="770ee-230">Is Indexed</span></span>             | <span data-ttu-id="770ee-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-231">False</span></span>                                                        |
| <span data-ttu-id="770ee-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="770ee-232">In Global Catalog</span></span>      | <span data-ttu-id="770ee-233">True</span><span class="sxs-lookup"><span data-stu-id="770ee-233">True</span></span>                                                         |
| <span data-ttu-id="770ee-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="770ee-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="770ee-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="770ee-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="770ee-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="770ee-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="770ee-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-238">Search-Flags</span></span>           | <span data-ttu-id="770ee-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="770ee-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="770ee-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-240">System-Flags</span></span>           | <span data-ttu-id="770ee-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="770ee-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="770ee-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="770ee-242">Classes used in</span></span>        | [<span data-ttu-id="770ee-243">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="770ee-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="770ee-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="770ee-244">Windows Server 2012</span></span>



| <span data-ttu-id="770ee-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="770ee-245">Entry</span></span> | <span data-ttu-id="770ee-246">Значение</span><span class="sxs-lookup"><span data-stu-id="770ee-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="770ee-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="770ee-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="770ee-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="770ee-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="770ee-249">System-Only</span></span>            | <span data-ttu-id="770ee-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-250">False</span></span>                                                        |
| <span data-ttu-id="770ee-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="770ee-251">Is-Single-Valued</span></span>       | <span data-ttu-id="770ee-252">True</span><span class="sxs-lookup"><span data-stu-id="770ee-252">True</span></span>                                                         |
| <span data-ttu-id="770ee-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="770ee-253">Is Indexed</span></span>             | <span data-ttu-id="770ee-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="770ee-254">False</span></span>                                                        |
| <span data-ttu-id="770ee-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="770ee-255">In Global Catalog</span></span>      | <span data-ttu-id="770ee-256">True</span><span class="sxs-lookup"><span data-stu-id="770ee-256">True</span></span>                                                         |
| <span data-ttu-id="770ee-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="770ee-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="770ee-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="770ee-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="770ee-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="770ee-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="770ee-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="770ee-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-261">Search-Flags</span></span>           | <span data-ttu-id="770ee-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="770ee-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="770ee-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="770ee-263">System-Flags</span></span>           | <span data-ttu-id="770ee-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="770ee-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="770ee-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="770ee-265">Classes used in</span></span>        | [<span data-ttu-id="770ee-266">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="770ee-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





