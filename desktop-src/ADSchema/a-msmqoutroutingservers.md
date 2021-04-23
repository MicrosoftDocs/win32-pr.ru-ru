---
title: Атрибут MSMQ-out-Routing-Servers
description: DN-ссылки на серверы маршрутизации MSMQ, через которые должен маршрутизироваться весь исходящий трафик этого компьютера.
ms.assetid: 169558e4-d2a6-4555-bc5f-7e6a89e51789
ms.tgt_platform: multiple
keywords:
- MSMQ-out-Routing-схема AD атрибутов серверов
- Схема AD атрибута Мсмкаутраутингсерверс
topic_type:
- apiref
api_name:
- MSMQ-Out-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc2265b2d809b7a73cd19faace87473552471a3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893442"
---
# <a name="msmq-out-routing-servers-attribute"></a><span data-ttu-id="21820-105">Атрибут MSMQ-out-Routing-Servers</span><span class="sxs-lookup"><span data-stu-id="21820-105">MSMQ-Out-Routing-Servers attribute</span></span>

<span data-ttu-id="21820-106">DN-ссылки на серверы маршрутизации MSMQ, через которые должен маршрутизироваться весь исходящий трафик этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="21820-106">DN links to MSMQ routing servers through which all outgoing traffic for this computer should be routed.</span></span>



