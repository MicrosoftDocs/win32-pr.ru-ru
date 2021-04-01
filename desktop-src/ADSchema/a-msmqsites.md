---
title: Атрибут MSMQ-Sites
description: Список сайтов, к которым принадлежит компьютер (массив узлов Обжектгуидс, обычно не более одного GUID).
ms.assetid: 0f6cfc3a-9edb-4291-a5df-06c0f1a6add8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MSMQ-Sites
- Схема AD атрибута Мсмкситес
topic_type:
- apiref
api_name:
- MSMQ-Sites
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47512a20301f3b1dca96c86efe604b0eacc4a73e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989807"
---
# <a name="msmq-sites-attribute"></a><span data-ttu-id="366fd-105">Атрибут MSMQ-Sites</span><span class="sxs-lookup"><span data-stu-id="366fd-105">MSMQ-Sites attribute</span></span>

<span data-ttu-id="366fd-106">Список сайтов, к которым принадлежит компьютер (массив узлов Обжектгуидс, обычно не более одного GUID).</span><span class="sxs-lookup"><span data-stu-id="366fd-106">The list of sites that the computer belongs to (an array of the sites' objectGUIDs, usually not more than one GUID).</span></span>



| <span data-ttu-id="366fd-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-107">Entry</span></span> | <span data-ttu-id="366fd-108">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="366fd-109">CN</span><span class="sxs-lookup"><span data-stu-id="366fd-109">CN</span></span>                | <span data-ttu-id="366fd-110">MSMQ-Sites</span><span class="sxs-lookup"><span data-stu-id="366fd-110">MSMQ-Sites</span></span>                                            |
| <span data-ttu-id="366fd-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="366fd-111">Ldap-Display-Name</span></span> | <span data-ttu-id="366fd-112">мсмкситес</span><span class="sxs-lookup"><span data-stu-id="366fd-112">mSMQSites</span></span>                                             |
| <span data-ttu-id="366fd-113">Размер</span><span class="sxs-lookup"><span data-stu-id="366fd-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="366fd-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="366fd-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="366fd-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="366fd-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="366fd-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-116">Attribute-Id</span></span>      | <span data-ttu-id="366fd-117">1.2.840.113556.1.4.927</span><span class="sxs-lookup"><span data-stu-id="366fd-117">1.2.840.113556.1.4.927</span></span>                                |
| <span data-ttu-id="366fd-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="366fd-118">System-Id-Guid</span></span>    | <span data-ttu-id="366fd-119">9a0dc32a-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="366fd-119">9a0dc32a-c100-11d1-bbc5-0080c76670c0</span></span>                  |
| <span data-ttu-id="366fd-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="366fd-120">Syntax</span></span>            | [<span data-ttu-id="366fd-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="366fd-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="366fd-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="366fd-122">Implementations</span></span>

-   [<span data-ttu-id="366fd-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="366fd-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="366fd-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="366fd-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="366fd-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="366fd-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="366fd-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="366fd-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="366fd-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="366fd-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="366fd-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="366fd-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="366fd-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="366fd-129">Windows 2000 Server</span></span>



| <span data-ttu-id="366fd-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-130">Entry</span></span> | <span data-ttu-id="366fd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="366fd-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="366fd-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="366fd-134">System-Only</span></span>            | <span data-ttu-id="366fd-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-135">False</span></span>                                                        |
| <span data-ttu-id="366fd-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="366fd-136">Is-Single-Valued</span></span>       | <span data-ttu-id="366fd-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-137">False</span></span>                                                        |
| <span data-ttu-id="366fd-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="366fd-138">Is Indexed</span></span>             | <span data-ttu-id="366fd-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-139">False</span></span>                                                        |
| <span data-ttu-id="366fd-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="366fd-140">In Global Catalog</span></span>      | <span data-ttu-id="366fd-141">True</span><span class="sxs-lookup"><span data-stu-id="366fd-141">True</span></span>                                                         |
| <span data-ttu-id="366fd-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="366fd-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="366fd-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="366fd-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="366fd-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="366fd-144">Range-Lower</span></span>            | <span data-ttu-id="366fd-145">16</span><span class="sxs-lookup"><span data-stu-id="366fd-145">16</span></span>                                                           |
| <span data-ttu-id="366fd-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="366fd-146">Range-Upper</span></span>            | <span data-ttu-id="366fd-147">16</span><span class="sxs-lookup"><span data-stu-id="366fd-147">16</span></span>                                                           |
| <span data-ttu-id="366fd-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-148">Search-Flags</span></span>           | <span data-ttu-id="366fd-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="366fd-149">0x00000000</span></span>                                                   |
| <span data-ttu-id="366fd-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-150">System-Flags</span></span>           | <span data-ttu-id="366fd-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="366fd-151">0x00000010</span></span>                                                   |
| <span data-ttu-id="366fd-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="366fd-152">Classes used in</span></span>        | [<span data-ttu-id="366fd-153">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="366fd-153">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="366fd-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="366fd-154">Windows Server 2003</span></span>



| <span data-ttu-id="366fd-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-155">Entry</span></span> | <span data-ttu-id="366fd-156">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="366fd-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="366fd-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="366fd-159">System-Only</span></span>            | <span data-ttu-id="366fd-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-160">False</span></span>                                                        |
| <span data-ttu-id="366fd-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="366fd-161">Is-Single-Valued</span></span>       | <span data-ttu-id="366fd-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-162">False</span></span>                                                        |
| <span data-ttu-id="366fd-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="366fd-163">Is Indexed</span></span>             | <span data-ttu-id="366fd-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-164">False</span></span>                                                        |
| <span data-ttu-id="366fd-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="366fd-165">In Global Catalog</span></span>      | <span data-ttu-id="366fd-166">True</span><span class="sxs-lookup"><span data-stu-id="366fd-166">True</span></span>                                                         |
| <span data-ttu-id="366fd-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="366fd-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="366fd-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="366fd-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="366fd-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="366fd-169">Range-Lower</span></span>            | <span data-ttu-id="366fd-170">16</span><span class="sxs-lookup"><span data-stu-id="366fd-170">16</span></span>                                                           |
| <span data-ttu-id="366fd-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="366fd-171">Range-Upper</span></span>            | <span data-ttu-id="366fd-172">16</span><span class="sxs-lookup"><span data-stu-id="366fd-172">16</span></span>                                                           |
| <span data-ttu-id="366fd-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-173">Search-Flags</span></span>           | <span data-ttu-id="366fd-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="366fd-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="366fd-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-175">System-Flags</span></span>           | <span data-ttu-id="366fd-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="366fd-176">0x00000010</span></span>                                                   |
| <span data-ttu-id="366fd-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="366fd-177">Classes used in</span></span>        | [<span data-ttu-id="366fd-178">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="366fd-178">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="366fd-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="366fd-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="366fd-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-180">Entry</span></span> | <span data-ttu-id="366fd-181">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="366fd-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="366fd-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="366fd-184">System-Only</span></span>            | <span data-ttu-id="366fd-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-185">False</span></span>                                                        |
| <span data-ttu-id="366fd-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="366fd-186">Is-Single-Valued</span></span>       | <span data-ttu-id="366fd-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-187">False</span></span>                                                        |
| <span data-ttu-id="366fd-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="366fd-188">Is Indexed</span></span>             | <span data-ttu-id="366fd-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-189">False</span></span>                                                        |
| <span data-ttu-id="366fd-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="366fd-190">In Global Catalog</span></span>      | <span data-ttu-id="366fd-191">True</span><span class="sxs-lookup"><span data-stu-id="366fd-191">True</span></span>                                                         |
| <span data-ttu-id="366fd-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="366fd-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="366fd-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="366fd-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="366fd-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="366fd-194">Range-Lower</span></span>            | <span data-ttu-id="366fd-195">16</span><span class="sxs-lookup"><span data-stu-id="366fd-195">16</span></span>                                                           |
| <span data-ttu-id="366fd-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="366fd-196">Range-Upper</span></span>            | <span data-ttu-id="366fd-197">16</span><span class="sxs-lookup"><span data-stu-id="366fd-197">16</span></span>                                                           |
| <span data-ttu-id="366fd-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-198">Search-Flags</span></span>           | <span data-ttu-id="366fd-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="366fd-199">0x00000000</span></span>                                                   |
| <span data-ttu-id="366fd-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-200">System-Flags</span></span>           | <span data-ttu-id="366fd-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="366fd-201">0x00000010</span></span>                                                   |
| <span data-ttu-id="366fd-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="366fd-202">Classes used in</span></span>        | [<span data-ttu-id="366fd-203">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="366fd-203">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="366fd-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="366fd-204">Windows Server 2008</span></span>



| <span data-ttu-id="366fd-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-205">Entry</span></span> | <span data-ttu-id="366fd-206">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-206">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="366fd-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="366fd-207">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-208">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="366fd-209">System-Only</span></span>            | <span data-ttu-id="366fd-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-210">False</span></span>                                                        |
| <span data-ttu-id="366fd-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="366fd-211">Is-Single-Valued</span></span>       | <span data-ttu-id="366fd-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-212">False</span></span>                                                        |
| <span data-ttu-id="366fd-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="366fd-213">Is Indexed</span></span>             | <span data-ttu-id="366fd-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-214">False</span></span>                                                        |
| <span data-ttu-id="366fd-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="366fd-215">In Global Catalog</span></span>      | <span data-ttu-id="366fd-216">True</span><span class="sxs-lookup"><span data-stu-id="366fd-216">True</span></span>                                                         |
| <span data-ttu-id="366fd-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="366fd-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="366fd-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="366fd-218">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="366fd-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="366fd-219">Range-Lower</span></span>            | <span data-ttu-id="366fd-220">16</span><span class="sxs-lookup"><span data-stu-id="366fd-220">16</span></span>                                                           |
| <span data-ttu-id="366fd-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="366fd-221">Range-Upper</span></span>            | <span data-ttu-id="366fd-222">16</span><span class="sxs-lookup"><span data-stu-id="366fd-222">16</span></span>                                                           |
| <span data-ttu-id="366fd-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-223">Search-Flags</span></span>           | <span data-ttu-id="366fd-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="366fd-224">0x00000000</span></span>                                                   |
| <span data-ttu-id="366fd-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-225">System-Flags</span></span>           | <span data-ttu-id="366fd-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="366fd-226">0x00000010</span></span>                                                   |
| <span data-ttu-id="366fd-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="366fd-227">Classes used in</span></span>        | [<span data-ttu-id="366fd-228">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="366fd-228">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="366fd-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="366fd-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="366fd-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-230">Entry</span></span> | <span data-ttu-id="366fd-231">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-231">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="366fd-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="366fd-232">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-233">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="366fd-234">System-Only</span></span>            | <span data-ttu-id="366fd-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-235">False</span></span>                                                        |
| <span data-ttu-id="366fd-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="366fd-236">Is-Single-Valued</span></span>       | <span data-ttu-id="366fd-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-237">False</span></span>                                                        |
| <span data-ttu-id="366fd-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="366fd-238">Is Indexed</span></span>             | <span data-ttu-id="366fd-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-239">False</span></span>                                                        |
| <span data-ttu-id="366fd-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="366fd-240">In Global Catalog</span></span>      | <span data-ttu-id="366fd-241">True</span><span class="sxs-lookup"><span data-stu-id="366fd-241">True</span></span>                                                         |
| <span data-ttu-id="366fd-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="366fd-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="366fd-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="366fd-243">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="366fd-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="366fd-244">Range-Lower</span></span>            | <span data-ttu-id="366fd-245">16</span><span class="sxs-lookup"><span data-stu-id="366fd-245">16</span></span>                                                           |
| <span data-ttu-id="366fd-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="366fd-246">Range-Upper</span></span>            | <span data-ttu-id="366fd-247">16</span><span class="sxs-lookup"><span data-stu-id="366fd-247">16</span></span>                                                           |
| <span data-ttu-id="366fd-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-248">Search-Flags</span></span>           | <span data-ttu-id="366fd-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="366fd-249">0x00000000</span></span>                                                   |
| <span data-ttu-id="366fd-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-250">System-Flags</span></span>           | <span data-ttu-id="366fd-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="366fd-251">0x00000010</span></span>                                                   |
| <span data-ttu-id="366fd-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="366fd-252">Classes used in</span></span>        | [<span data-ttu-id="366fd-253">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="366fd-253">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="366fd-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="366fd-254">Windows Server 2012</span></span>



| <span data-ttu-id="366fd-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="366fd-255">Entry</span></span> | <span data-ttu-id="366fd-256">Значение</span><span class="sxs-lookup"><span data-stu-id="366fd-256">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="366fd-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="366fd-257">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="366fd-258">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="366fd-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="366fd-259">System-Only</span></span>            | <span data-ttu-id="366fd-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-260">False</span></span>                                                        |
| <span data-ttu-id="366fd-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="366fd-261">Is-Single-Valued</span></span>       | <span data-ttu-id="366fd-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-262">False</span></span>                                                        |
| <span data-ttu-id="366fd-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="366fd-263">Is Indexed</span></span>             | <span data-ttu-id="366fd-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="366fd-264">False</span></span>                                                        |
| <span data-ttu-id="366fd-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="366fd-265">In Global Catalog</span></span>      | <span data-ttu-id="366fd-266">True</span><span class="sxs-lookup"><span data-stu-id="366fd-266">True</span></span>                                                         |
| <span data-ttu-id="366fd-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="366fd-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="366fd-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="366fd-268">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="366fd-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="366fd-269">Range-Lower</span></span>            | <span data-ttu-id="366fd-270">16</span><span class="sxs-lookup"><span data-stu-id="366fd-270">16</span></span>                                                           |
| <span data-ttu-id="366fd-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="366fd-271">Range-Upper</span></span>            | <span data-ttu-id="366fd-272">16</span><span class="sxs-lookup"><span data-stu-id="366fd-272">16</span></span>                                                           |
| <span data-ttu-id="366fd-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-273">Search-Flags</span></span>           | <span data-ttu-id="366fd-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="366fd-274">0x00000000</span></span>                                                   |
| <span data-ttu-id="366fd-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="366fd-275">System-Flags</span></span>           | <span data-ttu-id="366fd-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="366fd-276">0x00000010</span></span>                                                   |
| <span data-ttu-id="366fd-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="366fd-277">Classes used in</span></span>        | [<span data-ttu-id="366fd-278">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="366fd-278">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





