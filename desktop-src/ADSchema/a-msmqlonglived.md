---
title: MSMQ — атрибут долгосрочного существования
description: Срок жизни сообщений MSMQ по умолчанию.
ms.assetid: e47bcb0e-6e30-4300-9cfa-c553c2842416
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута долгосрочного существования MSMQ
- Схема AD атрибута Мсмклонгливед
topic_type:
- apiref
api_name:
- MSMQ-Long-Lived
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d175a6ed59114eaa591f8e45a9c1291652d9e037
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493779"
---
# <a name="msmq-long-lived-attribute"></a><span data-ttu-id="c536e-105">MSMQ — атрибут долгосрочного существования</span><span class="sxs-lookup"><span data-stu-id="c536e-105">MSMQ-Long-Lived attribute</span></span>

<span data-ttu-id="c536e-106">Срок жизни сообщений MSMQ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c536e-106">The default time to live of MSMQ messages.</span></span>



| <span data-ttu-id="c536e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-107">Entry</span></span> | <span data-ttu-id="c536e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c536e-109">CN</span><span class="sxs-lookup"><span data-stu-id="c536e-109">CN</span></span>                | <span data-ttu-id="c536e-110">MSMQ — долгосрочные</span><span class="sxs-lookup"><span data-stu-id="c536e-110">MSMQ-Long-Lived</span></span>                      |
| <span data-ttu-id="c536e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c536e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c536e-112">мсмклонгливед</span><span class="sxs-lookup"><span data-stu-id="c536e-112">mSMQLongLived</span></span>                        |
| <span data-ttu-id="c536e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c536e-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="c536e-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c536e-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c536e-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c536e-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c536e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-116">Attribute-Id</span></span>      | <span data-ttu-id="c536e-117">1.2.840.113556.1.4.941</span><span class="sxs-lookup"><span data-stu-id="c536e-117">1.2.840.113556.1.4.941</span></span>               |
| <span data-ttu-id="c536e-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c536e-118">System-Id-Guid</span></span>    | <span data-ttu-id="c536e-119">9a0dc335-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="c536e-119">9a0dc335-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="c536e-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c536e-120">Syntax</span></span>            | [<span data-ttu-id="c536e-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="c536e-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c536e-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c536e-122">Implementations</span></span>

-   [<span data-ttu-id="c536e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c536e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c536e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c536e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c536e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c536e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c536e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c536e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c536e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c536e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c536e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c536e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c536e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c536e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c536e-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-130">Entry</span></span> | <span data-ttu-id="c536e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c536e-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c536e-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c536e-134">System-Only</span></span>            | <span data-ttu-id="c536e-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-135">False</span></span>                                                                   |
| <span data-ttu-id="c536e-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c536e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c536e-137">True</span><span class="sxs-lookup"><span data-stu-id="c536e-137">True</span></span>                                                                    |
| <span data-ttu-id="c536e-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c536e-138">Is Indexed</span></span>             | <span data-ttu-id="c536e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-139">False</span></span>                                                                   |
| <span data-ttu-id="c536e-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c536e-140">In Global Catalog</span></span>      | <span data-ttu-id="c536e-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-141">False</span></span>                                                                   |
| <span data-ttu-id="c536e-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c536e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c536e-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c536e-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c536e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c536e-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c536e-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-146">Search-Flags</span></span>           | <span data-ttu-id="c536e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c536e-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="c536e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-148">System-Flags</span></span>           | <span data-ttu-id="c536e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c536e-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="c536e-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c536e-150">Classes used in</span></span>        | [<span data-ttu-id="c536e-151">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="c536e-151">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c536e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c536e-152">Windows Server 2003</span></span>



| <span data-ttu-id="c536e-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-153">Entry</span></span> | <span data-ttu-id="c536e-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c536e-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c536e-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="c536e-157">System-Only</span></span>            | <span data-ttu-id="c536e-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-158">False</span></span>                                                                   |
| <span data-ttu-id="c536e-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c536e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="c536e-160">True</span><span class="sxs-lookup"><span data-stu-id="c536e-160">True</span></span>                                                                    |
| <span data-ttu-id="c536e-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c536e-161">Is Indexed</span></span>             | <span data-ttu-id="c536e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-162">False</span></span>                                                                   |
| <span data-ttu-id="c536e-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c536e-163">In Global Catalog</span></span>      | <span data-ttu-id="c536e-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-164">False</span></span>                                                                   |
| <span data-ttu-id="c536e-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c536e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="c536e-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c536e-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c536e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c536e-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c536e-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-169">Search-Flags</span></span>           | <span data-ttu-id="c536e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c536e-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="c536e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-171">System-Flags</span></span>           | <span data-ttu-id="c536e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c536e-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="c536e-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c536e-173">Classes used in</span></span>        | [<span data-ttu-id="c536e-174">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="c536e-174">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c536e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c536e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c536e-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-176">Entry</span></span> | <span data-ttu-id="c536e-177">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c536e-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c536e-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="c536e-180">System-Only</span></span>            | <span data-ttu-id="c536e-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-181">False</span></span>                                                                   |
| <span data-ttu-id="c536e-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c536e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="c536e-183">True</span><span class="sxs-lookup"><span data-stu-id="c536e-183">True</span></span>                                                                    |
| <span data-ttu-id="c536e-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c536e-184">Is Indexed</span></span>             | <span data-ttu-id="c536e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-185">False</span></span>                                                                   |
| <span data-ttu-id="c536e-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c536e-186">In Global Catalog</span></span>      | <span data-ttu-id="c536e-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-187">False</span></span>                                                                   |
| <span data-ttu-id="c536e-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c536e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="c536e-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c536e-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c536e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c536e-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c536e-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-192">Search-Flags</span></span>           | <span data-ttu-id="c536e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c536e-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="c536e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-194">System-Flags</span></span>           | <span data-ttu-id="c536e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c536e-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="c536e-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c536e-196">Classes used in</span></span>        | [<span data-ttu-id="c536e-197">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="c536e-197">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c536e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c536e-198">Windows Server 2008</span></span>



| <span data-ttu-id="c536e-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-199">Entry</span></span> | <span data-ttu-id="c536e-200">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c536e-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c536e-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="c536e-203">System-Only</span></span>            | <span data-ttu-id="c536e-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-204">False</span></span>                                                                   |
| <span data-ttu-id="c536e-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c536e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="c536e-206">True</span><span class="sxs-lookup"><span data-stu-id="c536e-206">True</span></span>                                                                    |
| <span data-ttu-id="c536e-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c536e-207">Is Indexed</span></span>             | <span data-ttu-id="c536e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-208">False</span></span>                                                                   |
| <span data-ttu-id="c536e-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c536e-209">In Global Catalog</span></span>      | <span data-ttu-id="c536e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-210">False</span></span>                                                                   |
| <span data-ttu-id="c536e-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c536e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="c536e-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c536e-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c536e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c536e-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c536e-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-215">Search-Flags</span></span>           | <span data-ttu-id="c536e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c536e-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="c536e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-217">System-Flags</span></span>           | <span data-ttu-id="c536e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c536e-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="c536e-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c536e-219">Classes used in</span></span>        | [<span data-ttu-id="c536e-220">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="c536e-220">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c536e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c536e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c536e-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-222">Entry</span></span> | <span data-ttu-id="c536e-223">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c536e-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c536e-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="c536e-226">System-Only</span></span>            | <span data-ttu-id="c536e-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-227">False</span></span>                                                                   |
| <span data-ttu-id="c536e-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c536e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="c536e-229">True</span><span class="sxs-lookup"><span data-stu-id="c536e-229">True</span></span>                                                                    |
| <span data-ttu-id="c536e-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c536e-230">Is Indexed</span></span>             | <span data-ttu-id="c536e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-231">False</span></span>                                                                   |
| <span data-ttu-id="c536e-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c536e-232">In Global Catalog</span></span>      | <span data-ttu-id="c536e-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-233">False</span></span>                                                                   |
| <span data-ttu-id="c536e-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c536e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="c536e-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c536e-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c536e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c536e-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c536e-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-238">Search-Flags</span></span>           | <span data-ttu-id="c536e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c536e-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="c536e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-240">System-Flags</span></span>           | <span data-ttu-id="c536e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c536e-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="c536e-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c536e-242">Classes used in</span></span>        | [<span data-ttu-id="c536e-243">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="c536e-243">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c536e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c536e-244">Windows Server 2012</span></span>



| <span data-ttu-id="c536e-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="c536e-245">Entry</span></span> | <span data-ttu-id="c536e-246">Значение</span><span class="sxs-lookup"><span data-stu-id="c536e-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c536e-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c536e-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c536e-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="c536e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="c536e-249">System-Only</span></span>            | <span data-ttu-id="c536e-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-250">False</span></span>                                                                   |
| <span data-ttu-id="c536e-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c536e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="c536e-252">True</span><span class="sxs-lookup"><span data-stu-id="c536e-252">True</span></span>                                                                    |
| <span data-ttu-id="c536e-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c536e-253">Is Indexed</span></span>             | <span data-ttu-id="c536e-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-254">False</span></span>                                                                   |
| <span data-ttu-id="c536e-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c536e-255">In Global Catalog</span></span>      | <span data-ttu-id="c536e-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="c536e-256">False</span></span>                                                                   |
| <span data-ttu-id="c536e-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c536e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="c536e-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c536e-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="c536e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c536e-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c536e-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="c536e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-261">Search-Flags</span></span>           | <span data-ttu-id="c536e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c536e-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="c536e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c536e-263">System-Flags</span></span>           | <span data-ttu-id="c536e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c536e-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="c536e-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c536e-265">Classes used in</span></span>        | [<span data-ttu-id="c536e-266">**MSMQ-Enterprise-параметры**</span><span class="sxs-lookup"><span data-stu-id="c536e-266">**MSMQ-Enterprise-Settings**</span></span>](c-msmqenterprisesettings.md)<br/> |



 

 





