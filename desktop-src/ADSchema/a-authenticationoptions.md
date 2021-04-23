---
title: Атрибут Authentication-Options
description: Параметры проверки подлинности, используемые в ADSI для привязки к объектам служб каталогов.
ms.assetid: a6dc4591-d825-456a-8f77-78cb3c91af9f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Authentication-Options
- Схема AD атрибута authenticationOptions
topic_type:
- apiref
api_name:
- Authentication-Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa9c422dfe196ab002c02c361759461f43965d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138307"
---
# <a name="authentication-options-attribute"></a><span data-ttu-id="cec5f-105">Атрибут Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="cec5f-105">Authentication-Options attribute</span></span>

<span data-ttu-id="cec5f-106">Параметры проверки подлинности, используемые в ADSI для привязки к объектам служб каталогов.</span><span class="sxs-lookup"><span data-stu-id="cec5f-106">The authentication options used in ADSI to bind to directory services objects.</span></span>



| <span data-ttu-id="cec5f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-107">Entry</span></span> | <span data-ttu-id="cec5f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec5f-109">CN</span><span class="sxs-lookup"><span data-stu-id="cec5f-109">CN</span></span>                | <span data-ttu-id="cec5f-110">Authentication-Options</span><span class="sxs-lookup"><span data-stu-id="cec5f-110">Authentication-Options</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="cec5f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cec5f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cec5f-112">authenticationOptions</span><span class="sxs-lookup"><span data-stu-id="cec5f-112">authenticationOptions</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cec5f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cec5f-113">Size</span></span>              | <span data-ttu-id="cec5f-114">4 байта.</span><span class="sxs-lookup"><span data-stu-id="cec5f-114">4 bytes.</span></span> <span data-ttu-id="cec5f-115">Значения, определенные в IADS. h: общедоступная \_ \_ Проверка подлинности ADS, рекламные объявления, \_ использование \_ шифрования 0x2, объявления, использование \_ \_ протокола SSL 0x2, ADS \_ ReadOnly Server 0x4, рекламные объявления, запрос на рекламу \_ \_ \_ , учетные записи 0x8, баннеры \_ без \_ проверки подлинности, реклама \_ \_ \_ \_ \_ использование \_ запечатывания 0x80</span><span class="sxs-lookup"><span data-stu-id="cec5f-115">Values defined in IADS.h: ADS\_SECURE\_AUTHENTICATION 0x1, ADS\_USE\_ENCRYPTION 0x2, ADS\_USE\_SSL 0x2, ADS\_READONLY\_SERVER 0x4, ADS\_PROMPT\_CREDENTIALS 0x8, ADS\_NO\_AUTHENTICATION 0x10, ADS\_FAST\_BIND 0x20, ADS\_USE\_SIGNING 0x40, ADS\_USE\_SEALING 0x80</span></span> |
| <span data-ttu-id="cec5f-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cec5f-116">Update Privilege</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cec5f-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cec5f-117">Update Frequency</span></span>  | \-                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cec5f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-118">Attribute-Id</span></span>      | <span data-ttu-id="cec5f-119">1.2.840.113556.1.4.11</span><span class="sxs-lookup"><span data-stu-id="cec5f-119">1.2.840.113556.1.4.11</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cec5f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cec5f-120">System-Id-Guid</span></span>    | <span data-ttu-id="cec5f-121">bf967928-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="cec5f-121">bf967928-0de6-11d0-a285-00aa003049e2</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="cec5f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cec5f-122">Syntax</span></span>            | [<span data-ttu-id="cec5f-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="cec5f-123">**Enumeration**</span></span>](s-enumeration.md)                                                                                                                                                                                                                                         |



## <a name="implementations"></a><span data-ttu-id="cec5f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cec5f-124">Implementations</span></span>

