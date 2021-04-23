---
title: MS-DS-вход-время-синхронизация-атрибут интервала
description: Этот атрибут определяет степень гранулярности (в днях), с которой время последнего входа пользователя или компьютера, записанное в атрибут lastLogonTimestamp, реплицируется на все контроллеры домена в домене.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Interval для службы MS-DS-logon-Time-Sync
- Схема AD атрибута msDS-ЛогонтимесинЦинтервал
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536275"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a><span data-ttu-id="8e7eb-105">MS-DS-вход-время-синхронизация-атрибут интервала</span><span class="sxs-lookup"><span data-stu-id="8e7eb-105">ms-DS-Logon-Time-Sync-Interval attribute</span></span>

<span data-ttu-id="8e7eb-106">Этот атрибут определяет степень гранулярности (в днях), с которой время последнего входа пользователя или компьютера, записанное в атрибут lastLogonTimestamp, реплицируется на все контроллеры домена в домене.</span><span class="sxs-lookup"><span data-stu-id="8e7eb-106">This attribute controls the granularity, in days, with which the last logon time for a user or computer, recorded in the lastLogonTimestamp attribute, is replicated to all DCs in a domain.</span></span>



| <span data-ttu-id="8e7eb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e7eb-107">Entry</span></span> | <span data-ttu-id="8e7eb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8e7eb-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7eb-109">CN</span><span class="sxs-lookup"><span data-stu-id="8e7eb-109">CN</span></span>                | <span data-ttu-id="8e7eb-110">MS-DS-вход в систему-время-синхронизация-интервал</span><span class="sxs-lookup"><span data-stu-id="8e7eb-110">ms-DS-Logon-Time-Sync-Interval</span></span>                                                                             |
| <span data-ttu-id="8e7eb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8e7eb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8e7eb-112">msDS-ЛогонтимесинЦинтервал</span><span class="sxs-lookup"><span data-stu-id="8e7eb-112">msDS-LogonTimeSyncInterval</span></span>                                                                                 |
| <span data-ttu-id="8e7eb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8e7eb-113">Size</span></span>              | <span data-ttu-id="8e7eb-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="8e7eb-114">4 bytes</span></span>                                                                                                    |
| <span data-ttu-id="8e7eb-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8e7eb-115">Update Privilege</span></span>  | <span data-ttu-id="8e7eb-116">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="8e7eb-116">Domain administrator</span></span>                                                                                       |
| <span data-ttu-id="8e7eb-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8e7eb-117">Update Frequency</span></span>  | <span data-ttu-id="8e7eb-118">В редких случаях, поскольку это параметр политики, он обновляется только в том случае, если требуется изменить политику на уровне домена.</span><span class="sxs-lookup"><span data-stu-id="8e7eb-118">Rarely, since this is a policy setting, it is updated only when a change in domain-wide policy is desired.</span></span> |
| <span data-ttu-id="8e7eb-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8e7eb-119">Attribute-Id</span></span>      | <span data-ttu-id="8e7eb-120">1.2.840.113556.1.4.1784</span><span class="sxs-lookup"><span data-stu-id="8e7eb-120">1.2.840.113556.1.4.1784</span></span>                                                                                    |
| <span data-ttu-id="8e7eb-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8e7eb-121">System-Id-Guid</span></span>    | <span data-ttu-id="8e7eb-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span><span class="sxs-lookup"><span data-stu-id="8e7eb-122">ad7940f8-e43a-4a42-83bc-d688e59ea605</span></span>                                                                       |
| <span data-ttu-id="8e7eb-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e7eb-123">Syntax</span></span>            | [<span data-ttu-id="8e7eb-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-124">**Enumeration**</span></span>](s-enumeration.md)                                                                       |



## <a name="implementations"></a><span data-ttu-id="8e7eb-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8e7eb-125">Implementations</span></span>

