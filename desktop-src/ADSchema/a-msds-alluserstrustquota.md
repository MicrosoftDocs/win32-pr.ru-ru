---
title: Атрибут MS-DS-All-Users-Trust-Quota
description: Используется для принудительного применения общей квоты пользователей к общему количеству Trusted-Domain объектов, созданных с помощью право доступа New Control, CREATE-Inbound-лесами-Trust.
ms.assetid: 77e70a26-99b4-4b49-a984-6809d02f6fb8
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута квоты MS-DS-All-Users-Trust
- Схема AD атрибута msDS-Аллусерструсткуота
topic_type:
- apiref
api_name:
- MS-DS-All-Users-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0538ff38f1eb57f339a8e0e244a378a36dd92498
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805039"
---
# <a name="ms-ds-all-users-trust-quota-attribute"></a><span data-ttu-id="fbfd8-105">Атрибут MS-DS-All-Users-Trust-Quota</span><span class="sxs-lookup"><span data-stu-id="fbfd8-105">MS-DS-All-Users-Trust-Quota attribute</span></span>

<span data-ttu-id="fbfd8-106">Используется для принудительного применения общей квоты пользователей к общему количеству Trusted-Domain объектов, созданных с помощью право доступа New Control, CREATE-Inbound-лесами-Trust.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-106">Used to enforce a combined users quota on the total number of Trusted-Domain objects created by using the new control access right, Create-Inbound-Forest-Trust.</span></span>



