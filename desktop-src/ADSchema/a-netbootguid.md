---
title: Атрибут нетбут-GUID
description: Бездисковая Загрузка встроенного идентификатора GUID компьютера. Соответствует MAC-адресу сетевого адаптера компьютера.
ms.assetid: 60ce0482-79a3-499a-9607-f1f496e297d0
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута нетбут-GUID
- Схема AD атрибута Нетбутгуид
topic_type:
- apiref
api_name:
- Netboot-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7c09d6f9139580ad329b47f13999d348abf5a87
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893738"
---
# <a name="netboot-guid-attribute"></a><span data-ttu-id="ff8d9-106">Атрибут нетбут-GUID</span><span class="sxs-lookup"><span data-stu-id="ff8d9-106">Netboot-GUID attribute</span></span>

<span data-ttu-id="ff8d9-107">Бездисковая Загрузка: встроенный GUID компьютера.</span><span class="sxs-lookup"><span data-stu-id="ff8d9-107">Diskless boot: A computer's on-board GUID.</span></span> <span data-ttu-id="ff8d9-108">Соответствует MAC-адресу сетевого адаптера компьютера.</span><span class="sxs-lookup"><span data-stu-id="ff8d9-108">Corresponds to the computer's network card MAC address.</span></span>



| <span data-ttu-id="ff8d9-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-109">Entry</span></span> | <span data-ttu-id="ff8d9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ff8d9-111">CN</span><span class="sxs-lookup"><span data-stu-id="ff8d9-111">CN</span></span>                | <span data-ttu-id="ff8d9-112">Нетбут — GUID</span><span class="sxs-lookup"><span data-stu-id="ff8d9-112">Netboot-GUID</span></span>                                          |
| <span data-ttu-id="ff8d9-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ff8d9-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ff8d9-114">нетбутгуид</span><span class="sxs-lookup"><span data-stu-id="ff8d9-114">netbootGUID</span></span>                                           |
| <span data-ttu-id="ff8d9-115">Размер</span><span class="sxs-lookup"><span data-stu-id="ff8d9-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ff8d9-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ff8d9-116">Update Privilege</span></span>  | <span data-ttu-id="ff8d9-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="ff8d9-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="ff8d9-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ff8d9-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ff8d9-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-119">Attribute-Id</span></span>      | <span data-ttu-id="ff8d9-120">1.2.840.113556.1.4.359</span><span class="sxs-lookup"><span data-stu-id="ff8d9-120">1.2.840.113556.1.4.359</span></span>                                |
| <span data-ttu-id="ff8d9-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ff8d9-121">System-Id-Guid</span></span>    | <span data-ttu-id="ff8d9-122">3e978921-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="ff8d9-122">3e978921-8c01-11d0-afda-00c04fd930c9</span></span>                  |
| <span data-ttu-id="ff8d9-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff8d9-123">Syntax</span></span>            | [<span data-ttu-id="ff8d9-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ff8d9-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ff8d9-125">Implementations</span></span>

-   [<span data-ttu-id="ff8d9-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ff8d9-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ff8d9-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ff8d9-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ff8d9-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ff8d9-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ff8d9-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ff8d9-132">Windows 2000 Server</span></span>



| <span data-ttu-id="ff8d9-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-133">Entry</span></span> | <span data-ttu-id="ff8d9-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-134">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ff8d9-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ff8d9-135">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-136">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff8d9-137">System-Only</span></span>            | <span data-ttu-id="ff8d9-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ff8d9-138">False</span></span>                                     |
| <span data-ttu-id="ff8d9-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ff8d9-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ff8d9-140">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-140">True</span></span>                                      |
| <span data-ttu-id="ff8d9-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ff8d9-141">Is Indexed</span></span>             | <span data-ttu-id="ff8d9-142">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-142">True</span></span>                                      |
| <span data-ttu-id="ff8d9-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ff8d9-143">In Global Catalog</span></span>      | <span data-ttu-id="ff8d9-144">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-144">True</span></span>                                      |
| <span data-ttu-id="ff8d9-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ff8d9-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff8d9-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff8d9-146">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ff8d9-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff8d9-147">Range-Lower</span></span>            | <span data-ttu-id="ff8d9-148">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-148">16</span></span>                                        |
| <span data-ttu-id="ff8d9-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff8d9-149">Range-Upper</span></span>            | <span data-ttu-id="ff8d9-150">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-150">16</span></span>                                        |
| <span data-ttu-id="ff8d9-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-151">Search-Flags</span></span>           | <span data-ttu-id="ff8d9-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff8d9-152">0x00000001</span></span>                                |
| <span data-ttu-id="ff8d9-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-153">System-Flags</span></span>           | <span data-ttu-id="ff8d9-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff8d9-154">0x00000010</span></span>                                |
| <span data-ttu-id="ff8d9-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ff8d9-155">Classes used in</span></span>        | [<span data-ttu-id="ff8d9-156">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-156">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ff8d9-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ff8d9-157">Windows Server 2003</span></span>



| <span data-ttu-id="ff8d9-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-158">Entry</span></span> | <span data-ttu-id="ff8d9-159">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-159">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ff8d9-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ff8d9-160">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-161">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff8d9-162">System-Only</span></span>            | <span data-ttu-id="ff8d9-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="ff8d9-163">False</span></span>                                     |
| <span data-ttu-id="ff8d9-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ff8d9-164">Is-Single-Valued</span></span>       | <span data-ttu-id="ff8d9-165">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-165">True</span></span>                                      |
| <span data-ttu-id="ff8d9-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ff8d9-166">Is Indexed</span></span>             | <span data-ttu-id="ff8d9-167">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-167">True</span></span>                                      |
| <span data-ttu-id="ff8d9-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ff8d9-168">In Global Catalog</span></span>      | <span data-ttu-id="ff8d9-169">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-169">True</span></span>                                      |
| <span data-ttu-id="ff8d9-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ff8d9-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff8d9-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff8d9-171">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ff8d9-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff8d9-172">Range-Lower</span></span>            | <span data-ttu-id="ff8d9-173">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-173">16</span></span>                                        |
| <span data-ttu-id="ff8d9-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff8d9-174">Range-Upper</span></span>            | <span data-ttu-id="ff8d9-175">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-175">16</span></span>                                        |
| <span data-ttu-id="ff8d9-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-176">Search-Flags</span></span>           | <span data-ttu-id="ff8d9-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff8d9-177">0x00000001</span></span>                                |
| <span data-ttu-id="ff8d9-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-178">System-Flags</span></span>           | <span data-ttu-id="ff8d9-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff8d9-179">0x00000010</span></span>                                |
| <span data-ttu-id="ff8d9-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ff8d9-180">Classes used in</span></span>        | [<span data-ttu-id="ff8d9-181">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-181">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ff8d9-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ff8d9-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ff8d9-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-183">Entry</span></span> | <span data-ttu-id="ff8d9-184">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-184">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ff8d9-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ff8d9-185">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-186">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff8d9-187">System-Only</span></span>            | <span data-ttu-id="ff8d9-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="ff8d9-188">False</span></span>                                     |
| <span data-ttu-id="ff8d9-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ff8d9-189">Is-Single-Valued</span></span>       | <span data-ttu-id="ff8d9-190">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-190">True</span></span>                                      |
| <span data-ttu-id="ff8d9-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ff8d9-191">Is Indexed</span></span>             | <span data-ttu-id="ff8d9-192">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-192">True</span></span>                                      |
| <span data-ttu-id="ff8d9-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ff8d9-193">In Global Catalog</span></span>      | <span data-ttu-id="ff8d9-194">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-194">True</span></span>                                      |
| <span data-ttu-id="ff8d9-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ff8d9-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff8d9-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff8d9-196">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ff8d9-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff8d9-197">Range-Lower</span></span>            | <span data-ttu-id="ff8d9-198">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-198">16</span></span>                                        |
| <span data-ttu-id="ff8d9-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff8d9-199">Range-Upper</span></span>            | <span data-ttu-id="ff8d9-200">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-200">16</span></span>                                        |
| <span data-ttu-id="ff8d9-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-201">Search-Flags</span></span>           | <span data-ttu-id="ff8d9-202">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff8d9-202">0x00000001</span></span>                                |
| <span data-ttu-id="ff8d9-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-203">System-Flags</span></span>           | <span data-ttu-id="ff8d9-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff8d9-204">0x00000010</span></span>                                |
| <span data-ttu-id="ff8d9-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ff8d9-205">Classes used in</span></span>        | [<span data-ttu-id="ff8d9-206">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-206">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ff8d9-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff8d9-207">Windows Server 2008</span></span>



| <span data-ttu-id="ff8d9-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-208">Entry</span></span> | <span data-ttu-id="ff8d9-209">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-209">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ff8d9-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ff8d9-210">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-211">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff8d9-212">System-Only</span></span>            | <span data-ttu-id="ff8d9-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="ff8d9-213">False</span></span>                                     |
| <span data-ttu-id="ff8d9-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ff8d9-214">Is-Single-Valued</span></span>       | <span data-ttu-id="ff8d9-215">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-215">True</span></span>                                      |
| <span data-ttu-id="ff8d9-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ff8d9-216">Is Indexed</span></span>             | <span data-ttu-id="ff8d9-217">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-217">True</span></span>                                      |
| <span data-ttu-id="ff8d9-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ff8d9-218">In Global Catalog</span></span>      | <span data-ttu-id="ff8d9-219">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-219">True</span></span>                                      |
| <span data-ttu-id="ff8d9-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ff8d9-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff8d9-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff8d9-221">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ff8d9-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff8d9-222">Range-Lower</span></span>            | <span data-ttu-id="ff8d9-223">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-223">16</span></span>                                        |
| <span data-ttu-id="ff8d9-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff8d9-224">Range-Upper</span></span>            | <span data-ttu-id="ff8d9-225">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-225">16</span></span>                                        |
| <span data-ttu-id="ff8d9-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-226">Search-Flags</span></span>           | <span data-ttu-id="ff8d9-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff8d9-227">0x00000001</span></span>                                |
| <span data-ttu-id="ff8d9-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-228">System-Flags</span></span>           | <span data-ttu-id="ff8d9-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff8d9-229">0x00000010</span></span>                                |
| <span data-ttu-id="ff8d9-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ff8d9-230">Classes used in</span></span>        | [<span data-ttu-id="ff8d9-231">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-231">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ff8d9-232">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ff8d9-232">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ff8d9-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-233">Entry</span></span> | <span data-ttu-id="ff8d9-234">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-234">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ff8d9-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ff8d9-235">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-236">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff8d9-237">System-Only</span></span>            | <span data-ttu-id="ff8d9-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="ff8d9-238">False</span></span>                                     |
| <span data-ttu-id="ff8d9-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ff8d9-239">Is-Single-Valued</span></span>       | <span data-ttu-id="ff8d9-240">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-240">True</span></span>                                      |
| <span data-ttu-id="ff8d9-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ff8d9-241">Is Indexed</span></span>             | <span data-ttu-id="ff8d9-242">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-242">True</span></span>                                      |
| <span data-ttu-id="ff8d9-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ff8d9-243">In Global Catalog</span></span>      | <span data-ttu-id="ff8d9-244">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-244">True</span></span>                                      |
| <span data-ttu-id="ff8d9-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ff8d9-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff8d9-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff8d9-246">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ff8d9-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff8d9-247">Range-Lower</span></span>            | <span data-ttu-id="ff8d9-248">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-248">16</span></span>                                        |
| <span data-ttu-id="ff8d9-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff8d9-249">Range-Upper</span></span>            | <span data-ttu-id="ff8d9-250">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-250">16</span></span>                                        |
| <span data-ttu-id="ff8d9-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-251">Search-Flags</span></span>           | <span data-ttu-id="ff8d9-252">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff8d9-252">0x00000001</span></span>                                |
| <span data-ttu-id="ff8d9-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-253">System-Flags</span></span>           | <span data-ttu-id="ff8d9-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff8d9-254">0x00000010</span></span>                                |
| <span data-ttu-id="ff8d9-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ff8d9-255">Classes used in</span></span>        | [<span data-ttu-id="ff8d9-256">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-256">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ff8d9-257">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ff8d9-257">Windows Server 2012</span></span>



| <span data-ttu-id="ff8d9-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="ff8d9-258">Entry</span></span> | <span data-ttu-id="ff8d9-259">Значение</span><span class="sxs-lookup"><span data-stu-id="ff8d9-259">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ff8d9-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ff8d9-260">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ff8d9-261">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ff8d9-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="ff8d9-262">System-Only</span></span>            | <span data-ttu-id="ff8d9-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="ff8d9-263">False</span></span>                                     |
| <span data-ttu-id="ff8d9-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ff8d9-264">Is-Single-Valued</span></span>       | <span data-ttu-id="ff8d9-265">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-265">True</span></span>                                      |
| <span data-ttu-id="ff8d9-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ff8d9-266">Is Indexed</span></span>             | <span data-ttu-id="ff8d9-267">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-267">True</span></span>                                      |
| <span data-ttu-id="ff8d9-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ff8d9-268">In Global Catalog</span></span>      | <span data-ttu-id="ff8d9-269">True</span><span class="sxs-lookup"><span data-stu-id="ff8d9-269">True</span></span>                                      |
| <span data-ttu-id="ff8d9-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ff8d9-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="ff8d9-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ff8d9-271">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ff8d9-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ff8d9-272">Range-Lower</span></span>            | <span data-ttu-id="ff8d9-273">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-273">16</span></span>                                        |
| <span data-ttu-id="ff8d9-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ff8d9-274">Range-Upper</span></span>            | <span data-ttu-id="ff8d9-275">16</span><span class="sxs-lookup"><span data-stu-id="ff8d9-275">16</span></span>                                        |
| <span data-ttu-id="ff8d9-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-276">Search-Flags</span></span>           | <span data-ttu-id="ff8d9-277">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ff8d9-277">0x00000001</span></span>                                |
| <span data-ttu-id="ff8d9-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ff8d9-278">System-Flags</span></span>           | <span data-ttu-id="ff8d9-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ff8d9-279">0x00000010</span></span>                                |
| <span data-ttu-id="ff8d9-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ff8d9-280">Classes used in</span></span>        | [<span data-ttu-id="ff8d9-281">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ff8d9-281">**Computer**</span></span>](c-computer.md)<br/> |



 

 