-   [<span data-ttu-id="8e7eb-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8e7eb-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8e7eb-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8e7eb-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8e7eb-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="8e7eb-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8e7eb-131">Windows Server 2003</span></span>



| <span data-ttu-id="8e7eb-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e7eb-132">Entry</span></span> | <span data-ttu-id="8e7eb-133">Значение</span><span class="sxs-lookup"><span data-stu-id="8e7eb-133">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e7eb-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e7eb-134">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e7eb-135">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e7eb-136">System-Only</span></span>            | <span data-ttu-id="8e7eb-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-137">False</span></span>                                        |
| <span data-ttu-id="8e7eb-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e7eb-138">Is-Single-Valued</span></span>       | <span data-ttu-id="8e7eb-139">True</span><span class="sxs-lookup"><span data-stu-id="8e7eb-139">True</span></span>                                         |
| <span data-ttu-id="8e7eb-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e7eb-140">Is Indexed</span></span>             | <span data-ttu-id="8e7eb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-141">False</span></span>                                        |
| <span data-ttu-id="8e7eb-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e7eb-142">In Global Catalog</span></span>      | <span data-ttu-id="8e7eb-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-143">False</span></span>                                        |
| <span data-ttu-id="8e7eb-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e7eb-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e7eb-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e7eb-145">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e7eb-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e7eb-146">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e7eb-147">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-148">Search-Flags</span></span>           | <span data-ttu-id="8e7eb-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e7eb-149">0x00000000</span></span>                                   |
| <span data-ttu-id="8e7eb-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-150">System-Flags</span></span>           | <span data-ttu-id="8e7eb-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e7eb-151">0x00000010</span></span>                                   |
| <span data-ttu-id="8e7eb-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e7eb-152">Classes used in</span></span>        | [<span data-ttu-id="8e7eb-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8e7eb-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8e7eb-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8e7eb-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e7eb-155">Entry</span></span> | <span data-ttu-id="8e7eb-156">Значение</span><span class="sxs-lookup"><span data-stu-id="8e7eb-156">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e7eb-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e7eb-157">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e7eb-158">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e7eb-159">System-Only</span></span>            | <span data-ttu-id="8e7eb-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-160">False</span></span>                                        |
| <span data-ttu-id="8e7eb-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e7eb-161">Is-Single-Valued</span></span>       | <span data-ttu-id="8e7eb-162">True</span><span class="sxs-lookup"><span data-stu-id="8e7eb-162">True</span></span>                                         |
| <span data-ttu-id="8e7eb-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e7eb-163">Is Indexed</span></span>             | <span data-ttu-id="8e7eb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-164">False</span></span>                                        |
| <span data-ttu-id="8e7eb-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e7eb-165">In Global Catalog</span></span>      | <span data-ttu-id="8e7eb-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-166">False</span></span>                                        |
| <span data-ttu-id="8e7eb-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e7eb-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e7eb-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e7eb-168">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e7eb-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e7eb-169">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e7eb-170">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-171">Search-Flags</span></span>           | <span data-ttu-id="8e7eb-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e7eb-172">0x00000000</span></span>                                   |
| <span data-ttu-id="8e7eb-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-173">System-Flags</span></span>           | <span data-ttu-id="8e7eb-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e7eb-174">0x00000010</span></span>                                   |
| <span data-ttu-id="8e7eb-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e7eb-175">Classes used in</span></span>        | [<span data-ttu-id="8e7eb-176">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-176">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8e7eb-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e7eb-177">Windows Server 2008</span></span>



| <span data-ttu-id="8e7eb-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e7eb-178">Entry</span></span> | <span data-ttu-id="8e7eb-179">Значение</span><span class="sxs-lookup"><span data-stu-id="8e7eb-179">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e7eb-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e7eb-180">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e7eb-181">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e7eb-182">System-Only</span></span>            | <span data-ttu-id="8e7eb-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-183">False</span></span>                                        |
| <span data-ttu-id="8e7eb-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e7eb-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8e7eb-185">True</span><span class="sxs-lookup"><span data-stu-id="8e7eb-185">True</span></span>                                         |
| <span data-ttu-id="8e7eb-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e7eb-186">Is Indexed</span></span>             | <span data-ttu-id="8e7eb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-187">False</span></span>                                        |
| <span data-ttu-id="8e7eb-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e7eb-188">In Global Catalog</span></span>      | <span data-ttu-id="8e7eb-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-189">False</span></span>                                        |
| <span data-ttu-id="8e7eb-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e7eb-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e7eb-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e7eb-191">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e7eb-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e7eb-192">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e7eb-193">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-194">Search-Flags</span></span>           | <span data-ttu-id="8e7eb-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e7eb-195">0x00000000</span></span>                                   |
| <span data-ttu-id="8e7eb-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-196">System-Flags</span></span>           | <span data-ttu-id="8e7eb-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e7eb-197">0x00000010</span></span>                                   |
| <span data-ttu-id="8e7eb-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e7eb-198">Classes used in</span></span>        | [<span data-ttu-id="8e7eb-199">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-199">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8e7eb-200">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8e7eb-200">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8e7eb-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e7eb-201">Entry</span></span> | <span data-ttu-id="8e7eb-202">Значение</span><span class="sxs-lookup"><span data-stu-id="8e7eb-202">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e7eb-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e7eb-203">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e7eb-204">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e7eb-205">System-Only</span></span>            | <span data-ttu-id="8e7eb-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-206">False</span></span>                                        |
| <span data-ttu-id="8e7eb-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e7eb-207">Is-Single-Valued</span></span>       | <span data-ttu-id="8e7eb-208">True</span><span class="sxs-lookup"><span data-stu-id="8e7eb-208">True</span></span>                                         |
| <span data-ttu-id="8e7eb-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e7eb-209">Is Indexed</span></span>             | <span data-ttu-id="8e7eb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-210">False</span></span>                                        |
| <span data-ttu-id="8e7eb-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e7eb-211">In Global Catalog</span></span>      | <span data-ttu-id="8e7eb-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-212">False</span></span>                                        |
| <span data-ttu-id="8e7eb-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e7eb-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e7eb-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e7eb-214">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e7eb-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e7eb-215">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e7eb-216">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-217">Search-Flags</span></span>           | <span data-ttu-id="8e7eb-218">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e7eb-218">0x00000000</span></span>                                   |
| <span data-ttu-id="8e7eb-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-219">System-Flags</span></span>           | <span data-ttu-id="8e7eb-220">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e7eb-220">0x00000010</span></span>                                   |
| <span data-ttu-id="8e7eb-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e7eb-221">Classes used in</span></span>        | [<span data-ttu-id="8e7eb-222">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-222">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8e7eb-223">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8e7eb-223">Windows Server 2012</span></span>



| <span data-ttu-id="8e7eb-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="8e7eb-224">Entry</span></span> | <span data-ttu-id="8e7eb-225">Значение</span><span class="sxs-lookup"><span data-stu-id="8e7eb-225">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="8e7eb-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8e7eb-226">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8e7eb-227">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="8e7eb-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="8e7eb-228">System-Only</span></span>            | <span data-ttu-id="8e7eb-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-229">False</span></span>                                        |
| <span data-ttu-id="8e7eb-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8e7eb-230">Is-Single-Valued</span></span>       | <span data-ttu-id="8e7eb-231">True</span><span class="sxs-lookup"><span data-stu-id="8e7eb-231">True</span></span>                                         |
| <span data-ttu-id="8e7eb-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8e7eb-232">Is Indexed</span></span>             | <span data-ttu-id="8e7eb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-233">False</span></span>                                        |
| <span data-ttu-id="8e7eb-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8e7eb-234">In Global Catalog</span></span>      | <span data-ttu-id="8e7eb-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="8e7eb-235">False</span></span>                                        |
| <span data-ttu-id="8e7eb-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8e7eb-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="8e7eb-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8e7eb-237">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="8e7eb-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8e7eb-238">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8e7eb-239">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="8e7eb-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-240">Search-Flags</span></span>           | <span data-ttu-id="8e7eb-241">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8e7eb-241">0x00000000</span></span>                                   |
| <span data-ttu-id="8e7eb-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8e7eb-242">System-Flags</span></span>           | <span data-ttu-id="8e7eb-243">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8e7eb-243">0x00000010</span></span>                                   |
| <span data-ttu-id="8e7eb-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8e7eb-244">Classes used in</span></span>        | [<span data-ttu-id="8e7eb-245">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="8e7eb-245">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





