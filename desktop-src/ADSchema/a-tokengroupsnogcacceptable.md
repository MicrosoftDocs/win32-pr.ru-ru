---
title: Токен-Groups-No-GC-приемлемый атрибут
description: Этот атрибут содержит список идентификаторов безопасности из-за операции расширения членства в группе для данного пользователя или компьютера. Невозможно получить группы токенов, если отсутствует глобальный каталог для получения транзитивных обратных членств.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Токенные группы-No-GC-приемлемая схема AD атрибутов
- Схема AD атрибута Токенграупсногкакцептабле
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a87c4b8996586c8c35ed4c815b954dad02b5db03
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893254"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a><span data-ttu-id="b640b-106">Токен-Groups-No-GC-приемлемый атрибут</span><span class="sxs-lookup"><span data-stu-id="b640b-106">Token-Groups-No-GC-Acceptable attribute</span></span>

<span data-ttu-id="b640b-107">Этот атрибут содержит список идентификаторов безопасности из-за операции расширения членства в группе для данного пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="b640b-107">This attribute contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="b640b-108">Невозможно получить группы токенов, если отсутствует глобальный каталог для получения транзитивных обратных членств.</span><span class="sxs-lookup"><span data-stu-id="b640b-108">Token groups cannot be retrieved if a Global Catalog is not present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="b640b-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-109">Entry</span></span> | <span data-ttu-id="b640b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="b640b-111">CN</span><span class="sxs-lookup"><span data-stu-id="b640b-111">CN</span></span>                | <span data-ttu-id="b640b-112">Токены-группы-No-GC-приемлемые</span><span class="sxs-lookup"><span data-stu-id="b640b-112">Token-Groups-No-GC-Acceptable</span></span>        |
| <span data-ttu-id="b640b-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b640b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="b640b-114">токенграупсногкакцептабле</span><span class="sxs-lookup"><span data-stu-id="b640b-114">tokenGroupsNoGCAcceptable</span></span>            |
| <span data-ttu-id="b640b-115">Размер</span><span class="sxs-lookup"><span data-stu-id="b640b-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="b640b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b640b-116">Update Privilege</span></span>  | <span data-ttu-id="b640b-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b640b-117">The system sets this value.</span></span>          |
| <span data-ttu-id="b640b-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b640b-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="b640b-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-119">Attribute-Id</span></span>      | <span data-ttu-id="b640b-120">1.2.840.113556.1.4.1303</span><span class="sxs-lookup"><span data-stu-id="b640b-120">1.2.840.113556.1.4.1303</span></span>              |
| <span data-ttu-id="b640b-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b640b-121">System-Id-Guid</span></span>    | <span data-ttu-id="b640b-122">040fc392-33df-11d2-98b2-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="b640b-122">040fc392-33df-11d2-98b2-0000f87a57d4</span></span> |
| <span data-ttu-id="b640b-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b640b-123">Syntax</span></span>            | [<span data-ttu-id="b640b-124">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="b640b-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="b640b-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b640b-125">Implementations</span></span>

-   [<span data-ttu-id="b640b-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b640b-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b640b-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b640b-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b640b-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b640b-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b640b-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b640b-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b640b-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b640b-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b640b-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b640b-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b640b-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b640b-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b640b-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-133">Entry</span></span> | <span data-ttu-id="b640b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-134">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b640b-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b640b-135">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-136">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="b640b-137">System-Only</span></span>            | <span data-ttu-id="b640b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-138">False</span></span>                                                        |
| <span data-ttu-id="b640b-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b640b-139">Is-Single-Valued</span></span>       | <span data-ttu-id="b640b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-140">False</span></span>                                                        |
| <span data-ttu-id="b640b-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b640b-141">Is Indexed</span></span>             | <span data-ttu-id="b640b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-142">False</span></span>                                                        |
| <span data-ttu-id="b640b-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b640b-143">In Global Catalog</span></span>      | <span data-ttu-id="b640b-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-144">False</span></span>                                                        |
| <span data-ttu-id="b640b-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b640b-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="b640b-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b640b-146">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b640b-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b640b-147">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b640b-148">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-149">Search-Flags</span></span>           | <span data-ttu-id="b640b-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b640b-150">0x00000000</span></span>                                                   |
| <span data-ttu-id="b640b-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-151">System-Flags</span></span>           | <span data-ttu-id="b640b-152">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b640b-152">0x08000014</span></span>                                                   |
| <span data-ttu-id="b640b-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b640b-153">Classes used in</span></span>        | [<span data-ttu-id="b640b-154">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="b640b-154">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b640b-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b640b-155">Windows Server 2003</span></span>



| <span data-ttu-id="b640b-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-156">Entry</span></span> | <span data-ttu-id="b640b-157">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-157">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b640b-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b640b-158">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-159">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b640b-160">System-Only</span></span>            | <span data-ttu-id="b640b-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-161">False</span></span>                                                        |
| <span data-ttu-id="b640b-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b640b-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b640b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-163">False</span></span>                                                        |
| <span data-ttu-id="b640b-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b640b-164">Is Indexed</span></span>             | <span data-ttu-id="b640b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-165">False</span></span>                                                        |
| <span data-ttu-id="b640b-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b640b-166">In Global Catalog</span></span>      | <span data-ttu-id="b640b-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-167">False</span></span>                                                        |
| <span data-ttu-id="b640b-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b640b-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b640b-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b640b-169">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b640b-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b640b-170">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b640b-171">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-172">Search-Flags</span></span>           | <span data-ttu-id="b640b-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b640b-173">0x00000000</span></span>                                                   |
| <span data-ttu-id="b640b-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-174">System-Flags</span></span>           | <span data-ttu-id="b640b-175">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b640b-175">0x08000014</span></span>                                                   |
| <span data-ttu-id="b640b-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b640b-176">Classes used in</span></span>        | [<span data-ttu-id="b640b-177">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="b640b-177">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b640b-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b640b-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b640b-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-179">Entry</span></span> | <span data-ttu-id="b640b-180">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-180">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b640b-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b640b-181">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-182">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="b640b-183">System-Only</span></span>            | <span data-ttu-id="b640b-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-184">False</span></span>                                                        |
| <span data-ttu-id="b640b-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b640b-185">Is-Single-Valued</span></span>       | <span data-ttu-id="b640b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-186">False</span></span>                                                        |
| <span data-ttu-id="b640b-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b640b-187">Is Indexed</span></span>             | <span data-ttu-id="b640b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-188">False</span></span>                                                        |
| <span data-ttu-id="b640b-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b640b-189">In Global Catalog</span></span>      | <span data-ttu-id="b640b-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-190">False</span></span>                                                        |
| <span data-ttu-id="b640b-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b640b-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="b640b-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b640b-192">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b640b-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b640b-193">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b640b-194">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-195">Search-Flags</span></span>           | <span data-ttu-id="b640b-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b640b-196">0x00000000</span></span>                                                   |
| <span data-ttu-id="b640b-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-197">System-Flags</span></span>           | <span data-ttu-id="b640b-198">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b640b-198">0x08000014</span></span>                                                   |
| <span data-ttu-id="b640b-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b640b-199">Classes used in</span></span>        | [<span data-ttu-id="b640b-200">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="b640b-200">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b640b-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b640b-201">Windows Server 2008</span></span>



| <span data-ttu-id="b640b-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-202">Entry</span></span> | <span data-ttu-id="b640b-203">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-203">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b640b-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b640b-204">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-205">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="b640b-206">System-Only</span></span>            | <span data-ttu-id="b640b-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-207">False</span></span>                                                        |
| <span data-ttu-id="b640b-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b640b-208">Is-Single-Valued</span></span>       | <span data-ttu-id="b640b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-209">False</span></span>                                                        |
| <span data-ttu-id="b640b-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b640b-210">Is Indexed</span></span>             | <span data-ttu-id="b640b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-211">False</span></span>                                                        |
| <span data-ttu-id="b640b-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b640b-212">In Global Catalog</span></span>      | <span data-ttu-id="b640b-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-213">False</span></span>                                                        |
| <span data-ttu-id="b640b-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b640b-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="b640b-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b640b-215">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b640b-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b640b-216">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b640b-217">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-218">Search-Flags</span></span>           | <span data-ttu-id="b640b-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b640b-219">0x00000000</span></span>                                                   |
| <span data-ttu-id="b640b-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-220">System-Flags</span></span>           | <span data-ttu-id="b640b-221">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b640b-221">0x08000014</span></span>                                                   |
| <span data-ttu-id="b640b-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b640b-222">Classes used in</span></span>        | [<span data-ttu-id="b640b-223">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="b640b-223">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b640b-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b640b-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b640b-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-225">Entry</span></span> | <span data-ttu-id="b640b-226">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-226">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b640b-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b640b-227">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-228">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="b640b-229">System-Only</span></span>            | <span data-ttu-id="b640b-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-230">False</span></span>                                                        |
| <span data-ttu-id="b640b-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b640b-231">Is-Single-Valued</span></span>       | <span data-ttu-id="b640b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-232">False</span></span>                                                        |
| <span data-ttu-id="b640b-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b640b-233">Is Indexed</span></span>             | <span data-ttu-id="b640b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-234">False</span></span>                                                        |
| <span data-ttu-id="b640b-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b640b-235">In Global Catalog</span></span>      | <span data-ttu-id="b640b-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-236">False</span></span>                                                        |
| <span data-ttu-id="b640b-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b640b-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="b640b-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b640b-238">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b640b-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b640b-239">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b640b-240">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-241">Search-Flags</span></span>           | <span data-ttu-id="b640b-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b640b-242">0x00000000</span></span>                                                   |
| <span data-ttu-id="b640b-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-243">System-Flags</span></span>           | <span data-ttu-id="b640b-244">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b640b-244">0x08000014</span></span>                                                   |
| <span data-ttu-id="b640b-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b640b-245">Classes used in</span></span>        | [<span data-ttu-id="b640b-246">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="b640b-246">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b640b-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b640b-247">Windows Server 2012</span></span>



| <span data-ttu-id="b640b-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="b640b-248">Entry</span></span> | <span data-ttu-id="b640b-249">Значение</span><span class="sxs-lookup"><span data-stu-id="b640b-249">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="b640b-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b640b-250">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b640b-251">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="b640b-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="b640b-252">System-Only</span></span>            | <span data-ttu-id="b640b-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-253">False</span></span>                                                        |
| <span data-ttu-id="b640b-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b640b-254">Is-Single-Valued</span></span>       | <span data-ttu-id="b640b-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-255">False</span></span>                                                        |
| <span data-ttu-id="b640b-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b640b-256">Is Indexed</span></span>             | <span data-ttu-id="b640b-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-257">False</span></span>                                                        |
| <span data-ttu-id="b640b-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b640b-258">In Global Catalog</span></span>      | <span data-ttu-id="b640b-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="b640b-259">False</span></span>                                                        |
| <span data-ttu-id="b640b-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b640b-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="b640b-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b640b-261">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="b640b-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b640b-262">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b640b-263">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="b640b-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-264">Search-Flags</span></span>           | <span data-ttu-id="b640b-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b640b-265">0x00000000</span></span>                                                   |
| <span data-ttu-id="b640b-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b640b-266">System-Flags</span></span>           | <span data-ttu-id="b640b-267">0x08000014</span><span class="sxs-lookup"><span data-stu-id="b640b-267">0x08000014</span></span>                                                   |
| <span data-ttu-id="b640b-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b640b-268">Classes used in</span></span>        | [<span data-ttu-id="b640b-269">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="b640b-269">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





