---
title: Атрибут Initial-auth-исходящий
description: Содержит сведения о первоначальной исходящей проверке подлинности, отправленной сервером аутентификации для данного домена клиенту, который запросил проверку подлинности.
ms.assetid: cc5ceb14-0424-4caa-bcd9-1e48988af67a
ms.tgt_platform: multiple
keywords:
- Начальная проверка подлинности-схема AD исходящего атрибута
- Схема AD атрибута Инитиалаусаутгоинг
topic_type:
- apiref
api_name:
- Initial-Auth-Outgoing
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84faaa443c9589e04f4998dc41d72fe870b5f2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138142"
---
# <a name="initial-auth-outgoing-attribute"></a><span data-ttu-id="e5d68-105">Атрибут Initial-auth-исходящий</span><span class="sxs-lookup"><span data-stu-id="e5d68-105">Initial-Auth-Outgoing attribute</span></span>

<span data-ttu-id="e5d68-106">Содержит сведения о первоначальной исходящей проверке подлинности, отправленной сервером аутентификации для данного домена клиенту, который запросил проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="e5d68-106">Contains information about an initial outgoing authentication sent by the authentication server for this domain to the client that requested authentication.</span></span> <span data-ttu-id="e5d68-107">Сервер, использующий этот атрибут, получает авторизацию от сервера проверки подлинности и отправляет его клиенту.</span><span class="sxs-lookup"><span data-stu-id="e5d68-107">The server that uses this attribute receives the authorization from the authentication server and sends it to the client.</span></span>



