---
title: Атрибут локальной политики — флаги
description: Флаги, определяющие, где компьютер получает политику. Локальная политика — ссылка.
ms.assetid: 1f2fa723-507a-4e27-a325-8bd6f6cb6bd6
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "Локальная политика — флаг"
- Схема AD атрибута Локалполицифлагс
topic_type:
- apiref
api_name:
- Local-Policy-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc077fe793a523b41974280ada7e54b82335d733
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655245"
---
# <a name="local-policy-flags-attribute"></a><span data-ttu-id="a38c0-106">Атрибут локальной политики — флаги</span><span class="sxs-lookup"><span data-stu-id="a38c0-106">Local-Policy-Flags attribute</span></span>

<span data-ttu-id="a38c0-107">Флаги, определяющие, где компьютер получает политику.</span><span class="sxs-lookup"><span data-stu-id="a38c0-107">Flags that determine where a computer gets its policy.</span></span> <span data-ttu-id="a38c0-108">Локальная политика — ссылка.</span><span class="sxs-lookup"><span data-stu-id="a38c0-108">Local-Policy-Reference.</span></span>



| <span data-ttu-id="a38c0-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-109">Entry</span></span> | <span data-ttu-id="a38c0-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="a38c0-111">CN</span><span class="sxs-lookup"><span data-stu-id="a38c0-111">CN</span></span>                | <span data-ttu-id="a38c0-112">Локальные-политика — флаги</span><span class="sxs-lookup"><span data-stu-id="a38c0-112">Local-Policy-Flags</span></span>                   |
| <span data-ttu-id="a38c0-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a38c0-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a38c0-114">локалполицифлагс</span><span class="sxs-lookup"><span data-stu-id="a38c0-114">localPolicyFlags</span></span>                     |
| <span data-ttu-id="a38c0-115">Размер</span><span class="sxs-lookup"><span data-stu-id="a38c0-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="a38c0-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a38c0-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="a38c0-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a38c0-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="a38c0-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-118">Attribute-Id</span></span>      | <span data-ttu-id="a38c0-119">1.2.840.113556.1.4.56</span><span class="sxs-lookup"><span data-stu-id="a38c0-119">1.2.840.113556.1.4.56</span></span>                |
| <span data-ttu-id="a38c0-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a38c0-120">System-Id-Guid</span></span>    | <span data-ttu-id="a38c0-121">bf96799e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a38c0-121">bf96799e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="a38c0-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a38c0-122">Syntax</span></span>            | [<span data-ttu-id="a38c0-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a38c0-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="a38c0-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a38c0-124">Implementations</span></span>