| <span data-ttu-id="fbfd8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfd8-107">Entry</span></span> | <span data-ttu-id="fbfd8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfd8-108">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="fbfd8-109">CN</span><span class="sxs-lookup"><span data-stu-id="fbfd8-109">CN</span></span>                | <span data-ttu-id="fbfd8-110">MS-DS-All-Users-Trust — квота</span><span class="sxs-lookup"><span data-stu-id="fbfd8-110">MS-DS-All-Users-Trust-Quota</span></span>               |
| <span data-ttu-id="fbfd8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="fbfd8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="fbfd8-112">msDS-Аллусерструсткуота</span><span class="sxs-lookup"><span data-stu-id="fbfd8-112">msDS-AllUsersTrustQuota</span></span>                   |
| <span data-ttu-id="fbfd8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="fbfd8-113">Size</span></span>              | \-                                        |
| <span data-ttu-id="fbfd8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="fbfd8-114">Update Privilege</span></span>  | <span data-ttu-id="fbfd8-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="fbfd8-115">Domain administrator</span></span>                      |
| <span data-ttu-id="fbfd8-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="fbfd8-116">Update Frequency</span></span>  | <span data-ttu-id="fbfd8-117">При создании леса и редко после него.</span><span class="sxs-lookup"><span data-stu-id="fbfd8-117">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="fbfd8-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="fbfd8-118">Attribute-Id</span></span>      | <span data-ttu-id="fbfd8-119">1.2.840.113556.1.4.1789</span><span class="sxs-lookup"><span data-stu-id="fbfd8-119">1.2.840.113556.1.4.1789</span></span>                   |
| <span data-ttu-id="fbfd8-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="fbfd8-120">System-Id-Guid</span></span>    | <span data-ttu-id="fbfd8-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span><span class="sxs-lookup"><span data-stu-id="fbfd8-121">d3aa4a5c-4e03-4810-97aa-2b339e7a434b</span></span>      |
| <span data-ttu-id="fbfd8-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbfd8-122">Syntax</span></span>            | [<span data-ttu-id="fbfd8-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-123">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="fbfd8-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="fbfd8-124">Implementations</span></span>

-   [<span data-ttu-id="fbfd8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="fbfd8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="fbfd8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="fbfd8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="fbfd8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="fbfd8-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fbfd8-130">Windows Server 2003</span></span>



| <span data-ttu-id="fbfd8-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfd8-131">Entry</span></span> | <span data-ttu-id="fbfd8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfd8-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfd8-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfd8-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfd8-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfd8-135">System-Only</span></span>            | <span data-ttu-id="fbfd8-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-136">False</span></span>                                        |
| <span data-ttu-id="fbfd8-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfd8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfd8-138">True</span><span class="sxs-lookup"><span data-stu-id="fbfd8-138">True</span></span>                                         |
| <span data-ttu-id="fbfd8-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfd8-139">Is Indexed</span></span>             | <span data-ttu-id="fbfd8-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-140">False</span></span>                                        |
| <span data-ttu-id="fbfd8-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfd8-141">In Global Catalog</span></span>      | <span data-ttu-id="fbfd8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-142">False</span></span>                                        |
| <span data-ttu-id="fbfd8-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfd8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfd8-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfd8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfd8-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfd8-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-147">Search-Flags</span></span>           | <span data-ttu-id="fbfd8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfd8-148">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfd8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-149">System-Flags</span></span>           | <span data-ttu-id="fbfd8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfd8-150">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfd8-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfd8-151">Classes used in</span></span>        | [<span data-ttu-id="fbfd8-152">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-152">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="fbfd8-153">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="fbfd8-153">Windows Server 2003 R2</span></span>



| <span data-ttu-id="fbfd8-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfd8-154">Entry</span></span> | <span data-ttu-id="fbfd8-155">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfd8-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfd8-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfd8-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfd8-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfd8-158">System-Only</span></span>            | <span data-ttu-id="fbfd8-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-159">False</span></span>                                        |
| <span data-ttu-id="fbfd8-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfd8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfd8-161">True</span><span class="sxs-lookup"><span data-stu-id="fbfd8-161">True</span></span>                                         |
| <span data-ttu-id="fbfd8-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfd8-162">Is Indexed</span></span>             | <span data-ttu-id="fbfd8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-163">False</span></span>                                        |
| <span data-ttu-id="fbfd8-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfd8-164">In Global Catalog</span></span>      | <span data-ttu-id="fbfd8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-165">False</span></span>                                        |
| <span data-ttu-id="fbfd8-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfd8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfd8-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfd8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfd8-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfd8-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-170">Search-Flags</span></span>           | <span data-ttu-id="fbfd8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfd8-171">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfd8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-172">System-Flags</span></span>           | <span data-ttu-id="fbfd8-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfd8-173">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfd8-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfd8-174">Classes used in</span></span>        | [<span data-ttu-id="fbfd8-175">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-175">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="fbfd8-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbfd8-176">Windows Server 2008</span></span>



| <span data-ttu-id="fbfd8-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfd8-177">Entry</span></span> | <span data-ttu-id="fbfd8-178">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfd8-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfd8-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfd8-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfd8-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfd8-181">System-Only</span></span>            | <span data-ttu-id="fbfd8-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-182">False</span></span>                                        |
| <span data-ttu-id="fbfd8-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfd8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfd8-184">True</span><span class="sxs-lookup"><span data-stu-id="fbfd8-184">True</span></span>                                         |
| <span data-ttu-id="fbfd8-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfd8-185">Is Indexed</span></span>             | <span data-ttu-id="fbfd8-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-186">False</span></span>                                        |
| <span data-ttu-id="fbfd8-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfd8-187">In Global Catalog</span></span>      | <span data-ttu-id="fbfd8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-188">False</span></span>                                        |
| <span data-ttu-id="fbfd8-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfd8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfd8-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfd8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfd8-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfd8-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-193">Search-Flags</span></span>           | <span data-ttu-id="fbfd8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfd8-194">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfd8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-195">System-Flags</span></span>           | <span data-ttu-id="fbfd8-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfd8-196">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfd8-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfd8-197">Classes used in</span></span>        | [<span data-ttu-id="fbfd8-198">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-198">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="fbfd8-199">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbfd8-199">Windows Server 2008 R2</span></span>



| <span data-ttu-id="fbfd8-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfd8-200">Entry</span></span> | <span data-ttu-id="fbfd8-201">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfd8-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfd8-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfd8-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfd8-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfd8-204">System-Only</span></span>            | <span data-ttu-id="fbfd8-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-205">False</span></span>                                        |
| <span data-ttu-id="fbfd8-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfd8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfd8-207">True</span><span class="sxs-lookup"><span data-stu-id="fbfd8-207">True</span></span>                                         |
| <span data-ttu-id="fbfd8-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfd8-208">Is Indexed</span></span>             | <span data-ttu-id="fbfd8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-209">False</span></span>                                        |
| <span data-ttu-id="fbfd8-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfd8-210">In Global Catalog</span></span>      | <span data-ttu-id="fbfd8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-211">False</span></span>                                        |
| <span data-ttu-id="fbfd8-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfd8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfd8-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfd8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfd8-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfd8-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-216">Search-Flags</span></span>           | <span data-ttu-id="fbfd8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfd8-217">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfd8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-218">System-Flags</span></span>           | <span data-ttu-id="fbfd8-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfd8-219">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfd8-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfd8-220">Classes used in</span></span>        | [<span data-ttu-id="fbfd8-221">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-221">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="fbfd8-222">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbfd8-222">Windows Server 2012</span></span>



| <span data-ttu-id="fbfd8-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="fbfd8-223">Entry</span></span> | <span data-ttu-id="fbfd8-224">Значение</span><span class="sxs-lookup"><span data-stu-id="fbfd8-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="fbfd8-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="fbfd8-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="fbfd8-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="fbfd8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="fbfd8-227">System-Only</span></span>            | <span data-ttu-id="fbfd8-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-228">False</span></span>                                        |
| <span data-ttu-id="fbfd8-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="fbfd8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="fbfd8-230">True</span><span class="sxs-lookup"><span data-stu-id="fbfd8-230">True</span></span>                                         |
| <span data-ttu-id="fbfd8-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="fbfd8-231">Is Indexed</span></span>             | <span data-ttu-id="fbfd8-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-232">False</span></span>                                        |
| <span data-ttu-id="fbfd8-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="fbfd8-233">In Global Catalog</span></span>      | <span data-ttu-id="fbfd8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="fbfd8-234">False</span></span>                                        |
| <span data-ttu-id="fbfd8-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="fbfd8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="fbfd8-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="fbfd8-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="fbfd8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="fbfd8-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="fbfd8-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="fbfd8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-239">Search-Flags</span></span>           | <span data-ttu-id="fbfd8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="fbfd8-240">0x00000000</span></span>                                   |
| <span data-ttu-id="fbfd8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="fbfd8-241">System-Flags</span></span>           | <span data-ttu-id="fbfd8-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="fbfd8-242">0x00000010</span></span>                                   |
| <span data-ttu-id="fbfd8-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="fbfd8-243">Classes used in</span></span>        | [<span data-ttu-id="fbfd8-244">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="fbfd8-244">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