| <span data-ttu-id="e5d68-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-108">Entry</span></span> | <span data-ttu-id="e5d68-109">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-109">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="e5d68-110">CN</span><span class="sxs-lookup"><span data-stu-id="e5d68-110">CN</span></span>                | <span data-ttu-id="e5d68-111">Initial-auth-исходящий трафик</span><span class="sxs-lookup"><span data-stu-id="e5d68-111">Initial-Auth-Outgoing</span></span>                       |
| <span data-ttu-id="e5d68-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e5d68-112">Ldap-Display-Name</span></span> | <span data-ttu-id="e5d68-113">инитиалаусаутгоинг</span><span class="sxs-lookup"><span data-stu-id="e5d68-113">initialAuthOutgoing</span></span>                         |
| <span data-ttu-id="e5d68-114">Размер</span><span class="sxs-lookup"><span data-stu-id="e5d68-114">Size</span></span>              | \-                                          |
| <span data-ttu-id="e5d68-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e5d68-115">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="e5d68-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e5d68-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="e5d68-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-117">Attribute-Id</span></span>      | <span data-ttu-id="e5d68-118">1.2.840.113556.1.4.540</span><span class="sxs-lookup"><span data-stu-id="e5d68-118">1.2.840.113556.1.4.540</span></span>                      |
| <span data-ttu-id="e5d68-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e5d68-119">System-Id-Guid</span></span>    | <span data-ttu-id="e5d68-120">52458024-ca6a-11D0-аффф-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e5d68-120">52458024-ca6a-11d0-afff-0000f80367c1</span></span>        |
| <span data-ttu-id="e5d68-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5d68-121">Syntax</span></span>            | [<span data-ttu-id="e5d68-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e5d68-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="e5d68-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e5d68-123">Implementations</span></span>

-   [<span data-ttu-id="e5d68-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e5d68-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e5d68-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e5d68-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e5d68-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e5d68-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e5d68-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e5d68-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e5d68-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e5d68-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e5d68-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e5d68-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e5d68-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5d68-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e5d68-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-131">Entry</span></span> | <span data-ttu-id="e5d68-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5d68-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e5d68-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-134">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5d68-135">System-Only</span></span>            | <span data-ttu-id="e5d68-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-136">False</span></span>                                                |
| <span data-ttu-id="e5d68-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e5d68-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e5d68-138">True</span><span class="sxs-lookup"><span data-stu-id="e5d68-138">True</span></span>                                                 |
| <span data-ttu-id="e5d68-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e5d68-139">Is Indexed</span></span>             | <span data-ttu-id="e5d68-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-140">False</span></span>                                                |
| <span data-ttu-id="e5d68-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e5d68-141">In Global Catalog</span></span>      | <span data-ttu-id="e5d68-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-142">False</span></span>                                                |
| <span data-ttu-id="e5d68-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e5d68-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5d68-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5d68-144">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5d68-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5d68-145">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5d68-146">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-147">Search-Flags</span></span>           | <span data-ttu-id="e5d68-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5d68-148">0x00000000</span></span>                                           |
| <span data-ttu-id="e5d68-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-149">System-Flags</span></span>           | <span data-ttu-id="e5d68-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5d68-150">0x00000010</span></span>                                           |
| <span data-ttu-id="e5d68-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e5d68-151">Classes used in</span></span>        | [<span data-ttu-id="e5d68-152">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="e5d68-152">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e5d68-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e5d68-153">Windows Server 2003</span></span>



| <span data-ttu-id="e5d68-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-154">Entry</span></span> | <span data-ttu-id="e5d68-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-155">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5d68-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e5d68-156">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-157">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5d68-158">System-Only</span></span>            | <span data-ttu-id="e5d68-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-159">False</span></span>                                                |
| <span data-ttu-id="e5d68-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e5d68-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e5d68-161">True</span><span class="sxs-lookup"><span data-stu-id="e5d68-161">True</span></span>                                                 |
| <span data-ttu-id="e5d68-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e5d68-162">Is Indexed</span></span>             | <span data-ttu-id="e5d68-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-163">False</span></span>                                                |
| <span data-ttu-id="e5d68-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e5d68-164">In Global Catalog</span></span>      | <span data-ttu-id="e5d68-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-165">False</span></span>                                                |
| <span data-ttu-id="e5d68-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e5d68-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5d68-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5d68-167">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5d68-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5d68-168">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5d68-169">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-170">Search-Flags</span></span>           | <span data-ttu-id="e5d68-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5d68-171">0x00000000</span></span>                                           |
| <span data-ttu-id="e5d68-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-172">System-Flags</span></span>           | <span data-ttu-id="e5d68-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5d68-173">0x00000010</span></span>                                           |
| <span data-ttu-id="e5d68-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e5d68-174">Classes used in</span></span>        | [<span data-ttu-id="e5d68-175">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="e5d68-175">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e5d68-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e5d68-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e5d68-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-177">Entry</span></span> | <span data-ttu-id="e5d68-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-178">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5d68-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e5d68-179">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-180">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5d68-181">System-Only</span></span>            | <span data-ttu-id="e5d68-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-182">False</span></span>                                                |
| <span data-ttu-id="e5d68-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e5d68-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e5d68-184">True</span><span class="sxs-lookup"><span data-stu-id="e5d68-184">True</span></span>                                                 |
| <span data-ttu-id="e5d68-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e5d68-185">Is Indexed</span></span>             | <span data-ttu-id="e5d68-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-186">False</span></span>                                                |
| <span data-ttu-id="e5d68-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e5d68-187">In Global Catalog</span></span>      | <span data-ttu-id="e5d68-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-188">False</span></span>                                                |
| <span data-ttu-id="e5d68-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e5d68-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5d68-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5d68-190">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5d68-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5d68-191">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5d68-192">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-193">Search-Flags</span></span>           | <span data-ttu-id="e5d68-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5d68-194">0x00000000</span></span>                                           |
| <span data-ttu-id="e5d68-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-195">System-Flags</span></span>           | <span data-ttu-id="e5d68-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5d68-196">0x00000010</span></span>                                           |
| <span data-ttu-id="e5d68-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e5d68-197">Classes used in</span></span>        | [<span data-ttu-id="e5d68-198">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="e5d68-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e5d68-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5d68-199">Windows Server 2008</span></span>



| <span data-ttu-id="e5d68-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-200">Entry</span></span> | <span data-ttu-id="e5d68-201">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-201">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5d68-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e5d68-202">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-203">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5d68-204">System-Only</span></span>            | <span data-ttu-id="e5d68-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-205">False</span></span>                                                |
| <span data-ttu-id="e5d68-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e5d68-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e5d68-207">True</span><span class="sxs-lookup"><span data-stu-id="e5d68-207">True</span></span>                                                 |
| <span data-ttu-id="e5d68-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e5d68-208">Is Indexed</span></span>             | <span data-ttu-id="e5d68-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-209">False</span></span>                                                |
| <span data-ttu-id="e5d68-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e5d68-210">In Global Catalog</span></span>      | <span data-ttu-id="e5d68-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-211">False</span></span>                                                |
| <span data-ttu-id="e5d68-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e5d68-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5d68-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5d68-213">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5d68-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5d68-214">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5d68-215">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-216">Search-Flags</span></span>           | <span data-ttu-id="e5d68-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5d68-217">0x00000000</span></span>                                           |
| <span data-ttu-id="e5d68-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-218">System-Flags</span></span>           | <span data-ttu-id="e5d68-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5d68-219">0x00000010</span></span>                                           |
| <span data-ttu-id="e5d68-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e5d68-220">Classes used in</span></span>        | [<span data-ttu-id="e5d68-221">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="e5d68-221">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e5d68-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e5d68-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e5d68-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-223">Entry</span></span> | <span data-ttu-id="e5d68-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-224">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5d68-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e5d68-225">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-226">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5d68-227">System-Only</span></span>            | <span data-ttu-id="e5d68-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-228">False</span></span>                                                |
| <span data-ttu-id="e5d68-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e5d68-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e5d68-230">True</span><span class="sxs-lookup"><span data-stu-id="e5d68-230">True</span></span>                                                 |
| <span data-ttu-id="e5d68-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e5d68-231">Is Indexed</span></span>             | <span data-ttu-id="e5d68-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-232">False</span></span>                                                |
| <span data-ttu-id="e5d68-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e5d68-233">In Global Catalog</span></span>      | <span data-ttu-id="e5d68-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-234">False</span></span>                                                |
| <span data-ttu-id="e5d68-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e5d68-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5d68-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5d68-236">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5d68-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5d68-237">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5d68-238">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-239">Search-Flags</span></span>           | <span data-ttu-id="e5d68-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5d68-240">0x00000000</span></span>                                           |
| <span data-ttu-id="e5d68-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-241">System-Flags</span></span>           | <span data-ttu-id="e5d68-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5d68-242">0x00000010</span></span>                                           |
| <span data-ttu-id="e5d68-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e5d68-243">Classes used in</span></span>        | [<span data-ttu-id="e5d68-244">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="e5d68-244">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e5d68-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5d68-245">Windows Server 2012</span></span>



| <span data-ttu-id="e5d68-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="e5d68-246">Entry</span></span> | <span data-ttu-id="e5d68-247">Значение</span><span class="sxs-lookup"><span data-stu-id="e5d68-247">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="e5d68-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e5d68-248">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e5d68-249">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="e5d68-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e5d68-250">System-Only</span></span>            | <span data-ttu-id="e5d68-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-251">False</span></span>                                                |
| <span data-ttu-id="e5d68-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e5d68-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e5d68-253">True</span><span class="sxs-lookup"><span data-stu-id="e5d68-253">True</span></span>                                                 |
| <span data-ttu-id="e5d68-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e5d68-254">Is Indexed</span></span>             | <span data-ttu-id="e5d68-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-255">False</span></span>                                                |
| <span data-ttu-id="e5d68-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e5d68-256">In Global Catalog</span></span>      | <span data-ttu-id="e5d68-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="e5d68-257">False</span></span>                                                |
| <span data-ttu-id="e5d68-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e5d68-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e5d68-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e5d68-259">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="e5d68-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e5d68-260">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e5d68-261">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="e5d68-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-262">Search-Flags</span></span>           | <span data-ttu-id="e5d68-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e5d68-263">0x00000000</span></span>                                           |
| <span data-ttu-id="e5d68-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e5d68-264">System-Flags</span></span>           | <span data-ttu-id="e5d68-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e5d68-265">0x00000010</span></span>                                           |
| <span data-ttu-id="e5d68-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e5d68-266">Classes used in</span></span>        | [<span data-ttu-id="e5d68-267">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="e5d68-267">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





