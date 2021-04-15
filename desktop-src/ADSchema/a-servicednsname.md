---
title: Service-DNS-атрибут Name
description: DNS-имя для поиска сервера, на котором запущена эта служба.
ms.assetid: b2852276-30f5-4c2a-9f72-9df0d7c0c994
ms.tgt_platform: multiple
keywords:
- Service-DNS-имя атрибута AD, схема
- Схема AD атрибута serviceDNSName
topic_type:
- apiref
api_name:
- Service-DNS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b881587a1358a6e7a3a814efb80af122ac5669
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536149"
---
# <a name="service-dns-name-attribute"></a><span data-ttu-id="8d967-105">Service-DNS-атрибут Name</span><span class="sxs-lookup"><span data-stu-id="8d967-105">Service-DNS-Name attribute</span></span>

<span data-ttu-id="8d967-106">DNS-имя для поиска сервера, на котором запущена эта служба.</span><span class="sxs-lookup"><span data-stu-id="8d967-106">The DNS name to look up to find a server running this service.</span></span>



| <span data-ttu-id="8d967-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-107">Entry</span></span> | <span data-ttu-id="8d967-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8d967-109">CN</span><span class="sxs-lookup"><span data-stu-id="8d967-109">CN</span></span>                | <span data-ttu-id="8d967-110">Service-DNS-имя</span><span class="sxs-lookup"><span data-stu-id="8d967-110">Service-DNS-Name</span></span>                            |
| <span data-ttu-id="8d967-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8d967-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8d967-112">serviceDNSName</span><span class="sxs-lookup"><span data-stu-id="8d967-112">serviceDNSName</span></span>                              |
| <span data-ttu-id="8d967-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8d967-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8d967-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8d967-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="8d967-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8d967-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8d967-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-116">Attribute-Id</span></span>      | <span data-ttu-id="8d967-117">1.2.840.113556.1.4.657</span><span class="sxs-lookup"><span data-stu-id="8d967-117">1.2.840.113556.1.4.657</span></span>                      |
| <span data-ttu-id="8d967-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8d967-118">System-Id-Guid</span></span>    | <span data-ttu-id="8d967-119">28630eb8-41d5-11d1-a9c1-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="8d967-119">28630eb8-41d5-11d1-a9c1-0000f80367c1</span></span>        |
| <span data-ttu-id="8d967-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d967-120">Syntax</span></span>            | [<span data-ttu-id="8d967-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8d967-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8d967-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8d967-122">Implementations</span></span>

-   [<span data-ttu-id="8d967-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8d967-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8d967-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8d967-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8d967-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8d967-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8d967-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8d967-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8d967-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8d967-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8d967-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8d967-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8d967-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8d967-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8d967-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-130">Entry</span></span> | <span data-ttu-id="8d967-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8d967-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8d967-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d967-134">System-Only</span></span>            | <span data-ttu-id="8d967-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-135">False</span></span>                                                                   |
| <span data-ttu-id="8d967-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8d967-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8d967-137">True</span><span class="sxs-lookup"><span data-stu-id="8d967-137">True</span></span>                                                                    |
| <span data-ttu-id="8d967-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8d967-138">Is Indexed</span></span>             | <span data-ttu-id="8d967-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-139">False</span></span>                                                                   |
| <span data-ttu-id="8d967-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8d967-140">In Global Catalog</span></span>      | <span data-ttu-id="8d967-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-141">False</span></span>                                                                   |
| <span data-ttu-id="8d967-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8d967-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d967-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d967-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8d967-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d967-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d967-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-146">Search-Flags</span></span>           | <span data-ttu-id="8d967-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d967-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="8d967-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-148">System-Flags</span></span>           | <span data-ttu-id="8d967-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d967-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="8d967-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8d967-150">Classes used in</span></span>        | [<span data-ttu-id="8d967-151">**Служба — точка подключения**</span><span class="sxs-lookup"><span data-stu-id="8d967-151">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8d967-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8d967-152">Windows Server 2003</span></span>



| <span data-ttu-id="8d967-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-153">Entry</span></span> | <span data-ttu-id="8d967-154">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8d967-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8d967-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d967-157">System-Only</span></span>            | <span data-ttu-id="8d967-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-158">False</span></span>                                                                   |
| <span data-ttu-id="8d967-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8d967-159">Is-Single-Valued</span></span>       | <span data-ttu-id="8d967-160">True</span><span class="sxs-lookup"><span data-stu-id="8d967-160">True</span></span>                                                                    |
| <span data-ttu-id="8d967-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8d967-161">Is Indexed</span></span>             | <span data-ttu-id="8d967-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-162">False</span></span>                                                                   |
| <span data-ttu-id="8d967-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8d967-163">In Global Catalog</span></span>      | <span data-ttu-id="8d967-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-164">False</span></span>                                                                   |
| <span data-ttu-id="8d967-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8d967-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d967-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d967-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8d967-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d967-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d967-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-169">Search-Flags</span></span>           | <span data-ttu-id="8d967-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d967-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="8d967-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-171">System-Flags</span></span>           | <span data-ttu-id="8d967-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d967-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="8d967-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8d967-173">Classes used in</span></span>        | [<span data-ttu-id="8d967-174">**Служба — точка подключения**</span><span class="sxs-lookup"><span data-stu-id="8d967-174">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8d967-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8d967-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8d967-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-176">Entry</span></span> | <span data-ttu-id="8d967-177">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8d967-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8d967-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d967-180">System-Only</span></span>            | <span data-ttu-id="8d967-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-181">False</span></span>                                                                   |
| <span data-ttu-id="8d967-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8d967-182">Is-Single-Valued</span></span>       | <span data-ttu-id="8d967-183">True</span><span class="sxs-lookup"><span data-stu-id="8d967-183">True</span></span>                                                                    |
| <span data-ttu-id="8d967-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8d967-184">Is Indexed</span></span>             | <span data-ttu-id="8d967-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-185">False</span></span>                                                                   |
| <span data-ttu-id="8d967-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8d967-186">In Global Catalog</span></span>      | <span data-ttu-id="8d967-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-187">False</span></span>                                                                   |
| <span data-ttu-id="8d967-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8d967-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d967-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d967-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8d967-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d967-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d967-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-192">Search-Flags</span></span>           | <span data-ttu-id="8d967-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d967-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="8d967-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-194">System-Flags</span></span>           | <span data-ttu-id="8d967-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d967-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="8d967-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8d967-196">Classes used in</span></span>        | [<span data-ttu-id="8d967-197">**Служба — точка подключения**</span><span class="sxs-lookup"><span data-stu-id="8d967-197">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8d967-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d967-198">Windows Server 2008</span></span>



| <span data-ttu-id="8d967-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-199">Entry</span></span> | <span data-ttu-id="8d967-200">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8d967-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8d967-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d967-203">System-Only</span></span>            | <span data-ttu-id="8d967-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-204">False</span></span>                                                                   |
| <span data-ttu-id="8d967-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8d967-205">Is-Single-Valued</span></span>       | <span data-ttu-id="8d967-206">True</span><span class="sxs-lookup"><span data-stu-id="8d967-206">True</span></span>                                                                    |
| <span data-ttu-id="8d967-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8d967-207">Is Indexed</span></span>             | <span data-ttu-id="8d967-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-208">False</span></span>                                                                   |
| <span data-ttu-id="8d967-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8d967-209">In Global Catalog</span></span>      | <span data-ttu-id="8d967-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-210">False</span></span>                                                                   |
| <span data-ttu-id="8d967-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8d967-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d967-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d967-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8d967-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d967-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d967-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-215">Search-Flags</span></span>           | <span data-ttu-id="8d967-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d967-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="8d967-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-217">System-Flags</span></span>           | <span data-ttu-id="8d967-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d967-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="8d967-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8d967-219">Classes used in</span></span>        | [<span data-ttu-id="8d967-220">**Служба — точка подключения**</span><span class="sxs-lookup"><span data-stu-id="8d967-220">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8d967-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8d967-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8d967-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-222">Entry</span></span> | <span data-ttu-id="8d967-223">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8d967-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8d967-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d967-226">System-Only</span></span>            | <span data-ttu-id="8d967-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-227">False</span></span>                                                                   |
| <span data-ttu-id="8d967-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8d967-228">Is-Single-Valued</span></span>       | <span data-ttu-id="8d967-229">True</span><span class="sxs-lookup"><span data-stu-id="8d967-229">True</span></span>                                                                    |
| <span data-ttu-id="8d967-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8d967-230">Is Indexed</span></span>             | <span data-ttu-id="8d967-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-231">False</span></span>                                                                   |
| <span data-ttu-id="8d967-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8d967-232">In Global Catalog</span></span>      | <span data-ttu-id="8d967-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-233">False</span></span>                                                                   |
| <span data-ttu-id="8d967-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8d967-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d967-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d967-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8d967-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d967-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d967-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-238">Search-Flags</span></span>           | <span data-ttu-id="8d967-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d967-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="8d967-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-240">System-Flags</span></span>           | <span data-ttu-id="8d967-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d967-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="8d967-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8d967-242">Classes used in</span></span>        | [<span data-ttu-id="8d967-243">**Служба — точка подключения**</span><span class="sxs-lookup"><span data-stu-id="8d967-243">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8d967-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8d967-244">Windows Server 2012</span></span>



| <span data-ttu-id="8d967-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="8d967-245">Entry</span></span> | <span data-ttu-id="8d967-246">Значение</span><span class="sxs-lookup"><span data-stu-id="8d967-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8d967-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8d967-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8d967-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="8d967-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="8d967-249">System-Only</span></span>            | <span data-ttu-id="8d967-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-250">False</span></span>                                                                   |
| <span data-ttu-id="8d967-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8d967-251">Is-Single-Valued</span></span>       | <span data-ttu-id="8d967-252">True</span><span class="sxs-lookup"><span data-stu-id="8d967-252">True</span></span>                                                                    |
| <span data-ttu-id="8d967-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8d967-253">Is Indexed</span></span>             | <span data-ttu-id="8d967-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-254">False</span></span>                                                                   |
| <span data-ttu-id="8d967-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8d967-255">In Global Catalog</span></span>      | <span data-ttu-id="8d967-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8d967-256">False</span></span>                                                                   |
| <span data-ttu-id="8d967-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8d967-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="8d967-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8d967-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="8d967-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8d967-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8d967-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="8d967-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-261">Search-Flags</span></span>           | <span data-ttu-id="8d967-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8d967-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="8d967-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8d967-263">System-Flags</span></span>           | <span data-ttu-id="8d967-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8d967-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="8d967-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8d967-265">Classes used in</span></span>        | [<span data-ttu-id="8d967-266">**Служба — точка подключения**</span><span class="sxs-lookup"><span data-stu-id="8d967-266">**Service-Connection-Point**</span></span>](c-serviceconnectionpoint.md)<br/> |



 

 





