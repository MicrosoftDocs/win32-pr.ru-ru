---
title: ACS — незарезервированный-TX — атрибут Limit
description: Максимальная пропускная способность, которую пользовательское приложение может передать, прежде чем заместить резервирование.
ms.assetid: 5ead8e5b-31e8-438e-8d1b-9aae8601dfc9
ms.tgt_platform: multiple
keywords:
- ACS — незарезервированная — схема AD для атрибута с ограничением TX
- Схема AD атрибута Акснонресерведткслимит
topic_type:
- apiref
api_name:
- ACS-Non-Reserved-Tx-Limit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999b1775640624b7825b38ae1632d70773bc75b3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654996"
---
# <a name="acs-non-reserved-tx-limit-attribute"></a><span data-ttu-id="f0d32-105">ACS — незарезервированный-TX — атрибут Limit</span><span class="sxs-lookup"><span data-stu-id="f0d32-105">ACS-Non-Reserved-Tx-Limit attribute</span></span>

<span data-ttu-id="f0d32-106">Максимальная пропускная способность, которую пользовательское приложение может передать, прежде чем заместить резервирование.</span><span class="sxs-lookup"><span data-stu-id="f0d32-106">The maximum bandwidth a user application can transmit before a reservation is in place.</span></span>



| <span data-ttu-id="f0d32-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-107">Entry</span></span> | <span data-ttu-id="f0d32-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="f0d32-109">CN</span><span class="sxs-lookup"><span data-stu-id="f0d32-109">CN</span></span>                | <span data-ttu-id="f0d32-110">ACS-не зарезервировано-TX-Limit</span><span class="sxs-lookup"><span data-stu-id="f0d32-110">ACS-Non-Reserved-Tx-Limit</span></span>            |
| <span data-ttu-id="f0d32-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f0d32-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f0d32-112">акснонресерведткслимит</span><span class="sxs-lookup"><span data-stu-id="f0d32-112">aCSNonReservedTxLimit</span></span>                |
| <span data-ttu-id="f0d32-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f0d32-113">Size</span></span>              | <span data-ttu-id="f0d32-114">8 байт</span><span class="sxs-lookup"><span data-stu-id="f0d32-114">8 bytes</span></span>                              |
| <span data-ttu-id="f0d32-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f0d32-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="f0d32-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f0d32-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="f0d32-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-117">Attribute-Id</span></span>      | <span data-ttu-id="f0d32-118">1.2.840.113556.1.4.780</span><span class="sxs-lookup"><span data-stu-id="f0d32-118">1.2.840.113556.1.4.780</span></span>               |
| <span data-ttu-id="f0d32-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f0d32-119">System-Id-Guid</span></span>    | <span data-ttu-id="f0d32-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f0d32-120">1cb355a2-56d0-11d1-a9c6-0000f80367c1</span></span> |
| <span data-ttu-id="f0d32-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0d32-121">Syntax</span></span>            | [<span data-ttu-id="f0d32-122">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="f0d32-122">**Interval**</span></span>](s-interval.md)       |



## <a name="implementations"></a><span data-ttu-id="f0d32-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f0d32-123">Implementations</span></span>

