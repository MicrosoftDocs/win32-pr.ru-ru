---
title: Trust-auth-исходящий атрибут
description: Сведения о проверке подлинности для исходящей части доверия.
ms.assetid: 0b63554b-b57e-4ca5-8a78-2bce5ebfea2f
ms.tgt_platform: multiple
keywords:
- Trust-auth-схема AD исходящего атрибута
- Схема AD атрибута Трустаусаутгоинг
topic_type:
- apiref
api_name:
- Trust-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee1d462767f5ad756c936eb30f455c7982663ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804810"
---
# <a name="trust-auth-outgoing-attribute"></a><span data-ttu-id="44336-105">Trust-auth-исходящий атрибут</span><span class="sxs-lookup"><span data-stu-id="44336-105">Trust-Auth-Outgoing attribute</span></span>

<span data-ttu-id="44336-106">Сведения о проверке подлинности для исходящей части доверия.</span><span class="sxs-lookup"><span data-stu-id="44336-106">Authentication information for the outgoing portion of a trust.</span></span>



| <span data-ttu-id="44336-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-107">Entry</span></span> | <span data-ttu-id="44336-108">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="44336-109">CN</span><span class="sxs-lookup"><span data-stu-id="44336-109">CN</span></span>                | <span data-ttu-id="44336-110">Trust-auth-исходящий трафик</span><span class="sxs-lookup"><span data-stu-id="44336-110">Trust-Auth-Outgoing</span></span>                                   |
| <span data-ttu-id="44336-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="44336-111">Ldap-Display-Name</span></span> | <span data-ttu-id="44336-112">трустаусаутгоинг</span><span class="sxs-lookup"><span data-stu-id="44336-112">trustAuthOutgoing</span></span>                                     |
| <span data-ttu-id="44336-113">Размер</span><span class="sxs-lookup"><span data-stu-id="44336-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="44336-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="44336-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="44336-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="44336-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="44336-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="44336-116">Attribute-Id</span></span>      | <span data-ttu-id="44336-117">1.2.840.113556.1.4.135</span><span class="sxs-lookup"><span data-stu-id="44336-117">1.2.840.113556.1.4.135</span></span>                                |
| <span data-ttu-id="44336-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="44336-118">System-Id-Guid</span></span>    | <span data-ttu-id="44336-119">bf967a5f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="44336-119">bf967a5f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="44336-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44336-120">Syntax</span></span>            | [<span data-ttu-id="44336-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="44336-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="44336-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="44336-122">Implementations</span></span>

