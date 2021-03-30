---
title: Атрибут Netboot-Initialization
description: Путь загрузки по умолчанию для бездисковой загрузки.
ms.assetid: 359f9fff-1630-4c47-9221-1a2cc6249567
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Netboot-Initialization
- Схема AD атрибута Нетбутинитиализатион
topic_type:
- apiref
api_name:
- Netboot-Initialization
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4232d57b38e87386b340810f5edea47f2e409c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804589"
---
# <a name="netboot-initialization-attribute"></a><span data-ttu-id="2b11f-105">Атрибут Netboot-Initialization</span><span class="sxs-lookup"><span data-stu-id="2b11f-105">Netboot-Initialization attribute</span></span>

<span data-ttu-id="2b11f-106">Путь загрузки по умолчанию для бездисковой загрузки.</span><span class="sxs-lookup"><span data-stu-id="2b11f-106">Default boot path for diskless boot.</span></span>



| <span data-ttu-id="2b11f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-107">Entry</span></span> | <span data-ttu-id="2b11f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="2b11f-109">CN</span><span class="sxs-lookup"><span data-stu-id="2b11f-109">CN</span></span>                | <span data-ttu-id="2b11f-110">Netboot-Initialization</span><span class="sxs-lookup"><span data-stu-id="2b11f-110">Netboot-Initialization</span></span>                      |
| <span data-ttu-id="2b11f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2b11f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2b11f-112">нетбутинитиализатион</span><span class="sxs-lookup"><span data-stu-id="2b11f-112">netbootInitialization</span></span>                       |
| <span data-ttu-id="2b11f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2b11f-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="2b11f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2b11f-114">Update Privilege</span></span>  | <span data-ttu-id="2b11f-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="2b11f-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="2b11f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2b11f-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="2b11f-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-117">Attribute-Id</span></span>      | <span data-ttu-id="2b11f-118">1.2.840.113556.1.4.358</span><span class="sxs-lookup"><span data-stu-id="2b11f-118">1.2.840.113556.1.4.358</span></span>                      |
| <span data-ttu-id="2b11f-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2b11f-119">System-Id-Guid</span></span>    | <span data-ttu-id="2b11f-120">3e978920-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="2b11f-120">3e978920-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="2b11f-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b11f-121">Syntax</span></span>            | [<span data-ttu-id="2b11f-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2b11f-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="2b11f-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2b11f-123">Implementations</span></span>

-   [<span data-ttu-id="2b11f-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2b11f-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2b11f-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2b11f-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2b11f-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2b11f-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2b11f-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2b11f-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2b11f-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2b11f-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2b11f-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2b11f-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2b11f-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b11f-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2b11f-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-131">Entry</span></span> | <span data-ttu-id="2b11f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-132">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2b11f-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b11f-133">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-134">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b11f-135">System-Only</span></span>            | <span data-ttu-id="2b11f-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-136">False</span></span>                                     |
| <span data-ttu-id="2b11f-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b11f-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2b11f-138">True</span><span class="sxs-lookup"><span data-stu-id="2b11f-138">True</span></span>                                      |
| <span data-ttu-id="2b11f-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b11f-139">Is Indexed</span></span>             | <span data-ttu-id="2b11f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-140">False</span></span>                                     |
| <span data-ttu-id="2b11f-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b11f-141">In Global Catalog</span></span>      | <span data-ttu-id="2b11f-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-142">False</span></span>                                     |
| <span data-ttu-id="2b11f-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b11f-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b11f-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b11f-144">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="2b11f-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b11f-145">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b11f-146">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-147">Search-Flags</span></span>           | <span data-ttu-id="2b11f-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b11f-148">0x00000000</span></span>                                |
| <span data-ttu-id="2b11f-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-149">System-Flags</span></span>           | <span data-ttu-id="2b11f-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b11f-150">0x00000010</span></span>                                |
| <span data-ttu-id="2b11f-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b11f-151">Classes used in</span></span>        | [<span data-ttu-id="2b11f-152">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="2b11f-152">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2b11f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2b11f-153">Windows Server 2003</span></span>



| <span data-ttu-id="2b11f-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-154">Entry</span></span> | <span data-ttu-id="2b11f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-155">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2b11f-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b11f-156">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-157">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b11f-158">System-Only</span></span>            | <span data-ttu-id="2b11f-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-159">False</span></span>                                     |
| <span data-ttu-id="2b11f-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b11f-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2b11f-161">True</span><span class="sxs-lookup"><span data-stu-id="2b11f-161">True</span></span>                                      |
| <span data-ttu-id="2b11f-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b11f-162">Is Indexed</span></span>             | <span data-ttu-id="2b11f-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-163">False</span></span>                                     |
| <span data-ttu-id="2b11f-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b11f-164">In Global Catalog</span></span>      | <span data-ttu-id="2b11f-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-165">False</span></span>                                     |
| <span data-ttu-id="2b11f-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b11f-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b11f-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b11f-167">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="2b11f-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b11f-168">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b11f-169">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-170">Search-Flags</span></span>           | <span data-ttu-id="2b11f-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b11f-171">0x00000000</span></span>                                |
| <span data-ttu-id="2b11f-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-172">System-Flags</span></span>           | <span data-ttu-id="2b11f-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b11f-173">0x00000010</span></span>                                |
| <span data-ttu-id="2b11f-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b11f-174">Classes used in</span></span>        | [<span data-ttu-id="2b11f-175">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="2b11f-175">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2b11f-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2b11f-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2b11f-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-177">Entry</span></span> | <span data-ttu-id="2b11f-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-178">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2b11f-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b11f-179">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-180">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b11f-181">System-Only</span></span>            | <span data-ttu-id="2b11f-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-182">False</span></span>                                     |
| <span data-ttu-id="2b11f-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b11f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2b11f-184">True</span><span class="sxs-lookup"><span data-stu-id="2b11f-184">True</span></span>                                      |
| <span data-ttu-id="2b11f-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b11f-185">Is Indexed</span></span>             | <span data-ttu-id="2b11f-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-186">False</span></span>                                     |
| <span data-ttu-id="2b11f-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b11f-187">In Global Catalog</span></span>      | <span data-ttu-id="2b11f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-188">False</span></span>                                     |
| <span data-ttu-id="2b11f-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b11f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b11f-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b11f-190">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="2b11f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b11f-191">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b11f-192">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-193">Search-Flags</span></span>           | <span data-ttu-id="2b11f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b11f-194">0x00000000</span></span>                                |
| <span data-ttu-id="2b11f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-195">System-Flags</span></span>           | <span data-ttu-id="2b11f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b11f-196">0x00000010</span></span>                                |
| <span data-ttu-id="2b11f-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b11f-197">Classes used in</span></span>        | [<span data-ttu-id="2b11f-198">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="2b11f-198">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2b11f-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b11f-199">Windows Server 2008</span></span>



| <span data-ttu-id="2b11f-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-200">Entry</span></span> | <span data-ttu-id="2b11f-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-201">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2b11f-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b11f-202">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-203">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b11f-204">System-Only</span></span>            | <span data-ttu-id="2b11f-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-205">False</span></span>                                     |
| <span data-ttu-id="2b11f-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b11f-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2b11f-207">True</span><span class="sxs-lookup"><span data-stu-id="2b11f-207">True</span></span>                                      |
| <span data-ttu-id="2b11f-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b11f-208">Is Indexed</span></span>             | <span data-ttu-id="2b11f-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-209">False</span></span>                                     |
| <span data-ttu-id="2b11f-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b11f-210">In Global Catalog</span></span>      | <span data-ttu-id="2b11f-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-211">False</span></span>                                     |
| <span data-ttu-id="2b11f-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b11f-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b11f-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b11f-213">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="2b11f-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b11f-214">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b11f-215">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-216">Search-Flags</span></span>           | <span data-ttu-id="2b11f-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b11f-217">0x00000000</span></span>                                |
| <span data-ttu-id="2b11f-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-218">System-Flags</span></span>           | <span data-ttu-id="2b11f-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b11f-219">0x00000010</span></span>                                |
| <span data-ttu-id="2b11f-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b11f-220">Classes used in</span></span>        | [<span data-ttu-id="2b11f-221">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="2b11f-221">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2b11f-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2b11f-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2b11f-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-223">Entry</span></span> | <span data-ttu-id="2b11f-224">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-224">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2b11f-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b11f-225">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-226">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b11f-227">System-Only</span></span>            | <span data-ttu-id="2b11f-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-228">False</span></span>                                     |
| <span data-ttu-id="2b11f-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b11f-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2b11f-230">True</span><span class="sxs-lookup"><span data-stu-id="2b11f-230">True</span></span>                                      |
| <span data-ttu-id="2b11f-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b11f-231">Is Indexed</span></span>             | <span data-ttu-id="2b11f-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-232">False</span></span>                                     |
| <span data-ttu-id="2b11f-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b11f-233">In Global Catalog</span></span>      | <span data-ttu-id="2b11f-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-234">False</span></span>                                     |
| <span data-ttu-id="2b11f-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b11f-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b11f-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b11f-236">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="2b11f-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b11f-237">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b11f-238">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-239">Search-Flags</span></span>           | <span data-ttu-id="2b11f-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b11f-240">0x00000000</span></span>                                |
| <span data-ttu-id="2b11f-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-241">System-Flags</span></span>           | <span data-ttu-id="2b11f-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b11f-242">0x00000010</span></span>                                |
| <span data-ttu-id="2b11f-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b11f-243">Classes used in</span></span>        | [<span data-ttu-id="2b11f-244">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="2b11f-244">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2b11f-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b11f-245">Windows Server 2012</span></span>



| <span data-ttu-id="2b11f-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="2b11f-246">Entry</span></span> | <span data-ttu-id="2b11f-247">Значение</span><span class="sxs-lookup"><span data-stu-id="2b11f-247">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="2b11f-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2b11f-248">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2b11f-249">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="2b11f-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2b11f-250">System-Only</span></span>            | <span data-ttu-id="2b11f-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-251">False</span></span>                                     |
| <span data-ttu-id="2b11f-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2b11f-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2b11f-253">True</span><span class="sxs-lookup"><span data-stu-id="2b11f-253">True</span></span>                                      |
| <span data-ttu-id="2b11f-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2b11f-254">Is Indexed</span></span>             | <span data-ttu-id="2b11f-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-255">False</span></span>                                     |
| <span data-ttu-id="2b11f-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2b11f-256">In Global Catalog</span></span>      | <span data-ttu-id="2b11f-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2b11f-257">False</span></span>                                     |
| <span data-ttu-id="2b11f-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2b11f-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2b11f-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2b11f-259">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="2b11f-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2b11f-260">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2b11f-261">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="2b11f-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-262">Search-Flags</span></span>           | <span data-ttu-id="2b11f-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2b11f-263">0x00000000</span></span>                                |
| <span data-ttu-id="2b11f-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2b11f-264">System-Flags</span></span>           | <span data-ttu-id="2b11f-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2b11f-265">0x00000010</span></span>                                |
| <span data-ttu-id="2b11f-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2b11f-266">Classes used in</span></span>        | [<span data-ttu-id="2b11f-267">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="2b11f-267">**Computer**</span></span>](c-computer.md)<br/> |



 

 





