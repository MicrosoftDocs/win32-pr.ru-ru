---
title: Атрибут квоты MS-DS-на пользователя (Trust)
description: Используется для принудительного применения квоты для каждого пользователя при создании Trusted-Domain объектов, которым разрешено право на доступ к новому элементу управления, CREATE-Inbound-лесами-Trust.
ms.assetid: 3b198b24-5282-4d13-8d35-88f34c11ce94
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута квоты MS-DS-на пользователя и доверия
- Схема AD атрибута msDS-Перусертрусткуота
topic_type:
- apiref
api_name:
- MS-DS-Per-User-Trust-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3bd6ffcac01de8997f806e6aa8a8e3bd6afbb66
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655435"
---
# <a name="ms-ds-per-user-trust-quota-attribute"></a><span data-ttu-id="42439-105">Атрибут квоты MS-DS-на пользователя (Trust)</span><span class="sxs-lookup"><span data-stu-id="42439-105">MS-DS-Per-User-Trust-Quota attribute</span></span>

<span data-ttu-id="42439-106">Используется для принудительного применения квоты для каждого пользователя при создании Trusted-Domain объектов, которым разрешено право на доступ к новому элементу управления, CREATE-Inbound-лесами-Trust.</span><span class="sxs-lookup"><span data-stu-id="42439-106">Used to enforce a per-user quota for creating Trusted-Domain objects that are authorized by the new control access right, Create-Inbound-Forest-Trust.</span></span> <span data-ttu-id="42439-107">Этот атрибут ограничивает количество объектов Trusted-Domain, которые могут быть созданы одним пользователем без прав администратора.</span><span class="sxs-lookup"><span data-stu-id="42439-107">This attribute limits the number of Trusted-Domain objects that can be created by a single non-admin user.</span></span>



