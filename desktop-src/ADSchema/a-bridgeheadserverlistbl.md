---
title: Плацдарм-Server-List-BL, атрибут
description: Список серверов, являющихся серверами-плацдармами для репликации.
ms.assetid: b84176af-c6d2-4390-92d1-d29949da0691
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута-сервера-плацдарма BL
- Схема AD атрибута Бриджехеадсерверлистбл
topic_type:
- apiref
api_name:
- Bridgehead-Server-List-BL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df941f323916682158c6c1c3ac59856b31da03f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138298"
---
# <a name="bridgehead-server-list-bl-attribute"></a><span data-ttu-id="b7821-105">Плацдарм-Server-List-BL, атрибут</span><span class="sxs-lookup"><span data-stu-id="b7821-105">Bridgehead-Server-List-BL attribute</span></span>

<span data-ttu-id="b7821-106">Список серверов, являющихся серверами-плацдармами для репликации.</span><span class="sxs-lookup"><span data-stu-id="b7821-106">The list of servers that are bridgeheads for replication.</span></span>



| <span data-ttu-id="b7821-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-107">Entry</span></span> | <span data-ttu-id="b7821-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="b7821-109">CN</span><span class="sxs-lookup"><span data-stu-id="b7821-109">CN</span></span>                | <span data-ttu-id="b7821-110">Плацдарм-Server-List-BL</span><span class="sxs-lookup"><span data-stu-id="b7821-110">Bridgehead-Server-List-BL</span></span>               |
| <span data-ttu-id="b7821-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b7821-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b7821-112">бриджехеадсерверлистбл</span><span class="sxs-lookup"><span data-stu-id="b7821-112">bridgeheadServerListBL</span></span>                  |
| <span data-ttu-id="b7821-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b7821-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="b7821-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b7821-114">Update Privilege</span></span>  | <span data-ttu-id="b7821-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="b7821-115">This value is set by the system.</span></span>        |
| <span data-ttu-id="b7821-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b7821-116">Update Frequency</span></span>  | <span data-ttu-id="b7821-117">При настройке сайта.</span><span class="sxs-lookup"><span data-stu-id="b7821-117">Whenever a site is setup.</span></span>               |
| <span data-ttu-id="b7821-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-118">Attribute-Id</span></span>      | <span data-ttu-id="b7821-119">1.2.840.113556.1.4.820</span><span class="sxs-lookup"><span data-stu-id="b7821-119">1.2.840.113556.1.4.820</span></span>                  |
| <span data-ttu-id="b7821-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b7821-120">System-Id-Guid</span></span>    | <span data-ttu-id="b7821-121">d50c2cdb-8951-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b7821-121">d50c2cdb-8951-11d1-aebc-0000f80367c1</span></span>    |
| <span data-ttu-id="b7821-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7821-122">Syntax</span></span>            | [<span data-ttu-id="b7821-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="b7821-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="b7821-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b7821-124">Implementations</span></span>

-   [<span data-ttu-id="b7821-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7821-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7821-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7821-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7821-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="b7821-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="b7821-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7821-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7821-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7821-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7821-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7821-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7821-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7821-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7821-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7821-132">Windows 2000 Server</span></span>



| <span data-ttu-id="b7821-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-133">Entry</span></span> | <span data-ttu-id="b7821-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-134">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-135">Link-Id</span></span>                | <span data-ttu-id="b7821-136">99</span><span class="sxs-lookup"><span data-stu-id="b7821-136">99</span></span>                              |
| <span data-ttu-id="b7821-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-137">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-138">System-Only</span></span>            | <span data-ttu-id="b7821-139">True</span><span class="sxs-lookup"><span data-stu-id="b7821-139">True</span></span>                            |
| <span data-ttu-id="b7821-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-140">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-141">False</span></span>                           |
| <span data-ttu-id="b7821-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-142">Is Indexed</span></span>             | <span data-ttu-id="b7821-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-143">False</span></span>                           |
| <span data-ttu-id="b7821-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-144">In Global Catalog</span></span>      | <span data-ttu-id="b7821-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-145">False</span></span>                           |
| <span data-ttu-id="b7821-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-147">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-148">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-149">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-150">Search-Flags</span></span>           | <span data-ttu-id="b7821-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-151">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-152">System-Flags</span></span>           | <span data-ttu-id="b7821-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-153">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-154">Classes used in</span></span>        | [<span data-ttu-id="b7821-155">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-155">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7821-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7821-156">Windows Server 2003</span></span>



| <span data-ttu-id="b7821-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-157">Entry</span></span> | <span data-ttu-id="b7821-158">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-158">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-159">Link-Id</span></span>                | <span data-ttu-id="b7821-160">99</span><span class="sxs-lookup"><span data-stu-id="b7821-160">99</span></span>                              |
| <span data-ttu-id="b7821-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-161">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-162">System-Only</span></span>            | <span data-ttu-id="b7821-163">True</span><span class="sxs-lookup"><span data-stu-id="b7821-163">True</span></span>                            |
| <span data-ttu-id="b7821-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-164">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-165">False</span></span>                           |
| <span data-ttu-id="b7821-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-166">Is Indexed</span></span>             | <span data-ttu-id="b7821-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-167">False</span></span>                           |
| <span data-ttu-id="b7821-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-168">In Global Catalog</span></span>      | <span data-ttu-id="b7821-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-169">False</span></span>                           |
| <span data-ttu-id="b7821-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-171">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-172">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-173">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-174">Search-Flags</span></span>           | <span data-ttu-id="b7821-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-175">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-176">System-Flags</span></span>           | <span data-ttu-id="b7821-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-177">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-178">Classes used in</span></span>        | [<span data-ttu-id="b7821-179">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-179">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="b7821-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="b7821-180">ADAM</span></span>



| <span data-ttu-id="b7821-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-181">Entry</span></span> | <span data-ttu-id="b7821-182">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-182">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-183">Link-Id</span></span>                | <span data-ttu-id="b7821-184">99</span><span class="sxs-lookup"><span data-stu-id="b7821-184">99</span></span>                              |
| <span data-ttu-id="b7821-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-185">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-186">System-Only</span></span>            | <span data-ttu-id="b7821-187">True</span><span class="sxs-lookup"><span data-stu-id="b7821-187">True</span></span>                            |
| <span data-ttu-id="b7821-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-188">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-189">False</span></span>                           |
| <span data-ttu-id="b7821-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-190">Is Indexed</span></span>             | <span data-ttu-id="b7821-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-191">False</span></span>                           |
| <span data-ttu-id="b7821-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-192">In Global Catalog</span></span>      | <span data-ttu-id="b7821-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-193">False</span></span>                           |
| <span data-ttu-id="b7821-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-195">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-196">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-197">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-198">Search-Flags</span></span>           | <span data-ttu-id="b7821-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-199">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-200">System-Flags</span></span>           | <span data-ttu-id="b7821-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-201">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-202">Classes used in</span></span>        | [<span data-ttu-id="b7821-203">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-203">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7821-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7821-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7821-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-205">Entry</span></span> | <span data-ttu-id="b7821-206">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-206">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-207">Link-Id</span></span>                | <span data-ttu-id="b7821-208">99</span><span class="sxs-lookup"><span data-stu-id="b7821-208">99</span></span>                              |
| <span data-ttu-id="b7821-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-209">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-210">System-Only</span></span>            | <span data-ttu-id="b7821-211">True</span><span class="sxs-lookup"><span data-stu-id="b7821-211">True</span></span>                            |
| <span data-ttu-id="b7821-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-212">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-213">False</span></span>                           |
| <span data-ttu-id="b7821-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-214">Is Indexed</span></span>             | <span data-ttu-id="b7821-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-215">False</span></span>                           |
| <span data-ttu-id="b7821-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-216">In Global Catalog</span></span>      | <span data-ttu-id="b7821-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-217">False</span></span>                           |
| <span data-ttu-id="b7821-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-219">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-220">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-221">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-222">Search-Flags</span></span>           | <span data-ttu-id="b7821-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-223">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-224">System-Flags</span></span>           | <span data-ttu-id="b7821-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-225">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-226">Classes used in</span></span>        | [<span data-ttu-id="b7821-227">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-227">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7821-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7821-228">Windows Server 2008</span></span>



| <span data-ttu-id="b7821-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-229">Entry</span></span> | <span data-ttu-id="b7821-230">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-230">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-231">Link-Id</span></span>                | <span data-ttu-id="b7821-232">99</span><span class="sxs-lookup"><span data-stu-id="b7821-232">99</span></span>                              |
| <span data-ttu-id="b7821-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-233">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-234">System-Only</span></span>            | <span data-ttu-id="b7821-235">True</span><span class="sxs-lookup"><span data-stu-id="b7821-235">True</span></span>                            |
| <span data-ttu-id="b7821-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-237">False</span></span>                           |
| <span data-ttu-id="b7821-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-238">Is Indexed</span></span>             | <span data-ttu-id="b7821-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-239">False</span></span>                           |
| <span data-ttu-id="b7821-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-240">In Global Catalog</span></span>      | <span data-ttu-id="b7821-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-241">False</span></span>                           |
| <span data-ttu-id="b7821-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-243">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-244">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-245">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-246">Search-Flags</span></span>           | <span data-ttu-id="b7821-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-247">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-248">System-Flags</span></span>           | <span data-ttu-id="b7821-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-249">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-250">Classes used in</span></span>        | [<span data-ttu-id="b7821-251">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-251">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7821-252">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7821-252">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7821-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-253">Entry</span></span> | <span data-ttu-id="b7821-254">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-254">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-255">Link-Id</span></span>                | <span data-ttu-id="b7821-256">99</span><span class="sxs-lookup"><span data-stu-id="b7821-256">99</span></span>                              |
| <span data-ttu-id="b7821-257">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-257">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-258">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-258">System-Only</span></span>            | <span data-ttu-id="b7821-259">True</span><span class="sxs-lookup"><span data-stu-id="b7821-259">True</span></span>                            |
| <span data-ttu-id="b7821-260">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-260">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-261">False</span></span>                           |
| <span data-ttu-id="b7821-262">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-262">Is Indexed</span></span>             | <span data-ttu-id="b7821-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-263">False</span></span>                           |
| <span data-ttu-id="b7821-264">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-264">In Global Catalog</span></span>      | <span data-ttu-id="b7821-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-265">False</span></span>                           |
| <span data-ttu-id="b7821-266">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-266">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-267">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-267">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-268">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-268">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-269">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-269">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-270">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-270">Search-Flags</span></span>           | <span data-ttu-id="b7821-271">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-271">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-272">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-272">System-Flags</span></span>           | <span data-ttu-id="b7821-273">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-273">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-274">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-274">Classes used in</span></span>        | [<span data-ttu-id="b7821-275">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-275">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7821-276">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7821-276">Windows Server 2012</span></span>



| <span data-ttu-id="b7821-277">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7821-277">Entry</span></span> | <span data-ttu-id="b7821-278">Значение</span><span class="sxs-lookup"><span data-stu-id="b7821-278">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="b7821-279">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7821-279">Link-Id</span></span>                | <span data-ttu-id="b7821-280">99</span><span class="sxs-lookup"><span data-stu-id="b7821-280">99</span></span>                              |
| <span data-ttu-id="b7821-281">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7821-281">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="b7821-282">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7821-282">System-Only</span></span>            | <span data-ttu-id="b7821-283">True</span><span class="sxs-lookup"><span data-stu-id="b7821-283">True</span></span>                            |
| <span data-ttu-id="b7821-284">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7821-284">Is-Single-Valued</span></span>       | <span data-ttu-id="b7821-285">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-285">False</span></span>                           |
| <span data-ttu-id="b7821-286">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7821-286">Is Indexed</span></span>             | <span data-ttu-id="b7821-287">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-287">False</span></span>                           |
| <span data-ttu-id="b7821-288">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7821-288">In Global Catalog</span></span>      | <span data-ttu-id="b7821-289">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7821-289">False</span></span>                           |
| <span data-ttu-id="b7821-290">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7821-290">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7821-291">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7821-291">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="b7821-292">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7821-292">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="b7821-293">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7821-293">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="b7821-294">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-294">Search-Flags</span></span>           | <span data-ttu-id="b7821-295">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7821-295">0x00000000</span></span>                      |
| <span data-ttu-id="b7821-296">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7821-296">System-Flags</span></span>           | <span data-ttu-id="b7821-297">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b7821-297">0x00000010</span></span>                      |
| <span data-ttu-id="b7821-298">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7821-298">Classes used in</span></span>        | [<span data-ttu-id="b7821-299">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="b7821-299">**Top**</span></span>](c-top.md)<br/> |



 

 





