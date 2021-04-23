---
title: Атрибут короткого имени сервера
description: Пред-Windows 2000 имя сервера, совместимое с серверами печати.
ms.assetid: 639704f4-e2b6-43e1-9b1b-6afffe8f0f6a
ms.tgt_platform: multiple
keywords:
- Краткое имя-схема атрибута AD
- Схема AD атрибута Шортсервернаме
topic_type:
- apiref
api_name:
- Short-Server-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e71b7cf5687b530bf76c673187d5152089d885d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989765"
---
# <a name="short-server-name-attribute"></a><span data-ttu-id="8395e-105">Атрибут короткого имени сервера</span><span class="sxs-lookup"><span data-stu-id="8395e-105">Short-Server-Name attribute</span></span>

<span data-ttu-id="8395e-106">Пред-Windows 2000 имя сервера, совместимое с серверами печати.</span><span class="sxs-lookup"><span data-stu-id="8395e-106">Pre-Windows 2000 compatible server name for print servers.</span></span>



| <span data-ttu-id="8395e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-107">Entry</span></span> | <span data-ttu-id="8395e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8395e-109">CN</span><span class="sxs-lookup"><span data-stu-id="8395e-109">CN</span></span>                | <span data-ttu-id="8395e-110">Короткое имя сервера</span><span class="sxs-lookup"><span data-stu-id="8395e-110">Short-Server-Name</span></span>                           |
| <span data-ttu-id="8395e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8395e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8395e-112">shortServerName</span><span class="sxs-lookup"><span data-stu-id="8395e-112">shortServerName</span></span>                             |
| <span data-ttu-id="8395e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8395e-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="8395e-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8395e-114">Update Privilege</span></span>  | <span data-ttu-id="8395e-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="8395e-115">Domain administrator</span></span>                        |
| <span data-ttu-id="8395e-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8395e-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8395e-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-117">Attribute-Id</span></span>      | <span data-ttu-id="8395e-118">1.2.840.113556.1.4.1209</span><span class="sxs-lookup"><span data-stu-id="8395e-118">1.2.840.113556.1.4.1209</span></span>                     |
| <span data-ttu-id="8395e-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8395e-119">System-Id-Guid</span></span>    | <span data-ttu-id="8395e-120">45b01501-c419-11d1-bbc9-0080c76670c0</span><span class="sxs-lookup"><span data-stu-id="8395e-120">45b01501-c419-11d1-bbc9-0080c76670c0</span></span>        |
| <span data-ttu-id="8395e-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8395e-121">Syntax</span></span>            | [<span data-ttu-id="8395e-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8395e-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8395e-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8395e-123">Implementations</span></span>

-   [<span data-ttu-id="8395e-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8395e-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8395e-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8395e-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8395e-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8395e-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8395e-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8395e-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8395e-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8395e-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8395e-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8395e-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8395e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8395e-130">Windows 2000 Server</span></span>



| <span data-ttu-id="8395e-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-131">Entry</span></span> | <span data-ttu-id="8395e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-132">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="8395e-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8395e-133">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-134">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="8395e-135">System-Only</span></span>            | <span data-ttu-id="8395e-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-136">False</span></span>                                          |
| <span data-ttu-id="8395e-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8395e-137">Is-Single-Valued</span></span>       | <span data-ttu-id="8395e-138">True</span><span class="sxs-lookup"><span data-stu-id="8395e-138">True</span></span>                                           |
| <span data-ttu-id="8395e-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8395e-139">Is Indexed</span></span>             | <span data-ttu-id="8395e-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-140">False</span></span>                                          |
| <span data-ttu-id="8395e-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8395e-141">In Global Catalog</span></span>      | <span data-ttu-id="8395e-142">True</span><span class="sxs-lookup"><span data-stu-id="8395e-142">True</span></span>                                           |
| <span data-ttu-id="8395e-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8395e-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="8395e-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8395e-144">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="8395e-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8395e-145">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="8395e-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8395e-146">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="8395e-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-147">Search-Flags</span></span>           | <span data-ttu-id="8395e-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8395e-148">0x00000000</span></span>                                     |
| <span data-ttu-id="8395e-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-149">System-Flags</span></span>           | <span data-ttu-id="8395e-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8395e-150">0x00000010</span></span>                                     |
| <span data-ttu-id="8395e-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8395e-151">Classes used in</span></span>        | [<span data-ttu-id="8395e-152">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="8395e-152">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8395e-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8395e-153">Windows Server 2003</span></span>



| <span data-ttu-id="8395e-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-154">Entry</span></span> | <span data-ttu-id="8395e-155">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-155">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="8395e-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8395e-156">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-157">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8395e-158">System-Only</span></span>            | <span data-ttu-id="8395e-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-159">False</span></span>                                          |
| <span data-ttu-id="8395e-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8395e-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8395e-161">True</span><span class="sxs-lookup"><span data-stu-id="8395e-161">True</span></span>                                           |
| <span data-ttu-id="8395e-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8395e-162">Is Indexed</span></span>             | <span data-ttu-id="8395e-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-163">False</span></span>                                          |
| <span data-ttu-id="8395e-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8395e-164">In Global Catalog</span></span>      | <span data-ttu-id="8395e-165">True</span><span class="sxs-lookup"><span data-stu-id="8395e-165">True</span></span>                                           |
| <span data-ttu-id="8395e-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8395e-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8395e-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8395e-167">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="8395e-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8395e-168">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="8395e-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8395e-169">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="8395e-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-170">Search-Flags</span></span>           | <span data-ttu-id="8395e-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8395e-171">0x00000000</span></span>                                     |
| <span data-ttu-id="8395e-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-172">System-Flags</span></span>           | <span data-ttu-id="8395e-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8395e-173">0x00000010</span></span>                                     |
| <span data-ttu-id="8395e-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8395e-174">Classes used in</span></span>        | [<span data-ttu-id="8395e-175">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="8395e-175">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8395e-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8395e-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8395e-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-177">Entry</span></span> | <span data-ttu-id="8395e-178">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-178">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="8395e-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8395e-179">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-180">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="8395e-181">System-Only</span></span>            | <span data-ttu-id="8395e-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-182">False</span></span>                                          |
| <span data-ttu-id="8395e-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8395e-183">Is-Single-Valued</span></span>       | <span data-ttu-id="8395e-184">True</span><span class="sxs-lookup"><span data-stu-id="8395e-184">True</span></span>                                           |
| <span data-ttu-id="8395e-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8395e-185">Is Indexed</span></span>             | <span data-ttu-id="8395e-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-186">False</span></span>                                          |
| <span data-ttu-id="8395e-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8395e-187">In Global Catalog</span></span>      | <span data-ttu-id="8395e-188">True</span><span class="sxs-lookup"><span data-stu-id="8395e-188">True</span></span>                                           |
| <span data-ttu-id="8395e-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8395e-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="8395e-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8395e-190">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="8395e-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8395e-191">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="8395e-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8395e-192">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="8395e-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-193">Search-Flags</span></span>           | <span data-ttu-id="8395e-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8395e-194">0x00000000</span></span>                                     |
| <span data-ttu-id="8395e-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-195">System-Flags</span></span>           | <span data-ttu-id="8395e-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8395e-196">0x00000010</span></span>                                     |
| <span data-ttu-id="8395e-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8395e-197">Classes used in</span></span>        | [<span data-ttu-id="8395e-198">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="8395e-198">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8395e-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8395e-199">Windows Server 2008</span></span>



| <span data-ttu-id="8395e-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-200">Entry</span></span> | <span data-ttu-id="8395e-201">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-201">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="8395e-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8395e-202">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-203">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="8395e-204">System-Only</span></span>            | <span data-ttu-id="8395e-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-205">False</span></span>                                          |
| <span data-ttu-id="8395e-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8395e-206">Is-Single-Valued</span></span>       | <span data-ttu-id="8395e-207">True</span><span class="sxs-lookup"><span data-stu-id="8395e-207">True</span></span>                                           |
| <span data-ttu-id="8395e-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8395e-208">Is Indexed</span></span>             | <span data-ttu-id="8395e-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-209">False</span></span>                                          |
| <span data-ttu-id="8395e-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8395e-210">In Global Catalog</span></span>      | <span data-ttu-id="8395e-211">True</span><span class="sxs-lookup"><span data-stu-id="8395e-211">True</span></span>                                           |
| <span data-ttu-id="8395e-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8395e-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="8395e-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8395e-213">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="8395e-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8395e-214">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="8395e-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8395e-215">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="8395e-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-216">Search-Flags</span></span>           | <span data-ttu-id="8395e-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8395e-217">0x00000000</span></span>                                     |
| <span data-ttu-id="8395e-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-218">System-Flags</span></span>           | <span data-ttu-id="8395e-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8395e-219">0x00000010</span></span>                                     |
| <span data-ttu-id="8395e-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8395e-220">Classes used in</span></span>        | [<span data-ttu-id="8395e-221">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="8395e-221">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8395e-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8395e-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8395e-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-223">Entry</span></span> | <span data-ttu-id="8395e-224">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-224">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="8395e-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8395e-225">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-226">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="8395e-227">System-Only</span></span>            | <span data-ttu-id="8395e-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-228">False</span></span>                                          |
| <span data-ttu-id="8395e-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8395e-229">Is-Single-Valued</span></span>       | <span data-ttu-id="8395e-230">True</span><span class="sxs-lookup"><span data-stu-id="8395e-230">True</span></span>                                           |
| <span data-ttu-id="8395e-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8395e-231">Is Indexed</span></span>             | <span data-ttu-id="8395e-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-232">False</span></span>                                          |
| <span data-ttu-id="8395e-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8395e-233">In Global Catalog</span></span>      | <span data-ttu-id="8395e-234">True</span><span class="sxs-lookup"><span data-stu-id="8395e-234">True</span></span>                                           |
| <span data-ttu-id="8395e-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8395e-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="8395e-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8395e-236">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="8395e-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8395e-237">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="8395e-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8395e-238">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="8395e-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-239">Search-Flags</span></span>           | <span data-ttu-id="8395e-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8395e-240">0x00000000</span></span>                                     |
| <span data-ttu-id="8395e-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-241">System-Flags</span></span>           | <span data-ttu-id="8395e-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8395e-242">0x00000010</span></span>                                     |
| <span data-ttu-id="8395e-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8395e-243">Classes used in</span></span>        | [<span data-ttu-id="8395e-244">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="8395e-244">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8395e-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8395e-245">Windows Server 2012</span></span>



| <span data-ttu-id="8395e-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="8395e-246">Entry</span></span> | <span data-ttu-id="8395e-247">Значение</span><span class="sxs-lookup"><span data-stu-id="8395e-247">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="8395e-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8395e-248">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8395e-249">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="8395e-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="8395e-250">System-Only</span></span>            | <span data-ttu-id="8395e-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-251">False</span></span>                                          |
| <span data-ttu-id="8395e-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8395e-252">Is-Single-Valued</span></span>       | <span data-ttu-id="8395e-253">True</span><span class="sxs-lookup"><span data-stu-id="8395e-253">True</span></span>                                           |
| <span data-ttu-id="8395e-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8395e-254">Is Indexed</span></span>             | <span data-ttu-id="8395e-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="8395e-255">False</span></span>                                          |
| <span data-ttu-id="8395e-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8395e-256">In Global Catalog</span></span>      | <span data-ttu-id="8395e-257">True</span><span class="sxs-lookup"><span data-stu-id="8395e-257">True</span></span>                                           |
| <span data-ttu-id="8395e-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8395e-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="8395e-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8395e-259">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="8395e-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8395e-260">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="8395e-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8395e-261">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="8395e-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-262">Search-Flags</span></span>           | <span data-ttu-id="8395e-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8395e-263">0x00000000</span></span>                                     |
| <span data-ttu-id="8395e-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8395e-264">System-Flags</span></span>           | <span data-ttu-id="8395e-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8395e-265">0x00000010</span></span>                                     |
| <span data-ttu-id="8395e-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8395e-266">Classes used in</span></span>        | [<span data-ttu-id="8395e-267">**Очередь печати**</span><span class="sxs-lookup"><span data-stu-id="8395e-267">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