| <span data-ttu-id="42439-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="42439-108">Entry</span></span> | <span data-ttu-id="42439-109">Значение</span><span class="sxs-lookup"><span data-stu-id="42439-109">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="42439-110">CN</span><span class="sxs-lookup"><span data-stu-id="42439-110">CN</span></span>                | <span data-ttu-id="42439-111">Квота MS-DS-на пользователя — доверие</span><span class="sxs-lookup"><span data-stu-id="42439-111">MS-DS-Per-User-Trust-Quota</span></span>                |
| <span data-ttu-id="42439-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="42439-112">Ldap-Display-Name</span></span> | <span data-ttu-id="42439-113">msDS-Перусертрусткуота</span><span class="sxs-lookup"><span data-stu-id="42439-113">msDS-PerUserTrustQuota</span></span>                    |
| <span data-ttu-id="42439-114">Размер</span><span class="sxs-lookup"><span data-stu-id="42439-114">Size</span></span>              | \-                                        |
| <span data-ttu-id="42439-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="42439-115">Update Privilege</span></span>  | <span data-ttu-id="42439-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="42439-116">Domain administrator</span></span>                      |
| <span data-ttu-id="42439-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="42439-117">Update Frequency</span></span>  | <span data-ttu-id="42439-118">При создании леса и редко после него.</span><span class="sxs-lookup"><span data-stu-id="42439-118">At forest creation and rarely after that.</span></span> |
| <span data-ttu-id="42439-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="42439-119">Attribute-Id</span></span>      | <span data-ttu-id="42439-120">1.2.840.113556.1.4.1788</span><span class="sxs-lookup"><span data-stu-id="42439-120">1.2.840.113556.1.4.1788</span></span>                   |
| <span data-ttu-id="42439-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="42439-121">System-Id-Guid</span></span>    | <span data-ttu-id="42439-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span><span class="sxs-lookup"><span data-stu-id="42439-122">d161adf0-ca24-4993-a3aa-8b2c981302e8</span></span>      |
| <span data-ttu-id="42439-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42439-123">Syntax</span></span>            | [<span data-ttu-id="42439-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="42439-124">**Enumeration**</span></span>](s-enumeration.md)      |



## <a name="implementations"></a><span data-ttu-id="42439-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="42439-125">Implementations</span></span>

-   [<span data-ttu-id="42439-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="42439-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="42439-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="42439-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="42439-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="42439-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="42439-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="42439-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="42439-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="42439-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="42439-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42439-131">Windows Server 2003</span></span>



| <span data-ttu-id="42439-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="42439-132">Entry</span></span> | <span data-ttu-id="42439-133">Значение</span><span class="sxs-lookup"><span data-stu-id="42439-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="42439-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="42439-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42439-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="42439-136">System-Only</span></span>            | <span data-ttu-id="42439-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-137">False</span></span>                                        |
| <span data-ttu-id="42439-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="42439-138">Is-Single-Valued</span></span>       | <span data-ttu-id="42439-139">True</span><span class="sxs-lookup"><span data-stu-id="42439-139">True</span></span>                                         |
| <span data-ttu-id="42439-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="42439-140">Is Indexed</span></span>             | <span data-ttu-id="42439-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-141">False</span></span>                                        |
| <span data-ttu-id="42439-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="42439-142">In Global Catalog</span></span>      | <span data-ttu-id="42439-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-143">False</span></span>                                        |
| <span data-ttu-id="42439-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="42439-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="42439-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42439-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="42439-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42439-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="42439-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42439-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="42439-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-148">Search-Flags</span></span>           | <span data-ttu-id="42439-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42439-149">0x00000000</span></span>                                   |
| <span data-ttu-id="42439-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-150">System-Flags</span></span>           | <span data-ttu-id="42439-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42439-151">0x00000010</span></span>                                   |
| <span data-ttu-id="42439-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="42439-152">Classes used in</span></span>        | [<span data-ttu-id="42439-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="42439-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="42439-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="42439-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="42439-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="42439-155">Entry</span></span> | <span data-ttu-id="42439-156">Значение</span><span class="sxs-lookup"><span data-stu-id="42439-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="42439-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="42439-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42439-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="42439-159">System-Only</span></span>            | <span data-ttu-id="42439-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-160">False</span></span>                                        |
| <span data-ttu-id="42439-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="42439-161">Is-Single-Valued</span></span>       | <span data-ttu-id="42439-162">True</span><span class="sxs-lookup"><span data-stu-id="42439-162">True</span></span>                                         |
| <span data-ttu-id="42439-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="42439-163">Is Indexed</span></span>             | <span data-ttu-id="42439-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-164">False</span></span>                                        |
| <span data-ttu-id="42439-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="42439-165">In Global Catalog</span></span>      | <span data-ttu-id="42439-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-166">False</span></span>                                        |
| <span data-ttu-id="42439-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="42439-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="42439-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42439-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="42439-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42439-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="42439-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42439-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="42439-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-171">Search-Flags</span></span>           | <span data-ttu-id="42439-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42439-172">0x00000000</span></span>                                   |
| <span data-ttu-id="42439-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-173">System-Flags</span></span>           | <span data-ttu-id="42439-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42439-174">0x00000010</span></span>                                   |
| <span data-ttu-id="42439-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="42439-175">Classes used in</span></span>        | [<span data-ttu-id="42439-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="42439-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="42439-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42439-177">Windows Server 2008</span></span>



| <span data-ttu-id="42439-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="42439-178">Entry</span></span> | <span data-ttu-id="42439-179">Значение</span><span class="sxs-lookup"><span data-stu-id="42439-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="42439-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="42439-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42439-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="42439-182">System-Only</span></span>            | <span data-ttu-id="42439-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-183">False</span></span>                                        |
| <span data-ttu-id="42439-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="42439-184">Is-Single-Valued</span></span>       | <span data-ttu-id="42439-185">True</span><span class="sxs-lookup"><span data-stu-id="42439-185">True</span></span>                                         |
| <span data-ttu-id="42439-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="42439-186">Is Indexed</span></span>             | <span data-ttu-id="42439-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-187">False</span></span>                                        |
| <span data-ttu-id="42439-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="42439-188">In Global Catalog</span></span>      | <span data-ttu-id="42439-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-189">False</span></span>                                        |
| <span data-ttu-id="42439-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="42439-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="42439-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42439-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="42439-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42439-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="42439-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42439-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="42439-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-194">Search-Flags</span></span>           | <span data-ttu-id="42439-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42439-195">0x00000000</span></span>                                   |
| <span data-ttu-id="42439-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-196">System-Flags</span></span>           | <span data-ttu-id="42439-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42439-197">0x00000010</span></span>                                   |
| <span data-ttu-id="42439-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="42439-198">Classes used in</span></span>        | [<span data-ttu-id="42439-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="42439-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="42439-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="42439-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="42439-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="42439-201">Entry</span></span> | <span data-ttu-id="42439-202">Значение</span><span class="sxs-lookup"><span data-stu-id="42439-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="42439-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="42439-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42439-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="42439-205">System-Only</span></span>            | <span data-ttu-id="42439-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-206">False</span></span>                                        |
| <span data-ttu-id="42439-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="42439-207">Is-Single-Valued</span></span>       | <span data-ttu-id="42439-208">True</span><span class="sxs-lookup"><span data-stu-id="42439-208">True</span></span>                                         |
| <span data-ttu-id="42439-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="42439-209">Is Indexed</span></span>             | <span data-ttu-id="42439-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-210">False</span></span>                                        |
| <span data-ttu-id="42439-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="42439-211">In Global Catalog</span></span>      | <span data-ttu-id="42439-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-212">False</span></span>                                        |
| <span data-ttu-id="42439-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="42439-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="42439-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42439-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="42439-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42439-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="42439-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42439-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="42439-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-217">Search-Flags</span></span>           | <span data-ttu-id="42439-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42439-218">0x00000000</span></span>                                   |
| <span data-ttu-id="42439-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-219">System-Flags</span></span>           | <span data-ttu-id="42439-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42439-220">0x00000010</span></span>                                   |
| <span data-ttu-id="42439-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="42439-221">Classes used in</span></span>        | [<span data-ttu-id="42439-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="42439-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="42439-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42439-223">Windows Server 2012</span></span>



| <span data-ttu-id="42439-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="42439-224">Entry</span></span> | <span data-ttu-id="42439-225">Значение</span><span class="sxs-lookup"><span data-stu-id="42439-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="42439-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="42439-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="42439-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="42439-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="42439-228">System-Only</span></span>            | <span data-ttu-id="42439-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-229">False</span></span>                                        |
| <span data-ttu-id="42439-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="42439-230">Is-Single-Valued</span></span>       | <span data-ttu-id="42439-231">True</span><span class="sxs-lookup"><span data-stu-id="42439-231">True</span></span>                                         |
| <span data-ttu-id="42439-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="42439-232">Is Indexed</span></span>             | <span data-ttu-id="42439-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-233">False</span></span>                                        |
| <span data-ttu-id="42439-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="42439-234">In Global Catalog</span></span>      | <span data-ttu-id="42439-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="42439-235">False</span></span>                                        |
| <span data-ttu-id="42439-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="42439-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="42439-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="42439-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="42439-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="42439-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="42439-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="42439-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="42439-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-240">Search-Flags</span></span>           | <span data-ttu-id="42439-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42439-241">0x00000000</span></span>                                   |
| <span data-ttu-id="42439-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="42439-242">System-Flags</span></span>           | <span data-ttu-id="42439-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42439-243">0x00000010</span></span>                                   |
| <span data-ttu-id="42439-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="42439-244">Classes used in</span></span>        | [<span data-ttu-id="42439-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="42439-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





