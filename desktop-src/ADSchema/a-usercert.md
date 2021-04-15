---
title: Атрибут User-Cert
description: Nortel v1 или DMS.
ms.assetid: f0aa19ad-0599-4e38-b49b-0a24241f1a23
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута User-Cert
- Схема AD атрибута Усерцерт
topic_type:
- apiref
api_name:
- User-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a041375ba9e00539c51d1022b0f053b79c6eae1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655033"
---
# <a name="user-cert-attribute"></a><span data-ttu-id="f7720-105">Атрибут User-Cert</span><span class="sxs-lookup"><span data-stu-id="f7720-105">User-Cert attribute</span></span>

<span data-ttu-id="f7720-106">Nortel v1 или DMS.</span><span class="sxs-lookup"><span data-stu-id="f7720-106">Nortel v1 or DMS certificates.</span></span>



| <span data-ttu-id="f7720-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-107">Entry</span></span> | <span data-ttu-id="f7720-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="f7720-109">CN</span><span class="sxs-lookup"><span data-stu-id="f7720-109">CN</span></span>                | <span data-ttu-id="f7720-110">User-Cert</span><span class="sxs-lookup"><span data-stu-id="f7720-110">User-Cert</span></span>                                             |
| <span data-ttu-id="f7720-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f7720-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f7720-112">усерцерт</span><span class="sxs-lookup"><span data-stu-id="f7720-112">userCert</span></span>                                              |
| <span data-ttu-id="f7720-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f7720-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="f7720-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f7720-114">Update Privilege</span></span>  | <span data-ttu-id="f7720-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="f7720-115">This value is set by the system.</span></span>                      |
| <span data-ttu-id="f7720-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f7720-116">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="f7720-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-117">Attribute-Id</span></span>      | <span data-ttu-id="f7720-118">1.2.840.113556.1.4.645</span><span class="sxs-lookup"><span data-stu-id="f7720-118">1.2.840.113556.1.4.645</span></span>                                |
| <span data-ttu-id="f7720-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f7720-119">System-Id-Guid</span></span>    | <span data-ttu-id="f7720-120">bf967a69-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f7720-120">bf967a69-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="f7720-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7720-121">Syntax</span></span>            | [<span data-ttu-id="f7720-122">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="f7720-122">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="f7720-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f7720-123">Implementations</span></span>

