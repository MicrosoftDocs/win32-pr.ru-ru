---
title: Атрибут From-Server
description: Различающееся имя исходного сервера репликации.
ms.assetid: c4ff05fe-21a7-4b59-90f8-f3bd723285fa
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута From-Server
- Схема AD атрибута Фромсервер
topic_type:
- apiref
api_name:
- From-Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd24e6c19ab10e1537d908405d8d13f7e9db5e2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989530"
---
# <a name="from-server-attribute"></a><span data-ttu-id="2eff9-105">Атрибут From-Server</span><span class="sxs-lookup"><span data-stu-id="2eff9-105">From-Server attribute</span></span>

<span data-ttu-id="2eff9-106">Различающееся имя исходного сервера репликации.</span><span class="sxs-lookup"><span data-stu-id="2eff9-106">The distinguished name of the replication source server.</span></span>



| <span data-ttu-id="2eff9-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-107">Entry</span></span> | <span data-ttu-id="2eff9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="2eff9-109">CN</span><span class="sxs-lookup"><span data-stu-id="2eff9-109">CN</span></span>                | <span data-ttu-id="2eff9-110">From-Server</span><span class="sxs-lookup"><span data-stu-id="2eff9-110">From-Server</span></span>                             |
| <span data-ttu-id="2eff9-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2eff9-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2eff9-112">фромсервер</span><span class="sxs-lookup"><span data-stu-id="2eff9-112">fromServer</span></span>                              |
| <span data-ttu-id="2eff9-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2eff9-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="2eff9-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2eff9-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="2eff9-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2eff9-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="2eff9-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-116">Attribute-Id</span></span>      | <span data-ttu-id="2eff9-117">1.2.840.113556.1.4.40</span><span class="sxs-lookup"><span data-stu-id="2eff9-117">1.2.840.113556.1.4.40</span></span>                   |
| <span data-ttu-id="2eff9-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2eff9-118">System-Id-Guid</span></span>    | <span data-ttu-id="2eff9-119">bf967979-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="2eff9-119">bf967979-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="2eff9-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2eff9-120">Syntax</span></span>            | [<span data-ttu-id="2eff9-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="2eff9-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="2eff9-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2eff9-122">Implementations</span></span>

-   [<span data-ttu-id="2eff9-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2eff9-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2eff9-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2eff9-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2eff9-125">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="2eff9-125">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="2eff9-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2eff9-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2eff9-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2eff9-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2eff9-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2eff9-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2eff9-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2eff9-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2eff9-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2eff9-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2eff9-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-131">Entry</span></span> | <span data-ttu-id="2eff9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-132">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-133">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-134">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-135">System-Only</span></span>            | <span data-ttu-id="2eff9-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-136">False</span></span>                                                  |
| <span data-ttu-id="2eff9-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-138">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-138">True</span></span>                                                   |
| <span data-ttu-id="2eff9-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-139">Is Indexed</span></span>             | <span data-ttu-id="2eff9-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-140">False</span></span>                                                  |
| <span data-ttu-id="2eff9-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-141">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-142">False</span></span>                                                  |
| <span data-ttu-id="2eff9-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-144">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-145">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-146">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-147">Search-Flags</span></span>           | <span data-ttu-id="2eff9-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eff9-148">0x00000000</span></span>                                             |
| <span data-ttu-id="2eff9-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-149">System-Flags</span></span>           | <span data-ttu-id="2eff9-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-150">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-151">Classes used in</span></span>        | [<span data-ttu-id="2eff9-152">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-152">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2eff9-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2eff9-153">Windows Server 2003</span></span>



| <span data-ttu-id="2eff9-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-154">Entry</span></span> | <span data-ttu-id="2eff9-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-155">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-156">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-157">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-158">System-Only</span></span>            | <span data-ttu-id="2eff9-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-159">False</span></span>                                                  |
| <span data-ttu-id="2eff9-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-161">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-161">True</span></span>                                                   |
| <span data-ttu-id="2eff9-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-162">Is Indexed</span></span>             | <span data-ttu-id="2eff9-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-163">False</span></span>                                                  |
| <span data-ttu-id="2eff9-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-164">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-165">False</span></span>                                                  |
| <span data-ttu-id="2eff9-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-167">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-168">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-169">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-170">Search-Flags</span></span>           | <span data-ttu-id="2eff9-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eff9-171">0x00000000</span></span>                                             |
| <span data-ttu-id="2eff9-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-172">System-Flags</span></span>           | <span data-ttu-id="2eff9-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-173">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-174">Classes used in</span></span>        | [<span data-ttu-id="2eff9-175">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-175">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="adam"></a><span data-ttu-id="2eff9-176">ADAM</span><span class="sxs-lookup"><span data-stu-id="2eff9-176">ADAM</span></span>



| <span data-ttu-id="2eff9-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-177">Entry</span></span> | <span data-ttu-id="2eff9-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-178">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-179">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-180">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-181">System-Only</span></span>            | <span data-ttu-id="2eff9-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-182">False</span></span>                                                  |
| <span data-ttu-id="2eff9-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-184">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-184">True</span></span>                                                   |
| <span data-ttu-id="2eff9-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-185">Is Indexed</span></span>             | <span data-ttu-id="2eff9-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-186">False</span></span>                                                  |
| <span data-ttu-id="2eff9-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-187">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-188">False</span></span>                                                  |
| <span data-ttu-id="2eff9-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-190">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-191">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-192">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-193">Search-Flags</span></span>           | <span data-ttu-id="2eff9-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eff9-194">0x00000000</span></span>                                             |
| <span data-ttu-id="2eff9-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-195">System-Flags</span></span>           | <span data-ttu-id="2eff9-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-196">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-197">Classes used in</span></span>        | [<span data-ttu-id="2eff9-198">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-198">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2eff9-199">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2eff9-199">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2eff9-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-200">Entry</span></span> | <span data-ttu-id="2eff9-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-201">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-202">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-203">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-204">System-Only</span></span>            | <span data-ttu-id="2eff9-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-205">False</span></span>                                                  |
| <span data-ttu-id="2eff9-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-207">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-207">True</span></span>                                                   |
| <span data-ttu-id="2eff9-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-208">Is Indexed</span></span>             | <span data-ttu-id="2eff9-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-209">False</span></span>                                                  |
| <span data-ttu-id="2eff9-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-210">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-211">False</span></span>                                                  |
| <span data-ttu-id="2eff9-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-213">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-214">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-215">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-216">Search-Flags</span></span>           | <span data-ttu-id="2eff9-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2eff9-217">0x00000000</span></span>                                             |
| <span data-ttu-id="2eff9-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-218">System-Flags</span></span>           | <span data-ttu-id="2eff9-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-219">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-220">Classes used in</span></span>        | [<span data-ttu-id="2eff9-221">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-221">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2eff9-222">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eff9-222">Windows Server 2008</span></span>



| <span data-ttu-id="2eff9-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-223">Entry</span></span> | <span data-ttu-id="2eff9-224">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-224">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-225">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-226">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-227">System-Only</span></span>            | <span data-ttu-id="2eff9-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-228">False</span></span>                                                  |
| <span data-ttu-id="2eff9-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-230">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-230">True</span></span>                                                   |
| <span data-ttu-id="2eff9-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-231">Is Indexed</span></span>             | <span data-ttu-id="2eff9-232">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-232">True</span></span>                                                   |
| <span data-ttu-id="2eff9-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-233">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-234">False</span></span>                                                  |
| <span data-ttu-id="2eff9-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-236">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-237">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-238">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-239">Search-Flags</span></span>           | <span data-ttu-id="2eff9-240">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2eff9-240">0x00000001</span></span>                                             |
| <span data-ttu-id="2eff9-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-241">System-Flags</span></span>           | <span data-ttu-id="2eff9-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-242">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-243">Classes used in</span></span>        | [<span data-ttu-id="2eff9-244">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-244">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2eff9-245">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2eff9-245">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2eff9-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-246">Entry</span></span> | <span data-ttu-id="2eff9-247">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-247">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-248">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-249">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-250">System-Only</span></span>            | <span data-ttu-id="2eff9-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-251">False</span></span>                                                  |
| <span data-ttu-id="2eff9-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-253">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-253">True</span></span>                                                   |
| <span data-ttu-id="2eff9-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-254">Is Indexed</span></span>             | <span data-ttu-id="2eff9-255">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-255">True</span></span>                                                   |
| <span data-ttu-id="2eff9-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-256">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-257">False</span></span>                                                  |
| <span data-ttu-id="2eff9-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-259">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-260">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-261">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-262">Search-Flags</span></span>           | <span data-ttu-id="2eff9-263">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2eff9-263">0x00000001</span></span>                                             |
| <span data-ttu-id="2eff9-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-264">System-Flags</span></span>           | <span data-ttu-id="2eff9-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-265">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-266">Classes used in</span></span>        | [<span data-ttu-id="2eff9-267">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-267">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2eff9-268">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2eff9-268">Windows Server 2012</span></span>



| <span data-ttu-id="2eff9-269">Ввод</span><span class="sxs-lookup"><span data-stu-id="2eff9-269">Entry</span></span> | <span data-ttu-id="2eff9-270">Значение</span><span class="sxs-lookup"><span data-stu-id="2eff9-270">Value</span></span> |
|------------------------|--------------------------------------------------------|
| <span data-ttu-id="2eff9-271">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2eff9-271">Link-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-272">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2eff9-272">MAPI-Id</span></span>                | \-                                                     |
| <span data-ttu-id="2eff9-273">System-Only</span><span class="sxs-lookup"><span data-stu-id="2eff9-273">System-Only</span></span>            | <span data-ttu-id="2eff9-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-274">False</span></span>                                                  |
| <span data-ttu-id="2eff9-275">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2eff9-275">Is-Single-Valued</span></span>       | <span data-ttu-id="2eff9-276">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-276">True</span></span>                                                   |
| <span data-ttu-id="2eff9-277">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2eff9-277">Is Indexed</span></span>             | <span data-ttu-id="2eff9-278">True</span><span class="sxs-lookup"><span data-stu-id="2eff9-278">True</span></span>                                                   |
| <span data-ttu-id="2eff9-279">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2eff9-279">In Global Catalog</span></span>      | <span data-ttu-id="2eff9-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="2eff9-280">False</span></span>                                                  |
| <span data-ttu-id="2eff9-281">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2eff9-281">NT-Security-Descriptor</span></span> | <span data-ttu-id="2eff9-282">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2eff9-282">O:BAG:BAD:S:</span></span>                                           |
| <span data-ttu-id="2eff9-283">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2eff9-283">Range-Lower</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2eff9-284">Range-Upper</span></span>            | \-                                                     |
| <span data-ttu-id="2eff9-285">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-285">Search-Flags</span></span>           | <span data-ttu-id="2eff9-286">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2eff9-286">0x00000001</span></span>                                             |
| <span data-ttu-id="2eff9-287">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2eff9-287">System-Flags</span></span>           | <span data-ttu-id="2eff9-288">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2eff9-288">0x00000010</span></span>                                             |
| <span data-ttu-id="2eff9-289">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2eff9-289">Classes used in</span></span>        | [<span data-ttu-id="2eff9-290">**NTDS — подключение**</span><span class="sxs-lookup"><span data-stu-id="2eff9-290">**NTDS-Connection**</span></span>](c-ntdsconnection.md)<br/> |



 

 





