---
title: атрибут RPC-NS-Priority
description: Приоритет данной записи профиля RPC.
ms.assetid: a4904b21-53b7-48e3-814a-948427984fcd
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "RPC-NS-Priority"
- Схема AD атрибута Рпкнсприорити
topic_type:
- apiref
api_name:
- rpc-Ns-Priority
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc2b472262d118ee4896935157d45952846db0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804553"
---
# <a name="rpc-ns-priority-attribute"></a><span data-ttu-id="e0305-105">атрибут RPC-NS-Priority</span><span class="sxs-lookup"><span data-stu-id="e0305-105">rpc-Ns-Priority attribute</span></span>

<span data-ttu-id="e0305-106">Приоритет данной записи профиля RPC.</span><span class="sxs-lookup"><span data-stu-id="e0305-106">The priority of a given RPC profile entry.</span></span>



| <span data-ttu-id="e0305-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-107">Entry</span></span> | <span data-ttu-id="e0305-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="e0305-109">CN</span><span class="sxs-lookup"><span data-stu-id="e0305-109">CN</span></span>                | <span data-ttu-id="e0305-110">RPC-NS-Priority</span><span class="sxs-lookup"><span data-stu-id="e0305-110">rpc-Ns-Priority</span></span>                      |
| <span data-ttu-id="e0305-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e0305-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e0305-112">рпкнсприорити</span><span class="sxs-lookup"><span data-stu-id="e0305-112">rpcNsPriority</span></span>                        |
| <span data-ttu-id="e0305-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e0305-113">Size</span></span>              | <span data-ttu-id="e0305-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="e0305-114">4 bytes</span></span>                              |
| <span data-ttu-id="e0305-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e0305-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="e0305-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e0305-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="e0305-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-117">Attribute-Id</span></span>      | <span data-ttu-id="e0305-118">1.2.840.113556.1.4.117</span><span class="sxs-lookup"><span data-stu-id="e0305-118">1.2.840.113556.1.4.117</span></span>               |
| <span data-ttu-id="e0305-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e0305-119">System-Id-Guid</span></span>    | <span data-ttu-id="e0305-120">bf967a27-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e0305-120">bf967a27-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="e0305-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0305-121">Syntax</span></span>            | [<span data-ttu-id="e0305-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="e0305-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="e0305-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e0305-123">Implementations</span></span>