-   [<span data-ttu-id="a38c0-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a38c0-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a38c0-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a38c0-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a38c0-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a38c0-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a38c0-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a38c0-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a38c0-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a38c0-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a38c0-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a38c0-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a38c0-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a38c0-131">Windows 2000 Server</span></span>



| <span data-ttu-id="a38c0-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-132">Entry</span></span> | <span data-ttu-id="a38c0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a38c0-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a38c0-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="a38c0-136">System-Only</span></span>            | <span data-ttu-id="a38c0-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-137">False</span></span>                                     |
| <span data-ttu-id="a38c0-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a38c0-138">Is-Single-Valued</span></span>       | <span data-ttu-id="a38c0-139">True</span><span class="sxs-lookup"><span data-stu-id="a38c0-139">True</span></span>                                      |
| <span data-ttu-id="a38c0-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a38c0-140">Is Indexed</span></span>             | <span data-ttu-id="a38c0-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-141">False</span></span>                                     |
| <span data-ttu-id="a38c0-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a38c0-142">In Global Catalog</span></span>      | <span data-ttu-id="a38c0-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-143">False</span></span>                                     |
| <span data-ttu-id="a38c0-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a38c0-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="a38c0-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a38c0-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a38c0-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a38c0-146">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a38c0-147">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-148">Search-Flags</span></span>           | <span data-ttu-id="a38c0-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a38c0-149">0x00000000</span></span>                                |
| <span data-ttu-id="a38c0-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-150">System-Flags</span></span>           | <span data-ttu-id="a38c0-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a38c0-151">0x00000010</span></span>                                |
| <span data-ttu-id="a38c0-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a38c0-152">Classes used in</span></span>        | [<span data-ttu-id="a38c0-153">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a38c0-153">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a38c0-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a38c0-154">Windows Server 2003</span></span>



| <span data-ttu-id="a38c0-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-155">Entry</span></span> | <span data-ttu-id="a38c0-156">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-156">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a38c0-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a38c0-157">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-158">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="a38c0-159">System-Only</span></span>            | <span data-ttu-id="a38c0-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-160">False</span></span>                                     |
| <span data-ttu-id="a38c0-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a38c0-161">Is-Single-Valued</span></span>       | <span data-ttu-id="a38c0-162">True</span><span class="sxs-lookup"><span data-stu-id="a38c0-162">True</span></span>                                      |
| <span data-ttu-id="a38c0-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a38c0-163">Is Indexed</span></span>             | <span data-ttu-id="a38c0-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-164">False</span></span>                                     |
| <span data-ttu-id="a38c0-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a38c0-165">In Global Catalog</span></span>      | <span data-ttu-id="a38c0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-166">False</span></span>                                     |
| <span data-ttu-id="a38c0-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a38c0-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="a38c0-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a38c0-168">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a38c0-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a38c0-169">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a38c0-170">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-171">Search-Flags</span></span>           | <span data-ttu-id="a38c0-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a38c0-172">0x00000000</span></span>                                |
| <span data-ttu-id="a38c0-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-173">System-Flags</span></span>           | <span data-ttu-id="a38c0-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a38c0-174">0x00000010</span></span>                                |
| <span data-ttu-id="a38c0-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a38c0-175">Classes used in</span></span>        | [<span data-ttu-id="a38c0-176">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a38c0-176">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a38c0-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a38c0-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a38c0-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-178">Entry</span></span> | <span data-ttu-id="a38c0-179">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-179">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a38c0-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a38c0-180">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-181">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="a38c0-182">System-Only</span></span>            | <span data-ttu-id="a38c0-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-183">False</span></span>                                     |
| <span data-ttu-id="a38c0-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a38c0-184">Is-Single-Valued</span></span>       | <span data-ttu-id="a38c0-185">True</span><span class="sxs-lookup"><span data-stu-id="a38c0-185">True</span></span>                                      |
| <span data-ttu-id="a38c0-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a38c0-186">Is Indexed</span></span>             | <span data-ttu-id="a38c0-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-187">False</span></span>                                     |
| <span data-ttu-id="a38c0-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a38c0-188">In Global Catalog</span></span>      | <span data-ttu-id="a38c0-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-189">False</span></span>                                     |
| <span data-ttu-id="a38c0-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a38c0-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="a38c0-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a38c0-191">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a38c0-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a38c0-192">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a38c0-193">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-194">Search-Flags</span></span>           | <span data-ttu-id="a38c0-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a38c0-195">0x00000000</span></span>                                |
| <span data-ttu-id="a38c0-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-196">System-Flags</span></span>           | <span data-ttu-id="a38c0-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a38c0-197">0x00000010</span></span>                                |
| <span data-ttu-id="a38c0-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a38c0-198">Classes used in</span></span>        | [<span data-ttu-id="a38c0-199">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a38c0-199">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a38c0-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a38c0-200">Windows Server 2008</span></span>



| <span data-ttu-id="a38c0-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-201">Entry</span></span> | <span data-ttu-id="a38c0-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-202">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a38c0-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a38c0-203">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-204">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="a38c0-205">System-Only</span></span>            | <span data-ttu-id="a38c0-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-206">False</span></span>                                     |
| <span data-ttu-id="a38c0-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a38c0-207">Is-Single-Valued</span></span>       | <span data-ttu-id="a38c0-208">True</span><span class="sxs-lookup"><span data-stu-id="a38c0-208">True</span></span>                                      |
| <span data-ttu-id="a38c0-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a38c0-209">Is Indexed</span></span>             | <span data-ttu-id="a38c0-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-210">False</span></span>                                     |
| <span data-ttu-id="a38c0-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a38c0-211">In Global Catalog</span></span>      | <span data-ttu-id="a38c0-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-212">False</span></span>                                     |
| <span data-ttu-id="a38c0-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a38c0-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="a38c0-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a38c0-214">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a38c0-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a38c0-215">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a38c0-216">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-217">Search-Flags</span></span>           | <span data-ttu-id="a38c0-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a38c0-218">0x00000000</span></span>                                |
| <span data-ttu-id="a38c0-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-219">System-Flags</span></span>           | <span data-ttu-id="a38c0-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a38c0-220">0x00000010</span></span>                                |
| <span data-ttu-id="a38c0-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a38c0-221">Classes used in</span></span>        | [<span data-ttu-id="a38c0-222">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a38c0-222">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a38c0-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a38c0-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a38c0-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-224">Entry</span></span> | <span data-ttu-id="a38c0-225">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-225">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a38c0-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a38c0-226">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-227">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="a38c0-228">System-Only</span></span>            | <span data-ttu-id="a38c0-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-229">False</span></span>                                     |
| <span data-ttu-id="a38c0-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a38c0-230">Is-Single-Valued</span></span>       | <span data-ttu-id="a38c0-231">True</span><span class="sxs-lookup"><span data-stu-id="a38c0-231">True</span></span>                                      |
| <span data-ttu-id="a38c0-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a38c0-232">Is Indexed</span></span>             | <span data-ttu-id="a38c0-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-233">False</span></span>                                     |
| <span data-ttu-id="a38c0-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a38c0-234">In Global Catalog</span></span>      | <span data-ttu-id="a38c0-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-235">False</span></span>                                     |
| <span data-ttu-id="a38c0-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a38c0-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="a38c0-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a38c0-237">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a38c0-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a38c0-238">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a38c0-239">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-240">Search-Flags</span></span>           | <span data-ttu-id="a38c0-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a38c0-241">0x00000000</span></span>                                |
| <span data-ttu-id="a38c0-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-242">System-Flags</span></span>           | <span data-ttu-id="a38c0-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a38c0-243">0x00000010</span></span>                                |
| <span data-ttu-id="a38c0-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a38c0-244">Classes used in</span></span>        | [<span data-ttu-id="a38c0-245">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a38c0-245">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a38c0-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a38c0-246">Windows Server 2012</span></span>



| <span data-ttu-id="a38c0-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="a38c0-247">Entry</span></span> | <span data-ttu-id="a38c0-248">Значение</span><span class="sxs-lookup"><span data-stu-id="a38c0-248">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="a38c0-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a38c0-249">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a38c0-250">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="a38c0-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="a38c0-251">System-Only</span></span>            | <span data-ttu-id="a38c0-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-252">False</span></span>                                     |
| <span data-ttu-id="a38c0-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a38c0-253">Is-Single-Valued</span></span>       | <span data-ttu-id="a38c0-254">True</span><span class="sxs-lookup"><span data-stu-id="a38c0-254">True</span></span>                                      |
| <span data-ttu-id="a38c0-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a38c0-255">Is Indexed</span></span>             | <span data-ttu-id="a38c0-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-256">False</span></span>                                     |
| <span data-ttu-id="a38c0-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a38c0-257">In Global Catalog</span></span>      | <span data-ttu-id="a38c0-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="a38c0-258">False</span></span>                                     |
| <span data-ttu-id="a38c0-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a38c0-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="a38c0-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a38c0-260">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="a38c0-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a38c0-261">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a38c0-262">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="a38c0-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-263">Search-Flags</span></span>           | <span data-ttu-id="a38c0-264">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a38c0-264">0x00000000</span></span>                                |
| <span data-ttu-id="a38c0-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a38c0-265">System-Flags</span></span>           | <span data-ttu-id="a38c0-266">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a38c0-266">0x00000010</span></span>                                |
| <span data-ttu-id="a38c0-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a38c0-267">Classes used in</span></span>        | [<span data-ttu-id="a38c0-268">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="a38c0-268">**Computer**</span></span>](c-computer.md)<br/> |



 

 





