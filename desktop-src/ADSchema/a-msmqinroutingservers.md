---
title: Атрибут MSMQ-in-Routing-Servers
description: DN-ссылки на серверы маршрутизации MSMQ, через которые должен маршрутизироваться весь входящий трафик к этому компьютеру.
ms.assetid: a54d79a7-52f2-49ac-b23f-c3365a1f6921
ms.tgt_platform: multiple
keywords:
- MSMQ-in-Routing-схема AD атрибутов серверов
- Схема AD атрибута Мсмкинраутингсерверс
topic_type:
- apiref
api_name:
- MSMQ-In-Routing-Servers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46bd9f21552362ad4dceb5110af84b09bb096d5c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655396"
---
# <a name="msmq-in-routing-servers-attribute"></a><span data-ttu-id="7e35c-105">Атрибут MSMQ-in-Routing-Servers</span><span class="sxs-lookup"><span data-stu-id="7e35c-105">MSMQ-In-Routing-Servers attribute</span></span>

<span data-ttu-id="7e35c-106">DN-ссылки на серверы маршрутизации MSMQ, через которые должен маршрутизироваться весь входящий трафик к этому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="7e35c-106">DN links to MSMQ routing servers through which all incoming traffic to this computer should be routed.</span></span>



| <span data-ttu-id="7e35c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-107">Entry</span></span> | <span data-ttu-id="7e35c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="7e35c-109">CN</span><span class="sxs-lookup"><span data-stu-id="7e35c-109">CN</span></span>                | <span data-ttu-id="7e35c-110">MSMQ-in-Routing-серверы</span><span class="sxs-lookup"><span data-stu-id="7e35c-110">MSMQ-In-Routing-Servers</span></span>                 |
| <span data-ttu-id="7e35c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="7e35c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="7e35c-112">мсмкинраутингсерверс</span><span class="sxs-lookup"><span data-stu-id="7e35c-112">mSMQInRoutingServers</span></span>                    |
| <span data-ttu-id="7e35c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="7e35c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="7e35c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="7e35c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="7e35c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="7e35c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="7e35c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-116">Attribute-Id</span></span>      | <span data-ttu-id="7e35c-117">1.2.840.113556.1.4.929</span><span class="sxs-lookup"><span data-stu-id="7e35c-117">1.2.840.113556.1.4.929</span></span>                  |
| <span data-ttu-id="7e35c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="7e35c-118">System-Id-Guid</span></span>    | <span data-ttu-id="7e35c-119">9a0dc32c-c100-11d1-bbc5-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="7e35c-119">9a0dc32c-c100-11d1-bbc5-0080c76670c0</span></span>    |
| <span data-ttu-id="7e35c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e35c-120">Syntax</span></span>            | [<span data-ttu-id="7e35c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="7e35c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="7e35c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="7e35c-122">Implementations</span></span>

-   [<span data-ttu-id="7e35c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="7e35c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="7e35c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7e35c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="7e35c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="7e35c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="7e35c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="7e35c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="7e35c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="7e35c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="7e35c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="7e35c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="7e35c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7e35c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="7e35c-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-130">Entry</span></span> | <span data-ttu-id="7e35c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-131">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e35c-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e35c-132">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-133">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e35c-134">System-Only</span></span>            | <span data-ttu-id="7e35c-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-135">False</span></span>                                                        |
| <span data-ttu-id="7e35c-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e35c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="7e35c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-137">False</span></span>                                                        |
| <span data-ttu-id="7e35c-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e35c-138">Is Indexed</span></span>             | <span data-ttu-id="7e35c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-139">False</span></span>                                                        |
| <span data-ttu-id="7e35c-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e35c-140">In Global Catalog</span></span>      | <span data-ttu-id="7e35c-141">True</span><span class="sxs-lookup"><span data-stu-id="7e35c-141">True</span></span>                                                         |
| <span data-ttu-id="7e35c-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e35c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e35c-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e35c-143">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e35c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e35c-144">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e35c-145">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-146">Search-Flags</span></span>           | <span data-ttu-id="7e35c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e35c-147">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e35c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-148">System-Flags</span></span>           | <span data-ttu-id="7e35c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e35c-149">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e35c-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e35c-150">Classes used in</span></span>        | [<span data-ttu-id="7e35c-151">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="7e35c-151">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="7e35c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7e35c-152">Windows Server 2003</span></span>



| <span data-ttu-id="7e35c-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-153">Entry</span></span> | <span data-ttu-id="7e35c-154">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-154">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e35c-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e35c-155">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-156">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e35c-157">System-Only</span></span>            | <span data-ttu-id="7e35c-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-158">False</span></span>                                                        |
| <span data-ttu-id="7e35c-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e35c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="7e35c-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-160">False</span></span>                                                        |
| <span data-ttu-id="7e35c-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e35c-161">Is Indexed</span></span>             | <span data-ttu-id="7e35c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-162">False</span></span>                                                        |
| <span data-ttu-id="7e35c-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e35c-163">In Global Catalog</span></span>      | <span data-ttu-id="7e35c-164">True</span><span class="sxs-lookup"><span data-stu-id="7e35c-164">True</span></span>                                                         |
| <span data-ttu-id="7e35c-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e35c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e35c-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e35c-166">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e35c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e35c-167">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e35c-168">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-169">Search-Flags</span></span>           | <span data-ttu-id="7e35c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e35c-170">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e35c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-171">System-Flags</span></span>           | <span data-ttu-id="7e35c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e35c-172">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e35c-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e35c-173">Classes used in</span></span>        | [<span data-ttu-id="7e35c-174">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="7e35c-174">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="7e35c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="7e35c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="7e35c-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-176">Entry</span></span> | <span data-ttu-id="7e35c-177">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-177">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e35c-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e35c-178">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-179">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e35c-180">System-Only</span></span>            | <span data-ttu-id="7e35c-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-181">False</span></span>                                                        |
| <span data-ttu-id="7e35c-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e35c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="7e35c-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-183">False</span></span>                                                        |
| <span data-ttu-id="7e35c-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e35c-184">Is Indexed</span></span>             | <span data-ttu-id="7e35c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-185">False</span></span>                                                        |
| <span data-ttu-id="7e35c-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e35c-186">In Global Catalog</span></span>      | <span data-ttu-id="7e35c-187">True</span><span class="sxs-lookup"><span data-stu-id="7e35c-187">True</span></span>                                                         |
| <span data-ttu-id="7e35c-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e35c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e35c-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e35c-189">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e35c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e35c-190">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e35c-191">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-192">Search-Flags</span></span>           | <span data-ttu-id="7e35c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e35c-193">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e35c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-194">System-Flags</span></span>           | <span data-ttu-id="7e35c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e35c-195">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e35c-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e35c-196">Classes used in</span></span>        | [<span data-ttu-id="7e35c-197">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="7e35c-197">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="7e35c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e35c-198">Windows Server 2008</span></span>



| <span data-ttu-id="7e35c-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-199">Entry</span></span> | <span data-ttu-id="7e35c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-200">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e35c-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e35c-201">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-202">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e35c-203">System-Only</span></span>            | <span data-ttu-id="7e35c-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-204">False</span></span>                                                        |
| <span data-ttu-id="7e35c-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e35c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="7e35c-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-206">False</span></span>                                                        |
| <span data-ttu-id="7e35c-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e35c-207">Is Indexed</span></span>             | <span data-ttu-id="7e35c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-208">False</span></span>                                                        |
| <span data-ttu-id="7e35c-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e35c-209">In Global Catalog</span></span>      | <span data-ttu-id="7e35c-210">True</span><span class="sxs-lookup"><span data-stu-id="7e35c-210">True</span></span>                                                         |
| <span data-ttu-id="7e35c-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e35c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e35c-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e35c-212">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e35c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e35c-213">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e35c-214">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-215">Search-Flags</span></span>           | <span data-ttu-id="7e35c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e35c-216">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e35c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-217">System-Flags</span></span>           | <span data-ttu-id="7e35c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e35c-218">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e35c-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e35c-219">Classes used in</span></span>        | [<span data-ttu-id="7e35c-220">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="7e35c-220">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="7e35c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7e35c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="7e35c-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-222">Entry</span></span> | <span data-ttu-id="7e35c-223">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-223">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e35c-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e35c-224">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-225">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e35c-226">System-Only</span></span>            | <span data-ttu-id="7e35c-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-227">False</span></span>                                                        |
| <span data-ttu-id="7e35c-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e35c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="7e35c-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-229">False</span></span>                                                        |
| <span data-ttu-id="7e35c-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e35c-230">Is Indexed</span></span>             | <span data-ttu-id="7e35c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-231">False</span></span>                                                        |
| <span data-ttu-id="7e35c-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e35c-232">In Global Catalog</span></span>      | <span data-ttu-id="7e35c-233">True</span><span class="sxs-lookup"><span data-stu-id="7e35c-233">True</span></span>                                                         |
| <span data-ttu-id="7e35c-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e35c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e35c-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e35c-235">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e35c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e35c-236">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e35c-237">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-238">Search-Flags</span></span>           | <span data-ttu-id="7e35c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e35c-239">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e35c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-240">System-Flags</span></span>           | <span data-ttu-id="7e35c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e35c-241">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e35c-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e35c-242">Classes used in</span></span>        | [<span data-ttu-id="7e35c-243">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="7e35c-243">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="7e35c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7e35c-244">Windows Server 2012</span></span>



| <span data-ttu-id="7e35c-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="7e35c-245">Entry</span></span> | <span data-ttu-id="7e35c-246">Значение</span><span class="sxs-lookup"><span data-stu-id="7e35c-246">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="7e35c-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="7e35c-247">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="7e35c-248">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="7e35c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="7e35c-249">System-Only</span></span>            | <span data-ttu-id="7e35c-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-250">False</span></span>                                                        |
| <span data-ttu-id="7e35c-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="7e35c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="7e35c-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-252">False</span></span>                                                        |
| <span data-ttu-id="7e35c-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="7e35c-253">Is Indexed</span></span>             | <span data-ttu-id="7e35c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="7e35c-254">False</span></span>                                                        |
| <span data-ttu-id="7e35c-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="7e35c-255">In Global Catalog</span></span>      | <span data-ttu-id="7e35c-256">True</span><span class="sxs-lookup"><span data-stu-id="7e35c-256">True</span></span>                                                         |
| <span data-ttu-id="7e35c-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="7e35c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="7e35c-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="7e35c-258">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="7e35c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="7e35c-259">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="7e35c-260">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="7e35c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-261">Search-Flags</span></span>           | <span data-ttu-id="7e35c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7e35c-262">0x00000000</span></span>                                                   |
| <span data-ttu-id="7e35c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="7e35c-263">System-Flags</span></span>           | <span data-ttu-id="7e35c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7e35c-264">0x00000010</span></span>                                                   |
| <span data-ttu-id="7e35c-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="7e35c-265">Classes used in</span></span>        | [<span data-ttu-id="7e35c-266">**Конфигурация MSMQ**</span><span class="sxs-lookup"><span data-stu-id="7e35c-266">**MSMQ-Configuration**</span></span>](c-msmqconfiguration.md)<br/> |



 

 