-   [<span data-ttu-id="e0305-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e0305-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e0305-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e0305-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e0305-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e0305-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e0305-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e0305-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e0305-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e0305-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e0305-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e0305-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e0305-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0305-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e0305-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-131">Entry</span></span> | <span data-ttu-id="e0305-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-132">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e0305-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0305-133">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-134">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0305-135">System-Only</span></span>            | <span data-ttu-id="e0305-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-136">False</span></span>                                                         |
| <span data-ttu-id="e0305-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0305-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e0305-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-138">False</span></span>                                                         |
| <span data-ttu-id="e0305-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0305-139">Is Indexed</span></span>             | <span data-ttu-id="e0305-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-140">False</span></span>                                                         |
| <span data-ttu-id="e0305-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0305-141">In Global Catalog</span></span>      | <span data-ttu-id="e0305-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-142">False</span></span>                                                         |
| <span data-ttu-id="e0305-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0305-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0305-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0305-144">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e0305-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0305-145">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0305-146">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-147">Search-Flags</span></span>           | <span data-ttu-id="e0305-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0305-148">0x00000000</span></span>                                                    |
| <span data-ttu-id="e0305-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-149">System-Flags</span></span>           | <span data-ttu-id="e0305-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0305-150">0x00000010</span></span>                                                    |
| <span data-ttu-id="e0305-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0305-151">Classes used in</span></span>        | [<span data-ttu-id="e0305-152">**RPC-Profile-элемент**</span><span class="sxs-lookup"><span data-stu-id="e0305-152">**rpc-Profile-Element**</span></span>](c-rpcprofileelement.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e0305-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0305-153">Windows Server 2003</span></span>



| <span data-ttu-id="e0305-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-154">Entry</span></span> | <span data-ttu-id="e0305-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-155">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e0305-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0305-156">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-157">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0305-158">System-Only</span></span>            | <span data-ttu-id="e0305-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-159">False</span></span>                                                         |
| <span data-ttu-id="e0305-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0305-160">Is-Single-Valued</span></span>       | <span data-ttu-id="e0305-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-161">False</span></span>                                                         |
| <span data-ttu-id="e0305-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0305-162">Is Indexed</span></span>             | <span data-ttu-id="e0305-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-163">False</span></span>                                                         |
| <span data-ttu-id="e0305-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0305-164">In Global Catalog</span></span>      | <span data-ttu-id="e0305-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-165">False</span></span>                                                         |
| <span data-ttu-id="e0305-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0305-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0305-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0305-167">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e0305-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0305-168">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0305-169">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-170">Search-Flags</span></span>           | <span data-ttu-id="e0305-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0305-171">0x00000000</span></span>                                                    |
| <span data-ttu-id="e0305-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-172">System-Flags</span></span>           | <span data-ttu-id="e0305-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0305-173">0x00000010</span></span>                                                    |
| <span data-ttu-id="e0305-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0305-174">Classes used in</span></span>        | [<span data-ttu-id="e0305-175">**RPC-Profile-элемент**</span><span class="sxs-lookup"><span data-stu-id="e0305-175">**rpc-Profile-Element**</span></span>](c-rpcprofileelement.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e0305-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e0305-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e0305-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-177">Entry</span></span> | <span data-ttu-id="e0305-178">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-178">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e0305-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0305-179">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-180">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0305-181">System-Only</span></span>            | <span data-ttu-id="e0305-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-182">False</span></span>                                                         |
| <span data-ttu-id="e0305-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0305-183">Is-Single-Valued</span></span>       | <span data-ttu-id="e0305-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-184">False</span></span>                                                         |
| <span data-ttu-id="e0305-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0305-185">Is Indexed</span></span>             | <span data-ttu-id="e0305-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-186">False</span></span>                                                         |
| <span data-ttu-id="e0305-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0305-187">In Global Catalog</span></span>      | <span data-ttu-id="e0305-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-188">False</span></span>                                                         |
| <span data-ttu-id="e0305-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0305-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0305-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0305-190">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e0305-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0305-191">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0305-192">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-193">Search-Flags</span></span>           | <span data-ttu-id="e0305-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0305-194">0x00000000</span></span>                                                    |
| <span data-ttu-id="e0305-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-195">System-Flags</span></span>           | <span data-ttu-id="e0305-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0305-196">0x00000010</span></span>                                                    |
| <span data-ttu-id="e0305-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0305-197">Classes used in</span></span>        | [<span data-ttu-id="e0305-198">**RPC-Profile-элемент**</span><span class="sxs-lookup"><span data-stu-id="e0305-198">**rpc-Profile-Element**</span></span>](c-rpcprofileelement.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e0305-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0305-199">Windows Server 2008</span></span>



| <span data-ttu-id="e0305-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-200">Entry</span></span> | <span data-ttu-id="e0305-201">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-201">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e0305-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0305-202">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-203">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0305-204">System-Only</span></span>            | <span data-ttu-id="e0305-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-205">False</span></span>                                                         |
| <span data-ttu-id="e0305-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0305-206">Is-Single-Valued</span></span>       | <span data-ttu-id="e0305-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-207">False</span></span>                                                         |
| <span data-ttu-id="e0305-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0305-208">Is Indexed</span></span>             | <span data-ttu-id="e0305-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-209">False</span></span>                                                         |
| <span data-ttu-id="e0305-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0305-210">In Global Catalog</span></span>      | <span data-ttu-id="e0305-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-211">False</span></span>                                                         |
| <span data-ttu-id="e0305-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0305-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0305-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0305-213">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e0305-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0305-214">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0305-215">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-216">Search-Flags</span></span>           | <span data-ttu-id="e0305-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0305-217">0x00000000</span></span>                                                    |
| <span data-ttu-id="e0305-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-218">System-Flags</span></span>           | <span data-ttu-id="e0305-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0305-219">0x00000010</span></span>                                                    |
| <span data-ttu-id="e0305-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0305-220">Classes used in</span></span>        | [<span data-ttu-id="e0305-221">**RPC-Profile-элемент**</span><span class="sxs-lookup"><span data-stu-id="e0305-221">**rpc-Profile-Element**</span></span>](c-rpcprofileelement.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e0305-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e0305-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e0305-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-223">Entry</span></span> | <span data-ttu-id="e0305-224">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-224">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e0305-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0305-225">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-226">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0305-227">System-Only</span></span>            | <span data-ttu-id="e0305-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-228">False</span></span>                                                         |
| <span data-ttu-id="e0305-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0305-229">Is-Single-Valued</span></span>       | <span data-ttu-id="e0305-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-230">False</span></span>                                                         |
| <span data-ttu-id="e0305-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0305-231">Is Indexed</span></span>             | <span data-ttu-id="e0305-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-232">False</span></span>                                                         |
| <span data-ttu-id="e0305-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0305-233">In Global Catalog</span></span>      | <span data-ttu-id="e0305-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-234">False</span></span>                                                         |
| <span data-ttu-id="e0305-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0305-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0305-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0305-236">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e0305-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0305-237">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0305-238">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-239">Search-Flags</span></span>           | <span data-ttu-id="e0305-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0305-240">0x00000000</span></span>                                                    |
| <span data-ttu-id="e0305-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-241">System-Flags</span></span>           | <span data-ttu-id="e0305-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0305-242">0x00000010</span></span>                                                    |
| <span data-ttu-id="e0305-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0305-243">Classes used in</span></span>        | [<span data-ttu-id="e0305-244">**RPC-Profile-элемент**</span><span class="sxs-lookup"><span data-stu-id="e0305-244">**rpc-Profile-Element**</span></span>](c-rpcprofileelement.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e0305-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0305-245">Windows Server 2012</span></span>



| <span data-ttu-id="e0305-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="e0305-246">Entry</span></span> | <span data-ttu-id="e0305-247">Значение</span><span class="sxs-lookup"><span data-stu-id="e0305-247">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e0305-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e0305-248">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e0305-249">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="e0305-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="e0305-250">System-Only</span></span>            | <span data-ttu-id="e0305-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-251">False</span></span>                                                         |
| <span data-ttu-id="e0305-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e0305-252">Is-Single-Valued</span></span>       | <span data-ttu-id="e0305-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-253">False</span></span>                                                         |
| <span data-ttu-id="e0305-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e0305-254">Is Indexed</span></span>             | <span data-ttu-id="e0305-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-255">False</span></span>                                                         |
| <span data-ttu-id="e0305-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e0305-256">In Global Catalog</span></span>      | <span data-ttu-id="e0305-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="e0305-257">False</span></span>                                                         |
| <span data-ttu-id="e0305-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e0305-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="e0305-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e0305-259">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="e0305-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e0305-260">Range-Lower</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e0305-261">Range-Upper</span></span>            | \-                                                            |
| <span data-ttu-id="e0305-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-262">Search-Flags</span></span>           | <span data-ttu-id="e0305-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e0305-263">0x00000000</span></span>                                                    |
| <span data-ttu-id="e0305-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e0305-264">System-Flags</span></span>           | <span data-ttu-id="e0305-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e0305-265">0x00000010</span></span>                                                    |
| <span data-ttu-id="e0305-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e0305-266">Classes used in</span></span>        | [<span data-ttu-id="e0305-267">**RPC-Profile-элемент**</span><span class="sxs-lookup"><span data-stu-id="e0305-267">**rpc-Profile-Element**</span></span>](c-rpcprofileelement.md)<br/> |



 

 





