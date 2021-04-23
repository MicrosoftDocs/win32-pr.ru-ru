---
title: Отношение доверия — атрибут POSIX-offset
description: Смещение переносимого интерфейса операционной системы (POSIX) для доверенного домена.
ms.assetid: a1263f9f-1577-44b8-b7cc-317a8ecb37f1
ms.tgt_platform: multiple
keywords:
- Отношение доверия-схема AD атрибута-смещения POSIX
- Схема AD атрибута Трустпосиксоффсет
topic_type:
- apiref
api_name:
- Trust-Posix-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8f3dca090d44ea545dcc290b04d99131d50dc7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072096"
---
# <a name="trust-posix-offset-attribute"></a><span data-ttu-id="01ede-105">Отношение доверия — атрибут POSIX-offset</span><span class="sxs-lookup"><span data-stu-id="01ede-105">Trust-Posix-Offset attribute</span></span>

<span data-ttu-id="01ede-106">Смещение переносимого интерфейса операционной системы (POSIX) для доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="01ede-106">The Portable Operating System Interface (POSIX) offset for the trusted domain.</span></span>



| <span data-ttu-id="01ede-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-107">Entry</span></span> | <span data-ttu-id="01ede-108">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="01ede-109">CN</span><span class="sxs-lookup"><span data-stu-id="01ede-109">CN</span></span>                | <span data-ttu-id="01ede-110">Отношение доверия-POSIX-offset</span><span class="sxs-lookup"><span data-stu-id="01ede-110">Trust-Posix-Offset</span></span>                   |
| <span data-ttu-id="01ede-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="01ede-111">Ldap-Display-Name</span></span> | <span data-ttu-id="01ede-112">трустпосиксоффсет</span><span class="sxs-lookup"><span data-stu-id="01ede-112">trustPosixOffset</span></span>                     |
| <span data-ttu-id="01ede-113">Размер</span><span class="sxs-lookup"><span data-stu-id="01ede-113">Size</span></span>              | <span data-ttu-id="01ede-114">4 байта</span><span class="sxs-lookup"><span data-stu-id="01ede-114">4 bytes</span></span>                              |
| <span data-ttu-id="01ede-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="01ede-115">Update Privilege</span></span>  | <span data-ttu-id="01ede-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="01ede-116">This value is set by the system.</span></span>     |
| <span data-ttu-id="01ede-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="01ede-117">Update Frequency</span></span>  | <span data-ttu-id="01ede-118">При создании нового доверия.</span><span class="sxs-lookup"><span data-stu-id="01ede-118">When a new trust is created.</span></span>         |
| <span data-ttu-id="01ede-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-119">Attribute-Id</span></span>      | <span data-ttu-id="01ede-120">1.2.840.113556.1.4.134</span><span class="sxs-lookup"><span data-stu-id="01ede-120">1.2.840.113556.1.4.134</span></span>               |
| <span data-ttu-id="01ede-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="01ede-121">System-Id-Guid</span></span>    | <span data-ttu-id="01ede-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="01ede-122">bf967a5e-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="01ede-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01ede-123">Syntax</span></span>            | [<span data-ttu-id="01ede-124">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="01ede-124">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="01ede-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="01ede-125">Implementations</span></span>

-   [<span data-ttu-id="01ede-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="01ede-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="01ede-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="01ede-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="01ede-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="01ede-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="01ede-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="01ede-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="01ede-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="01ede-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="01ede-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="01ede-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="01ede-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="01ede-132">Windows 2000 Server</span></span>



| <span data-ttu-id="01ede-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-133">Entry</span></span> | <span data-ttu-id="01ede-134">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-134">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="01ede-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01ede-135">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-136">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="01ede-137">System-Only</span></span>            | <span data-ttu-id="01ede-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-138">False</span></span>                                                |
| <span data-ttu-id="01ede-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01ede-139">Is-Single-Valued</span></span>       | <span data-ttu-id="01ede-140">True</span><span class="sxs-lookup"><span data-stu-id="01ede-140">True</span></span>                                                 |
| <span data-ttu-id="01ede-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01ede-141">Is Indexed</span></span>             | <span data-ttu-id="01ede-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-142">False</span></span>                                                |
| <span data-ttu-id="01ede-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01ede-143">In Global Catalog</span></span>      | <span data-ttu-id="01ede-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-144">False</span></span>                                                |
| <span data-ttu-id="01ede-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01ede-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="01ede-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01ede-146">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="01ede-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01ede-147">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01ede-148">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-149">Search-Flags</span></span>           | <span data-ttu-id="01ede-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01ede-150">0x00000000</span></span>                                           |
| <span data-ttu-id="01ede-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-151">System-Flags</span></span>           | <span data-ttu-id="01ede-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01ede-152">0x00000010</span></span>                                           |
| <span data-ttu-id="01ede-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01ede-153">Classes used in</span></span>        | [<span data-ttu-id="01ede-154">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="01ede-154">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="01ede-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01ede-155">Windows Server 2003</span></span>



| <span data-ttu-id="01ede-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-156">Entry</span></span> | <span data-ttu-id="01ede-157">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-157">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="01ede-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01ede-158">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-159">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="01ede-160">System-Only</span></span>            | <span data-ttu-id="01ede-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-161">False</span></span>                                                |
| <span data-ttu-id="01ede-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01ede-162">Is-Single-Valued</span></span>       | <span data-ttu-id="01ede-163">True</span><span class="sxs-lookup"><span data-stu-id="01ede-163">True</span></span>                                                 |
| <span data-ttu-id="01ede-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01ede-164">Is Indexed</span></span>             | <span data-ttu-id="01ede-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-165">False</span></span>                                                |
| <span data-ttu-id="01ede-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01ede-166">In Global Catalog</span></span>      | <span data-ttu-id="01ede-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-167">False</span></span>                                                |
| <span data-ttu-id="01ede-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01ede-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="01ede-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01ede-169">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="01ede-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01ede-170">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01ede-171">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-172">Search-Flags</span></span>           | <span data-ttu-id="01ede-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01ede-173">0x00000000</span></span>                                           |
| <span data-ttu-id="01ede-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-174">System-Flags</span></span>           | <span data-ttu-id="01ede-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01ede-175">0x00000010</span></span>                                           |
| <span data-ttu-id="01ede-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01ede-176">Classes used in</span></span>        | [<span data-ttu-id="01ede-177">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="01ede-177">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="01ede-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="01ede-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="01ede-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-179">Entry</span></span> | <span data-ttu-id="01ede-180">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-180">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="01ede-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01ede-181">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-182">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="01ede-183">System-Only</span></span>            | <span data-ttu-id="01ede-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-184">False</span></span>                                                |
| <span data-ttu-id="01ede-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01ede-185">Is-Single-Valued</span></span>       | <span data-ttu-id="01ede-186">True</span><span class="sxs-lookup"><span data-stu-id="01ede-186">True</span></span>                                                 |
| <span data-ttu-id="01ede-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01ede-187">Is Indexed</span></span>             | <span data-ttu-id="01ede-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-188">False</span></span>                                                |
| <span data-ttu-id="01ede-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01ede-189">In Global Catalog</span></span>      | <span data-ttu-id="01ede-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-190">False</span></span>                                                |
| <span data-ttu-id="01ede-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01ede-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="01ede-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01ede-192">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="01ede-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01ede-193">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01ede-194">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-195">Search-Flags</span></span>           | <span data-ttu-id="01ede-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01ede-196">0x00000000</span></span>                                           |
| <span data-ttu-id="01ede-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-197">System-Flags</span></span>           | <span data-ttu-id="01ede-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01ede-198">0x00000010</span></span>                                           |
| <span data-ttu-id="01ede-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01ede-199">Classes used in</span></span>        | [<span data-ttu-id="01ede-200">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="01ede-200">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="01ede-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01ede-201">Windows Server 2008</span></span>



| <span data-ttu-id="01ede-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-202">Entry</span></span> | <span data-ttu-id="01ede-203">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-203">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="01ede-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01ede-204">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-205">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="01ede-206">System-Only</span></span>            | <span data-ttu-id="01ede-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-207">False</span></span>                                                |
| <span data-ttu-id="01ede-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01ede-208">Is-Single-Valued</span></span>       | <span data-ttu-id="01ede-209">True</span><span class="sxs-lookup"><span data-stu-id="01ede-209">True</span></span>                                                 |
| <span data-ttu-id="01ede-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01ede-210">Is Indexed</span></span>             | <span data-ttu-id="01ede-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-211">False</span></span>                                                |
| <span data-ttu-id="01ede-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01ede-212">In Global Catalog</span></span>      | <span data-ttu-id="01ede-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-213">False</span></span>                                                |
| <span data-ttu-id="01ede-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01ede-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="01ede-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01ede-215">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="01ede-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01ede-216">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01ede-217">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-218">Search-Flags</span></span>           | <span data-ttu-id="01ede-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01ede-219">0x00000000</span></span>                                           |
| <span data-ttu-id="01ede-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-220">System-Flags</span></span>           | <span data-ttu-id="01ede-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01ede-221">0x00000010</span></span>                                           |
| <span data-ttu-id="01ede-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01ede-222">Classes used in</span></span>        | [<span data-ttu-id="01ede-223">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="01ede-223">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="01ede-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01ede-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="01ede-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-225">Entry</span></span> | <span data-ttu-id="01ede-226">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-226">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="01ede-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01ede-227">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-228">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="01ede-229">System-Only</span></span>            | <span data-ttu-id="01ede-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-230">False</span></span>                                                |
| <span data-ttu-id="01ede-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01ede-231">Is-Single-Valued</span></span>       | <span data-ttu-id="01ede-232">True</span><span class="sxs-lookup"><span data-stu-id="01ede-232">True</span></span>                                                 |
| <span data-ttu-id="01ede-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01ede-233">Is Indexed</span></span>             | <span data-ttu-id="01ede-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-234">False</span></span>                                                |
| <span data-ttu-id="01ede-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01ede-235">In Global Catalog</span></span>      | <span data-ttu-id="01ede-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-236">False</span></span>                                                |
| <span data-ttu-id="01ede-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01ede-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="01ede-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01ede-238">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="01ede-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01ede-239">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01ede-240">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-241">Search-Flags</span></span>           | <span data-ttu-id="01ede-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01ede-242">0x00000000</span></span>                                           |
| <span data-ttu-id="01ede-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-243">System-Flags</span></span>           | <span data-ttu-id="01ede-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01ede-244">0x00000010</span></span>                                           |
| <span data-ttu-id="01ede-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01ede-245">Classes used in</span></span>        | [<span data-ttu-id="01ede-246">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="01ede-246">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="01ede-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="01ede-247">Windows Server 2012</span></span>



| <span data-ttu-id="01ede-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="01ede-248">Entry</span></span> | <span data-ttu-id="01ede-249">Значение</span><span class="sxs-lookup"><span data-stu-id="01ede-249">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="01ede-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="01ede-250">Link-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="01ede-251">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="01ede-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="01ede-252">System-Only</span></span>            | <span data-ttu-id="01ede-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-253">False</span></span>                                                |
| <span data-ttu-id="01ede-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="01ede-254">Is-Single-Valued</span></span>       | <span data-ttu-id="01ede-255">True</span><span class="sxs-lookup"><span data-stu-id="01ede-255">True</span></span>                                                 |
| <span data-ttu-id="01ede-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="01ede-256">Is Indexed</span></span>             | <span data-ttu-id="01ede-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-257">False</span></span>                                                |
| <span data-ttu-id="01ede-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="01ede-258">In Global Catalog</span></span>      | <span data-ttu-id="01ede-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="01ede-259">False</span></span>                                                |
| <span data-ttu-id="01ede-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="01ede-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="01ede-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="01ede-261">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="01ede-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="01ede-262">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="01ede-263">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="01ede-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-264">Search-Flags</span></span>           | <span data-ttu-id="01ede-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="01ede-265">0x00000000</span></span>                                           |
| <span data-ttu-id="01ede-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="01ede-266">System-Flags</span></span>           | <span data-ttu-id="01ede-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="01ede-267">0x00000010</span></span>                                           |
| <span data-ttu-id="01ede-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="01ede-268">Classes used in</span></span>        | [<span data-ttu-id="01ede-269">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="01ede-269">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





