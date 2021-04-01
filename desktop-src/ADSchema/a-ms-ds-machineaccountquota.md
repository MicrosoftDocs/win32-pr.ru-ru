---
title: Атрибут MS-DS-Machine-Account-Quota
description: Число учетных записей компьютеров, которые пользователь может создать в домене.
ms.assetid: bcfc6a9c-b891-48c2-9c42-8154345caf08
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута квоты MS-DS-Machine-Account
- Схема AD атрибута ms-DS-Мачинеаккаунткуота
topic_type:
- apiref
api_name:
- MS-DS-Machine-Account-Quota
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86de012aa876e5a0d52ac866048801872a365f1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138694"
---
# <a name="ms-ds-machine-account-quota-attribute"></a><span data-ttu-id="4b6ad-105">Атрибут MS-DS-Machine-Account-Quota</span><span class="sxs-lookup"><span data-stu-id="4b6ad-105">MS-DS-Machine-Account-Quota attribute</span></span>

<span data-ttu-id="4b6ad-106">Число учетных записей компьютеров, которые пользователь может создать в домене.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-106">The number of computer accounts that a user is allowed to create in a domain.</span></span>



| <span data-ttu-id="4b6ad-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-107">Entry</span></span> | <span data-ttu-id="4b6ad-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-108">Value</span></span> |
|-------------------|--------------------------------------------------|
| <span data-ttu-id="4b6ad-109">CN</span><span class="sxs-lookup"><span data-stu-id="4b6ad-109">CN</span></span>                | <span data-ttu-id="4b6ad-110">MS-DS-Machine-Account — квота</span><span class="sxs-lookup"><span data-stu-id="4b6ad-110">MS-DS-Machine-Account-Quota</span></span>                      |
| <span data-ttu-id="4b6ad-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4b6ad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4b6ad-112">MS-DS-Мачинеаккаунткуота</span><span class="sxs-lookup"><span data-stu-id="4b6ad-112">ms-DS-MachineAccountQuota</span></span>                        |
| <span data-ttu-id="4b6ad-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4b6ad-113">Size</span></span>              | <span data-ttu-id="4b6ad-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="4b6ad-114">4 bytes</span></span>                                          |
| <span data-ttu-id="4b6ad-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4b6ad-115">Update Privilege</span></span>  | <span data-ttu-id="4b6ad-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="4b6ad-116">Domain administrator</span></span>                             |
| <span data-ttu-id="4b6ad-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4b6ad-117">Update Frequency</span></span>  | <span data-ttu-id="4b6ad-118">Каждый раз, когда необходимо изменить квоту для домена.</span><span class="sxs-lookup"><span data-stu-id="4b6ad-118">Whenever the quota for a domain needs to change.</span></span> |
| <span data-ttu-id="4b6ad-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-119">Attribute-Id</span></span>      | <span data-ttu-id="4b6ad-120">1.2.840.113556.1.4.1411</span><span class="sxs-lookup"><span data-stu-id="4b6ad-120">1.2.840.113556.1.4.1411</span></span>                          |
| <span data-ttu-id="4b6ad-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4b6ad-121">System-Id-Guid</span></span>    | <span data-ttu-id="4b6ad-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="4b6ad-122">d064fb68-1480-11d3-91c1-0000f87a57d4</span></span>             |
| <span data-ttu-id="4b6ad-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b6ad-123">Syntax</span></span>            | [<span data-ttu-id="4b6ad-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-124">**Enumeration**</span></span>](s-enumeration.md)             |



## <a name="implementations"></a><span data-ttu-id="4b6ad-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4b6ad-125">Implementations</span></span>