-   [<span data-ttu-id="cec5f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cec5f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cec5f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cec5f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cec5f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cec5f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cec5f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cec5f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cec5f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cec5f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cec5f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cec5f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cec5f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cec5f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="cec5f-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-132">Entry</span></span> | <span data-ttu-id="cec5f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-133">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cec5f-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cec5f-134">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-135">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec5f-136">System-Only</span></span>            | <span data-ttu-id="cec5f-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-137">False</span></span>                                              |
| <span data-ttu-id="cec5f-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cec5f-138">Is-Single-Valued</span></span>       | <span data-ttu-id="cec5f-139">True</span><span class="sxs-lookup"><span data-stu-id="cec5f-139">True</span></span>                                               |
| <span data-ttu-id="cec5f-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cec5f-140">Is Indexed</span></span>             | <span data-ttu-id="cec5f-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-141">False</span></span>                                              |
| <span data-ttu-id="cec5f-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cec5f-142">In Global Catalog</span></span>      | <span data-ttu-id="cec5f-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-143">False</span></span>                                              |
| <span data-ttu-id="cec5f-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cec5f-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec5f-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cec5f-145">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cec5f-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec5f-146">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec5f-147">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-148">Search-Flags</span></span>           | <span data-ttu-id="cec5f-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec5f-149">0x00000000</span></span>                                         |
| <span data-ttu-id="cec5f-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-150">System-Flags</span></span>           | <span data-ttu-id="cec5f-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec5f-151">0x00000010</span></span>                                         |
| <span data-ttu-id="cec5f-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cec5f-152">Classes used in</span></span>        | [<span data-ttu-id="cec5f-153">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cec5f-153">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cec5f-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cec5f-154">Windows Server 2003</span></span>



| <span data-ttu-id="cec5f-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-155">Entry</span></span> | <span data-ttu-id="cec5f-156">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-156">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cec5f-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cec5f-157">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-158">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec5f-159">System-Only</span></span>            | <span data-ttu-id="cec5f-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-160">False</span></span>                                              |
| <span data-ttu-id="cec5f-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cec5f-161">Is-Single-Valued</span></span>       | <span data-ttu-id="cec5f-162">True</span><span class="sxs-lookup"><span data-stu-id="cec5f-162">True</span></span>                                               |
| <span data-ttu-id="cec5f-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cec5f-163">Is Indexed</span></span>             | <span data-ttu-id="cec5f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-164">False</span></span>                                              |
| <span data-ttu-id="cec5f-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cec5f-165">In Global Catalog</span></span>      | <span data-ttu-id="cec5f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-166">False</span></span>                                              |
| <span data-ttu-id="cec5f-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cec5f-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec5f-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cec5f-168">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cec5f-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec5f-169">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec5f-170">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-171">Search-Flags</span></span>           | <span data-ttu-id="cec5f-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec5f-172">0x00000000</span></span>                                         |
| <span data-ttu-id="cec5f-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-173">System-Flags</span></span>           | <span data-ttu-id="cec5f-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec5f-174">0x00000010</span></span>                                         |
| <span data-ttu-id="cec5f-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cec5f-175">Classes used in</span></span>        | [<span data-ttu-id="cec5f-176">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cec5f-176">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cec5f-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cec5f-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cec5f-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-178">Entry</span></span> | <span data-ttu-id="cec5f-179">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-179">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cec5f-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cec5f-180">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-181">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec5f-182">System-Only</span></span>            | <span data-ttu-id="cec5f-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-183">False</span></span>                                              |
| <span data-ttu-id="cec5f-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cec5f-184">Is-Single-Valued</span></span>       | <span data-ttu-id="cec5f-185">True</span><span class="sxs-lookup"><span data-stu-id="cec5f-185">True</span></span>                                               |
| <span data-ttu-id="cec5f-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cec5f-186">Is Indexed</span></span>             | <span data-ttu-id="cec5f-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-187">False</span></span>                                              |
| <span data-ttu-id="cec5f-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cec5f-188">In Global Catalog</span></span>      | <span data-ttu-id="cec5f-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-189">False</span></span>                                              |
| <span data-ttu-id="cec5f-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cec5f-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec5f-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cec5f-191">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cec5f-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec5f-192">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec5f-193">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-194">Search-Flags</span></span>           | <span data-ttu-id="cec5f-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec5f-195">0x00000000</span></span>                                         |
| <span data-ttu-id="cec5f-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-196">System-Flags</span></span>           | <span data-ttu-id="cec5f-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec5f-197">0x00000010</span></span>                                         |
| <span data-ttu-id="cec5f-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cec5f-198">Classes used in</span></span>        | [<span data-ttu-id="cec5f-199">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cec5f-199">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cec5f-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cec5f-200">Windows Server 2008</span></span>



| <span data-ttu-id="cec5f-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-201">Entry</span></span> | <span data-ttu-id="cec5f-202">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-202">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cec5f-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cec5f-203">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-204">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec5f-205">System-Only</span></span>            | <span data-ttu-id="cec5f-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-206">False</span></span>                                              |
| <span data-ttu-id="cec5f-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cec5f-207">Is-Single-Valued</span></span>       | <span data-ttu-id="cec5f-208">True</span><span class="sxs-lookup"><span data-stu-id="cec5f-208">True</span></span>                                               |
| <span data-ttu-id="cec5f-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cec5f-209">Is Indexed</span></span>             | <span data-ttu-id="cec5f-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-210">False</span></span>                                              |
| <span data-ttu-id="cec5f-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cec5f-211">In Global Catalog</span></span>      | <span data-ttu-id="cec5f-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-212">False</span></span>                                              |
| <span data-ttu-id="cec5f-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cec5f-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec5f-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cec5f-214">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cec5f-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec5f-215">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec5f-216">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-217">Search-Flags</span></span>           | <span data-ttu-id="cec5f-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec5f-218">0x00000000</span></span>                                         |
| <span data-ttu-id="cec5f-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-219">System-Flags</span></span>           | <span data-ttu-id="cec5f-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec5f-220">0x00000010</span></span>                                         |
| <span data-ttu-id="cec5f-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cec5f-221">Classes used in</span></span>        | [<span data-ttu-id="cec5f-222">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cec5f-222">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cec5f-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cec5f-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cec5f-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-224">Entry</span></span> | <span data-ttu-id="cec5f-225">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-225">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cec5f-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cec5f-226">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-227">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec5f-228">System-Only</span></span>            | <span data-ttu-id="cec5f-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-229">False</span></span>                                              |
| <span data-ttu-id="cec5f-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cec5f-230">Is-Single-Valued</span></span>       | <span data-ttu-id="cec5f-231">True</span><span class="sxs-lookup"><span data-stu-id="cec5f-231">True</span></span>                                               |
| <span data-ttu-id="cec5f-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cec5f-232">Is Indexed</span></span>             | <span data-ttu-id="cec5f-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-233">False</span></span>                                              |
| <span data-ttu-id="cec5f-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cec5f-234">In Global Catalog</span></span>      | <span data-ttu-id="cec5f-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-235">False</span></span>                                              |
| <span data-ttu-id="cec5f-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cec5f-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec5f-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cec5f-237">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cec5f-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec5f-238">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec5f-239">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-240">Search-Flags</span></span>           | <span data-ttu-id="cec5f-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec5f-241">0x00000000</span></span>                                         |
| <span data-ttu-id="cec5f-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-242">System-Flags</span></span>           | <span data-ttu-id="cec5f-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec5f-243">0x00000010</span></span>                                         |
| <span data-ttu-id="cec5f-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cec5f-244">Classes used in</span></span>        | [<span data-ttu-id="cec5f-245">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cec5f-245">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cec5f-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cec5f-246">Windows Server 2012</span></span>



| <span data-ttu-id="cec5f-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="cec5f-247">Entry</span></span> | <span data-ttu-id="cec5f-248">Значение</span><span class="sxs-lookup"><span data-stu-id="cec5f-248">Value</span></span> |
|------------------------|----------------------------------------------------|
| <span data-ttu-id="cec5f-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cec5f-249">Link-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cec5f-250">MAPI-Id</span></span>                | \-                                                 |
| <span data-ttu-id="cec5f-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="cec5f-251">System-Only</span></span>            | <span data-ttu-id="cec5f-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-252">False</span></span>                                              |
| <span data-ttu-id="cec5f-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cec5f-253">Is-Single-Valued</span></span>       | <span data-ttu-id="cec5f-254">True</span><span class="sxs-lookup"><span data-stu-id="cec5f-254">True</span></span>                                               |
| <span data-ttu-id="cec5f-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cec5f-255">Is Indexed</span></span>             | <span data-ttu-id="cec5f-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-256">False</span></span>                                              |
| <span data-ttu-id="cec5f-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cec5f-257">In Global Catalog</span></span>      | <span data-ttu-id="cec5f-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="cec5f-258">False</span></span>                                              |
| <span data-ttu-id="cec5f-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cec5f-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="cec5f-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cec5f-260">O:BAG:BAD:S:</span></span>                                       |
| <span data-ttu-id="cec5f-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cec5f-261">Range-Lower</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cec5f-262">Range-Upper</span></span>            | \-                                                 |
| <span data-ttu-id="cec5f-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-263">Search-Flags</span></span>           | <span data-ttu-id="cec5f-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cec5f-264">0x00000000</span></span>                                         |
| <span data-ttu-id="cec5f-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cec5f-265">System-Flags</span></span>           | <span data-ttu-id="cec5f-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cec5f-266">0x00000010</span></span>                                         |
| <span data-ttu-id="cec5f-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cec5f-267">Classes used in</span></span>        | [<span data-ttu-id="cec5f-268">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="cec5f-268">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> |



 

 





