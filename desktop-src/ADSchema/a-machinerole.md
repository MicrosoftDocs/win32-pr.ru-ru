---
title: Атрибут Machine-Role
description: Роль для компьютера DC, сервера или рабочей станции.
ms.assetid: 1aaab4e5-1220-4cb3-8819-dbeec729d26c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Machine-Role
- Схема AD атрибута Мачинероле
topic_type:
- apiref
api_name:
- Machine-Role
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c286c0380ab8dbc0e4947a656dcf5601f1662d09
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804745"
---
# <a name="machine-role-attribute"></a><span data-ttu-id="ebdeb-105">Атрибут Machine-Role</span><span class="sxs-lookup"><span data-stu-id="ebdeb-105">Machine-Role attribute</span></span>

<span data-ttu-id="ebdeb-106">Роль для компьютера: контроллер домена, сервер или рабочая станция.</span><span class="sxs-lookup"><span data-stu-id="ebdeb-106">Role for a machine: DC, Server, or Workstation.</span></span>



| <span data-ttu-id="ebdeb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-107">Entry</span></span> | <span data-ttu-id="ebdeb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="ebdeb-109">CN</span><span class="sxs-lookup"><span data-stu-id="ebdeb-109">CN</span></span>                | <span data-ttu-id="ebdeb-110">Machine-Role</span><span class="sxs-lookup"><span data-stu-id="ebdeb-110">Machine-Role</span></span>                         |
| <span data-ttu-id="ebdeb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ebdeb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ebdeb-112">мачинероле</span><span class="sxs-lookup"><span data-stu-id="ebdeb-112">machineRole</span></span>                          |
| <span data-ttu-id="ebdeb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ebdeb-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="ebdeb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ebdeb-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="ebdeb-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ebdeb-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="ebdeb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-116">Attribute-Id</span></span>      | <span data-ttu-id="ebdeb-117">1.2.840.113556.1.4.71</span><span class="sxs-lookup"><span data-stu-id="ebdeb-117">1.2.840.113556.1.4.71</span></span>                |
| <span data-ttu-id="ebdeb-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ebdeb-118">System-Id-Guid</span></span>    | <span data-ttu-id="ebdeb-119">bf9679b2-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="ebdeb-119">bf9679b2-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="ebdeb-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebdeb-120">Syntax</span></span>            | [<span data-ttu-id="ebdeb-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="ebdeb-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ebdeb-122">Implementations</span></span>

-   [<span data-ttu-id="ebdeb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ebdeb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ebdeb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ebdeb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ebdeb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ebdeb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ebdeb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ebdeb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="ebdeb-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-130">Entry</span></span> | <span data-ttu-id="ebdeb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-131">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ebdeb-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebdeb-132">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-133">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebdeb-134">System-Only</span></span>            | <span data-ttu-id="ebdeb-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-135">False</span></span>                                     |
| <span data-ttu-id="ebdeb-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebdeb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="ebdeb-137">True</span><span class="sxs-lookup"><span data-stu-id="ebdeb-137">True</span></span>                                      |
| <span data-ttu-id="ebdeb-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebdeb-138">Is Indexed</span></span>             | <span data-ttu-id="ebdeb-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-139">False</span></span>                                     |
| <span data-ttu-id="ebdeb-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebdeb-140">In Global Catalog</span></span>      | <span data-ttu-id="ebdeb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-141">False</span></span>                                     |
| <span data-ttu-id="ebdeb-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebdeb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebdeb-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebdeb-143">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ebdeb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebdeb-144">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebdeb-145">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-146">Search-Flags</span></span>           | <span data-ttu-id="ebdeb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebdeb-147">0x00000000</span></span>                                |
| <span data-ttu-id="ebdeb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-148">System-Flags</span></span>           | <span data-ttu-id="ebdeb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebdeb-149">0x00000010</span></span>                                |
| <span data-ttu-id="ebdeb-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebdeb-150">Classes used in</span></span>        | [<span data-ttu-id="ebdeb-151">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-151">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ebdeb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ebdeb-152">Windows Server 2003</span></span>



| <span data-ttu-id="ebdeb-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-153">Entry</span></span> | <span data-ttu-id="ebdeb-154">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-154">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ebdeb-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebdeb-155">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-156">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebdeb-157">System-Only</span></span>            | <span data-ttu-id="ebdeb-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-158">False</span></span>                                     |
| <span data-ttu-id="ebdeb-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebdeb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="ebdeb-160">True</span><span class="sxs-lookup"><span data-stu-id="ebdeb-160">True</span></span>                                      |
| <span data-ttu-id="ebdeb-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebdeb-161">Is Indexed</span></span>             | <span data-ttu-id="ebdeb-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-162">False</span></span>                                     |
| <span data-ttu-id="ebdeb-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebdeb-163">In Global Catalog</span></span>      | <span data-ttu-id="ebdeb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-164">False</span></span>                                     |
| <span data-ttu-id="ebdeb-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebdeb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebdeb-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebdeb-166">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ebdeb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebdeb-167">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebdeb-168">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-169">Search-Flags</span></span>           | <span data-ttu-id="ebdeb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebdeb-170">0x00000000</span></span>                                |
| <span data-ttu-id="ebdeb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-171">System-Flags</span></span>           | <span data-ttu-id="ebdeb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebdeb-172">0x00000010</span></span>                                |
| <span data-ttu-id="ebdeb-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebdeb-173">Classes used in</span></span>        | [<span data-ttu-id="ebdeb-174">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-174">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ebdeb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ebdeb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ebdeb-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-176">Entry</span></span> | <span data-ttu-id="ebdeb-177">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-177">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ebdeb-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebdeb-178">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-179">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebdeb-180">System-Only</span></span>            | <span data-ttu-id="ebdeb-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-181">False</span></span>                                     |
| <span data-ttu-id="ebdeb-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebdeb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="ebdeb-183">True</span><span class="sxs-lookup"><span data-stu-id="ebdeb-183">True</span></span>                                      |
| <span data-ttu-id="ebdeb-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebdeb-184">Is Indexed</span></span>             | <span data-ttu-id="ebdeb-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-185">False</span></span>                                     |
| <span data-ttu-id="ebdeb-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebdeb-186">In Global Catalog</span></span>      | <span data-ttu-id="ebdeb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-187">False</span></span>                                     |
| <span data-ttu-id="ebdeb-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebdeb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebdeb-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebdeb-189">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ebdeb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebdeb-190">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebdeb-191">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-192">Search-Flags</span></span>           | <span data-ttu-id="ebdeb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebdeb-193">0x00000000</span></span>                                |
| <span data-ttu-id="ebdeb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-194">System-Flags</span></span>           | <span data-ttu-id="ebdeb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebdeb-195">0x00000010</span></span>                                |
| <span data-ttu-id="ebdeb-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebdeb-196">Classes used in</span></span>        | [<span data-ttu-id="ebdeb-197">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-197">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ebdeb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebdeb-198">Windows Server 2008</span></span>



| <span data-ttu-id="ebdeb-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-199">Entry</span></span> | <span data-ttu-id="ebdeb-200">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-200">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ebdeb-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebdeb-201">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-202">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebdeb-203">System-Only</span></span>            | <span data-ttu-id="ebdeb-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-204">False</span></span>                                     |
| <span data-ttu-id="ebdeb-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebdeb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="ebdeb-206">True</span><span class="sxs-lookup"><span data-stu-id="ebdeb-206">True</span></span>                                      |
| <span data-ttu-id="ebdeb-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebdeb-207">Is Indexed</span></span>             | <span data-ttu-id="ebdeb-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-208">False</span></span>                                     |
| <span data-ttu-id="ebdeb-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebdeb-209">In Global Catalog</span></span>      | <span data-ttu-id="ebdeb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-210">False</span></span>                                     |
| <span data-ttu-id="ebdeb-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebdeb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebdeb-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebdeb-212">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ebdeb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebdeb-213">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebdeb-214">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-215">Search-Flags</span></span>           | <span data-ttu-id="ebdeb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebdeb-216">0x00000000</span></span>                                |
| <span data-ttu-id="ebdeb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-217">System-Flags</span></span>           | <span data-ttu-id="ebdeb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebdeb-218">0x00000010</span></span>                                |
| <span data-ttu-id="ebdeb-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebdeb-219">Classes used in</span></span>        | [<span data-ttu-id="ebdeb-220">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-220">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ebdeb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ebdeb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ebdeb-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-222">Entry</span></span> | <span data-ttu-id="ebdeb-223">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-223">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ebdeb-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebdeb-224">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-225">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebdeb-226">System-Only</span></span>            | <span data-ttu-id="ebdeb-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-227">False</span></span>                                     |
| <span data-ttu-id="ebdeb-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebdeb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="ebdeb-229">True</span><span class="sxs-lookup"><span data-stu-id="ebdeb-229">True</span></span>                                      |
| <span data-ttu-id="ebdeb-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebdeb-230">Is Indexed</span></span>             | <span data-ttu-id="ebdeb-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-231">False</span></span>                                     |
| <span data-ttu-id="ebdeb-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebdeb-232">In Global Catalog</span></span>      | <span data-ttu-id="ebdeb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-233">False</span></span>                                     |
| <span data-ttu-id="ebdeb-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebdeb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebdeb-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebdeb-235">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ebdeb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebdeb-236">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebdeb-237">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-238">Search-Flags</span></span>           | <span data-ttu-id="ebdeb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebdeb-239">0x00000000</span></span>                                |
| <span data-ttu-id="ebdeb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-240">System-Flags</span></span>           | <span data-ttu-id="ebdeb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebdeb-241">0x00000010</span></span>                                |
| <span data-ttu-id="ebdeb-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebdeb-242">Classes used in</span></span>        | [<span data-ttu-id="ebdeb-243">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-243">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ebdeb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ebdeb-244">Windows Server 2012</span></span>



| <span data-ttu-id="ebdeb-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="ebdeb-245">Entry</span></span> | <span data-ttu-id="ebdeb-246">Значение</span><span class="sxs-lookup"><span data-stu-id="ebdeb-246">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ebdeb-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ebdeb-247">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ebdeb-248">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ebdeb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="ebdeb-249">System-Only</span></span>            | <span data-ttu-id="ebdeb-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-250">False</span></span>                                     |
| <span data-ttu-id="ebdeb-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ebdeb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="ebdeb-252">True</span><span class="sxs-lookup"><span data-stu-id="ebdeb-252">True</span></span>                                      |
| <span data-ttu-id="ebdeb-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ebdeb-253">Is Indexed</span></span>             | <span data-ttu-id="ebdeb-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-254">False</span></span>                                     |
| <span data-ttu-id="ebdeb-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ebdeb-255">In Global Catalog</span></span>      | <span data-ttu-id="ebdeb-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="ebdeb-256">False</span></span>                                     |
| <span data-ttu-id="ebdeb-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ebdeb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="ebdeb-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ebdeb-258">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ebdeb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ebdeb-259">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ebdeb-260">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="ebdeb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-261">Search-Flags</span></span>           | <span data-ttu-id="ebdeb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ebdeb-262">0x00000000</span></span>                                |
| <span data-ttu-id="ebdeb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ebdeb-263">System-Flags</span></span>           | <span data-ttu-id="ebdeb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ebdeb-264">0x00000010</span></span>                                |
| <span data-ttu-id="ebdeb-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ebdeb-265">Classes used in</span></span>        | [<span data-ttu-id="ebdeb-266">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ebdeb-266">**Computer**</span></span>](c-computer.md)<br/> |



 

 





