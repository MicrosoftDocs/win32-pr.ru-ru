---
title: Атрибут Initial-auth-входящим
description: Содержит сведения о первоначальном входящем запросе проверки подлинности от клиента к серверу. Этот запрос отправляется этим сервером на сервер проверки подлинности для домена.
ms.assetid: d49d45ae-87fe-415d-8110-79b2b321f2b6
ms.tgt_platform: multiple
keywords:
- Initial-auth-схема Active Directory для входящих атрибутов
- Схема AD атрибута Инитиалаусинкоминг
topic_type:
- apiref
api_name:
- Initial-Auth-Incoming
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b00abd5b77b713fc03b5efb3d4cf45b97fc19
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804780"
---
# <a name="initial-auth-incoming-attribute"></a><span data-ttu-id="f2ed5-106">Атрибут Initial-auth-входящим</span><span class="sxs-lookup"><span data-stu-id="f2ed5-106">Initial-Auth-Incoming attribute</span></span>

<span data-ttu-id="f2ed5-107">Содержит сведения о первоначальном входящем запросе проверки подлинности от клиента к серверу.</span><span class="sxs-lookup"><span data-stu-id="f2ed5-107">Contains information about an initial incoming authentication request by a client to this server.</span></span> <span data-ttu-id="f2ed5-108">Этот запрос отправляется этим сервером на сервер проверки подлинности для домена.</span><span class="sxs-lookup"><span data-stu-id="f2ed5-108">This request is then sent by this server to the authentication server for the domain.</span></span>



| <span data-ttu-id="f2ed5-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-109">Entry</span></span> | <span data-ttu-id="f2ed5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f2ed5-111">CN</span><span class="sxs-lookup"><span data-stu-id="f2ed5-111">CN</span></span>                | <span data-ttu-id="f2ed5-112">Initial-auth-входящий</span><span class="sxs-lookup"><span data-stu-id="f2ed5-112">Initial-Auth-Incoming</span></span>                       |
| <span data-ttu-id="f2ed5-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f2ed5-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f2ed5-114">инитиалаусинкоминг</span><span class="sxs-lookup"><span data-stu-id="f2ed5-114">initialAuthIncoming</span></span>                         |
| <span data-ttu-id="f2ed5-115">Размер</span><span class="sxs-lookup"><span data-stu-id="f2ed5-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="f2ed5-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f2ed5-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f2ed5-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f2ed5-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f2ed5-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-118">Attribute-Id</span></span>      | <span data-ttu-id="f2ed5-119">1.2.840.113556.1.4.539</span><span class="sxs-lookup"><span data-stu-id="f2ed5-119">1.2.840.113556.1.4.539</span></span>                      |
| <span data-ttu-id="f2ed5-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f2ed5-120">System-Id-Guid</span></span>    | <span data-ttu-id="f2ed5-121">52458023-ca6a-11D0-аффф-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f2ed5-121">52458023-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="f2ed5-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2ed5-122">Syntax</span></span>            | [<span data-ttu-id="f2ed5-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f2ed5-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f2ed5-124">Implementations</span></span>

