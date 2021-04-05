---
title: Trust-auth-входящий атрибут
description: Сведения о проверке подлинности для входящей части доверия.
ms.assetid: 15d079f8-a77c-4baf-bb60-1af7a8e8da25
ms.tgt_platform: multiple
keywords:
- Trust-auth-схема Active Directory для входящего атрибута
- Схема AD атрибута Трустаусинкоминг
topic_type:
- apiref
api_name:
- Trust-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b605efb326ff9a75426a98810a6cc27f4d29adc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493680"
---
# <a name="trust-auth-incoming-attribute"></a><span data-ttu-id="4e6a1-105">Trust-auth-входящий атрибут</span><span class="sxs-lookup"><span data-stu-id="4e6a1-105">Trust-Auth-Incoming attribute</span></span>

<span data-ttu-id="4e6a1-106">Сведения о проверке подлинности для входящей части доверия.</span><span class="sxs-lookup"><span data-stu-id="4e6a1-106">Authentication information for the incoming portion of a trust.</span></span>



| <span data-ttu-id="4e6a1-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-107">Entry</span></span> | <span data-ttu-id="4e6a1-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4e6a1-109">CN</span><span class="sxs-lookup"><span data-stu-id="4e6a1-109">CN</span></span>                | <span data-ttu-id="4e6a1-110">Trust-auth-входящий</span><span class="sxs-lookup"><span data-stu-id="4e6a1-110">Trust-Auth-Incoming</span></span>                                   |
| <span data-ttu-id="4e6a1-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4e6a1-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4e6a1-112">трустаусинкоминг</span><span class="sxs-lookup"><span data-stu-id="4e6a1-112">trustAuthIncoming</span></span>                                     |
| <span data-ttu-id="4e6a1-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4e6a1-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4e6a1-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4e6a1-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="4e6a1-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4e6a1-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="4e6a1-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-116">Attribute-Id</span></span>      | <span data-ttu-id="4e6a1-117">1.2.840.113556.1.4.129</span><span class="sxs-lookup"><span data-stu-id="4e6a1-117">1.2.840.113556.1.4.129</span></span>                                |
| <span data-ttu-id="4e6a1-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4e6a1-118">System-Id-Guid</span></span>    | <span data-ttu-id="4e6a1-119">bf967a59-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4e6a1-119">bf967a59-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="4e6a1-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e6a1-120">Syntax</span></span>            | [<span data-ttu-id="4e6a1-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4e6a1-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4e6a1-122">Implementations</span></span>

