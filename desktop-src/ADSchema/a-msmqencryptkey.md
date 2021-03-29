---
title: Атрибут "MSMQ-Encrypt-Key"
description: Открытый ключ шифрования компьютера.
ms.assetid: 2213be9d-9c24-48f7-806a-039c1121d37d
ms.tgt_platform: multiple
keywords:
- Схема Active Directory для атрибутов шифрования MSMQ
- Схема AD атрибута Мсмкенкрипткэй
topic_type:
- apiref
api_name:
- MSMQ-Encrypt-Key
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2c4453deede78620cb76acfec062206812aa87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893782"
---
# <a name="msmq-encrypt-key-attribute"></a><span data-ttu-id="6113b-105">Атрибут "MSMQ-Encrypt-Key"</span><span class="sxs-lookup"><span data-stu-id="6113b-105">MSMQ-Encrypt-Key attribute</span></span>

<span data-ttu-id="6113b-106">Открытый ключ шифрования компьютера.</span><span class="sxs-lookup"><span data-stu-id="6113b-106">The computer's public encryption key.</span></span>



| <span data-ttu-id="6113b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-107">Entry</span></span> | <span data-ttu-id="6113b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6113b-109">CN</span><span class="sxs-lookup"><span data-stu-id="6113b-109">CN</span></span>                | <span data-ttu-id="6113b-110">MSMQ-Encrypt-Key</span><span class="sxs-lookup"><span data-stu-id="6113b-110">MSMQ-Encrypt-Key</span></span>                                      |
| <span data-ttu-id="6113b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6113b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6113b-112">мсмкенкрипткэй</span><span class="sxs-lookup"><span data-stu-id="6113b-112">mSMQEncryptKey</span></span>                                        |
| <span data-ttu-id="6113b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6113b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6113b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6113b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6113b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6113b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6113b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-116">Attribute-Id</span></span>      | <span data-ttu-id="6113b-117">1.2.840.113556.1.4.936</span><span class="sxs-lookup"><span data-stu-id="6113b-117">1.2.840.113556.1.4.936</span></span>                                |
| <span data-ttu-id="6113b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6113b-118">System-Id-Guid</span></span>    | <span data-ttu-id="6113b-119">9a0dc331-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6113b-119">9a0dc331-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="6113b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6113b-120">Syntax</span></span>            | [<span data-ttu-id="6113b-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="6113b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6113b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6113b-122">Implementations</span></span>

