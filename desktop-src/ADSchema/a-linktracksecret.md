---
title: Link-Track-секретный атрибут
description: Этот атрибут хранит ссылку на секретный ключ, который позволяет преобразовать зашифрованный файл в обычный текст.
ms.assetid: e476f4af-71a8-4bd9-a81d-f825bfbf267b
ms.tgt_platform: multiple
keywords:
- Схема ссылки — секретный атрибут Active Directory
- Схема AD атрибута Линктракксекрет
topic_type:
- apiref
api_name:
- Link-Track-Secret
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb172ec0985acc7c93c62796881c369c7ad0b82
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654942"
---
# <a name="link-track-secret-attribute"></a><span data-ttu-id="b1948-105">Link-Track-секретный атрибут</span><span class="sxs-lookup"><span data-stu-id="b1948-105">Link-Track-Secret attribute</span></span>

<span data-ttu-id="b1948-106">Этот атрибут хранит ссылку на секретный ключ, который позволяет преобразовать зашифрованный файл в обычный текст.</span><span class="sxs-lookup"><span data-stu-id="b1948-106">This attribute stores a link to a secret key that allows an encrypted file to be translated to plaintext.</span></span>



| <span data-ttu-id="b1948-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-107">Entry</span></span> | <span data-ttu-id="b1948-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b1948-109">CN</span><span class="sxs-lookup"><span data-stu-id="b1948-109">CN</span></span>                | <span data-ttu-id="b1948-110">Направление связи — секрет</span><span class="sxs-lookup"><span data-stu-id="b1948-110">Link-Track-Secret</span></span>                                     |
| <span data-ttu-id="b1948-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b1948-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b1948-112">линктракксекрет</span><span class="sxs-lookup"><span data-stu-id="b1948-112">linkTrackSecret</span></span>                                       |
| <span data-ttu-id="b1948-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b1948-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b1948-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b1948-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b1948-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b1948-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b1948-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-116">Attribute-Id</span></span>      | <span data-ttu-id="b1948-117">1.2.840.113556.1.4.269</span><span class="sxs-lookup"><span data-stu-id="b1948-117">1.2.840.113556.1.4.269</span></span>                                |
| <span data-ttu-id="b1948-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b1948-118">System-Id-Guid</span></span>    | <span data-ttu-id="b1948-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="b1948-119">2ae80fe2-47b4-11d0-a1a4-00c04fd930c9</span></span>                  |
| <span data-ttu-id="b1948-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1948-120">Syntax</span></span>            | [<span data-ttu-id="b1948-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="b1948-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b1948-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b1948-122">Implementations</span></span>

-   [<span data-ttu-id="b1948-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b1948-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b1948-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b1948-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b1948-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b1948-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b1948-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b1948-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b1948-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b1948-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b1948-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b1948-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b1948-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1948-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b1948-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-130">Entry</span></span> | <span data-ttu-id="b1948-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-131">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1948-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1948-132">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-133">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1948-134">System-Only</span></span>            | <span data-ttu-id="b1948-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-135">False</span></span>                                                          |
| <span data-ttu-id="b1948-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1948-136">Is-Single-Valued</span></span>       | <span data-ttu-id="b1948-137">True</span><span class="sxs-lookup"><span data-stu-id="b1948-137">True</span></span>                                                           |
| <span data-ttu-id="b1948-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1948-138">Is Indexed</span></span>             | <span data-ttu-id="b1948-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-139">False</span></span>                                                          |
| <span data-ttu-id="b1948-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1948-140">In Global Catalog</span></span>      | <span data-ttu-id="b1948-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-141">False</span></span>                                                          |
| <span data-ttu-id="b1948-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1948-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1948-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1948-143">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b1948-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1948-144">Range-Lower</span></span>            | <span data-ttu-id="b1948-145">0</span><span class="sxs-lookup"><span data-stu-id="b1948-145">0</span></span>                                                              |
| <span data-ttu-id="b1948-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1948-146">Range-Upper</span></span>            | <span data-ttu-id="b1948-147">16</span><span class="sxs-lookup"><span data-stu-id="b1948-147">16</span></span>                                                             |
| <span data-ttu-id="b1948-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-148">Search-Flags</span></span>           | <span data-ttu-id="b1948-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1948-149">0x00000000</span></span>                                                     |
| <span data-ttu-id="b1948-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-150">System-Flags</span></span>           | <span data-ttu-id="b1948-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1948-151">0x00000010</span></span>                                                     |
| <span data-ttu-id="b1948-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1948-152">Classes used in</span></span>        | [<span data-ttu-id="b1948-153">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="b1948-153">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b1948-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b1948-154">Windows Server 2003</span></span>



| <span data-ttu-id="b1948-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-155">Entry</span></span> | <span data-ttu-id="b1948-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-156">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1948-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1948-157">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-158">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1948-159">System-Only</span></span>            | <span data-ttu-id="b1948-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-160">False</span></span>                                                          |
| <span data-ttu-id="b1948-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1948-161">Is-Single-Valued</span></span>       | <span data-ttu-id="b1948-162">True</span><span class="sxs-lookup"><span data-stu-id="b1948-162">True</span></span>                                                           |
| <span data-ttu-id="b1948-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1948-163">Is Indexed</span></span>             | <span data-ttu-id="b1948-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-164">False</span></span>                                                          |
| <span data-ttu-id="b1948-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1948-165">In Global Catalog</span></span>      | <span data-ttu-id="b1948-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-166">False</span></span>                                                          |
| <span data-ttu-id="b1948-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1948-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1948-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1948-168">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b1948-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1948-169">Range-Lower</span></span>            | <span data-ttu-id="b1948-170">0</span><span class="sxs-lookup"><span data-stu-id="b1948-170">0</span></span>                                                              |
| <span data-ttu-id="b1948-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1948-171">Range-Upper</span></span>            | <span data-ttu-id="b1948-172">16</span><span class="sxs-lookup"><span data-stu-id="b1948-172">16</span></span>                                                             |
| <span data-ttu-id="b1948-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-173">Search-Flags</span></span>           | <span data-ttu-id="b1948-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1948-174">0x00000000</span></span>                                                     |
| <span data-ttu-id="b1948-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-175">System-Flags</span></span>           | <span data-ttu-id="b1948-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1948-176">0x00000010</span></span>                                                     |
| <span data-ttu-id="b1948-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1948-177">Classes used in</span></span>        | [<span data-ttu-id="b1948-178">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="b1948-178">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b1948-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b1948-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b1948-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-180">Entry</span></span> | <span data-ttu-id="b1948-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-181">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1948-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1948-182">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-183">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1948-184">System-Only</span></span>            | <span data-ttu-id="b1948-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-185">False</span></span>                                                          |
| <span data-ttu-id="b1948-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1948-186">Is-Single-Valued</span></span>       | <span data-ttu-id="b1948-187">True</span><span class="sxs-lookup"><span data-stu-id="b1948-187">True</span></span>                                                           |
| <span data-ttu-id="b1948-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1948-188">Is Indexed</span></span>             | <span data-ttu-id="b1948-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-189">False</span></span>                                                          |
| <span data-ttu-id="b1948-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1948-190">In Global Catalog</span></span>      | <span data-ttu-id="b1948-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-191">False</span></span>                                                          |
| <span data-ttu-id="b1948-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1948-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1948-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1948-193">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b1948-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1948-194">Range-Lower</span></span>            | <span data-ttu-id="b1948-195">0</span><span class="sxs-lookup"><span data-stu-id="b1948-195">0</span></span>                                                              |
| <span data-ttu-id="b1948-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1948-196">Range-Upper</span></span>            | <span data-ttu-id="b1948-197">16</span><span class="sxs-lookup"><span data-stu-id="b1948-197">16</span></span>                                                             |
| <span data-ttu-id="b1948-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-198">Search-Flags</span></span>           | <span data-ttu-id="b1948-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1948-199">0x00000000</span></span>                                                     |
| <span data-ttu-id="b1948-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-200">System-Flags</span></span>           | <span data-ttu-id="b1948-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1948-201">0x00000010</span></span>                                                     |
| <span data-ttu-id="b1948-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1948-202">Classes used in</span></span>        | [<span data-ttu-id="b1948-203">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="b1948-203">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b1948-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1948-204">Windows Server 2008</span></span>



| <span data-ttu-id="b1948-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-205">Entry</span></span> | <span data-ttu-id="b1948-206">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-206">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1948-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1948-207">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-208">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1948-209">System-Only</span></span>            | <span data-ttu-id="b1948-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-210">False</span></span>                                                          |
| <span data-ttu-id="b1948-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1948-211">Is-Single-Valued</span></span>       | <span data-ttu-id="b1948-212">True</span><span class="sxs-lookup"><span data-stu-id="b1948-212">True</span></span>                                                           |
| <span data-ttu-id="b1948-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1948-213">Is Indexed</span></span>             | <span data-ttu-id="b1948-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-214">False</span></span>                                                          |
| <span data-ttu-id="b1948-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1948-215">In Global Catalog</span></span>      | <span data-ttu-id="b1948-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-216">False</span></span>                                                          |
| <span data-ttu-id="b1948-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1948-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1948-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1948-218">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b1948-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1948-219">Range-Lower</span></span>            | <span data-ttu-id="b1948-220">0</span><span class="sxs-lookup"><span data-stu-id="b1948-220">0</span></span>                                                              |
| <span data-ttu-id="b1948-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1948-221">Range-Upper</span></span>            | <span data-ttu-id="b1948-222">16</span><span class="sxs-lookup"><span data-stu-id="b1948-222">16</span></span>                                                             |
| <span data-ttu-id="b1948-223">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-223">Search-Flags</span></span>           | <span data-ttu-id="b1948-224">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1948-224">0x00000000</span></span>                                                     |
| <span data-ttu-id="b1948-225">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-225">System-Flags</span></span>           | <span data-ttu-id="b1948-226">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1948-226">0x00000010</span></span>                                                     |
| <span data-ttu-id="b1948-227">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1948-227">Classes used in</span></span>        | [<span data-ttu-id="b1948-228">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="b1948-228">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b1948-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1948-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b1948-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-230">Entry</span></span> | <span data-ttu-id="b1948-231">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-231">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1948-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1948-232">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-233">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1948-234">System-Only</span></span>            | <span data-ttu-id="b1948-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-235">False</span></span>                                                          |
| <span data-ttu-id="b1948-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1948-236">Is-Single-Valued</span></span>       | <span data-ttu-id="b1948-237">True</span><span class="sxs-lookup"><span data-stu-id="b1948-237">True</span></span>                                                           |
| <span data-ttu-id="b1948-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1948-238">Is Indexed</span></span>             | <span data-ttu-id="b1948-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-239">False</span></span>                                                          |
| <span data-ttu-id="b1948-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1948-240">In Global Catalog</span></span>      | <span data-ttu-id="b1948-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-241">False</span></span>                                                          |
| <span data-ttu-id="b1948-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1948-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1948-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1948-243">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b1948-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1948-244">Range-Lower</span></span>            | <span data-ttu-id="b1948-245">0</span><span class="sxs-lookup"><span data-stu-id="b1948-245">0</span></span>                                                              |
| <span data-ttu-id="b1948-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1948-246">Range-Upper</span></span>            | <span data-ttu-id="b1948-247">16</span><span class="sxs-lookup"><span data-stu-id="b1948-247">16</span></span>                                                             |
| <span data-ttu-id="b1948-248">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-248">Search-Flags</span></span>           | <span data-ttu-id="b1948-249">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1948-249">0x00000000</span></span>                                                     |
| <span data-ttu-id="b1948-250">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-250">System-Flags</span></span>           | <span data-ttu-id="b1948-251">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1948-251">0x00000010</span></span>                                                     |
| <span data-ttu-id="b1948-252">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1948-252">Classes used in</span></span>        | [<span data-ttu-id="b1948-253">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="b1948-253">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b1948-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b1948-254">Windows Server 2012</span></span>



| <span data-ttu-id="b1948-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1948-255">Entry</span></span> | <span data-ttu-id="b1948-256">Значение</span><span class="sxs-lookup"><span data-stu-id="b1948-256">Value</span></span> |
|------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1948-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b1948-257">Link-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b1948-258">MAPI-Id</span></span>                | \-                                                             |
| <span data-ttu-id="b1948-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="b1948-259">System-Only</span></span>            | <span data-ttu-id="b1948-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-260">False</span></span>                                                          |
| <span data-ttu-id="b1948-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b1948-261">Is-Single-Valued</span></span>       | <span data-ttu-id="b1948-262">True</span><span class="sxs-lookup"><span data-stu-id="b1948-262">True</span></span>                                                           |
| <span data-ttu-id="b1948-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b1948-263">Is Indexed</span></span>             | <span data-ttu-id="b1948-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-264">False</span></span>                                                          |
| <span data-ttu-id="b1948-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b1948-265">In Global Catalog</span></span>      | <span data-ttu-id="b1948-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="b1948-266">False</span></span>                                                          |
| <span data-ttu-id="b1948-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b1948-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="b1948-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b1948-268">O:BAG:BAD:S:</span></span>                                                   |
| <span data-ttu-id="b1948-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b1948-269">Range-Lower</span></span>            | <span data-ttu-id="b1948-270">0</span><span class="sxs-lookup"><span data-stu-id="b1948-270">0</span></span>                                                              |
| <span data-ttu-id="b1948-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b1948-271">Range-Upper</span></span>            | <span data-ttu-id="b1948-272">16</span><span class="sxs-lookup"><span data-stu-id="b1948-272">16</span></span>                                                             |
| <span data-ttu-id="b1948-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-273">Search-Flags</span></span>           | <span data-ttu-id="b1948-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1948-274">0x00000000</span></span>                                                     |
| <span data-ttu-id="b1948-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b1948-275">System-Flags</span></span>           | <span data-ttu-id="b1948-276">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1948-276">0x00000010</span></span>                                                     |
| <span data-ttu-id="b1948-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b1948-277">Classes used in</span></span>        | [<span data-ttu-id="b1948-278">**Link-Track-Vol-запись**</span><span class="sxs-lookup"><span data-stu-id="b1948-278">**Link-Track-Vol-Entry**</span></span>](c-linktrackvolentry.md)<br/> |



 

 