| <span data-ttu-id="21820-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-107">Entry</span></span> | <span data-ttu-id="21820-108">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="21820-109">CN</span><span class="sxs-lookup"><span data-stu-id="21820-109">CN</span></span>                | <span data-ttu-id="21820-110">MSMQ-out-Routing-Servers</span><span class="sxs-lookup"><span data-stu-id="21820-110">MSMQ-Out-Routing-Servers</span></span>                |
| <span data-ttu-id="21820-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="21820-111">Ldap-Display-Name</span></span> | <span data-ttu-id="21820-112">мсмкаутраутингсерверс</span><span class="sxs-lookup"><span data-stu-id="21820-112">mSMQOutRoutingServers</span></span>                   |
| <span data-ttu-id="21820-113">Размер</span><span class="sxs-lookup"><span data-stu-id="21820-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="21820-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="21820-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="21820-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="21820-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="21820-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="21820-116">Attribute-Id</span></span>      | <span data-ttu-id="21820-117">1.2.840.113556.1.4.928</span><span class="sxs-lookup"><span data-stu-id="21820-117">1.2.840.113556.1.4.928</span></span>                  |
| <span data-ttu-id="21820-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="21820-118">System-Id-Guid</span></span>    | <span data-ttu-id="21820-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="21820-119">9a0dc32b-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="21820-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21820-120">Syntax</span></span>            | [<span data-ttu-id="21820-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="21820-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="21820-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="21820-122">Implementations</span></span>

-   [<span data-ttu-id="21820-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="21820-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="21820-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="21820-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="21820-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="21820-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="21820-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="21820-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="21820-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="21820-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="21820-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="21820-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="21820-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="21820-129">Windows 2000 Server</span></span>



| <span data-ttu-id="21820-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-130">Entry</span></span> | <span data-ttu-id="21820-131">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="21820-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21820-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21820-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="21820-134">System-Only</span></span>            | <span data-ttu-id="21820-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-135">False</span></span>                                                        |
| <span data-ttu-id="21820-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21820-136">Is-Single-Valued</span></span>       | <span data-ttu-id="21820-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-137">False</span></span>                                                        |
| <span data-ttu-id="21820-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21820-138">Is Indexed</span></span>             | <span data-ttu-id="21820-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-139">False</span></span>                                                        |
| <span data-ttu-id="21820-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21820-140">In Global Catalog</span></span>      | <span data-ttu-id="21820-141">True</span><span class="sxs-lookup"><span data-stu-id="21820-141">True</span></span>                                                         |
| <span data-ttu-id="21820-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21820-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="21820-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21820-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="21820-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21820-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="21820-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21820-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="21820-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-146">Search-Flags</span></span>           | <span data-ttu-id="21820-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21820-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="21820-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-148">System-Flags</span></span>           | <span data-ttu-id="21820-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21820-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="21820-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21820-150">Classes used in</span></span>        | [<span data-ttu-id="21820-151">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="21820-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="21820-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="21820-152">Windows Server 2003</span></span>



| <span data-ttu-id="21820-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-153">Entry</span></span> | <span data-ttu-id="21820-154">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="21820-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21820-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21820-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="21820-157">System-Only</span></span>            | <span data-ttu-id="21820-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-158">False</span></span>                                                        |
| <span data-ttu-id="21820-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21820-159">Is-Single-Valued</span></span>       | <span data-ttu-id="21820-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-160">False</span></span>                                                        |
| <span data-ttu-id="21820-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21820-161">Is Indexed</span></span>             | <span data-ttu-id="21820-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-162">False</span></span>                                                        |
| <span data-ttu-id="21820-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21820-163">In Global Catalog</span></span>      | <span data-ttu-id="21820-164">True</span><span class="sxs-lookup"><span data-stu-id="21820-164">True</span></span>                                                         |
| <span data-ttu-id="21820-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21820-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="21820-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21820-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="21820-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21820-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="21820-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21820-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="21820-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-169">Search-Flags</span></span>           | <span data-ttu-id="21820-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21820-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="21820-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-171">System-Flags</span></span>           | <span data-ttu-id="21820-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21820-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="21820-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21820-173">Classes used in</span></span>        | [<span data-ttu-id="21820-174">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="21820-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="21820-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="21820-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="21820-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-176">Entry</span></span> | <span data-ttu-id="21820-177">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="21820-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21820-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21820-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="21820-180">System-Only</span></span>            | <span data-ttu-id="21820-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-181">False</span></span>                                                        |
| <span data-ttu-id="21820-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21820-182">Is-Single-Valued</span></span>       | <span data-ttu-id="21820-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-183">False</span></span>                                                        |
| <span data-ttu-id="21820-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21820-184">Is Indexed</span></span>             | <span data-ttu-id="21820-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-185">False</span></span>                                                        |
| <span data-ttu-id="21820-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21820-186">In Global Catalog</span></span>      | <span data-ttu-id="21820-187">True</span><span class="sxs-lookup"><span data-stu-id="21820-187">True</span></span>                                                         |
| <span data-ttu-id="21820-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21820-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="21820-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21820-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="21820-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21820-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="21820-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21820-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="21820-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-192">Search-Flags</span></span>           | <span data-ttu-id="21820-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21820-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="21820-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-194">System-Flags</span></span>           | <span data-ttu-id="21820-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21820-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="21820-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21820-196">Classes used in</span></span>        | [<span data-ttu-id="21820-197">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="21820-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="21820-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21820-198">Windows Server 2008</span></span>



| <span data-ttu-id="21820-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-199">Entry</span></span> | <span data-ttu-id="21820-200">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="21820-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21820-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21820-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="21820-203">System-Only</span></span>            | <span data-ttu-id="21820-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-204">False</span></span>                                                        |
| <span data-ttu-id="21820-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21820-205">Is-Single-Valued</span></span>       | <span data-ttu-id="21820-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-206">False</span></span>                                                        |
| <span data-ttu-id="21820-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21820-207">Is Indexed</span></span>             | <span data-ttu-id="21820-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-208">False</span></span>                                                        |
| <span data-ttu-id="21820-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21820-209">In Global Catalog</span></span>      | <span data-ttu-id="21820-210">True</span><span class="sxs-lookup"><span data-stu-id="21820-210">True</span></span>                                                         |
| <span data-ttu-id="21820-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21820-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="21820-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21820-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="21820-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21820-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="21820-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21820-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="21820-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-215">Search-Flags</span></span>           | <span data-ttu-id="21820-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21820-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="21820-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-217">System-Flags</span></span>           | <span data-ttu-id="21820-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21820-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="21820-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21820-219">Classes used in</span></span>        | [<span data-ttu-id="21820-220">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="21820-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="21820-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21820-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="21820-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-222">Entry</span></span> | <span data-ttu-id="21820-223">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="21820-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21820-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21820-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="21820-226">System-Only</span></span>            | <span data-ttu-id="21820-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-227">False</span></span>                                                        |
| <span data-ttu-id="21820-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21820-228">Is-Single-Valued</span></span>       | <span data-ttu-id="21820-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-229">False</span></span>                                                        |
| <span data-ttu-id="21820-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21820-230">Is Indexed</span></span>             | <span data-ttu-id="21820-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-231">False</span></span>                                                        |
| <span data-ttu-id="21820-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21820-232">In Global Catalog</span></span>      | <span data-ttu-id="21820-233">True</span><span class="sxs-lookup"><span data-stu-id="21820-233">True</span></span>                                                         |
| <span data-ttu-id="21820-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21820-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="21820-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21820-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="21820-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21820-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="21820-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21820-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="21820-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-238">Search-Flags</span></span>           | <span data-ttu-id="21820-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21820-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="21820-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-240">System-Flags</span></span>           | <span data-ttu-id="21820-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21820-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="21820-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21820-242">Classes used in</span></span>        | [<span data-ttu-id="21820-243">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="21820-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="21820-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="21820-244">Windows Server 2012</span></span>



| <span data-ttu-id="21820-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="21820-245">Entry</span></span> | <span data-ttu-id="21820-246">Значение</span><span class="sxs-lookup"><span data-stu-id="21820-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="21820-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="21820-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="21820-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="21820-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="21820-249">System-Only</span></span>            | <span data-ttu-id="21820-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-250">False</span></span>                                                        |
| <span data-ttu-id="21820-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="21820-251">Is-Single-Valued</span></span>       | <span data-ttu-id="21820-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-252">False</span></span>                                                        |
| <span data-ttu-id="21820-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="21820-253">Is Indexed</span></span>             | <span data-ttu-id="21820-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="21820-254">False</span></span>                                                        |
| <span data-ttu-id="21820-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="21820-255">In Global Catalog</span></span>      | <span data-ttu-id="21820-256">True</span><span class="sxs-lookup"><span data-stu-id="21820-256">True</span></span>                                                         |
| <span data-ttu-id="21820-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="21820-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="21820-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="21820-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="21820-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="21820-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="21820-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="21820-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="21820-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-261">Search-Flags</span></span>           | <span data-ttu-id="21820-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="21820-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="21820-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="21820-263">System-Flags</span></span>           | <span data-ttu-id="21820-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="21820-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="21820-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="21820-265">Classes used in</span></span>        | [<span data-ttu-id="21820-266">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="21820-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