-   [<span data-ttu-id="6113b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6113b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6113b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6113b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6113b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6113b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6113b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6113b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6113b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6113b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6113b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6113b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6113b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6113b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6113b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-130">Entry</span></span> | <span data-ttu-id="6113b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6113b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6113b-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6113b-134">System-Only</span></span>            | <span data-ttu-id="6113b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-135">False</span></span>                                                        |
| <span data-ttu-id="6113b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6113b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6113b-137">True</span><span class="sxs-lookup"><span data-stu-id="6113b-137">True</span></span>                                                         |
| <span data-ttu-id="6113b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6113b-138">Is Indexed</span></span>             | <span data-ttu-id="6113b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-139">False</span></span>                                                        |
| <span data-ttu-id="6113b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6113b-140">In Global Catalog</span></span>      | <span data-ttu-id="6113b-141">True</span><span class="sxs-lookup"><span data-stu-id="6113b-141">True</span></span>                                                         |
| <span data-ttu-id="6113b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6113b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6113b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6113b-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6113b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6113b-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6113b-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-146">Search-Flags</span></span>           | <span data-ttu-id="6113b-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6113b-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="6113b-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-148">System-Flags</span></span>           | <span data-ttu-id="6113b-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6113b-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="6113b-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6113b-150">Classes used in</span></span>        | [<span data-ttu-id="6113b-151">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6113b-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6113b-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6113b-152">Windows Server 2003</span></span>



| <span data-ttu-id="6113b-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-153">Entry</span></span> | <span data-ttu-id="6113b-154">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6113b-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6113b-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6113b-157">System-Only</span></span>            | <span data-ttu-id="6113b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-158">False</span></span>                                                        |
| <span data-ttu-id="6113b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6113b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6113b-160">True</span><span class="sxs-lookup"><span data-stu-id="6113b-160">True</span></span>                                                         |
| <span data-ttu-id="6113b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6113b-161">Is Indexed</span></span>             | <span data-ttu-id="6113b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-162">False</span></span>                                                        |
| <span data-ttu-id="6113b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6113b-163">In Global Catalog</span></span>      | <span data-ttu-id="6113b-164">True</span><span class="sxs-lookup"><span data-stu-id="6113b-164">True</span></span>                                                         |
| <span data-ttu-id="6113b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6113b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6113b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6113b-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6113b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6113b-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6113b-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-169">Search-Flags</span></span>           | <span data-ttu-id="6113b-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6113b-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="6113b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-171">System-Flags</span></span>           | <span data-ttu-id="6113b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6113b-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="6113b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6113b-173">Classes used in</span></span>        | [<span data-ttu-id="6113b-174">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6113b-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6113b-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6113b-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6113b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-176">Entry</span></span> | <span data-ttu-id="6113b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6113b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6113b-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6113b-180">System-Only</span></span>            | <span data-ttu-id="6113b-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-181">False</span></span>                                                        |
| <span data-ttu-id="6113b-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6113b-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6113b-183">True</span><span class="sxs-lookup"><span data-stu-id="6113b-183">True</span></span>                                                         |
| <span data-ttu-id="6113b-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6113b-184">Is Indexed</span></span>             | <span data-ttu-id="6113b-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-185">False</span></span>                                                        |
| <span data-ttu-id="6113b-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6113b-186">In Global Catalog</span></span>      | <span data-ttu-id="6113b-187">True</span><span class="sxs-lookup"><span data-stu-id="6113b-187">True</span></span>                                                         |
| <span data-ttu-id="6113b-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6113b-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6113b-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6113b-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6113b-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6113b-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6113b-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-192">Search-Flags</span></span>           | <span data-ttu-id="6113b-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6113b-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="6113b-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-194">System-Flags</span></span>           | <span data-ttu-id="6113b-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6113b-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="6113b-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6113b-196">Classes used in</span></span>        | [<span data-ttu-id="6113b-197">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6113b-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6113b-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6113b-198">Windows Server 2008</span></span>



| <span data-ttu-id="6113b-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-199">Entry</span></span> | <span data-ttu-id="6113b-200">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6113b-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6113b-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6113b-203">System-Only</span></span>            | <span data-ttu-id="6113b-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-204">False</span></span>                                                        |
| <span data-ttu-id="6113b-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6113b-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6113b-206">True</span><span class="sxs-lookup"><span data-stu-id="6113b-206">True</span></span>                                                         |
| <span data-ttu-id="6113b-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6113b-207">Is Indexed</span></span>             | <span data-ttu-id="6113b-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-208">False</span></span>                                                        |
| <span data-ttu-id="6113b-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6113b-209">In Global Catalog</span></span>      | <span data-ttu-id="6113b-210">True</span><span class="sxs-lookup"><span data-stu-id="6113b-210">True</span></span>                                                         |
| <span data-ttu-id="6113b-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6113b-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6113b-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6113b-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6113b-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6113b-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6113b-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-215">Search-Flags</span></span>           | <span data-ttu-id="6113b-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6113b-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="6113b-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-217">System-Flags</span></span>           | <span data-ttu-id="6113b-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6113b-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="6113b-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6113b-219">Classes used in</span></span>        | [<span data-ttu-id="6113b-220">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6113b-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6113b-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6113b-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6113b-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-222">Entry</span></span> | <span data-ttu-id="6113b-223">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6113b-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6113b-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="6113b-226">System-Only</span></span>            | <span data-ttu-id="6113b-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-227">False</span></span>                                                        |
| <span data-ttu-id="6113b-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6113b-228">Is-Single-Valued</span></span>       | <span data-ttu-id="6113b-229">True</span><span class="sxs-lookup"><span data-stu-id="6113b-229">True</span></span>                                                         |
| <span data-ttu-id="6113b-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6113b-230">Is Indexed</span></span>             | <span data-ttu-id="6113b-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-231">False</span></span>                                                        |
| <span data-ttu-id="6113b-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6113b-232">In Global Catalog</span></span>      | <span data-ttu-id="6113b-233">True</span><span class="sxs-lookup"><span data-stu-id="6113b-233">True</span></span>                                                         |
| <span data-ttu-id="6113b-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6113b-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="6113b-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6113b-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6113b-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6113b-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6113b-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-238">Search-Flags</span></span>           | <span data-ttu-id="6113b-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6113b-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="6113b-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-240">System-Flags</span></span>           | <span data-ttu-id="6113b-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6113b-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="6113b-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6113b-242">Classes used in</span></span>        | [<span data-ttu-id="6113b-243">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6113b-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6113b-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6113b-244">Windows Server 2012</span></span>



| <span data-ttu-id="6113b-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="6113b-245">Entry</span></span> | <span data-ttu-id="6113b-246">Значение</span><span class="sxs-lookup"><span data-stu-id="6113b-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6113b-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6113b-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6113b-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6113b-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="6113b-249">System-Only</span></span>            | <span data-ttu-id="6113b-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-250">False</span></span>                                                        |
| <span data-ttu-id="6113b-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6113b-251">Is-Single-Valued</span></span>       | <span data-ttu-id="6113b-252">True</span><span class="sxs-lookup"><span data-stu-id="6113b-252">True</span></span>                                                         |
| <span data-ttu-id="6113b-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6113b-253">Is Indexed</span></span>             | <span data-ttu-id="6113b-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="6113b-254">False</span></span>                                                        |
| <span data-ttu-id="6113b-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6113b-255">In Global Catalog</span></span>      | <span data-ttu-id="6113b-256">True</span><span class="sxs-lookup"><span data-stu-id="6113b-256">True</span></span>                                                         |
| <span data-ttu-id="6113b-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6113b-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="6113b-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6113b-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6113b-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6113b-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6113b-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6113b-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-261">Search-Flags</span></span>           | <span data-ttu-id="6113b-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6113b-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="6113b-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6113b-263">System-Flags</span></span>           | <span data-ttu-id="6113b-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6113b-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="6113b-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6113b-265">Classes used in</span></span>        | [<span data-ttu-id="6113b-266">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6113b-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