-   [<span data-ttu-id="4e6a1-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4e6a1-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4e6a1-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4e6a1-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4e6a1-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4e6a1-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4e6a1-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4e6a1-129">Windows 2000 Server</span></span>



| <span data-ttu-id="4e6a1-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-130">Entry</span></span> | <span data-ttu-id="4e6a1-131">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6a1-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4e6a1-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e6a1-134">System-Only</span></span>            | <span data-ttu-id="4e6a1-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-135">False</span></span>                                                |
| <span data-ttu-id="4e6a1-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4e6a1-136">Is-Single-Valued</span></span>       | <span data-ttu-id="4e6a1-137">True</span><span class="sxs-lookup"><span data-stu-id="4e6a1-137">True</span></span>                                                 |
| <span data-ttu-id="4e6a1-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4e6a1-138">Is Indexed</span></span>             | <span data-ttu-id="4e6a1-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-139">False</span></span>                                                |
| <span data-ttu-id="4e6a1-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4e6a1-140">In Global Catalog</span></span>      | <span data-ttu-id="4e6a1-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-141">False</span></span>                                                |
| <span data-ttu-id="4e6a1-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4e6a1-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e6a1-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4e6a1-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4e6a1-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e6a1-144">Range-Lower</span></span>            | <span data-ttu-id="4e6a1-145">0</span><span class="sxs-lookup"><span data-stu-id="4e6a1-145">0</span></span>                                                    |
| <span data-ttu-id="4e6a1-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e6a1-146">Range-Upper</span></span>            | <span data-ttu-id="4e6a1-147">32767</span><span class="sxs-lookup"><span data-stu-id="4e6a1-147">32767</span></span>                                                |
| <span data-ttu-id="4e6a1-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-148">Search-Flags</span></span>           | <span data-ttu-id="4e6a1-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e6a1-149">0x00000000</span></span>                                           |
| <span data-ttu-id="4e6a1-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-150">System-Flags</span></span>           | <span data-ttu-id="4e6a1-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e6a1-151">0x00000010</span></span>                                           |
| <span data-ttu-id="4e6a1-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4e6a1-152">Classes used in</span></span>        | [<span data-ttu-id="4e6a1-153">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4e6a1-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e6a1-154">Windows Server 2003</span></span>



| <span data-ttu-id="4e6a1-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-155">Entry</span></span> | <span data-ttu-id="4e6a1-156">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6a1-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4e6a1-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e6a1-159">System-Only</span></span>            | <span data-ttu-id="4e6a1-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-160">False</span></span>                                                |
| <span data-ttu-id="4e6a1-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4e6a1-161">Is-Single-Valued</span></span>       | <span data-ttu-id="4e6a1-162">True</span><span class="sxs-lookup"><span data-stu-id="4e6a1-162">True</span></span>                                                 |
| <span data-ttu-id="4e6a1-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4e6a1-163">Is Indexed</span></span>             | <span data-ttu-id="4e6a1-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-164">False</span></span>                                                |
| <span data-ttu-id="4e6a1-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4e6a1-165">In Global Catalog</span></span>      | <span data-ttu-id="4e6a1-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-166">False</span></span>                                                |
| <span data-ttu-id="4e6a1-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4e6a1-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e6a1-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4e6a1-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4e6a1-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e6a1-169">Range-Lower</span></span>            | <span data-ttu-id="4e6a1-170">0</span><span class="sxs-lookup"><span data-stu-id="4e6a1-170">0</span></span>                                                    |
| <span data-ttu-id="4e6a1-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e6a1-171">Range-Upper</span></span>            | <span data-ttu-id="4e6a1-172">32767</span><span class="sxs-lookup"><span data-stu-id="4e6a1-172">32767</span></span>                                                |
| <span data-ttu-id="4e6a1-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-173">Search-Flags</span></span>           | <span data-ttu-id="4e6a1-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e6a1-174">0x00000000</span></span>                                           |
| <span data-ttu-id="4e6a1-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-175">System-Flags</span></span>           | <span data-ttu-id="4e6a1-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e6a1-176">0x00000010</span></span>                                           |
| <span data-ttu-id="4e6a1-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4e6a1-177">Classes used in</span></span>        | [<span data-ttu-id="4e6a1-178">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-178">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4e6a1-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4e6a1-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4e6a1-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-180">Entry</span></span> | <span data-ttu-id="4e6a1-181">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-181">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6a1-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4e6a1-182">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-183">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e6a1-184">System-Only</span></span>            | <span data-ttu-id="4e6a1-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-185">False</span></span>                                                |
| <span data-ttu-id="4e6a1-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4e6a1-186">Is-Single-Valued</span></span>       | <span data-ttu-id="4e6a1-187">True</span><span class="sxs-lookup"><span data-stu-id="4e6a1-187">True</span></span>                                                 |
| <span data-ttu-id="4e6a1-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4e6a1-188">Is Indexed</span></span>             | <span data-ttu-id="4e6a1-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-189">False</span></span>                                                |
| <span data-ttu-id="4e6a1-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4e6a1-190">In Global Catalog</span></span>      | <span data-ttu-id="4e6a1-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-191">False</span></span>                                                |
| <span data-ttu-id="4e6a1-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4e6a1-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e6a1-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4e6a1-193">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4e6a1-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e6a1-194">Range-Lower</span></span>            | <span data-ttu-id="4e6a1-195">0</span><span class="sxs-lookup"><span data-stu-id="4e6a1-195">0</span></span>                                                    |
| <span data-ttu-id="4e6a1-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e6a1-196">Range-Upper</span></span>            | <span data-ttu-id="4e6a1-197">32767</span><span class="sxs-lookup"><span data-stu-id="4e6a1-197">32767</span></span>                                                |
| <span data-ttu-id="4e6a1-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-198">Search-Flags</span></span>           | <span data-ttu-id="4e6a1-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e6a1-199">0x00000000</span></span>                                           |
| <span data-ttu-id="4e6a1-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-200">System-Flags</span></span>           | <span data-ttu-id="4e6a1-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e6a1-201">0x00000010</span></span>                                           |
| <span data-ttu-id="4e6a1-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4e6a1-202">Classes used in</span></span>        | [<span data-ttu-id="4e6a1-203">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-203">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4e6a1-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e6a1-204">Windows Server 2008</span></span>



| <span data-ttu-id="4e6a1-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-205">Entry</span></span> | <span data-ttu-id="4e6a1-206">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-206">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6a1-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4e6a1-207">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-208">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e6a1-209">System-Only</span></span>            | <span data-ttu-id="4e6a1-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-210">False</span></span>                                                |
| <span data-ttu-id="4e6a1-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4e6a1-211">Is-Single-Valued</span></span>       | <span data-ttu-id="4e6a1-212">True</span><span class="sxs-lookup"><span data-stu-id="4e6a1-212">True</span></span>                                                 |
| <span data-ttu-id="4e6a1-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4e6a1-213">Is Indexed</span></span>             | <span data-ttu-id="4e6a1-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-214">False</span></span>                                                |
| <span data-ttu-id="4e6a1-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4e6a1-215">In Global Catalog</span></span>      | <span data-ttu-id="4e6a1-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-216">False</span></span>                                                |
| <span data-ttu-id="4e6a1-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4e6a1-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e6a1-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4e6a1-218">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4e6a1-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e6a1-219">Range-Lower</span></span>            | <span data-ttu-id="4e6a1-220">0</span><span class="sxs-lookup"><span data-stu-id="4e6a1-220">0</span></span>                                                    |
| <span data-ttu-id="4e6a1-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e6a1-221">Range-Upper</span></span>            | <span data-ttu-id="4e6a1-222">32767</span><span class="sxs-lookup"><span data-stu-id="4e6a1-222">32767</span></span>                                                |
| <span data-ttu-id="4e6a1-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-223">Search-Flags</span></span>           | <span data-ttu-id="4e6a1-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e6a1-224">0x00000000</span></span>                                           |
| <span data-ttu-id="4e6a1-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-225">System-Flags</span></span>           | <span data-ttu-id="4e6a1-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e6a1-226">0x00000010</span></span>                                           |
| <span data-ttu-id="4e6a1-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4e6a1-227">Classes used in</span></span>        | [<span data-ttu-id="4e6a1-228">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-228">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4e6a1-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4e6a1-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4e6a1-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-230">Entry</span></span> | <span data-ttu-id="4e6a1-231">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-231">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6a1-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4e6a1-232">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-233">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e6a1-234">System-Only</span></span>            | <span data-ttu-id="4e6a1-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-235">False</span></span>                                                |
| <span data-ttu-id="4e6a1-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4e6a1-236">Is-Single-Valued</span></span>       | <span data-ttu-id="4e6a1-237">True</span><span class="sxs-lookup"><span data-stu-id="4e6a1-237">True</span></span>                                                 |
| <span data-ttu-id="4e6a1-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4e6a1-238">Is Indexed</span></span>             | <span data-ttu-id="4e6a1-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-239">False</span></span>                                                |
| <span data-ttu-id="4e6a1-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4e6a1-240">In Global Catalog</span></span>      | <span data-ttu-id="4e6a1-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-241">False</span></span>                                                |
| <span data-ttu-id="4e6a1-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4e6a1-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e6a1-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4e6a1-243">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4e6a1-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e6a1-244">Range-Lower</span></span>            | <span data-ttu-id="4e6a1-245">0</span><span class="sxs-lookup"><span data-stu-id="4e6a1-245">0</span></span>                                                    |
| <span data-ttu-id="4e6a1-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e6a1-246">Range-Upper</span></span>            | <span data-ttu-id="4e6a1-247">32767</span><span class="sxs-lookup"><span data-stu-id="4e6a1-247">32767</span></span>                                                |
| <span data-ttu-id="4e6a1-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-248">Search-Flags</span></span>           | <span data-ttu-id="4e6a1-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e6a1-249">0x00000000</span></span>                                           |
| <span data-ttu-id="4e6a1-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-250">System-Flags</span></span>           | <span data-ttu-id="4e6a1-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e6a1-251">0x00000010</span></span>                                           |
| <span data-ttu-id="4e6a1-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4e6a1-252">Classes used in</span></span>        | [<span data-ttu-id="4e6a1-253">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-253">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4e6a1-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4e6a1-254">Windows Server 2012</span></span>



| <span data-ttu-id="4e6a1-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="4e6a1-255">Entry</span></span> | <span data-ttu-id="4e6a1-256">Значение</span><span class="sxs-lookup"><span data-stu-id="4e6a1-256">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="4e6a1-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4e6a1-257">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4e6a1-258">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="4e6a1-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="4e6a1-259">System-Only</span></span>            | <span data-ttu-id="4e6a1-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-260">False</span></span>                                                |
| <span data-ttu-id="4e6a1-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4e6a1-261">Is-Single-Valued</span></span>       | <span data-ttu-id="4e6a1-262">True</span><span class="sxs-lookup"><span data-stu-id="4e6a1-262">True</span></span>                                                 |
| <span data-ttu-id="4e6a1-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4e6a1-263">Is Indexed</span></span>             | <span data-ttu-id="4e6a1-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-264">False</span></span>                                                |
| <span data-ttu-id="4e6a1-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4e6a1-265">In Global Catalog</span></span>      | <span data-ttu-id="4e6a1-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="4e6a1-266">False</span></span>                                                |
| <span data-ttu-id="4e6a1-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4e6a1-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="4e6a1-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4e6a1-268">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="4e6a1-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4e6a1-269">Range-Lower</span></span>            | <span data-ttu-id="4e6a1-270">0</span><span class="sxs-lookup"><span data-stu-id="4e6a1-270">0</span></span>                                                    |
| <span data-ttu-id="4e6a1-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4e6a1-271">Range-Upper</span></span>            | <span data-ttu-id="4e6a1-272">32767</span><span class="sxs-lookup"><span data-stu-id="4e6a1-272">32767</span></span>                                                |
| <span data-ttu-id="4e6a1-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-273">Search-Flags</span></span>           | <span data-ttu-id="4e6a1-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4e6a1-274">0x00000000</span></span>                                           |
| <span data-ttu-id="4e6a1-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4e6a1-275">System-Flags</span></span>           | <span data-ttu-id="4e6a1-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4e6a1-276">0x00000010</span></span>                                           |
| <span data-ttu-id="4e6a1-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4e6a1-277">Classes used in</span></span>        | [<span data-ttu-id="4e6a1-278">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="4e6a1-278">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





