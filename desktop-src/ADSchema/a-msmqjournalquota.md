---
title: Атрибут квоты MSMQ-Journal
description: Квота сообщений журнала MSMQ для компьютера.
ms.assetid: 0793b8fa-1b9a-495f-a9f2-21dd8c174038
ms.tgt_platform: multiple
keywords:
- Схема Active Directory для атрибутов квоты MSMQ
- Схема AD атрибута Мсмкжаурналкуота
topic_type:
- apiref
api_name:
- MSMQ-Journal-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb6c49a94049452ad595db8e709326ee562854ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989813"
---
# <a name="msmq-journal-quota-attribute"></a><span data-ttu-id="6fea0-105">Атрибут квоты MSMQ-Journal</span><span class="sxs-lookup"><span data-stu-id="6fea0-105">MSMQ-Journal-Quota attribute</span></span>

<span data-ttu-id="6fea0-106">Квота сообщений журнала MSMQ для компьютера.</span><span class="sxs-lookup"><span data-stu-id="6fea0-106">MSMQ journal messages quota of the computer.</span></span>



| <span data-ttu-id="6fea0-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-107">Entry</span></span> | <span data-ttu-id="6fea0-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6fea0-109">CN</span><span class="sxs-lookup"><span data-stu-id="6fea0-109">CN</span></span>                | <span data-ttu-id="6fea0-110">Очередь MSMQ — журнал — квота</span><span class="sxs-lookup"><span data-stu-id="6fea0-110">MSMQ-Journal-Quota</span></span>                   |
| <span data-ttu-id="6fea0-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6fea0-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6fea0-112">мсмкжаурналкуота</span><span class="sxs-lookup"><span data-stu-id="6fea0-112">mSMQJournalQuota</span></span>                     |
| <span data-ttu-id="6fea0-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6fea0-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="6fea0-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6fea0-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6fea0-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6fea0-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6fea0-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-116">Attribute-Id</span></span>      | <span data-ttu-id="6fea0-117">1.2.840.113556.1.4.921</span><span class="sxs-lookup"><span data-stu-id="6fea0-117">1.2.840.113556.1.4.921</span></span>               |
| <span data-ttu-id="6fea0-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6fea0-118">System-Id-Guid</span></span>    | <span data-ttu-id="6fea0-119">9a0dc324-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="6fea0-119">9a0dc324-c100-11d1-bbc5-0080c76670c0</span></span> |
| <span data-ttu-id="6fea0-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fea0-120">Syntax</span></span>            | [<span data-ttu-id="6fea0-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="6fea0-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6fea0-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6fea0-122">Implementations</span></span>

-   [<span data-ttu-id="6fea0-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6fea0-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6fea0-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6fea0-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6fea0-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6fea0-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6fea0-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6fea0-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6fea0-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6fea0-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6fea0-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6fea0-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6fea0-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6fea0-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6fea0-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-130">Entry</span></span> | <span data-ttu-id="6fea0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6fea0-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fea0-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fea0-134">System-Only</span></span>            | <span data-ttu-id="6fea0-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-135">False</span></span>                                                        |
| <span data-ttu-id="6fea0-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fea0-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6fea0-137">True</span><span class="sxs-lookup"><span data-stu-id="6fea0-137">True</span></span>                                                         |
| <span data-ttu-id="6fea0-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fea0-138">Is Indexed</span></span>             | <span data-ttu-id="6fea0-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-139">False</span></span>                                                        |
| <span data-ttu-id="6fea0-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fea0-140">In Global Catalog</span></span>      | <span data-ttu-id="6fea0-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-141">False</span></span>                                                        |
| <span data-ttu-id="6fea0-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fea0-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fea0-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fea0-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6fea0-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fea0-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fea0-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-146">Search-Flags</span></span>           | <span data-ttu-id="6fea0-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fea0-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="6fea0-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-148">System-Flags</span></span>           | <span data-ttu-id="6fea0-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fea0-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="6fea0-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fea0-150">Classes used in</span></span>        | [<span data-ttu-id="6fea0-151">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fea0-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6fea0-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6fea0-152">Windows Server 2003</span></span>



| <span data-ttu-id="6fea0-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-153">Entry</span></span> | <span data-ttu-id="6fea0-154">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6fea0-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fea0-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fea0-157">System-Only</span></span>            | <span data-ttu-id="6fea0-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-158">False</span></span>                                                        |
| <span data-ttu-id="6fea0-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fea0-159">Is-Single-Valued</span></span>       | <span data-ttu-id="6fea0-160">True</span><span class="sxs-lookup"><span data-stu-id="6fea0-160">True</span></span>                                                         |
| <span data-ttu-id="6fea0-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fea0-161">Is Indexed</span></span>             | <span data-ttu-id="6fea0-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-162">False</span></span>                                                        |
| <span data-ttu-id="6fea0-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fea0-163">In Global Catalog</span></span>      | <span data-ttu-id="6fea0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-164">False</span></span>                                                        |
| <span data-ttu-id="6fea0-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fea0-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fea0-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fea0-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6fea0-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fea0-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fea0-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-169">Search-Flags</span></span>           | <span data-ttu-id="6fea0-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fea0-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="6fea0-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-171">System-Flags</span></span>           | <span data-ttu-id="6fea0-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fea0-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="6fea0-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fea0-173">Classes used in</span></span>        | [<span data-ttu-id="6fea0-174">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fea0-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6fea0-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6fea0-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6fea0-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-176">Entry</span></span> | <span data-ttu-id="6fea0-177">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6fea0-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fea0-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fea0-180">System-Only</span></span>            | <span data-ttu-id="6fea0-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-181">False</span></span>                                                        |
| <span data-ttu-id="6fea0-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fea0-182">Is-Single-Valued</span></span>       | <span data-ttu-id="6fea0-183">True</span><span class="sxs-lookup"><span data-stu-id="6fea0-183">True</span></span>                                                         |
| <span data-ttu-id="6fea0-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fea0-184">Is Indexed</span></span>             | <span data-ttu-id="6fea0-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-185">False</span></span>                                                        |
| <span data-ttu-id="6fea0-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fea0-186">In Global Catalog</span></span>      | <span data-ttu-id="6fea0-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-187">False</span></span>                                                        |
| <span data-ttu-id="6fea0-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fea0-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fea0-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fea0-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6fea0-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fea0-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fea0-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-192">Search-Flags</span></span>           | <span data-ttu-id="6fea0-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fea0-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="6fea0-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-194">System-Flags</span></span>           | <span data-ttu-id="6fea0-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fea0-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="6fea0-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fea0-196">Classes used in</span></span>        | [<span data-ttu-id="6fea0-197">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fea0-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6fea0-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fea0-198">Windows Server 2008</span></span>



| <span data-ttu-id="6fea0-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-199">Entry</span></span> | <span data-ttu-id="6fea0-200">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6fea0-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fea0-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fea0-203">System-Only</span></span>            | <span data-ttu-id="6fea0-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-204">False</span></span>                                                        |
| <span data-ttu-id="6fea0-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fea0-205">Is-Single-Valued</span></span>       | <span data-ttu-id="6fea0-206">True</span><span class="sxs-lookup"><span data-stu-id="6fea0-206">True</span></span>                                                         |
| <span data-ttu-id="6fea0-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fea0-207">Is Indexed</span></span>             | <span data-ttu-id="6fea0-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-208">False</span></span>                                                        |
| <span data-ttu-id="6fea0-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fea0-209">In Global Catalog</span></span>      | <span data-ttu-id="6fea0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-210">False</span></span>                                                        |
| <span data-ttu-id="6fea0-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fea0-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fea0-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fea0-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6fea0-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fea0-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fea0-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-215">Search-Flags</span></span>           | <span data-ttu-id="6fea0-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fea0-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="6fea0-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-217">System-Flags</span></span>           | <span data-ttu-id="6fea0-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fea0-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="6fea0-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fea0-219">Classes used in</span></span>        | [<span data-ttu-id="6fea0-220">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fea0-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6fea0-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6fea0-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6fea0-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-222">Entry</span></span> | <span data-ttu-id="6fea0-223">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6fea0-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fea0-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fea0-226">System-Only</span></span>            | <span data-ttu-id="6fea0-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-227">False</span></span>                                                        |
| <span data-ttu-id="6fea0-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fea0-228">Is-Single-Valued</span></span>       | <span data-ttu-id="6fea0-229">True</span><span class="sxs-lookup"><span data-stu-id="6fea0-229">True</span></span>                                                         |
| <span data-ttu-id="6fea0-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fea0-230">Is Indexed</span></span>             | <span data-ttu-id="6fea0-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-231">False</span></span>                                                        |
| <span data-ttu-id="6fea0-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fea0-232">In Global Catalog</span></span>      | <span data-ttu-id="6fea0-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-233">False</span></span>                                                        |
| <span data-ttu-id="6fea0-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fea0-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fea0-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fea0-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6fea0-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fea0-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fea0-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-238">Search-Flags</span></span>           | <span data-ttu-id="6fea0-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fea0-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="6fea0-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-240">System-Flags</span></span>           | <span data-ttu-id="6fea0-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fea0-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="6fea0-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fea0-242">Classes used in</span></span>        | [<span data-ttu-id="6fea0-243">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fea0-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6fea0-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6fea0-244">Windows Server 2012</span></span>



| <span data-ttu-id="6fea0-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="6fea0-245">Entry</span></span> | <span data-ttu-id="6fea0-246">Значение</span><span class="sxs-lookup"><span data-stu-id="6fea0-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6fea0-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6fea0-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fea0-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="6fea0-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fea0-249">System-Only</span></span>            | <span data-ttu-id="6fea0-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-250">False</span></span>                                                        |
| <span data-ttu-id="6fea0-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6fea0-251">Is-Single-Valued</span></span>       | <span data-ttu-id="6fea0-252">True</span><span class="sxs-lookup"><span data-stu-id="6fea0-252">True</span></span>                                                         |
| <span data-ttu-id="6fea0-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6fea0-253">Is Indexed</span></span>             | <span data-ttu-id="6fea0-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-254">False</span></span>                                                        |
| <span data-ttu-id="6fea0-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6fea0-255">In Global Catalog</span></span>      | <span data-ttu-id="6fea0-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="6fea0-256">False</span></span>                                                        |
| <span data-ttu-id="6fea0-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6fea0-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fea0-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6fea0-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="6fea0-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fea0-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fea0-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="6fea0-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-261">Search-Flags</span></span>           | <span data-ttu-id="6fea0-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fea0-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="6fea0-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fea0-263">System-Flags</span></span>           | <span data-ttu-id="6fea0-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fea0-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="6fea0-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6fea0-265">Classes used in</span></span>        | [<span data-ttu-id="6fea0-266">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="6fea0-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





