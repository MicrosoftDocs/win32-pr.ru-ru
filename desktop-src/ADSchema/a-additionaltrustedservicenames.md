---
title: Атрибут "дополнительно-Trusted-Service-Names"
description: Список служб в домене, которые могут быть доверенными. Не используется AD.
ms.assetid: 0c574a99-4036-408b-807c-b4b3394624c7
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута "дополнительно-Trustd-Service-Names"
- Схема AD атрибута Аддитионалтрустедсервиценамес
topic_type:
- apiref
api_name:
- Additional-Trusted-Service-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8066190082cfe0f1bbb8825768ad135090a7a4f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655548"
---
# <a name="additional-trusted-service-names-attribute"></a><span data-ttu-id="1e52e-106">Атрибут "дополнительно-Trusted-Service-Names"</span><span class="sxs-lookup"><span data-stu-id="1e52e-106">Additional-Trusted-Service-Names attribute</span></span>

<span data-ttu-id="1e52e-107">Список служб в домене, которые могут быть доверенными.</span><span class="sxs-lookup"><span data-stu-id="1e52e-107">A list of services in the domain that can be trusted.</span></span> <span data-ttu-id="1e52e-108">Не используется AD.</span><span class="sxs-lookup"><span data-stu-id="1e52e-108">Not used by AD.</span></span>