-   [<span data-ttu-id="f7720-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f7720-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f7720-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f7720-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f7720-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f7720-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f7720-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f7720-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f7720-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f7720-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f7720-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f7720-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f7720-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f7720-130">Windows 2000 Server</span></span>



| <span data-ttu-id="f7720-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-131">Entry</span></span> | <span data-ttu-id="f7720-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-132">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7720-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7720-133">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7720-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-134">MAPI-Id</span></span>                | <span data-ttu-id="f7720-135">0x3A22</span><span class="sxs-lookup"><span data-stu-id="f7720-135">0x3A22</span></span>                                               |
| <span data-ttu-id="f7720-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7720-136">System-Only</span></span>            | <span data-ttu-id="f7720-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-137">False</span></span>                                                |
| <span data-ttu-id="f7720-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7720-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f7720-139">True</span><span class="sxs-lookup"><span data-stu-id="f7720-139">True</span></span>                                                 |
| <span data-ttu-id="f7720-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7720-140">Is Indexed</span></span>             | <span data-ttu-id="f7720-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-141">False</span></span>                                                |
| <span data-ttu-id="f7720-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7720-142">In Global Catalog</span></span>      | <span data-ttu-id="f7720-143">True</span><span class="sxs-lookup"><span data-stu-id="f7720-143">True</span></span>                                                 |
| <span data-ttu-id="f7720-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7720-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7720-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7720-145">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7720-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7720-146">Range-Lower</span></span>            | <span data-ttu-id="f7720-147">0</span><span class="sxs-lookup"><span data-stu-id="f7720-147">0</span></span>                                                    |
| <span data-ttu-id="f7720-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7720-148">Range-Upper</span></span>            | <span data-ttu-id="f7720-149">32767</span><span class="sxs-lookup"><span data-stu-id="f7720-149">32767</span></span>                                                |
| <span data-ttu-id="f7720-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-150">Search-Flags</span></span>           | <span data-ttu-id="f7720-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7720-151">0x00000000</span></span>                                           |
| <span data-ttu-id="f7720-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-152">System-Flags</span></span>           | <span data-ttu-id="f7720-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7720-153">0x00000010</span></span>                                           |
| <span data-ttu-id="f7720-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7720-154">Classes used in</span></span>        | [<span data-ttu-id="f7720-155">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="f7720-155">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f7720-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7720-156">Windows Server 2003</span></span>



| <span data-ttu-id="f7720-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-157">Entry</span></span> | <span data-ttu-id="f7720-158">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-158">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7720-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7720-159">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7720-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-160">MAPI-Id</span></span>                | <span data-ttu-id="f7720-161">0x3A22</span><span class="sxs-lookup"><span data-stu-id="f7720-161">0x3A22</span></span>                                               |
| <span data-ttu-id="f7720-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7720-162">System-Only</span></span>            | <span data-ttu-id="f7720-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-163">False</span></span>                                                |
| <span data-ttu-id="f7720-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7720-164">Is-Single-Valued</span></span>       | <span data-ttu-id="f7720-165">True</span><span class="sxs-lookup"><span data-stu-id="f7720-165">True</span></span>                                                 |
| <span data-ttu-id="f7720-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7720-166">Is Indexed</span></span>             | <span data-ttu-id="f7720-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-167">False</span></span>                                                |
| <span data-ttu-id="f7720-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7720-168">In Global Catalog</span></span>      | <span data-ttu-id="f7720-169">True</span><span class="sxs-lookup"><span data-stu-id="f7720-169">True</span></span>                                                 |
| <span data-ttu-id="f7720-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7720-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7720-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7720-171">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7720-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7720-172">Range-Lower</span></span>            | <span data-ttu-id="f7720-173">0</span><span class="sxs-lookup"><span data-stu-id="f7720-173">0</span></span>                                                    |
| <span data-ttu-id="f7720-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7720-174">Range-Upper</span></span>            | <span data-ttu-id="f7720-175">32767</span><span class="sxs-lookup"><span data-stu-id="f7720-175">32767</span></span>                                                |
| <span data-ttu-id="f7720-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-176">Search-Flags</span></span>           | <span data-ttu-id="f7720-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7720-177">0x00000000</span></span>                                           |
| <span data-ttu-id="f7720-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-178">System-Flags</span></span>           | <span data-ttu-id="f7720-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7720-179">0x00000010</span></span>                                           |
| <span data-ttu-id="f7720-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7720-180">Classes used in</span></span>        | [<span data-ttu-id="f7720-181">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="f7720-181">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f7720-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f7720-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f7720-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-183">Entry</span></span> | <span data-ttu-id="f7720-184">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-184">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7720-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7720-185">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7720-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-186">MAPI-Id</span></span>                | <span data-ttu-id="f7720-187">0x3A22</span><span class="sxs-lookup"><span data-stu-id="f7720-187">0x3A22</span></span>                                               |
| <span data-ttu-id="f7720-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7720-188">System-Only</span></span>            | <span data-ttu-id="f7720-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-189">False</span></span>                                                |
| <span data-ttu-id="f7720-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7720-190">Is-Single-Valued</span></span>       | <span data-ttu-id="f7720-191">True</span><span class="sxs-lookup"><span data-stu-id="f7720-191">True</span></span>                                                 |
| <span data-ttu-id="f7720-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7720-192">Is Indexed</span></span>             | <span data-ttu-id="f7720-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-193">False</span></span>                                                |
| <span data-ttu-id="f7720-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7720-194">In Global Catalog</span></span>      | <span data-ttu-id="f7720-195">True</span><span class="sxs-lookup"><span data-stu-id="f7720-195">True</span></span>                                                 |
| <span data-ttu-id="f7720-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7720-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7720-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7720-197">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7720-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7720-198">Range-Lower</span></span>            | <span data-ttu-id="f7720-199">0</span><span class="sxs-lookup"><span data-stu-id="f7720-199">0</span></span>                                                    |
| <span data-ttu-id="f7720-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7720-200">Range-Upper</span></span>            | <span data-ttu-id="f7720-201">32767</span><span class="sxs-lookup"><span data-stu-id="f7720-201">32767</span></span>                                                |
| <span data-ttu-id="f7720-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-202">Search-Flags</span></span>           | <span data-ttu-id="f7720-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7720-203">0x00000000</span></span>                                           |
| <span data-ttu-id="f7720-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-204">System-Flags</span></span>           | <span data-ttu-id="f7720-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7720-205">0x00000010</span></span>                                           |
| <span data-ttu-id="f7720-206">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7720-206">Classes used in</span></span>        | [<span data-ttu-id="f7720-207">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="f7720-207">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f7720-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7720-208">Windows Server 2008</span></span>



| <span data-ttu-id="f7720-209">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-209">Entry</span></span> | <span data-ttu-id="f7720-210">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-210">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7720-211">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7720-211">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7720-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-212">MAPI-Id</span></span>                | <span data-ttu-id="f7720-213">0x3A22</span><span class="sxs-lookup"><span data-stu-id="f7720-213">0x3A22</span></span>                                               |
| <span data-ttu-id="f7720-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7720-214">System-Only</span></span>            | <span data-ttu-id="f7720-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-215">False</span></span>                                                |
| <span data-ttu-id="f7720-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7720-216">Is-Single-Valued</span></span>       | <span data-ttu-id="f7720-217">True</span><span class="sxs-lookup"><span data-stu-id="f7720-217">True</span></span>                                                 |
| <span data-ttu-id="f7720-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7720-218">Is Indexed</span></span>             | <span data-ttu-id="f7720-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-219">False</span></span>                                                |
| <span data-ttu-id="f7720-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7720-220">In Global Catalog</span></span>      | <span data-ttu-id="f7720-221">True</span><span class="sxs-lookup"><span data-stu-id="f7720-221">True</span></span>                                                 |
| <span data-ttu-id="f7720-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7720-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7720-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7720-223">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7720-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7720-224">Range-Lower</span></span>            | <span data-ttu-id="f7720-225">0</span><span class="sxs-lookup"><span data-stu-id="f7720-225">0</span></span>                                                    |
| <span data-ttu-id="f7720-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7720-226">Range-Upper</span></span>            | <span data-ttu-id="f7720-227">32767</span><span class="sxs-lookup"><span data-stu-id="f7720-227">32767</span></span>                                                |
| <span data-ttu-id="f7720-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-228">Search-Flags</span></span>           | <span data-ttu-id="f7720-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7720-229">0x00000000</span></span>                                           |
| <span data-ttu-id="f7720-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-230">System-Flags</span></span>           | <span data-ttu-id="f7720-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7720-231">0x00000010</span></span>                                           |
| <span data-ttu-id="f7720-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7720-232">Classes used in</span></span>        | [<span data-ttu-id="f7720-233">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="f7720-233">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f7720-234">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f7720-234">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f7720-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-235">Entry</span></span> | <span data-ttu-id="f7720-236">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-236">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7720-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7720-237">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7720-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-238">MAPI-Id</span></span>                | <span data-ttu-id="f7720-239">0x3A22</span><span class="sxs-lookup"><span data-stu-id="f7720-239">0x3A22</span></span>                                               |
| <span data-ttu-id="f7720-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7720-240">System-Only</span></span>            | <span data-ttu-id="f7720-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-241">False</span></span>                                                |
| <span data-ttu-id="f7720-242">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7720-242">Is-Single-Valued</span></span>       | <span data-ttu-id="f7720-243">True</span><span class="sxs-lookup"><span data-stu-id="f7720-243">True</span></span>                                                 |
| <span data-ttu-id="f7720-244">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7720-244">Is Indexed</span></span>             | <span data-ttu-id="f7720-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-245">False</span></span>                                                |
| <span data-ttu-id="f7720-246">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7720-246">In Global Catalog</span></span>      | <span data-ttu-id="f7720-247">True</span><span class="sxs-lookup"><span data-stu-id="f7720-247">True</span></span>                                                 |
| <span data-ttu-id="f7720-248">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7720-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7720-249">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7720-249">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7720-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7720-250">Range-Lower</span></span>            | <span data-ttu-id="f7720-251">0</span><span class="sxs-lookup"><span data-stu-id="f7720-251">0</span></span>                                                    |
| <span data-ttu-id="f7720-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7720-252">Range-Upper</span></span>            | <span data-ttu-id="f7720-253">32767</span><span class="sxs-lookup"><span data-stu-id="f7720-253">32767</span></span>                                                |
| <span data-ttu-id="f7720-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-254">Search-Flags</span></span>           | <span data-ttu-id="f7720-255">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7720-255">0x00000000</span></span>                                           |
| <span data-ttu-id="f7720-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-256">System-Flags</span></span>           | <span data-ttu-id="f7720-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7720-257">0x00000010</span></span>                                           |
| <span data-ttu-id="f7720-258">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7720-258">Classes used in</span></span>        | [<span data-ttu-id="f7720-259">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="f7720-259">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f7720-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7720-260">Windows Server 2012</span></span>



| <span data-ttu-id="f7720-261">Ввод</span><span class="sxs-lookup"><span data-stu-id="f7720-261">Entry</span></span> | <span data-ttu-id="f7720-262">Значение</span><span class="sxs-lookup"><span data-stu-id="f7720-262">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="f7720-263">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f7720-263">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="f7720-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f7720-264">MAPI-Id</span></span>                | <span data-ttu-id="f7720-265">0x3A22</span><span class="sxs-lookup"><span data-stu-id="f7720-265">0x3A22</span></span>                                               |
| <span data-ttu-id="f7720-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="f7720-266">System-Only</span></span>            | <span data-ttu-id="f7720-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-267">False</span></span>                                                |
| <span data-ttu-id="f7720-268">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f7720-268">Is-Single-Valued</span></span>       | <span data-ttu-id="f7720-269">True</span><span class="sxs-lookup"><span data-stu-id="f7720-269">True</span></span>                                                 |
| <span data-ttu-id="f7720-270">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f7720-270">Is Indexed</span></span>             | <span data-ttu-id="f7720-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="f7720-271">False</span></span>                                                |
| <span data-ttu-id="f7720-272">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f7720-272">In Global Catalog</span></span>      | <span data-ttu-id="f7720-273">True</span><span class="sxs-lookup"><span data-stu-id="f7720-273">True</span></span>                                                 |
| <span data-ttu-id="f7720-274">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f7720-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="f7720-275">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f7720-275">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="f7720-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f7720-276">Range-Lower</span></span>            | <span data-ttu-id="f7720-277">0</span><span class="sxs-lookup"><span data-stu-id="f7720-277">0</span></span>                                                    |
| <span data-ttu-id="f7720-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f7720-278">Range-Upper</span></span>            | <span data-ttu-id="f7720-279">32767</span><span class="sxs-lookup"><span data-stu-id="f7720-279">32767</span></span>                                                |
| <span data-ttu-id="f7720-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-280">Search-Flags</span></span>           | <span data-ttu-id="f7720-281">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f7720-281">0x00000000</span></span>                                           |
| <span data-ttu-id="f7720-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f7720-282">System-Flags</span></span>           | <span data-ttu-id="f7720-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f7720-283">0x00000010</span></span>                                           |
| <span data-ttu-id="f7720-284">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f7720-284">Classes used in</span></span>        | [<span data-ttu-id="f7720-285">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="f7720-285">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> |



 

 





