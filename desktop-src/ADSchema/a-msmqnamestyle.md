---
title: Атрибут MSMQ-Name-Style
description: Соглашение о стиле имени компьютера.
ms.assetid: dff1c988-77a5-4454-b54c-bb52bf771401
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active Directory в стиле имен MSMQ
- Схема AD атрибута Мсмкнаместиле
topic_type:
- apiref
api_name:
- MSMQ-Name-Style
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9f61b3ec820e4f4771c3e470a19cf79c83e85aa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893445"
---
# <a name="msmq-name-style-attribute"></a><span data-ttu-id="b62d5-105">Атрибут MSMQ-Name-Style</span><span class="sxs-lookup"><span data-stu-id="b62d5-105">MSMQ-Name-Style attribute</span></span>

<span data-ttu-id="b62d5-106">Соглашение о стиле имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="b62d5-106">The convention of computer name style.</span></span>



| <span data-ttu-id="b62d5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-107">Entry</span></span> | <span data-ttu-id="b62d5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b62d5-109">CN</span><span class="sxs-lookup"><span data-stu-id="b62d5-109">CN</span></span>                | <span data-ttu-id="b62d5-110">MSMQ-Name-Style</span><span class="sxs-lookup"><span data-stu-id="b62d5-110">MSMQ-Name-Style</span></span>                      |
| <span data-ttu-id="b62d5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b62d5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b62d5-112">мсмкнаместиле</span><span class="sxs-lookup"><span data-stu-id="b62d5-112">mSMQNameStyle</span></span>                        |
| <span data-ttu-id="b62d5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b62d5-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="b62d5-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b62d5-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="b62d5-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b62d5-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b62d5-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-116">Attribute-Id</span></span>      | <span data-ttu-id="b62d5-117">1.2.840.113556.1.4.939</span><span class="sxs-lookup"><span data-stu-id="b62d5-117">1.2.840.113556.1.4.939</span></span>               |
| <span data-ttu-id="b62d5-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b62d5-118">System-Id-Guid</span></span>    | <span data-ttu-id="b62d5-119">9a0dc333-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="b62d5-119">9a0dc333-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="b62d5-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b62d5-120">Syntax</span></span>            | [<span data-ttu-id="b62d5-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="b62d5-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="b62d5-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b62d5-122">Implementations</span></span>

-   [<span data-ttu-id="b62d5-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b62d5-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b62d5-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b62d5-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b62d5-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b62d5-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b62d5-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b62d5-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b62d5-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b62d5-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b62d5-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b62d5-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b62d5-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b62d5-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b62d5-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-130">Entry</span></span> | <span data-ttu-id="b62d5-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b62d5-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b62d5-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b62d5-134">System-Only</span></span>            | <span data-ttu-id="b62d5-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-135">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b62d5-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b62d5-137">True</span><span class="sxs-lookup"><span data-stu-id="b62d5-137">True</span></span>                                                                    |
| <span data-ttu-id="b62d5-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b62d5-138">Is Indexed</span></span>             | <span data-ttu-id="b62d5-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-139">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b62d5-140">In Global Catalog</span></span>      | <span data-ttu-id="b62d5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-141">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b62d5-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b62d5-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b62d5-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b62d5-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b62d5-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b62d5-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-146">Search-Flags</span></span>           | <span data-ttu-id="b62d5-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b62d5-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="b62d5-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-148">System-Flags</span></span>           | <span data-ttu-id="b62d5-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b62d5-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="b62d5-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b62d5-150">Classes used in</span></span>        | [<span data-ttu-id="b62d5-151">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="b62d5-151">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b62d5-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b62d5-152">Windows Server 2003</span></span>



| <span data-ttu-id="b62d5-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-153">Entry</span></span> | <span data-ttu-id="b62d5-154">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b62d5-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b62d5-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="b62d5-157">System-Only</span></span>            | <span data-ttu-id="b62d5-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-158">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b62d5-159">Is-Single-Valued</span></span>       | <span data-ttu-id="b62d5-160">True</span><span class="sxs-lookup"><span data-stu-id="b62d5-160">True</span></span>                                                                    |
| <span data-ttu-id="b62d5-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b62d5-161">Is Indexed</span></span>             | <span data-ttu-id="b62d5-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-162">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b62d5-163">In Global Catalog</span></span>      | <span data-ttu-id="b62d5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-164">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b62d5-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="b62d5-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b62d5-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b62d5-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b62d5-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b62d5-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-169">Search-Flags</span></span>           | <span data-ttu-id="b62d5-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b62d5-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="b62d5-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-171">System-Flags</span></span>           | <span data-ttu-id="b62d5-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b62d5-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="b62d5-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b62d5-173">Classes used in</span></span>        | [<span data-ttu-id="b62d5-174">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="b62d5-174">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b62d5-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b62d5-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b62d5-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-176">Entry</span></span> | <span data-ttu-id="b62d5-177">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b62d5-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b62d5-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="b62d5-180">System-Only</span></span>            | <span data-ttu-id="b62d5-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-181">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b62d5-182">Is-Single-Valued</span></span>       | <span data-ttu-id="b62d5-183">True</span><span class="sxs-lookup"><span data-stu-id="b62d5-183">True</span></span>                                                                    |
| <span data-ttu-id="b62d5-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b62d5-184">Is Indexed</span></span>             | <span data-ttu-id="b62d5-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-185">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b62d5-186">In Global Catalog</span></span>      | <span data-ttu-id="b62d5-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-187">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b62d5-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="b62d5-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b62d5-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b62d5-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b62d5-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b62d5-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-192">Search-Flags</span></span>           | <span data-ttu-id="b62d5-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b62d5-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="b62d5-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-194">System-Flags</span></span>           | <span data-ttu-id="b62d5-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b62d5-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="b62d5-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b62d5-196">Classes used in</span></span>        | [<span data-ttu-id="b62d5-197">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="b62d5-197">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b62d5-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b62d5-198">Windows Server 2008</span></span>



| <span data-ttu-id="b62d5-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-199">Entry</span></span> | <span data-ttu-id="b62d5-200">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b62d5-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b62d5-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="b62d5-203">System-Only</span></span>            | <span data-ttu-id="b62d5-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-204">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b62d5-205">Is-Single-Valued</span></span>       | <span data-ttu-id="b62d5-206">True</span><span class="sxs-lookup"><span data-stu-id="b62d5-206">True</span></span>                                                                    |
| <span data-ttu-id="b62d5-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b62d5-207">Is Indexed</span></span>             | <span data-ttu-id="b62d5-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-208">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b62d5-209">In Global Catalog</span></span>      | <span data-ttu-id="b62d5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-210">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b62d5-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="b62d5-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b62d5-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b62d5-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b62d5-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b62d5-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-215">Search-Flags</span></span>           | <span data-ttu-id="b62d5-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b62d5-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="b62d5-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-217">System-Flags</span></span>           | <span data-ttu-id="b62d5-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b62d5-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="b62d5-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b62d5-219">Classes used in</span></span>        | [<span data-ttu-id="b62d5-220">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="b62d5-220">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b62d5-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b62d5-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b62d5-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-222">Entry</span></span> | <span data-ttu-id="b62d5-223">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b62d5-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b62d5-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="b62d5-226">System-Only</span></span>            | <span data-ttu-id="b62d5-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-227">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b62d5-228">Is-Single-Valued</span></span>       | <span data-ttu-id="b62d5-229">True</span><span class="sxs-lookup"><span data-stu-id="b62d5-229">True</span></span>                                                                    |
| <span data-ttu-id="b62d5-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b62d5-230">Is Indexed</span></span>             | <span data-ttu-id="b62d5-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-231">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b62d5-232">In Global Catalog</span></span>      | <span data-ttu-id="b62d5-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-233">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b62d5-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="b62d5-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b62d5-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b62d5-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b62d5-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b62d5-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-238">Search-Flags</span></span>           | <span data-ttu-id="b62d5-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b62d5-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="b62d5-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-240">System-Flags</span></span>           | <span data-ttu-id="b62d5-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b62d5-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="b62d5-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b62d5-242">Classes used in</span></span>        | [<span data-ttu-id="b62d5-243">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="b62d5-243">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b62d5-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b62d5-244">Windows Server 2012</span></span>



| <span data-ttu-id="b62d5-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="b62d5-245">Entry</span></span> | <span data-ttu-id="b62d5-246">Значение</span><span class="sxs-lookup"><span data-stu-id="b62d5-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="b62d5-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b62d5-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b62d5-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="b62d5-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="b62d5-249">System-Only</span></span>            | <span data-ttu-id="b62d5-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-250">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b62d5-251">Is-Single-Valued</span></span>       | <span data-ttu-id="b62d5-252">True</span><span class="sxs-lookup"><span data-stu-id="b62d5-252">True</span></span>                                                                    |
| <span data-ttu-id="b62d5-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b62d5-253">Is Indexed</span></span>             | <span data-ttu-id="b62d5-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-254">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b62d5-255">In Global Catalog</span></span>      | <span data-ttu-id="b62d5-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="b62d5-256">False</span></span>                                                                   |
| <span data-ttu-id="b62d5-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b62d5-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="b62d5-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b62d5-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="b62d5-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b62d5-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b62d5-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="b62d5-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-261">Search-Flags</span></span>           | <span data-ttu-id="b62d5-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b62d5-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="b62d5-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b62d5-263">System-Flags</span></span>           | <span data-ttu-id="b62d5-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b62d5-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="b62d5-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b62d5-265">Classes used in</span></span>        | [<span data-ttu-id="b62d5-266">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="b62d5-266">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



 

 