-   [<span data-ttu-id="44336-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="44336-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="44336-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="44336-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="44336-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="44336-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="44336-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="44336-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="44336-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="44336-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="44336-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="44336-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="44336-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44336-129">Windows 2000 Server</span></span>



| <span data-ttu-id="44336-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-130">Entry</span></span> | <span data-ttu-id="44336-131">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-131">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="44336-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44336-132">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44336-133">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="44336-134">System-Only</span></span>            | <span data-ttu-id="44336-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-135">False</span></span>                                                |
| <span data-ttu-id="44336-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44336-136">Is-Single-Valued</span></span>       | <span data-ttu-id="44336-137">True</span><span class="sxs-lookup"><span data-stu-id="44336-137">True</span></span>                                                 |
| <span data-ttu-id="44336-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44336-138">Is Indexed</span></span>             | <span data-ttu-id="44336-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-139">False</span></span>                                                |
| <span data-ttu-id="44336-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44336-140">In Global Catalog</span></span>      | <span data-ttu-id="44336-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-141">False</span></span>                                                |
| <span data-ttu-id="44336-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44336-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="44336-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44336-143">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="44336-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44336-144">Range-Lower</span></span>            | <span data-ttu-id="44336-145">0</span><span class="sxs-lookup"><span data-stu-id="44336-145">0</span></span>                                                    |
| <span data-ttu-id="44336-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44336-146">Range-Upper</span></span>            | <span data-ttu-id="44336-147">32767</span><span class="sxs-lookup"><span data-stu-id="44336-147">32767</span></span>                                                |
| <span data-ttu-id="44336-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-148">Search-Flags</span></span>           | <span data-ttu-id="44336-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44336-149">0x00000000</span></span>                                           |
| <span data-ttu-id="44336-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-150">System-Flags</span></span>           | <span data-ttu-id="44336-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44336-151">0x00000010</span></span>                                           |
| <span data-ttu-id="44336-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44336-152">Classes used in</span></span>        | [<span data-ttu-id="44336-153">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="44336-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="44336-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44336-154">Windows Server 2003</span></span>



| <span data-ttu-id="44336-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-155">Entry</span></span> | <span data-ttu-id="44336-156">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="44336-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44336-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44336-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="44336-159">System-Only</span></span>            | <span data-ttu-id="44336-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-160">False</span></span>                                                |
| <span data-ttu-id="44336-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44336-161">Is-Single-Valued</span></span>       | <span data-ttu-id="44336-162">True</span><span class="sxs-lookup"><span data-stu-id="44336-162">True</span></span>                                                 |
| <span data-ttu-id="44336-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44336-163">Is Indexed</span></span>             | <span data-ttu-id="44336-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-164">False</span></span>                                                |
| <span data-ttu-id="44336-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44336-165">In Global Catalog</span></span>      | <span data-ttu-id="44336-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-166">False</span></span>                                                |
| <span data-ttu-id="44336-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44336-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="44336-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44336-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="44336-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44336-169">Range-Lower</span></span>            | <span data-ttu-id="44336-170">0</span><span class="sxs-lookup"><span data-stu-id="44336-170">0</span></span>                                                    |
| <span data-ttu-id="44336-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44336-171">Range-Upper</span></span>            | <span data-ttu-id="44336-172">32767</span><span class="sxs-lookup"><span data-stu-id="44336-172">32767</span></span>                                                |
| <span data-ttu-id="44336-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-173">Search-Flags</span></span>           | <span data-ttu-id="44336-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44336-174">0x00000000</span></span>                                           |
| <span data-ttu-id="44336-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-175">System-Flags</span></span>           | <span data-ttu-id="44336-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44336-176">0x00000010</span></span>                                           |
| <span data-ttu-id="44336-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44336-177">Classes used in</span></span>        | [<span data-ttu-id="44336-178">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="44336-178">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="44336-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="44336-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="44336-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-180">Entry</span></span> | <span data-ttu-id="44336-181">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-181">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="44336-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44336-182">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44336-183">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="44336-184">System-Only</span></span>            | <span data-ttu-id="44336-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-185">False</span></span>                                                |
| <span data-ttu-id="44336-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44336-186">Is-Single-Valued</span></span>       | <span data-ttu-id="44336-187">True</span><span class="sxs-lookup"><span data-stu-id="44336-187">True</span></span>                                                 |
| <span data-ttu-id="44336-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44336-188">Is Indexed</span></span>             | <span data-ttu-id="44336-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-189">False</span></span>                                                |
| <span data-ttu-id="44336-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44336-190">In Global Catalog</span></span>      | <span data-ttu-id="44336-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-191">False</span></span>                                                |
| <span data-ttu-id="44336-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44336-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="44336-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44336-193">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="44336-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44336-194">Range-Lower</span></span>            | <span data-ttu-id="44336-195">0</span><span class="sxs-lookup"><span data-stu-id="44336-195">0</span></span>                                                    |
| <span data-ttu-id="44336-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44336-196">Range-Upper</span></span>            | <span data-ttu-id="44336-197">32767</span><span class="sxs-lookup"><span data-stu-id="44336-197">32767</span></span>                                                |
| <span data-ttu-id="44336-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-198">Search-Flags</span></span>           | <span data-ttu-id="44336-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44336-199">0x00000000</span></span>                                           |
| <span data-ttu-id="44336-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-200">System-Flags</span></span>           | <span data-ttu-id="44336-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44336-201">0x00000010</span></span>                                           |
| <span data-ttu-id="44336-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44336-202">Classes used in</span></span>        | [<span data-ttu-id="44336-203">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="44336-203">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="44336-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44336-204">Windows Server 2008</span></span>



| <span data-ttu-id="44336-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-205">Entry</span></span> | <span data-ttu-id="44336-206">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-206">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="44336-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44336-207">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44336-208">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="44336-209">System-Only</span></span>            | <span data-ttu-id="44336-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-210">False</span></span>                                                |
| <span data-ttu-id="44336-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44336-211">Is-Single-Valued</span></span>       | <span data-ttu-id="44336-212">True</span><span class="sxs-lookup"><span data-stu-id="44336-212">True</span></span>                                                 |
| <span data-ttu-id="44336-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44336-213">Is Indexed</span></span>             | <span data-ttu-id="44336-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-214">False</span></span>                                                |
| <span data-ttu-id="44336-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44336-215">In Global Catalog</span></span>      | <span data-ttu-id="44336-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-216">False</span></span>                                                |
| <span data-ttu-id="44336-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44336-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="44336-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44336-218">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="44336-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44336-219">Range-Lower</span></span>            | <span data-ttu-id="44336-220">0</span><span class="sxs-lookup"><span data-stu-id="44336-220">0</span></span>                                                    |
| <span data-ttu-id="44336-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44336-221">Range-Upper</span></span>            | <span data-ttu-id="44336-222">32767</span><span class="sxs-lookup"><span data-stu-id="44336-222">32767</span></span>                                                |
| <span data-ttu-id="44336-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-223">Search-Flags</span></span>           | <span data-ttu-id="44336-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44336-224">0x00000000</span></span>                                           |
| <span data-ttu-id="44336-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-225">System-Flags</span></span>           | <span data-ttu-id="44336-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44336-226">0x00000010</span></span>                                           |
| <span data-ttu-id="44336-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44336-227">Classes used in</span></span>        | [<span data-ttu-id="44336-228">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="44336-228">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="44336-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="44336-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="44336-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-230">Entry</span></span> | <span data-ttu-id="44336-231">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-231">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="44336-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44336-232">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44336-233">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="44336-234">System-Only</span></span>            | <span data-ttu-id="44336-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-235">False</span></span>                                                |
| <span data-ttu-id="44336-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44336-236">Is-Single-Valued</span></span>       | <span data-ttu-id="44336-237">True</span><span class="sxs-lookup"><span data-stu-id="44336-237">True</span></span>                                                 |
| <span data-ttu-id="44336-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44336-238">Is Indexed</span></span>             | <span data-ttu-id="44336-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-239">False</span></span>                                                |
| <span data-ttu-id="44336-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44336-240">In Global Catalog</span></span>      | <span data-ttu-id="44336-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-241">False</span></span>                                                |
| <span data-ttu-id="44336-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44336-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="44336-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44336-243">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="44336-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44336-244">Range-Lower</span></span>            | <span data-ttu-id="44336-245">0</span><span class="sxs-lookup"><span data-stu-id="44336-245">0</span></span>                                                    |
| <span data-ttu-id="44336-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44336-246">Range-Upper</span></span>            | <span data-ttu-id="44336-247">32767</span><span class="sxs-lookup"><span data-stu-id="44336-247">32767</span></span>                                                |
| <span data-ttu-id="44336-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-248">Search-Flags</span></span>           | <span data-ttu-id="44336-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44336-249">0x00000000</span></span>                                           |
| <span data-ttu-id="44336-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-250">System-Flags</span></span>           | <span data-ttu-id="44336-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44336-251">0x00000010</span></span>                                           |
| <span data-ttu-id="44336-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44336-252">Classes used in</span></span>        | [<span data-ttu-id="44336-253">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="44336-253">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="44336-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44336-254">Windows Server 2012</span></span>



| <span data-ttu-id="44336-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="44336-255">Entry</span></span> | <span data-ttu-id="44336-256">Значение</span><span class="sxs-lookup"><span data-stu-id="44336-256">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="44336-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="44336-257">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="44336-258">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="44336-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="44336-259">System-Only</span></span>            | <span data-ttu-id="44336-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-260">False</span></span>                                                |
| <span data-ttu-id="44336-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="44336-261">Is-Single-Valued</span></span>       | <span data-ttu-id="44336-262">True</span><span class="sxs-lookup"><span data-stu-id="44336-262">True</span></span>                                                 |
| <span data-ttu-id="44336-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="44336-263">Is Indexed</span></span>             | <span data-ttu-id="44336-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-264">False</span></span>                                                |
| <span data-ttu-id="44336-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="44336-265">In Global Catalog</span></span>      | <span data-ttu-id="44336-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="44336-266">False</span></span>                                                |
| <span data-ttu-id="44336-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="44336-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="44336-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="44336-268">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="44336-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="44336-269">Range-Lower</span></span>            | <span data-ttu-id="44336-270">0</span><span class="sxs-lookup"><span data-stu-id="44336-270">0</span></span>                                                    |
| <span data-ttu-id="44336-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="44336-271">Range-Upper</span></span>            | <span data-ttu-id="44336-272">32767</span><span class="sxs-lookup"><span data-stu-id="44336-272">32767</span></span>                                                |
| <span data-ttu-id="44336-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-273">Search-Flags</span></span>           | <span data-ttu-id="44336-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44336-274">0x00000000</span></span>                                           |
| <span data-ttu-id="44336-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="44336-275">System-Flags</span></span>           | <span data-ttu-id="44336-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="44336-276">0x00000010</span></span>                                           |
| <span data-ttu-id="44336-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="44336-277">Classes used in</span></span>        | [<span data-ttu-id="44336-278">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="44336-278">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





