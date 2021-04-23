---
title: ACS-Enable-RSVP-сообщение-атрибут ведения журнала
description: Значение true, если включено ведение журнала RSVP.
ms.assetid: acdb2e21-9d08-4cb6-80f3-6302311386fe
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута регистрации сообщений ACS-Enable-RSVP
- Схема AD атрибута Аксенаблерсвпмессажелоггинг
topic_type:
- apiref
api_name:
- ACS-Enable-RSVP-Message-Logging
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0537472a787d3689a259bfb79e9e4cd451c4aa1d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655556"
---
# <a name="acs-enable-rsvp-message-logging-attribute"></a><span data-ttu-id="ab47e-105">ACS-Enable-RSVP-сообщение-атрибут ведения журнала</span><span class="sxs-lookup"><span data-stu-id="ab47e-105">ACS-Enable-RSVP-Message-Logging attribute</span></span>

<span data-ttu-id="ab47e-106">Значение true, если включено ведение журнала RSVP.</span><span class="sxs-lookup"><span data-stu-id="ab47e-106">True if RSVP logging is enabled.</span></span>



| <span data-ttu-id="ab47e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-107">Entry</span></span> | <span data-ttu-id="ab47e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ab47e-109">CN</span><span class="sxs-lookup"><span data-stu-id="ab47e-109">CN</span></span>                | <span data-ttu-id="ab47e-110">ACS-Enable-RSVP-сообщение — ведение журнала</span><span class="sxs-lookup"><span data-stu-id="ab47e-110">ACS-Enable-RSVP-Message-Logging</span></span>      |
| <span data-ttu-id="ab47e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ab47e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ab47e-112">аксенаблерсвпмессажелоггинг</span><span class="sxs-lookup"><span data-stu-id="ab47e-112">aCSEnableRSVPMessageLogging</span></span>          |
| <span data-ttu-id="ab47e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ab47e-113">Size</span></span>              | <span data-ttu-id="ab47e-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="ab47e-114">4 bytes</span></span>                              |
| <span data-ttu-id="ab47e-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ab47e-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ab47e-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ab47e-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ab47e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-117">Attribute-Id</span></span>      | <span data-ttu-id="ab47e-118">1.2.840.113556.1.4.768</span><span class="sxs-lookup"><span data-stu-id="ab47e-118">1.2.840.113556.1.4.768</span></span>               |
| <span data-ttu-id="ab47e-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ab47e-119">System-Id-Guid</span></span>    | <span data-ttu-id="ab47e-120">7f561285-5301-11d1-a9c5-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="ab47e-120">7f561285-5301-11d1-a9c5-0000f80367c1</span></span> |
| <span data-ttu-id="ab47e-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab47e-121">Syntax</span></span>            | [<span data-ttu-id="ab47e-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="ab47e-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="ab47e-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ab47e-123">Implementations</span></span>

-   [<span data-ttu-id="ab47e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ab47e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ab47e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ab47e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ab47e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ab47e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ab47e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ab47e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ab47e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ab47e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ab47e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ab47e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ab47e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab47e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="ab47e-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-131">Entry</span></span> | <span data-ttu-id="ab47e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab47e-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab47e-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab47e-135">System-Only</span></span>            | <span data-ttu-id="ab47e-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-136">False</span></span>                                        |
| <span data-ttu-id="ab47e-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab47e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="ab47e-138">True</span><span class="sxs-lookup"><span data-stu-id="ab47e-138">True</span></span>                                         |
| <span data-ttu-id="ab47e-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab47e-139">Is Indexed</span></span>             | <span data-ttu-id="ab47e-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-140">False</span></span>                                        |
| <span data-ttu-id="ab47e-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab47e-141">In Global Catalog</span></span>      | <span data-ttu-id="ab47e-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-142">False</span></span>                                        |
| <span data-ttu-id="ab47e-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab47e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab47e-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab47e-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab47e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab47e-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab47e-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-147">Search-Flags</span></span>           | <span data-ttu-id="ab47e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab47e-148">0x00000000</span></span>                                   |
| <span data-ttu-id="ab47e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-149">System-Flags</span></span>           | <span data-ttu-id="ab47e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab47e-150">0x00000010</span></span>                                   |
| <span data-ttu-id="ab47e-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab47e-151">Classes used in</span></span>        | [<span data-ttu-id="ab47e-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab47e-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ab47e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ab47e-153">Windows Server 2003</span></span>



| <span data-ttu-id="ab47e-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-154">Entry</span></span> | <span data-ttu-id="ab47e-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab47e-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab47e-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab47e-158">System-Only</span></span>            | <span data-ttu-id="ab47e-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-159">False</span></span>                                        |
| <span data-ttu-id="ab47e-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab47e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="ab47e-161">True</span><span class="sxs-lookup"><span data-stu-id="ab47e-161">True</span></span>                                         |
| <span data-ttu-id="ab47e-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab47e-162">Is Indexed</span></span>             | <span data-ttu-id="ab47e-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-163">False</span></span>                                        |
| <span data-ttu-id="ab47e-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab47e-164">In Global Catalog</span></span>      | <span data-ttu-id="ab47e-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-165">False</span></span>                                        |
| <span data-ttu-id="ab47e-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab47e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab47e-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab47e-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab47e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab47e-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab47e-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-170">Search-Flags</span></span>           | <span data-ttu-id="ab47e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab47e-171">0x00000000</span></span>                                   |
| <span data-ttu-id="ab47e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-172">System-Flags</span></span>           | <span data-ttu-id="ab47e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab47e-173">0x00000010</span></span>                                   |
| <span data-ttu-id="ab47e-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab47e-174">Classes used in</span></span>        | [<span data-ttu-id="ab47e-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab47e-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ab47e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ab47e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ab47e-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-177">Entry</span></span> | <span data-ttu-id="ab47e-178">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab47e-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab47e-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab47e-181">System-Only</span></span>            | <span data-ttu-id="ab47e-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-182">False</span></span>                                        |
| <span data-ttu-id="ab47e-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab47e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="ab47e-184">True</span><span class="sxs-lookup"><span data-stu-id="ab47e-184">True</span></span>                                         |
| <span data-ttu-id="ab47e-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab47e-185">Is Indexed</span></span>             | <span data-ttu-id="ab47e-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-186">False</span></span>                                        |
| <span data-ttu-id="ab47e-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab47e-187">In Global Catalog</span></span>      | <span data-ttu-id="ab47e-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-188">False</span></span>                                        |
| <span data-ttu-id="ab47e-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab47e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab47e-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab47e-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab47e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab47e-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab47e-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-193">Search-Flags</span></span>           | <span data-ttu-id="ab47e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab47e-194">0x00000000</span></span>                                   |
| <span data-ttu-id="ab47e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-195">System-Flags</span></span>           | <span data-ttu-id="ab47e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab47e-196">0x00000010</span></span>                                   |
| <span data-ttu-id="ab47e-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab47e-197">Classes used in</span></span>        | [<span data-ttu-id="ab47e-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab47e-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ab47e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab47e-199">Windows Server 2008</span></span>



| <span data-ttu-id="ab47e-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-200">Entry</span></span> | <span data-ttu-id="ab47e-201">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab47e-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab47e-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab47e-204">System-Only</span></span>            | <span data-ttu-id="ab47e-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-205">False</span></span>                                        |
| <span data-ttu-id="ab47e-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab47e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="ab47e-207">True</span><span class="sxs-lookup"><span data-stu-id="ab47e-207">True</span></span>                                         |
| <span data-ttu-id="ab47e-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab47e-208">Is Indexed</span></span>             | <span data-ttu-id="ab47e-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-209">False</span></span>                                        |
| <span data-ttu-id="ab47e-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab47e-210">In Global Catalog</span></span>      | <span data-ttu-id="ab47e-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-211">False</span></span>                                        |
| <span data-ttu-id="ab47e-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab47e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab47e-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab47e-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab47e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab47e-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab47e-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-216">Search-Flags</span></span>           | <span data-ttu-id="ab47e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab47e-217">0x00000000</span></span>                                   |
| <span data-ttu-id="ab47e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-218">System-Flags</span></span>           | <span data-ttu-id="ab47e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab47e-219">0x00000010</span></span>                                   |
| <span data-ttu-id="ab47e-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab47e-220">Classes used in</span></span>        | [<span data-ttu-id="ab47e-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab47e-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ab47e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ab47e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ab47e-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-223">Entry</span></span> | <span data-ttu-id="ab47e-224">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab47e-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab47e-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab47e-227">System-Only</span></span>            | <span data-ttu-id="ab47e-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-228">False</span></span>                                        |
| <span data-ttu-id="ab47e-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab47e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="ab47e-230">True</span><span class="sxs-lookup"><span data-stu-id="ab47e-230">True</span></span>                                         |
| <span data-ttu-id="ab47e-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab47e-231">Is Indexed</span></span>             | <span data-ttu-id="ab47e-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-232">False</span></span>                                        |
| <span data-ttu-id="ab47e-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab47e-233">In Global Catalog</span></span>      | <span data-ttu-id="ab47e-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-234">False</span></span>                                        |
| <span data-ttu-id="ab47e-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab47e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab47e-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab47e-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab47e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab47e-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab47e-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-239">Search-Flags</span></span>           | <span data-ttu-id="ab47e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab47e-240">0x00000000</span></span>                                   |
| <span data-ttu-id="ab47e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-241">System-Flags</span></span>           | <span data-ttu-id="ab47e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab47e-242">0x00000010</span></span>                                   |
| <span data-ttu-id="ab47e-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab47e-243">Classes used in</span></span>        | [<span data-ttu-id="ab47e-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab47e-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ab47e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab47e-245">Windows Server 2012</span></span>



| <span data-ttu-id="ab47e-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="ab47e-246">Entry</span></span> | <span data-ttu-id="ab47e-247">Значение</span><span class="sxs-lookup"><span data-stu-id="ab47e-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="ab47e-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ab47e-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ab47e-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="ab47e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="ab47e-250">System-Only</span></span>            | <span data-ttu-id="ab47e-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-251">False</span></span>                                        |
| <span data-ttu-id="ab47e-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ab47e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="ab47e-253">True</span><span class="sxs-lookup"><span data-stu-id="ab47e-253">True</span></span>                                         |
| <span data-ttu-id="ab47e-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ab47e-254">Is Indexed</span></span>             | <span data-ttu-id="ab47e-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-255">False</span></span>                                        |
| <span data-ttu-id="ab47e-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ab47e-256">In Global Catalog</span></span>      | <span data-ttu-id="ab47e-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="ab47e-257">False</span></span>                                        |
| <span data-ttu-id="ab47e-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ab47e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="ab47e-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ab47e-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="ab47e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ab47e-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ab47e-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="ab47e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-262">Search-Flags</span></span>           | <span data-ttu-id="ab47e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ab47e-263">0x00000000</span></span>                                   |
| <span data-ttu-id="ab47e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ab47e-264">System-Flags</span></span>           | <span data-ttu-id="ab47e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ab47e-265">0x00000010</span></span>                                   |
| <span data-ttu-id="ab47e-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ab47e-266">Classes used in</span></span>        | [<span data-ttu-id="ab47e-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="ab47e-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