-   [<span data-ttu-id="f0d32-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f0d32-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f0d32-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0d32-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0d32-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0d32-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0d32-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0d32-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0d32-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0d32-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0d32-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0d32-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f0d32-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0d32-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f0d32-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-131">Entry</span></span> | <span data-ttu-id="f0d32-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f0d32-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0d32-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0d32-135">System-Only</span></span>            | <span data-ttu-id="f0d32-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-136">False</span></span>                                        |
| <span data-ttu-id="f0d32-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0d32-137">Is-Single-Valued</span></span>       | <span data-ttu-id="f0d32-138">True</span><span class="sxs-lookup"><span data-stu-id="f0d32-138">True</span></span>                                         |
| <span data-ttu-id="f0d32-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0d32-139">Is Indexed</span></span>             | <span data-ttu-id="f0d32-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-140">False</span></span>                                        |
| <span data-ttu-id="f0d32-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0d32-141">In Global Catalog</span></span>      | <span data-ttu-id="f0d32-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-142">False</span></span>                                        |
| <span data-ttu-id="f0d32-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0d32-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0d32-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0d32-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f0d32-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0d32-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0d32-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-147">Search-Flags</span></span>           | <span data-ttu-id="f0d32-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0d32-148">0x00000000</span></span>                                   |
| <span data-ttu-id="f0d32-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-149">System-Flags</span></span>           | <span data-ttu-id="f0d32-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0d32-150">0x00000010</span></span>                                   |
| <span data-ttu-id="f0d32-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0d32-151">Classes used in</span></span>        | [<span data-ttu-id="f0d32-152">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="f0d32-152">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f0d32-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0d32-153">Windows Server 2003</span></span>



| <span data-ttu-id="f0d32-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-154">Entry</span></span> | <span data-ttu-id="f0d32-155">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f0d32-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0d32-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0d32-158">System-Only</span></span>            | <span data-ttu-id="f0d32-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-159">False</span></span>                                        |
| <span data-ttu-id="f0d32-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0d32-160">Is-Single-Valued</span></span>       | <span data-ttu-id="f0d32-161">True</span><span class="sxs-lookup"><span data-stu-id="f0d32-161">True</span></span>                                         |
| <span data-ttu-id="f0d32-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0d32-162">Is Indexed</span></span>             | <span data-ttu-id="f0d32-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-163">False</span></span>                                        |
| <span data-ttu-id="f0d32-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0d32-164">In Global Catalog</span></span>      | <span data-ttu-id="f0d32-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-165">False</span></span>                                        |
| <span data-ttu-id="f0d32-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0d32-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0d32-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0d32-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f0d32-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0d32-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0d32-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-170">Search-Flags</span></span>           | <span data-ttu-id="f0d32-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0d32-171">0x00000000</span></span>                                   |
| <span data-ttu-id="f0d32-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-172">System-Flags</span></span>           | <span data-ttu-id="f0d32-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0d32-173">0x00000010</span></span>                                   |
| <span data-ttu-id="f0d32-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0d32-174">Classes used in</span></span>        | [<span data-ttu-id="f0d32-175">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="f0d32-175">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0d32-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0d32-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0d32-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-177">Entry</span></span> | <span data-ttu-id="f0d32-178">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f0d32-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0d32-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0d32-181">System-Only</span></span>            | <span data-ttu-id="f0d32-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-182">False</span></span>                                        |
| <span data-ttu-id="f0d32-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0d32-183">Is-Single-Valued</span></span>       | <span data-ttu-id="f0d32-184">True</span><span class="sxs-lookup"><span data-stu-id="f0d32-184">True</span></span>                                         |
| <span data-ttu-id="f0d32-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0d32-185">Is Indexed</span></span>             | <span data-ttu-id="f0d32-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-186">False</span></span>                                        |
| <span data-ttu-id="f0d32-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0d32-187">In Global Catalog</span></span>      | <span data-ttu-id="f0d32-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-188">False</span></span>                                        |
| <span data-ttu-id="f0d32-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0d32-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0d32-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0d32-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f0d32-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0d32-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0d32-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-193">Search-Flags</span></span>           | <span data-ttu-id="f0d32-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0d32-194">0x00000000</span></span>                                   |
| <span data-ttu-id="f0d32-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-195">System-Flags</span></span>           | <span data-ttu-id="f0d32-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0d32-196">0x00000010</span></span>                                   |
| <span data-ttu-id="f0d32-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0d32-197">Classes used in</span></span>        | [<span data-ttu-id="f0d32-198">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="f0d32-198">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0d32-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0d32-199">Windows Server 2008</span></span>



| <span data-ttu-id="f0d32-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-200">Entry</span></span> | <span data-ttu-id="f0d32-201">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f0d32-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0d32-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0d32-204">System-Only</span></span>            | <span data-ttu-id="f0d32-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-205">False</span></span>                                        |
| <span data-ttu-id="f0d32-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0d32-206">Is-Single-Valued</span></span>       | <span data-ttu-id="f0d32-207">True</span><span class="sxs-lookup"><span data-stu-id="f0d32-207">True</span></span>                                         |
| <span data-ttu-id="f0d32-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0d32-208">Is Indexed</span></span>             | <span data-ttu-id="f0d32-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-209">False</span></span>                                        |
| <span data-ttu-id="f0d32-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0d32-210">In Global Catalog</span></span>      | <span data-ttu-id="f0d32-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-211">False</span></span>                                        |
| <span data-ttu-id="f0d32-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0d32-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0d32-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0d32-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f0d32-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0d32-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0d32-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-216">Search-Flags</span></span>           | <span data-ttu-id="f0d32-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0d32-217">0x00000000</span></span>                                   |
| <span data-ttu-id="f0d32-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-218">System-Flags</span></span>           | <span data-ttu-id="f0d32-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0d32-219">0x00000010</span></span>                                   |
| <span data-ttu-id="f0d32-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0d32-220">Classes used in</span></span>        | [<span data-ttu-id="f0d32-221">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="f0d32-221">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0d32-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0d32-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0d32-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-223">Entry</span></span> | <span data-ttu-id="f0d32-224">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f0d32-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0d32-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0d32-227">System-Only</span></span>            | <span data-ttu-id="f0d32-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-228">False</span></span>                                        |
| <span data-ttu-id="f0d32-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0d32-229">Is-Single-Valued</span></span>       | <span data-ttu-id="f0d32-230">True</span><span class="sxs-lookup"><span data-stu-id="f0d32-230">True</span></span>                                         |
| <span data-ttu-id="f0d32-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0d32-231">Is Indexed</span></span>             | <span data-ttu-id="f0d32-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-232">False</span></span>                                        |
| <span data-ttu-id="f0d32-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0d32-233">In Global Catalog</span></span>      | <span data-ttu-id="f0d32-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-234">False</span></span>                                        |
| <span data-ttu-id="f0d32-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0d32-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0d32-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0d32-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f0d32-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0d32-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0d32-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-239">Search-Flags</span></span>           | <span data-ttu-id="f0d32-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0d32-240">0x00000000</span></span>                                   |
| <span data-ttu-id="f0d32-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-241">System-Flags</span></span>           | <span data-ttu-id="f0d32-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0d32-242">0x00000010</span></span>                                   |
| <span data-ttu-id="f0d32-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0d32-243">Classes used in</span></span>        | [<span data-ttu-id="f0d32-244">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="f0d32-244">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0d32-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0d32-245">Windows Server 2012</span></span>



| <span data-ttu-id="f0d32-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="f0d32-246">Entry</span></span> | <span data-ttu-id="f0d32-247">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d32-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="f0d32-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f0d32-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0d32-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="f0d32-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0d32-250">System-Only</span></span>            | <span data-ttu-id="f0d32-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-251">False</span></span>                                        |
| <span data-ttu-id="f0d32-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f0d32-252">Is-Single-Valued</span></span>       | <span data-ttu-id="f0d32-253">True</span><span class="sxs-lookup"><span data-stu-id="f0d32-253">True</span></span>                                         |
| <span data-ttu-id="f0d32-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f0d32-254">Is Indexed</span></span>             | <span data-ttu-id="f0d32-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-255">False</span></span>                                        |
| <span data-ttu-id="f0d32-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f0d32-256">In Global Catalog</span></span>      | <span data-ttu-id="f0d32-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="f0d32-257">False</span></span>                                        |
| <span data-ttu-id="f0d32-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f0d32-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0d32-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f0d32-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="f0d32-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0d32-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0d32-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="f0d32-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-262">Search-Flags</span></span>           | <span data-ttu-id="f0d32-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0d32-263">0x00000000</span></span>                                   |
| <span data-ttu-id="f0d32-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0d32-264">System-Flags</span></span>           | <span data-ttu-id="f0d32-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0d32-265">0x00000010</span></span>                                   |
| <span data-ttu-id="f0d32-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f0d32-266">Classes used in</span></span>        | [<span data-ttu-id="f0d32-267">**ACS — подсеть**</span><span class="sxs-lookup"><span data-stu-id="f0d32-267">**ACS-Subnet**</span></span>](c-acssubnet.md)<br/> |



 

 





