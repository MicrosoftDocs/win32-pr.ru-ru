---
title: Атрибут Token-Groups
description: Вычисленный атрибут, содержащий список идентификаторов безопасности из-за промежуточной операции расширения членства в группе для данного пользователя или компьютера. Невозможно получить группы токенов, если отсутствует глобальный каталог для получения транзитивных обратных членств.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Token-Groups
- Схема AD атрибута Токенграупс
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655041"
---
# <a name="token-groups-attribute"></a><span data-ttu-id="8a27e-106">Атрибут Token-Groups</span><span class="sxs-lookup"><span data-stu-id="8a27e-106">Token-Groups attribute</span></span>

<span data-ttu-id="8a27e-107">Вычисленный атрибут, содержащий список идентификаторов безопасности из-за промежуточной операции расширения членства в группе для данного пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="8a27e-107">A computed attribute that contains the list of SIDs due to a transitive group membership expansion operation on a given user or computer.</span></span> <span data-ttu-id="8a27e-108">Невозможно получить группы токенов, если отсутствует глобальный каталог для получения транзитивных обратных членств.</span><span class="sxs-lookup"><span data-stu-id="8a27e-108">Token Groups cannot be retrieved if no Global Catalog is present to retrieve the transitive reverse memberships.</span></span>



| <span data-ttu-id="8a27e-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-109">Entry</span></span> | <span data-ttu-id="8a27e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8a27e-111">CN</span><span class="sxs-lookup"><span data-stu-id="8a27e-111">CN</span></span>                | <span data-ttu-id="8a27e-112">Token-Groups</span><span class="sxs-lookup"><span data-stu-id="8a27e-112">Token-Groups</span></span>                         |
| <span data-ttu-id="8a27e-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8a27e-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8a27e-114">tokenGroups</span><span class="sxs-lookup"><span data-stu-id="8a27e-114">tokenGroups</span></span>                          |
| <span data-ttu-id="8a27e-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8a27e-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="8a27e-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8a27e-116">Update Privilege</span></span>  | <span data-ttu-id="8a27e-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="8a27e-117">This value is set by the system.</span></span>     |
| <span data-ttu-id="8a27e-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8a27e-118">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8a27e-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-119">Attribute-Id</span></span>      | <span data-ttu-id="8a27e-120">1.2.840.113556.1.4.1301</span><span class="sxs-lookup"><span data-stu-id="8a27e-120">1.2.840.113556.1.4.1301</span></span>              |
| <span data-ttu-id="8a27e-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8a27e-121">System-Id-Guid</span></span>    | <span data-ttu-id="8a27e-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span><span class="sxs-lookup"><span data-stu-id="8a27e-122">b7c69e6d-2cc7-11d2-854e-00a0c983f608</span></span> |
| <span data-ttu-id="8a27e-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a27e-123">Syntax</span></span>            | [<span data-ttu-id="8a27e-124">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="8a27e-124">**String(Sid)**</span></span>](s-string-sid.md)  |



## <a name="implementations"></a><span data-ttu-id="8a27e-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8a27e-125">Implementations</span></span>

