---
title: Атрибут квоты MS-DS-на пользователя — доверие — захоронение
description: Используется для принудительного применения квоты на пользователя для удаления объектов Trusted-Domain, когда Авторизация основана на идентификаторе безопасности пользователя.
ms.assetid: 4db98754-a2d1-43a4-b9cb-0e3fcbbf3ed9
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута квоты MS-DS-на пользователя-захоронение
- Схема AD атрибута msDS-Перусертрусттомбстонескуота
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Tombstones-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c94bb62b822552a863df99dac83e98462514c42
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655175"
---
# <a name="ms-ds-per-user-trust-tombstones-quota-attribute"></a><span data-ttu-id="59441-105">Атрибут квоты MS-DS-на пользователя — доверие — захоронение</span><span class="sxs-lookup"><span data-stu-id="59441-105">MS-DS-Per-User-Trust-Tombstones-Quota attribute</span></span>

<span data-ttu-id="59441-106">Используется для принудительного применения квоты на пользователя для удаления объектов Trusted-Domain, когда Авторизация основана на идентификаторе безопасности пользователя.</span><span class="sxs-lookup"><span data-stu-id="59441-106">Used to enforce a per-user quota for deleting Trusted-Domain objects when authorization is based on matching the user's SID.</span></span>



| <span data-ttu-id="59441-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="59441-107">Entry</span></span> | <span data-ttu-id="59441-108">Значение</span><span class="sxs-lookup"><span data-stu-id="59441-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="59441-109">CN</span><span class="sxs-lookup"><span data-stu-id="59441-109">CN</span></span>                | <span data-ttu-id="59441-110">MS-DS-на пользователя-захоронение — квота</span><span class="sxs-lookup"><span data-stu-id="59441-110">MS-DS-Per-User-Trust-Tombstones-Quota</span></span>     |
| <span data-ttu-id="59441-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="59441-111">Ldap-Display-Name</span></span> | <span data-ttu-id="59441-112">msDS-Перусертрусттомбстонескуота</span><span class="sxs-lookup"><span data-stu-id="59441-112">msDS-PerUserTrustTombstonesQuota</span></span>          |
| <span data-ttu-id="59441-113">Размер</span><span class="sxs-lookup"><span data-stu-id="59441-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="59441-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="59441-114">Update Privilege</span></span>  | <span data-ttu-id="59441-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="59441-115">Domain administrator</span></span>                      |
| <span data-ttu-id="59441-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="59441-116">Update Frequency</span></span>  | <span data-ttu-id="59441-117">При создании леса и редко после него.</span><span class="sxs-lookup"><span data-stu-id="59441-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="59441-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="59441-118">Attribute-Id</span></span>      | <span data-ttu-id="59441-119">1.2.840.113556.1.4.1790</span><span class="sxs-lookup"><span data-stu-id="59441-119">1.2.840.113556.1.4.1790</span></span>                   |
| <span data-ttu-id="59441-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="59441-120">System-Id-Guid</span></span>    | <span data-ttu-id="59441-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span><span class="sxs-lookup"><span data-stu-id="59441-121">8b70a6c6-50f9-4fa3-a71e-1ce03040449b</span></span>      |
| <span data-ttu-id="59441-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59441-122">Syntax</span></span>            | [<span data-ttu-id="59441-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="59441-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="59441-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="59441-124">Implementations</span></span>

-   [<span data-ttu-id="59441-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="59441-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="59441-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="59441-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="59441-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="59441-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="59441-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="59441-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="59441-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="59441-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="59441-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="59441-130">Windows Server 2003</span></span>



| <span data-ttu-id="59441-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="59441-131">Entry</span></span> | <span data-ttu-id="59441-132">Значение</span><span class="sxs-lookup"><span data-stu-id="59441-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="59441-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59441-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59441-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="59441-135">System-Only</span></span>            | <span data-ttu-id="59441-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-136">False</span></span>                                        |
| <span data-ttu-id="59441-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59441-137">Is-Single-Valued</span></span>       | <span data-ttu-id="59441-138">True</span><span class="sxs-lookup"><span data-stu-id="59441-138">True</span></span>                                         |
| <span data-ttu-id="59441-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59441-139">Is Indexed</span></span>             | <span data-ttu-id="59441-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-140">False</span></span>                                        |
| <span data-ttu-id="59441-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59441-141">In Global Catalog</span></span>      | <span data-ttu-id="59441-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-142">False</span></span>                                        |
| <span data-ttu-id="59441-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59441-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="59441-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59441-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="59441-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59441-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="59441-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59441-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="59441-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-147">Search-Flags</span></span>           | <span data-ttu-id="59441-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59441-148">0x00000000</span></span>                                   |
| <span data-ttu-id="59441-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-149">System-Flags</span></span>           | <span data-ttu-id="59441-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59441-150">0x00000010</span></span>                                   |
| <span data-ttu-id="59441-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59441-151">Classes used in</span></span>        | [<span data-ttu-id="59441-152">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="59441-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="59441-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="59441-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="59441-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="59441-154">Entry</span></span> | <span data-ttu-id="59441-155">Значение</span><span class="sxs-lookup"><span data-stu-id="59441-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="59441-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59441-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59441-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="59441-158">System-Only</span></span>            | <span data-ttu-id="59441-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-159">False</span></span>                                        |
| <span data-ttu-id="59441-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59441-160">Is-Single-Valued</span></span>       | <span data-ttu-id="59441-161">True</span><span class="sxs-lookup"><span data-stu-id="59441-161">True</span></span>                                         |
| <span data-ttu-id="59441-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59441-162">Is Indexed</span></span>             | <span data-ttu-id="59441-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-163">False</span></span>                                        |
| <span data-ttu-id="59441-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59441-164">In Global Catalog</span></span>      | <span data-ttu-id="59441-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-165">False</span></span>                                        |
| <span data-ttu-id="59441-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59441-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="59441-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59441-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="59441-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59441-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="59441-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59441-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="59441-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-170">Search-Flags</span></span>           | <span data-ttu-id="59441-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59441-171">0x00000000</span></span>                                   |
| <span data-ttu-id="59441-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-172">System-Flags</span></span>           | <span data-ttu-id="59441-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59441-173">0x00000010</span></span>                                   |
| <span data-ttu-id="59441-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59441-174">Classes used in</span></span>        | [<span data-ttu-id="59441-175">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="59441-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="59441-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59441-176">Windows Server 2008</span></span>



| <span data-ttu-id="59441-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="59441-177">Entry</span></span> | <span data-ttu-id="59441-178">Значение</span><span class="sxs-lookup"><span data-stu-id="59441-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="59441-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59441-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59441-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="59441-181">System-Only</span></span>            | <span data-ttu-id="59441-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-182">False</span></span>                                        |
| <span data-ttu-id="59441-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59441-183">Is-Single-Valued</span></span>       | <span data-ttu-id="59441-184">True</span><span class="sxs-lookup"><span data-stu-id="59441-184">True</span></span>                                         |
| <span data-ttu-id="59441-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59441-185">Is Indexed</span></span>             | <span data-ttu-id="59441-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-186">False</span></span>                                        |
| <span data-ttu-id="59441-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59441-187">In Global Catalog</span></span>      | <span data-ttu-id="59441-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-188">False</span></span>                                        |
| <span data-ttu-id="59441-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59441-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="59441-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59441-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="59441-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59441-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="59441-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59441-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="59441-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-193">Search-Flags</span></span>           | <span data-ttu-id="59441-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59441-194">0x00000000</span></span>                                   |
| <span data-ttu-id="59441-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-195">System-Flags</span></span>           | <span data-ttu-id="59441-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59441-196">0x00000010</span></span>                                   |
| <span data-ttu-id="59441-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59441-197">Classes used in</span></span>        | [<span data-ttu-id="59441-198">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="59441-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="59441-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="59441-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="59441-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="59441-200">Entry</span></span> | <span data-ttu-id="59441-201">Значение</span><span class="sxs-lookup"><span data-stu-id="59441-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="59441-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59441-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59441-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="59441-204">System-Only</span></span>            | <span data-ttu-id="59441-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-205">False</span></span>                                        |
| <span data-ttu-id="59441-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59441-206">Is-Single-Valued</span></span>       | <span data-ttu-id="59441-207">True</span><span class="sxs-lookup"><span data-stu-id="59441-207">True</span></span>                                         |
| <span data-ttu-id="59441-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59441-208">Is Indexed</span></span>             | <span data-ttu-id="59441-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-209">False</span></span>                                        |
| <span data-ttu-id="59441-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59441-210">In Global Catalog</span></span>      | <span data-ttu-id="59441-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-211">False</span></span>                                        |
| <span data-ttu-id="59441-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59441-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="59441-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59441-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="59441-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59441-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="59441-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59441-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="59441-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-216">Search-Flags</span></span>           | <span data-ttu-id="59441-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59441-217">0x00000000</span></span>                                   |
| <span data-ttu-id="59441-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-218">System-Flags</span></span>           | <span data-ttu-id="59441-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59441-219">0x00000010</span></span>                                   |
| <span data-ttu-id="59441-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59441-220">Classes used in</span></span>        | [<span data-ttu-id="59441-221">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="59441-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="59441-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59441-222">Windows Server 2012</span></span>



| <span data-ttu-id="59441-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="59441-223">Entry</span></span> | <span data-ttu-id="59441-224">Значение</span><span class="sxs-lookup"><span data-stu-id="59441-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="59441-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="59441-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="59441-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="59441-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="59441-227">System-Only</span></span>            | <span data-ttu-id="59441-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-228">False</span></span>                                        |
| <span data-ttu-id="59441-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="59441-229">Is-Single-Valued</span></span>       | <span data-ttu-id="59441-230">True</span><span class="sxs-lookup"><span data-stu-id="59441-230">True</span></span>                                         |
| <span data-ttu-id="59441-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="59441-231">Is Indexed</span></span>             | <span data-ttu-id="59441-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-232">False</span></span>                                        |
| <span data-ttu-id="59441-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="59441-233">In Global Catalog</span></span>      | <span data-ttu-id="59441-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="59441-234">False</span></span>                                        |
| <span data-ttu-id="59441-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="59441-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="59441-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="59441-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="59441-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="59441-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="59441-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="59441-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="59441-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-239">Search-Flags</span></span>           | <span data-ttu-id="59441-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="59441-240">0x00000000</span></span>                                   |
| <span data-ttu-id="59441-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="59441-241">System-Flags</span></span>           | <span data-ttu-id="59441-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="59441-242">0x00000010</span></span>                                   |
| <span data-ttu-id="59441-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="59441-243">Classes used in</span></span>        | [<span data-ttu-id="59441-244">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="59441-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