-   [<span data-ttu-id="4b6ad-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4b6ad-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4b6ad-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4b6ad-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4b6ad-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4b6ad-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4b6ad-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b6ad-132">Windows 2000 Server</span></span>



| <span data-ttu-id="4b6ad-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-133">Entry</span></span> | <span data-ttu-id="4b6ad-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-134">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b6ad-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b6ad-135">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-136">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b6ad-137">System-Only</span></span>            | <span data-ttu-id="4b6ad-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-138">False</span></span>                                        |
| <span data-ttu-id="4b6ad-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b6ad-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4b6ad-140">True</span><span class="sxs-lookup"><span data-stu-id="4b6ad-140">True</span></span>                                         |
| <span data-ttu-id="4b6ad-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b6ad-141">Is Indexed</span></span>             | <span data-ttu-id="4b6ad-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-142">False</span></span>                                        |
| <span data-ttu-id="4b6ad-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b6ad-143">In Global Catalog</span></span>      | <span data-ttu-id="4b6ad-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-144">False</span></span>                                        |
| <span data-ttu-id="4b6ad-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b6ad-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b6ad-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b6ad-146">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b6ad-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b6ad-147">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b6ad-148">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-149">Search-Flags</span></span>           | <span data-ttu-id="4b6ad-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b6ad-150">0x00000000</span></span>                                   |
| <span data-ttu-id="4b6ad-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-151">System-Flags</span></span>           | <span data-ttu-id="4b6ad-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b6ad-152">0x00000010</span></span>                                   |
| <span data-ttu-id="4b6ad-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b6ad-153">Classes used in</span></span>        | [<span data-ttu-id="4b6ad-154">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4b6ad-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b6ad-155">Windows Server 2003</span></span>



| <span data-ttu-id="4b6ad-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-156">Entry</span></span> | <span data-ttu-id="4b6ad-157">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-157">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b6ad-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b6ad-158">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-159">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b6ad-160">System-Only</span></span>            | <span data-ttu-id="4b6ad-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-161">False</span></span>                                        |
| <span data-ttu-id="4b6ad-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b6ad-162">Is-Single-Valued</span></span>       | <span data-ttu-id="4b6ad-163">True</span><span class="sxs-lookup"><span data-stu-id="4b6ad-163">True</span></span>                                         |
| <span data-ttu-id="4b6ad-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b6ad-164">Is Indexed</span></span>             | <span data-ttu-id="4b6ad-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-165">False</span></span>                                        |
| <span data-ttu-id="4b6ad-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b6ad-166">In Global Catalog</span></span>      | <span data-ttu-id="4b6ad-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-167">False</span></span>                                        |
| <span data-ttu-id="4b6ad-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b6ad-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b6ad-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b6ad-169">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b6ad-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b6ad-170">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b6ad-171">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-172">Search-Flags</span></span>           | <span data-ttu-id="4b6ad-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b6ad-173">0x00000000</span></span>                                   |
| <span data-ttu-id="4b6ad-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-174">System-Flags</span></span>           | <span data-ttu-id="4b6ad-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b6ad-175">0x00000010</span></span>                                   |
| <span data-ttu-id="4b6ad-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b6ad-176">Classes used in</span></span>        | [<span data-ttu-id="4b6ad-177">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-177">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4b6ad-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4b6ad-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4b6ad-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-179">Entry</span></span> | <span data-ttu-id="4b6ad-180">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-180">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b6ad-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b6ad-181">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-182">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b6ad-183">System-Only</span></span>            | <span data-ttu-id="4b6ad-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-184">False</span></span>                                        |
| <span data-ttu-id="4b6ad-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b6ad-185">Is-Single-Valued</span></span>       | <span data-ttu-id="4b6ad-186">True</span><span class="sxs-lookup"><span data-stu-id="4b6ad-186">True</span></span>                                         |
| <span data-ttu-id="4b6ad-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b6ad-187">Is Indexed</span></span>             | <span data-ttu-id="4b6ad-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-188">False</span></span>                                        |
| <span data-ttu-id="4b6ad-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b6ad-189">In Global Catalog</span></span>      | <span data-ttu-id="4b6ad-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-190">False</span></span>                                        |
| <span data-ttu-id="4b6ad-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b6ad-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b6ad-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b6ad-192">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b6ad-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b6ad-193">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b6ad-194">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-195">Search-Flags</span></span>           | <span data-ttu-id="4b6ad-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b6ad-196">0x00000000</span></span>                                   |
| <span data-ttu-id="4b6ad-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-197">System-Flags</span></span>           | <span data-ttu-id="4b6ad-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b6ad-198">0x00000010</span></span>                                   |
| <span data-ttu-id="4b6ad-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b6ad-199">Classes used in</span></span>        | [<span data-ttu-id="4b6ad-200">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-200">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4b6ad-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b6ad-201">Windows Server 2008</span></span>



| <span data-ttu-id="4b6ad-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-202">Entry</span></span> | <span data-ttu-id="4b6ad-203">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-203">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b6ad-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b6ad-204">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-205">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b6ad-206">System-Only</span></span>            | <span data-ttu-id="4b6ad-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-207">False</span></span>                                        |
| <span data-ttu-id="4b6ad-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b6ad-208">Is-Single-Valued</span></span>       | <span data-ttu-id="4b6ad-209">True</span><span class="sxs-lookup"><span data-stu-id="4b6ad-209">True</span></span>                                         |
| <span data-ttu-id="4b6ad-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b6ad-210">Is Indexed</span></span>             | <span data-ttu-id="4b6ad-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-211">False</span></span>                                        |
| <span data-ttu-id="4b6ad-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b6ad-212">In Global Catalog</span></span>      | <span data-ttu-id="4b6ad-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-213">False</span></span>                                        |
| <span data-ttu-id="4b6ad-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b6ad-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b6ad-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b6ad-215">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b6ad-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b6ad-216">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b6ad-217">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-218">Search-Flags</span></span>           | <span data-ttu-id="4b6ad-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b6ad-219">0x00000000</span></span>                                   |
| <span data-ttu-id="4b6ad-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-220">System-Flags</span></span>           | <span data-ttu-id="4b6ad-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b6ad-221">0x00000010</span></span>                                   |
| <span data-ttu-id="4b6ad-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b6ad-222">Classes used in</span></span>        | [<span data-ttu-id="4b6ad-223">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-223">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4b6ad-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b6ad-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4b6ad-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-225">Entry</span></span> | <span data-ttu-id="4b6ad-226">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-226">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b6ad-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b6ad-227">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-228">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b6ad-229">System-Only</span></span>            | <span data-ttu-id="4b6ad-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-230">False</span></span>                                        |
| <span data-ttu-id="4b6ad-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b6ad-231">Is-Single-Valued</span></span>       | <span data-ttu-id="4b6ad-232">True</span><span class="sxs-lookup"><span data-stu-id="4b6ad-232">True</span></span>                                         |
| <span data-ttu-id="4b6ad-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b6ad-233">Is Indexed</span></span>             | <span data-ttu-id="4b6ad-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-234">False</span></span>                                        |
| <span data-ttu-id="4b6ad-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b6ad-235">In Global Catalog</span></span>      | <span data-ttu-id="4b6ad-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-236">False</span></span>                                        |
| <span data-ttu-id="4b6ad-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b6ad-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b6ad-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b6ad-238">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b6ad-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b6ad-239">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b6ad-240">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-241">Search-Flags</span></span>           | <span data-ttu-id="4b6ad-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b6ad-242">0x00000000</span></span>                                   |
| <span data-ttu-id="4b6ad-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-243">System-Flags</span></span>           | <span data-ttu-id="4b6ad-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b6ad-244">0x00000010</span></span>                                   |
| <span data-ttu-id="4b6ad-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b6ad-245">Classes used in</span></span>        | [<span data-ttu-id="4b6ad-246">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-246">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4b6ad-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4b6ad-247">Windows Server 2012</span></span>



| <span data-ttu-id="4b6ad-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="4b6ad-248">Entry</span></span> | <span data-ttu-id="4b6ad-249">Значение</span><span class="sxs-lookup"><span data-stu-id="4b6ad-249">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="4b6ad-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4b6ad-250">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4b6ad-251">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="4b6ad-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="4b6ad-252">System-Only</span></span>            | <span data-ttu-id="4b6ad-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-253">False</span></span>                                        |
| <span data-ttu-id="4b6ad-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4b6ad-254">Is-Single-Valued</span></span>       | <span data-ttu-id="4b6ad-255">True</span><span class="sxs-lookup"><span data-stu-id="4b6ad-255">True</span></span>                                         |
| <span data-ttu-id="4b6ad-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4b6ad-256">Is Indexed</span></span>             | <span data-ttu-id="4b6ad-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-257">False</span></span>                                        |
| <span data-ttu-id="4b6ad-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4b6ad-258">In Global Catalog</span></span>      | <span data-ttu-id="4b6ad-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="4b6ad-259">False</span></span>                                        |
| <span data-ttu-id="4b6ad-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4b6ad-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="4b6ad-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4b6ad-261">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="4b6ad-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4b6ad-262">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4b6ad-263">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="4b6ad-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-264">Search-Flags</span></span>           | <span data-ttu-id="4b6ad-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4b6ad-265">0x00000000</span></span>                                   |
| <span data-ttu-id="4b6ad-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4b6ad-266">System-Flags</span></span>           | <span data-ttu-id="4b6ad-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4b6ad-267">0x00000010</span></span>                                   |
| <span data-ttu-id="4b6ad-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4b6ad-268">Classes used in</span></span>        | [<span data-ttu-id="4b6ad-269">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="4b6ad-269">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