-   [<span data-ttu-id="8a27e-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8a27e-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8a27e-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8a27e-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8a27e-128">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8a27e-128">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="8a27e-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8a27e-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8a27e-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8a27e-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8a27e-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8a27e-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8a27e-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8a27e-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8a27e-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a27e-133">Windows 2000 Server</span></span>



| <span data-ttu-id="8a27e-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-134">Entry</span></span> | <span data-ttu-id="8a27e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-135">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-136">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-137">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-138">System-Only</span></span>            | <span data-ttu-id="8a27e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-139">False</span></span>                                                        |
| <span data-ttu-id="8a27e-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-140">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-141">False</span></span>                                                        |
| <span data-ttu-id="8a27e-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-142">Is Indexed</span></span>             | <span data-ttu-id="8a27e-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-143">False</span></span>                                                        |
| <span data-ttu-id="8a27e-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-144">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-145">False</span></span>                                                        |
| <span data-ttu-id="8a27e-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-147">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-148">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-149">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-150">Search-Flags</span></span>           | <span data-ttu-id="8a27e-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-151">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-152">System-Flags</span></span>           | <span data-ttu-id="8a27e-153">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-153">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-154">Classes used in</span></span>        | [<span data-ttu-id="8a27e-155">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-155">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8a27e-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a27e-156">Windows Server 2003</span></span>



| <span data-ttu-id="8a27e-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-157">Entry</span></span> | <span data-ttu-id="8a27e-158">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-158">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-159">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-160">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-161">System-Only</span></span>            | <span data-ttu-id="8a27e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-162">False</span></span>                                                        |
| <span data-ttu-id="8a27e-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-163">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-164">False</span></span>                                                        |
| <span data-ttu-id="8a27e-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-165">Is Indexed</span></span>             | <span data-ttu-id="8a27e-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-166">False</span></span>                                                        |
| <span data-ttu-id="8a27e-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-167">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-168">False</span></span>                                                        |
| <span data-ttu-id="8a27e-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-170">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-171">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-172">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-173">Search-Flags</span></span>           | <span data-ttu-id="8a27e-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-174">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-175">System-Flags</span></span>           | <span data-ttu-id="8a27e-176">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-176">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-177">Classes used in</span></span>        | [<span data-ttu-id="8a27e-178">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-178">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="8a27e-179">ADAM</span><span class="sxs-lookup"><span data-stu-id="8a27e-179">ADAM</span></span>



| <span data-ttu-id="8a27e-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-180">Entry</span></span> | <span data-ttu-id="8a27e-181">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-181">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-182">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-183">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-184">System-Only</span></span>            | <span data-ttu-id="8a27e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-185">False</span></span>                                                        |
| <span data-ttu-id="8a27e-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-186">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-187">False</span></span>                                                        |
| <span data-ttu-id="8a27e-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-188">Is Indexed</span></span>             | <span data-ttu-id="8a27e-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-189">False</span></span>                                                        |
| <span data-ttu-id="8a27e-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-190">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-191">False</span></span>                                                        |
| <span data-ttu-id="8a27e-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-193">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-194">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-195">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-196">Search-Flags</span></span>           | <span data-ttu-id="8a27e-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-197">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-198">System-Flags</span></span>           | <span data-ttu-id="8a27e-199">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-199">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-200">Classes used in</span></span>        | [<span data-ttu-id="8a27e-201">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-201">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8a27e-202">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8a27e-202">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8a27e-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-203">Entry</span></span> | <span data-ttu-id="8a27e-204">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-204">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-205">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-206">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-207">System-Only</span></span>            | <span data-ttu-id="8a27e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-208">False</span></span>                                                        |
| <span data-ttu-id="8a27e-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-209">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-210">False</span></span>                                                        |
| <span data-ttu-id="8a27e-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-211">Is Indexed</span></span>             | <span data-ttu-id="8a27e-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-212">False</span></span>                                                        |
| <span data-ttu-id="8a27e-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-213">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-214">False</span></span>                                                        |
| <span data-ttu-id="8a27e-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-216">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-217">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-218">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-219">Search-Flags</span></span>           | <span data-ttu-id="8a27e-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-220">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-221">System-Flags</span></span>           | <span data-ttu-id="8a27e-222">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-222">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-223">Classes used in</span></span>        | [<span data-ttu-id="8a27e-224">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-224">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8a27e-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a27e-225">Windows Server 2008</span></span>



| <span data-ttu-id="8a27e-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-226">Entry</span></span> | <span data-ttu-id="8a27e-227">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-227">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-228">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-229">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-230">System-Only</span></span>            | <span data-ttu-id="8a27e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-231">False</span></span>                                                        |
| <span data-ttu-id="8a27e-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-232">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-233">False</span></span>                                                        |
| <span data-ttu-id="8a27e-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-234">Is Indexed</span></span>             | <span data-ttu-id="8a27e-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-235">False</span></span>                                                        |
| <span data-ttu-id="8a27e-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-236">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-237">False</span></span>                                                        |
| <span data-ttu-id="8a27e-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-239">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-240">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-241">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-242">Search-Flags</span></span>           | <span data-ttu-id="8a27e-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-243">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-244">System-Flags</span></span>           | <span data-ttu-id="8a27e-245">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-245">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-246">Classes used in</span></span>        | [<span data-ttu-id="8a27e-247">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-247">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8a27e-248">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a27e-248">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8a27e-249">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-249">Entry</span></span> | <span data-ttu-id="8a27e-250">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-250">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-251">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-251">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-252">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-252">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-253">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-253">System-Only</span></span>            | <span data-ttu-id="8a27e-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-254">False</span></span>                                                        |
| <span data-ttu-id="8a27e-255">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-255">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-256">False</span></span>                                                        |
| <span data-ttu-id="8a27e-257">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-257">Is Indexed</span></span>             | <span data-ttu-id="8a27e-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-258">False</span></span>                                                        |
| <span data-ttu-id="8a27e-259">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-259">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-260">False</span></span>                                                        |
| <span data-ttu-id="8a27e-261">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-261">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-262">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-262">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-263">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-263">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-264">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-264">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-265">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-265">Search-Flags</span></span>           | <span data-ttu-id="8a27e-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-266">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-267">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-267">System-Flags</span></span>           | <span data-ttu-id="8a27e-268">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-268">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-269">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-269">Classes used in</span></span>        | [<span data-ttu-id="8a27e-270">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-270">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8a27e-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8a27e-271">Windows Server 2012</span></span>



| <span data-ttu-id="8a27e-272">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a27e-272">Entry</span></span> | <span data-ttu-id="8a27e-273">Значение</span><span class="sxs-lookup"><span data-stu-id="8a27e-273">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8a27e-274">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a27e-274">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-275">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a27e-275">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="8a27e-276">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a27e-276">System-Only</span></span>            | <span data-ttu-id="8a27e-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-277">False</span></span>                                                        |
| <span data-ttu-id="8a27e-278">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a27e-278">Is-Single-Valued</span></span>       | <span data-ttu-id="8a27e-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-279">False</span></span>                                                        |
| <span data-ttu-id="8a27e-280">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a27e-280">Is Indexed</span></span>             | <span data-ttu-id="8a27e-281">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-281">False</span></span>                                                        |
| <span data-ttu-id="8a27e-282">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a27e-282">In Global Catalog</span></span>      | <span data-ttu-id="8a27e-283">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a27e-283">False</span></span>                                                        |
| <span data-ttu-id="8a27e-284">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a27e-284">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a27e-285">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a27e-285">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="8a27e-286">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a27e-286">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a27e-287">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="8a27e-288">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-288">Search-Flags</span></span>           | <span data-ttu-id="8a27e-289">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a27e-289">0x00000000</span></span>                                                   |
| <span data-ttu-id="8a27e-290">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a27e-290">System-Flags</span></span>           | <span data-ttu-id="8a27e-291">0x08000014</span><span class="sxs-lookup"><span data-stu-id="8a27e-291">0x08000014</span></span>                                                   |
| <span data-ttu-id="8a27e-292">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a27e-292">Classes used in</span></span>        | [<span data-ttu-id="8a27e-293">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="8a27e-293">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





