---
title: атрибут членства MS-DS-Cache-Membership
description: Атрибут "MS-DS-Cache-Membership" используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.
ms.assetid: e54c5d55-d292-4a6e-942a-3818f5d75301
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута членства MS-DS-Cache-Membership
- msDS — схема AD атрибута членства в кэше
topic_type:
- apiref
api_name:
- ms-DS-Cached-Membership
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936c5c21d33d19ee51dba7f1dec0b03299cee346
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536281"
---
# <a name="ms-ds-cached-membership-attribute"></a><span data-ttu-id="07f1b-105">атрибут членства MS-DS-Cache-Membership</span><span class="sxs-lookup"><span data-stu-id="07f1b-105">ms-DS-Cached-Membership attribute</span></span>

<span data-ttu-id="07f1b-106">Атрибут " **MS-DS-Cache-Membership** " используется диспетчером учетных записей безопасности для расширения группы во время оценки маркера.</span><span class="sxs-lookup"><span data-stu-id="07f1b-106">The **ms-DS-Cached-Membership** attribute is used by the Security Accounts Manager for group expansion during token evaluation.</span></span>



| <span data-ttu-id="07f1b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="07f1b-107">Entry</span></span> | <span data-ttu-id="07f1b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="07f1b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="07f1b-109">CN</span><span class="sxs-lookup"><span data-stu-id="07f1b-109">CN</span></span>                | <span data-ttu-id="07f1b-110">MS-DS-Cache-Membership</span><span class="sxs-lookup"><span data-stu-id="07f1b-110">ms-DS-Cached-Membership</span></span>                               |
| <span data-ttu-id="07f1b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="07f1b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="07f1b-112">msDS — кэширование членства</span><span class="sxs-lookup"><span data-stu-id="07f1b-112">msDS-Cached-Membership</span></span>                                |
| <span data-ttu-id="07f1b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="07f1b-113">Size</span></span>              | <span data-ttu-id="07f1b-114">Двоичный BLOB-объект размером до 3 килобайт.</span><span class="sxs-lookup"><span data-stu-id="07f1b-114">Binary BLOB of up to 3 kilobytes.</span></span>                     |
| <span data-ttu-id="07f1b-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="07f1b-115">Update Privilege</span></span>  | <span data-ttu-id="07f1b-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="07f1b-116">This value is set by the system.</span></span>                      |
| <span data-ttu-id="07f1b-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="07f1b-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="07f1b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="07f1b-118">Attribute-Id</span></span>      | <span data-ttu-id="07f1b-119">1.2.840.113556.1.4.1441</span><span class="sxs-lookup"><span data-stu-id="07f1b-119">1.2.840.113556.1.4.1441</span></span>                               |
| <span data-ttu-id="07f1b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="07f1b-120">System-Id-Guid</span></span>    | <span data-ttu-id="07f1b-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span><span class="sxs-lookup"><span data-stu-id="07f1b-121">69cab008-cdd4-4bc9-bab8-0ff37efe1b20</span></span>                  |
| <span data-ttu-id="07f1b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07f1b-122">Syntax</span></span>            | [<span data-ttu-id="07f1b-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="07f1b-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="07f1b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="07f1b-124">Implementations</span></span>

-   [<span data-ttu-id="07f1b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="07f1b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="07f1b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="07f1b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="07f1b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="07f1b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="07f1b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="07f1b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="07f1b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="07f1b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="07f1b-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="07f1b-130">Windows Server 2003</span></span>



| <span data-ttu-id="07f1b-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="07f1b-131">Entry</span></span> | <span data-ttu-id="07f1b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="07f1b-132">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="07f1b-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="07f1b-133">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07f1b-134">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="07f1b-135">System-Only</span></span>            | <span data-ttu-id="07f1b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-136">False</span></span>                             |
| <span data-ttu-id="07f1b-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="07f1b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="07f1b-138">True</span><span class="sxs-lookup"><span data-stu-id="07f1b-138">True</span></span>                              |
| <span data-ttu-id="07f1b-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="07f1b-139">Is Indexed</span></span>             | <span data-ttu-id="07f1b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-140">False</span></span>                             |
| <span data-ttu-id="07f1b-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="07f1b-141">In Global Catalog</span></span>      | <span data-ttu-id="07f1b-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-142">False</span></span>                             |
| <span data-ttu-id="07f1b-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="07f1b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="07f1b-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="07f1b-144">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="07f1b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07f1b-145">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="07f1b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07f1b-146">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="07f1b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-147">Search-Flags</span></span>           | <span data-ttu-id="07f1b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07f1b-148">0x00000000</span></span>                        |
| <span data-ttu-id="07f1b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-149">System-Flags</span></span>           | <span data-ttu-id="07f1b-150">0x00000011</span><span class="sxs-lookup"><span data-stu-id="07f1b-150">0x00000011</span></span>                        |
| <span data-ttu-id="07f1b-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="07f1b-151">Classes used in</span></span>        | [<span data-ttu-id="07f1b-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="07f1b-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="07f1b-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="07f1b-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="07f1b-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="07f1b-154">Entry</span></span> | <span data-ttu-id="07f1b-155">Значение</span><span class="sxs-lookup"><span data-stu-id="07f1b-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="07f1b-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="07f1b-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07f1b-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="07f1b-158">System-Only</span></span>            | <span data-ttu-id="07f1b-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-159">False</span></span>                             |
| <span data-ttu-id="07f1b-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="07f1b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="07f1b-161">True</span><span class="sxs-lookup"><span data-stu-id="07f1b-161">True</span></span>                              |
| <span data-ttu-id="07f1b-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="07f1b-162">Is Indexed</span></span>             | <span data-ttu-id="07f1b-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-163">False</span></span>                             |
| <span data-ttu-id="07f1b-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="07f1b-164">In Global Catalog</span></span>      | <span data-ttu-id="07f1b-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-165">False</span></span>                             |
| <span data-ttu-id="07f1b-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="07f1b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="07f1b-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="07f1b-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="07f1b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07f1b-168">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="07f1b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07f1b-169">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="07f1b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-170">Search-Flags</span></span>           | <span data-ttu-id="07f1b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07f1b-171">0x00000000</span></span>                        |
| <span data-ttu-id="07f1b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-172">System-Flags</span></span>           | <span data-ttu-id="07f1b-173">0x00000011</span><span class="sxs-lookup"><span data-stu-id="07f1b-173">0x00000011</span></span>                        |
| <span data-ttu-id="07f1b-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="07f1b-174">Classes used in</span></span>        | [<span data-ttu-id="07f1b-175">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="07f1b-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="07f1b-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07f1b-176">Windows Server 2008</span></span>



| <span data-ttu-id="07f1b-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="07f1b-177">Entry</span></span> | <span data-ttu-id="07f1b-178">Значение</span><span class="sxs-lookup"><span data-stu-id="07f1b-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="07f1b-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="07f1b-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07f1b-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="07f1b-181">System-Only</span></span>            | <span data-ttu-id="07f1b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-182">False</span></span>                             |
| <span data-ttu-id="07f1b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="07f1b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="07f1b-184">True</span><span class="sxs-lookup"><span data-stu-id="07f1b-184">True</span></span>                              |
| <span data-ttu-id="07f1b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="07f1b-185">Is Indexed</span></span>             | <span data-ttu-id="07f1b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-186">False</span></span>                             |
| <span data-ttu-id="07f1b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="07f1b-187">In Global Catalog</span></span>      | <span data-ttu-id="07f1b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-188">False</span></span>                             |
| <span data-ttu-id="07f1b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="07f1b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="07f1b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="07f1b-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="07f1b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07f1b-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="07f1b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07f1b-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="07f1b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-193">Search-Flags</span></span>           | <span data-ttu-id="07f1b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07f1b-194">0x00000000</span></span>                        |
| <span data-ttu-id="07f1b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-195">System-Flags</span></span>           | <span data-ttu-id="07f1b-196">0x00000011</span><span class="sxs-lookup"><span data-stu-id="07f1b-196">0x00000011</span></span>                        |
| <span data-ttu-id="07f1b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="07f1b-197">Classes used in</span></span>        | [<span data-ttu-id="07f1b-198">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="07f1b-198">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="07f1b-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07f1b-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="07f1b-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="07f1b-200">Entry</span></span> | <span data-ttu-id="07f1b-201">Значение</span><span class="sxs-lookup"><span data-stu-id="07f1b-201">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="07f1b-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="07f1b-202">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07f1b-203">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="07f1b-204">System-Only</span></span>            | <span data-ttu-id="07f1b-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-205">False</span></span>                             |
| <span data-ttu-id="07f1b-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="07f1b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="07f1b-207">True</span><span class="sxs-lookup"><span data-stu-id="07f1b-207">True</span></span>                              |
| <span data-ttu-id="07f1b-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="07f1b-208">Is Indexed</span></span>             | <span data-ttu-id="07f1b-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-209">False</span></span>                             |
| <span data-ttu-id="07f1b-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="07f1b-210">In Global Catalog</span></span>      | <span data-ttu-id="07f1b-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-211">False</span></span>                             |
| <span data-ttu-id="07f1b-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="07f1b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="07f1b-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="07f1b-213">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="07f1b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07f1b-214">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="07f1b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07f1b-215">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="07f1b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-216">Search-Flags</span></span>           | <span data-ttu-id="07f1b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07f1b-217">0x00000000</span></span>                        |
| <span data-ttu-id="07f1b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-218">System-Flags</span></span>           | <span data-ttu-id="07f1b-219">0x00000011</span><span class="sxs-lookup"><span data-stu-id="07f1b-219">0x00000011</span></span>                        |
| <span data-ttu-id="07f1b-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="07f1b-220">Classes used in</span></span>        | [<span data-ttu-id="07f1b-221">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="07f1b-221">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="07f1b-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07f1b-222">Windows Server 2012</span></span>



| <span data-ttu-id="07f1b-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="07f1b-223">Entry</span></span> | <span data-ttu-id="07f1b-224">Значение</span><span class="sxs-lookup"><span data-stu-id="07f1b-224">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="07f1b-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="07f1b-225">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07f1b-226">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="07f1b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="07f1b-227">System-Only</span></span>            | <span data-ttu-id="07f1b-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-228">False</span></span>                             |
| <span data-ttu-id="07f1b-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="07f1b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="07f1b-230">True</span><span class="sxs-lookup"><span data-stu-id="07f1b-230">True</span></span>                              |
| <span data-ttu-id="07f1b-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="07f1b-231">Is Indexed</span></span>             | <span data-ttu-id="07f1b-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-232">False</span></span>                             |
| <span data-ttu-id="07f1b-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="07f1b-233">In Global Catalog</span></span>      | <span data-ttu-id="07f1b-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="07f1b-234">False</span></span>                             |
| <span data-ttu-id="07f1b-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="07f1b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="07f1b-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="07f1b-236">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="07f1b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07f1b-237">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="07f1b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07f1b-238">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="07f1b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-239">Search-Flags</span></span>           | <span data-ttu-id="07f1b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07f1b-240">0x00000000</span></span>                        |
| <span data-ttu-id="07f1b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07f1b-241">System-Flags</span></span>           | <span data-ttu-id="07f1b-242">0x00000011</span><span class="sxs-lookup"><span data-stu-id="07f1b-242">0x00000011</span></span>                        |
| <span data-ttu-id="07f1b-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="07f1b-243">Classes used in</span></span>        | [<span data-ttu-id="07f1b-244">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="07f1b-244">**User**</span></span>](c-user.md)<br/> |



 

 