-   [<span data-ttu-id="f2ed5-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f2ed5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f2ed5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f2ed5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f2ed5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f2ed5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f2ed5-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f2ed5-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f2ed5-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-132">Entry</span></span> | <span data-ttu-id="f2ed5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ed5-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2ed5-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ed5-136">System-Only</span></span>            | <span data-ttu-id="f2ed5-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-137">False</span></span>                                                |
| <span data-ttu-id="f2ed5-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2ed5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ed5-139">True</span><span class="sxs-lookup"><span data-stu-id="f2ed5-139">True</span></span>                                                 |
| <span data-ttu-id="f2ed5-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2ed5-140">Is Indexed</span></span>             | <span data-ttu-id="f2ed5-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-141">False</span></span>                                                |
| <span data-ttu-id="f2ed5-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2ed5-142">In Global Catalog</span></span>      | <span data-ttu-id="f2ed5-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-143">False</span></span>                                                |
| <span data-ttu-id="f2ed5-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2ed5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ed5-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ed5-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f2ed5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ed5-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ed5-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-148">Search-Flags</span></span>           | <span data-ttu-id="f2ed5-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ed5-149">0x00000000</span></span>                                           |
| <span data-ttu-id="f2ed5-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-150">System-Flags</span></span>           | <span data-ttu-id="f2ed5-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ed5-151">0x00000010</span></span>                                           |
| <span data-ttu-id="f2ed5-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2ed5-152">Classes used in</span></span>        | [<span data-ttu-id="f2ed5-153">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f2ed5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f2ed5-154">Windows Server 2003</span></span>



| <span data-ttu-id="f2ed5-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-155">Entry</span></span> | <span data-ttu-id="f2ed5-156">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ed5-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2ed5-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ed5-159">System-Only</span></span>            | <span data-ttu-id="f2ed5-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-160">False</span></span>                                                |
| <span data-ttu-id="f2ed5-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2ed5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ed5-162">True</span><span class="sxs-lookup"><span data-stu-id="f2ed5-162">True</span></span>                                                 |
| <span data-ttu-id="f2ed5-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2ed5-163">Is Indexed</span></span>             | <span data-ttu-id="f2ed5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-164">False</span></span>                                                |
| <span data-ttu-id="f2ed5-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2ed5-165">In Global Catalog</span></span>      | <span data-ttu-id="f2ed5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-166">False</span></span>                                                |
| <span data-ttu-id="f2ed5-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2ed5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ed5-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ed5-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f2ed5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ed5-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ed5-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-171">Search-Flags</span></span>           | <span data-ttu-id="f2ed5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ed5-172">0x00000000</span></span>                                           |
| <span data-ttu-id="f2ed5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-173">System-Flags</span></span>           | <span data-ttu-id="f2ed5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ed5-174">0x00000010</span></span>                                           |
| <span data-ttu-id="f2ed5-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2ed5-175">Classes used in</span></span>        | [<span data-ttu-id="f2ed5-176">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f2ed5-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f2ed5-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f2ed5-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-178">Entry</span></span> | <span data-ttu-id="f2ed5-179">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ed5-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2ed5-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ed5-182">System-Only</span></span>            | <span data-ttu-id="f2ed5-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-183">False</span></span>                                                |
| <span data-ttu-id="f2ed5-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2ed5-184">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ed5-185">True</span><span class="sxs-lookup"><span data-stu-id="f2ed5-185">True</span></span>                                                 |
| <span data-ttu-id="f2ed5-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2ed5-186">Is Indexed</span></span>             | <span data-ttu-id="f2ed5-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-187">False</span></span>                                                |
| <span data-ttu-id="f2ed5-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2ed5-188">In Global Catalog</span></span>      | <span data-ttu-id="f2ed5-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-189">False</span></span>                                                |
| <span data-ttu-id="f2ed5-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2ed5-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ed5-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ed5-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f2ed5-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ed5-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ed5-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-194">Search-Flags</span></span>           | <span data-ttu-id="f2ed5-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ed5-195">0x00000000</span></span>                                           |
| <span data-ttu-id="f2ed5-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-196">System-Flags</span></span>           | <span data-ttu-id="f2ed5-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ed5-197">0x00000010</span></span>                                           |
| <span data-ttu-id="f2ed5-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2ed5-198">Classes used in</span></span>        | [<span data-ttu-id="f2ed5-199">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f2ed5-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2ed5-200">Windows Server 2008</span></span>



| <span data-ttu-id="f2ed5-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-201">Entry</span></span> | <span data-ttu-id="f2ed5-202">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ed5-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2ed5-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ed5-205">System-Only</span></span>            | <span data-ttu-id="f2ed5-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-206">False</span></span>                                                |
| <span data-ttu-id="f2ed5-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2ed5-207">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ed5-208">True</span><span class="sxs-lookup"><span data-stu-id="f2ed5-208">True</span></span>                                                 |
| <span data-ttu-id="f2ed5-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2ed5-209">Is Indexed</span></span>             | <span data-ttu-id="f2ed5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-210">False</span></span>                                                |
| <span data-ttu-id="f2ed5-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2ed5-211">In Global Catalog</span></span>      | <span data-ttu-id="f2ed5-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-212">False</span></span>                                                |
| <span data-ttu-id="f2ed5-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2ed5-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ed5-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ed5-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f2ed5-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ed5-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ed5-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-217">Search-Flags</span></span>           | <span data-ttu-id="f2ed5-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ed5-218">0x00000000</span></span>                                           |
| <span data-ttu-id="f2ed5-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-219">System-Flags</span></span>           | <span data-ttu-id="f2ed5-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ed5-220">0x00000010</span></span>                                           |
| <span data-ttu-id="f2ed5-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2ed5-221">Classes used in</span></span>        | [<span data-ttu-id="f2ed5-222">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f2ed5-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f2ed5-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f2ed5-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-224">Entry</span></span> | <span data-ttu-id="f2ed5-225">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ed5-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2ed5-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ed5-228">System-Only</span></span>            | <span data-ttu-id="f2ed5-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-229">False</span></span>                                                |
| <span data-ttu-id="f2ed5-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2ed5-230">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ed5-231">True</span><span class="sxs-lookup"><span data-stu-id="f2ed5-231">True</span></span>                                                 |
| <span data-ttu-id="f2ed5-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2ed5-232">Is Indexed</span></span>             | <span data-ttu-id="f2ed5-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-233">False</span></span>                                                |
| <span data-ttu-id="f2ed5-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2ed5-234">In Global Catalog</span></span>      | <span data-ttu-id="f2ed5-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-235">False</span></span>                                                |
| <span data-ttu-id="f2ed5-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2ed5-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ed5-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ed5-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f2ed5-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ed5-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ed5-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-240">Search-Flags</span></span>           | <span data-ttu-id="f2ed5-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ed5-241">0x00000000</span></span>                                           |
| <span data-ttu-id="f2ed5-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-242">System-Flags</span></span>           | <span data-ttu-id="f2ed5-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ed5-243">0x00000010</span></span>                                           |
| <span data-ttu-id="f2ed5-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2ed5-244">Classes used in</span></span>        | [<span data-ttu-id="f2ed5-245">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f2ed5-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f2ed5-246">Windows Server 2012</span></span>



| <span data-ttu-id="f2ed5-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="f2ed5-247">Entry</span></span> | <span data-ttu-id="f2ed5-248">Значение</span><span class="sxs-lookup"><span data-stu-id="f2ed5-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f2ed5-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f2ed5-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f2ed5-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f2ed5-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="f2ed5-251">System-Only</span></span>            | <span data-ttu-id="f2ed5-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-252">False</span></span>                                                |
| <span data-ttu-id="f2ed5-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f2ed5-253">Is-Single-Valued</span></span>       | <span data-ttu-id="f2ed5-254">True</span><span class="sxs-lookup"><span data-stu-id="f2ed5-254">True</span></span>                                                 |
| <span data-ttu-id="f2ed5-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f2ed5-255">Is Indexed</span></span>             | <span data-ttu-id="f2ed5-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-256">False</span></span>                                                |
| <span data-ttu-id="f2ed5-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f2ed5-257">In Global Catalog</span></span>      | <span data-ttu-id="f2ed5-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="f2ed5-258">False</span></span>                                                |
| <span data-ttu-id="f2ed5-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f2ed5-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="f2ed5-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f2ed5-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f2ed5-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f2ed5-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f2ed5-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="f2ed5-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-263">Search-Flags</span></span>           | <span data-ttu-id="f2ed5-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f2ed5-264">0x00000000</span></span>                                           |
| <span data-ttu-id="f2ed5-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f2ed5-265">System-Flags</span></span>           | <span data-ttu-id="f2ed5-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f2ed5-266">0x00000010</span></span>                                           |
| <span data-ttu-id="f2ed5-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f2ed5-267">Classes used in</span></span>        | [<span data-ttu-id="f2ed5-268">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="f2ed5-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