| <span data-ttu-id="1e52e-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-109">Entry</span></span> | <span data-ttu-id="1e52e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1e52e-111">CN</span><span class="sxs-lookup"><span data-stu-id="1e52e-111">CN</span></span>                | <span data-ttu-id="1e52e-112">Дополнительные-доверенные имена служб</span><span class="sxs-lookup"><span data-stu-id="1e52e-112">Additional-Trusted-Service-Names</span></span>            |
| <span data-ttu-id="1e52e-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1e52e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1e52e-114">аддитионалтрустедсервиценамес</span><span class="sxs-lookup"><span data-stu-id="1e52e-114">additionalTrustedServiceNames</span></span>               |
| <span data-ttu-id="1e52e-115">Размер</span><span class="sxs-lookup"><span data-stu-id="1e52e-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="1e52e-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1e52e-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="1e52e-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1e52e-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1e52e-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-118">Attribute-Id</span></span>      | <span data-ttu-id="1e52e-119">1.2.840.113556.1.4.889</span><span class="sxs-lookup"><span data-stu-id="1e52e-119">1.2.840.113556.1.4.889</span></span>                      |
| <span data-ttu-id="1e52e-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1e52e-120">System-Id-Guid</span></span>    | <span data-ttu-id="1e52e-121">032160be-9824-11d1-aec0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1e52e-121">032160be-9824-11d1-aec0-0000f80367c1</span></span>        |
| <span data-ttu-id="1e52e-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e52e-122">Syntax</span></span>            | [<span data-ttu-id="1e52e-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="1e52e-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1e52e-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1e52e-124">Implementations</span></span>

-   [<span data-ttu-id="1e52e-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1e52e-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1e52e-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e52e-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e52e-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e52e-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e52e-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e52e-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e52e-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e52e-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e52e-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e52e-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1e52e-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e52e-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1e52e-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-132">Entry</span></span> | <span data-ttu-id="1e52e-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-133">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1e52e-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e52e-134">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-135">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e52e-136">System-Only</span></span>            | <span data-ttu-id="1e52e-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-137">False</span></span>                                                |
| <span data-ttu-id="1e52e-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e52e-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1e52e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-139">False</span></span>                                                |
| <span data-ttu-id="1e52e-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e52e-140">Is Indexed</span></span>             | <span data-ttu-id="1e52e-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-141">False</span></span>                                                |
| <span data-ttu-id="1e52e-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e52e-142">In Global Catalog</span></span>      | <span data-ttu-id="1e52e-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-143">False</span></span>                                                |
| <span data-ttu-id="1e52e-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e52e-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e52e-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e52e-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1e52e-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e52e-146">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e52e-147">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-148">Search-Flags</span></span>           | <span data-ttu-id="1e52e-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e52e-149">0x00000000</span></span>                                           |
| <span data-ttu-id="1e52e-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-150">System-Flags</span></span>           | <span data-ttu-id="1e52e-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e52e-151">0x00000010</span></span>                                           |
| <span data-ttu-id="1e52e-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e52e-152">Classes used in</span></span>        | [<span data-ttu-id="1e52e-153">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1e52e-153">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1e52e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e52e-154">Windows Server 2003</span></span>



| <span data-ttu-id="1e52e-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-155">Entry</span></span> | <span data-ttu-id="1e52e-156">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-156">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1e52e-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e52e-157">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-158">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e52e-159">System-Only</span></span>            | <span data-ttu-id="1e52e-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-160">False</span></span>                                                |
| <span data-ttu-id="1e52e-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e52e-161">Is-Single-Valued</span></span>       | <span data-ttu-id="1e52e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-162">False</span></span>                                                |
| <span data-ttu-id="1e52e-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e52e-163">Is Indexed</span></span>             | <span data-ttu-id="1e52e-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-164">False</span></span>                                                |
| <span data-ttu-id="1e52e-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e52e-165">In Global Catalog</span></span>      | <span data-ttu-id="1e52e-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-166">False</span></span>                                                |
| <span data-ttu-id="1e52e-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e52e-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e52e-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e52e-168">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1e52e-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e52e-169">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e52e-170">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-171">Search-Flags</span></span>           | <span data-ttu-id="1e52e-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e52e-172">0x00000000</span></span>                                           |
| <span data-ttu-id="1e52e-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-173">System-Flags</span></span>           | <span data-ttu-id="1e52e-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e52e-174">0x00000010</span></span>                                           |
| <span data-ttu-id="1e52e-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e52e-175">Classes used in</span></span>        | [<span data-ttu-id="1e52e-176">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1e52e-176">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e52e-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e52e-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e52e-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-178">Entry</span></span> | <span data-ttu-id="1e52e-179">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-179">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1e52e-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e52e-180">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-181">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e52e-182">System-Only</span></span>            | <span data-ttu-id="1e52e-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-183">False</span></span>                                                |
| <span data-ttu-id="1e52e-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e52e-184">Is-Single-Valued</span></span>       | <span data-ttu-id="1e52e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-185">False</span></span>                                                |
| <span data-ttu-id="1e52e-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e52e-186">Is Indexed</span></span>             | <span data-ttu-id="1e52e-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-187">False</span></span>                                                |
| <span data-ttu-id="1e52e-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e52e-188">In Global Catalog</span></span>      | <span data-ttu-id="1e52e-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-189">False</span></span>                                                |
| <span data-ttu-id="1e52e-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e52e-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e52e-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e52e-191">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1e52e-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e52e-192">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e52e-193">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-194">Search-Flags</span></span>           | <span data-ttu-id="1e52e-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e52e-195">0x00000000</span></span>                                           |
| <span data-ttu-id="1e52e-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-196">System-Flags</span></span>           | <span data-ttu-id="1e52e-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e52e-197">0x00000010</span></span>                                           |
| <span data-ttu-id="1e52e-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e52e-198">Classes used in</span></span>        | [<span data-ttu-id="1e52e-199">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1e52e-199">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1e52e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e52e-200">Windows Server 2008</span></span>



| <span data-ttu-id="1e52e-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-201">Entry</span></span> | <span data-ttu-id="1e52e-202">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-202">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1e52e-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e52e-203">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-204">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e52e-205">System-Only</span></span>            | <span data-ttu-id="1e52e-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-206">False</span></span>                                                |
| <span data-ttu-id="1e52e-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e52e-207">Is-Single-Valued</span></span>       | <span data-ttu-id="1e52e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-208">False</span></span>                                                |
| <span data-ttu-id="1e52e-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e52e-209">Is Indexed</span></span>             | <span data-ttu-id="1e52e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-210">False</span></span>                                                |
| <span data-ttu-id="1e52e-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e52e-211">In Global Catalog</span></span>      | <span data-ttu-id="1e52e-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-212">False</span></span>                                                |
| <span data-ttu-id="1e52e-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e52e-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e52e-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e52e-214">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1e52e-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e52e-215">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e52e-216">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-217">Search-Flags</span></span>           | <span data-ttu-id="1e52e-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e52e-218">0x00000000</span></span>                                           |
| <span data-ttu-id="1e52e-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-219">System-Flags</span></span>           | <span data-ttu-id="1e52e-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e52e-220">0x00000010</span></span>                                           |
| <span data-ttu-id="1e52e-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e52e-221">Classes used in</span></span>        | [<span data-ttu-id="1e52e-222">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1e52e-222">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e52e-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e52e-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e52e-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-224">Entry</span></span> | <span data-ttu-id="1e52e-225">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-225">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1e52e-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e52e-226">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-227">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e52e-228">System-Only</span></span>            | <span data-ttu-id="1e52e-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-229">False</span></span>                                                |
| <span data-ttu-id="1e52e-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e52e-230">Is-Single-Valued</span></span>       | <span data-ttu-id="1e52e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-231">False</span></span>                                                |
| <span data-ttu-id="1e52e-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e52e-232">Is Indexed</span></span>             | <span data-ttu-id="1e52e-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-233">False</span></span>                                                |
| <span data-ttu-id="1e52e-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e52e-234">In Global Catalog</span></span>      | <span data-ttu-id="1e52e-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-235">False</span></span>                                                |
| <span data-ttu-id="1e52e-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e52e-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e52e-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e52e-237">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1e52e-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e52e-238">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e52e-239">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-240">Search-Flags</span></span>           | <span data-ttu-id="1e52e-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e52e-241">0x00000000</span></span>                                           |
| <span data-ttu-id="1e52e-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-242">System-Flags</span></span>           | <span data-ttu-id="1e52e-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e52e-243">0x00000010</span></span>                                           |
| <span data-ttu-id="1e52e-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e52e-244">Classes used in</span></span>        | [<span data-ttu-id="1e52e-245">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1e52e-245">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1e52e-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e52e-246">Windows Server 2012</span></span>



| <span data-ttu-id="1e52e-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e52e-247">Entry</span></span> | <span data-ttu-id="1e52e-248">Значение</span><span class="sxs-lookup"><span data-stu-id="1e52e-248">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="1e52e-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e52e-249">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e52e-250">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="1e52e-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e52e-251">System-Only</span></span>            | <span data-ttu-id="1e52e-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-252">False</span></span>                                                |
| <span data-ttu-id="1e52e-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e52e-253">Is-Single-Valued</span></span>       | <span data-ttu-id="1e52e-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-254">False</span></span>                                                |
| <span data-ttu-id="1e52e-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e52e-255">Is Indexed</span></span>             | <span data-ttu-id="1e52e-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-256">False</span></span>                                                |
| <span data-ttu-id="1e52e-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e52e-257">In Global Catalog</span></span>      | <span data-ttu-id="1e52e-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e52e-258">False</span></span>                                                |
| <span data-ttu-id="1e52e-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e52e-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e52e-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e52e-260">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="1e52e-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e52e-261">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e52e-262">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="1e52e-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-263">Search-Flags</span></span>           | <span data-ttu-id="1e52e-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e52e-264">0x00000000</span></span>                                           |
| <span data-ttu-id="1e52e-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e52e-265">System-Flags</span></span>           | <span data-ttu-id="1e52e-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e52e-266">0x00000010</span></span>                                           |
| <span data-ttu-id="1e52e-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e52e-267">Classes used in</span></span>        | [<span data-ttu-id="1e52e-268">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1e52e-268">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





