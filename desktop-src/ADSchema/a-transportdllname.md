---
title: Атрибут имени транспорта-DLL
description: Имя библиотеки DLL, которая будет управлять транспортом.
ms.assetid: a6b078ec-8738-4c57-9d94-05a96dbc645b
ms.tgt_platform: multiple
keywords:
- Имя схемы AD атрибута Transport-DLL
- Схема AD атрибута Транспортдллнаме
topic_type:
- apiref
api_name:
- Transport-DLL-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c118a2f7553c86de4b3c36b2904a3b7d75518a2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655281"
---
# <a name="transport-dll-name-attribute"></a><span data-ttu-id="1e885-105">Атрибут имени транспорта-DLL</span><span class="sxs-lookup"><span data-stu-id="1e885-105">Transport-DLL-Name attribute</span></span>

<span data-ttu-id="1e885-106">Имя библиотеки DLL, которая будет управлять транспортом.</span><span class="sxs-lookup"><span data-stu-id="1e885-106">The name of the DLL that will manage a transport.</span></span>



| <span data-ttu-id="1e885-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-107">Entry</span></span> | <span data-ttu-id="1e885-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1e885-109">CN</span><span class="sxs-lookup"><span data-stu-id="1e885-109">CN</span></span>                | <span data-ttu-id="1e885-110">Transport-DLL-Name</span><span class="sxs-lookup"><span data-stu-id="1e885-110">Transport-DLL-Name</span></span>                          |
| <span data-ttu-id="1e885-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1e885-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1e885-112">транспортдллнаме</span><span class="sxs-lookup"><span data-stu-id="1e885-112">transportDLLName</span></span>                            |
| <span data-ttu-id="1e885-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1e885-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1e885-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1e885-114">Update Privilege</span></span>  | <span data-ttu-id="1e885-115">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="1e885-115">This value is set by the system.</span></span>            |
| <span data-ttu-id="1e885-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1e885-116">Update Frequency</span></span>  | <span data-ttu-id="1e885-117">При подключении сайтов.</span><span class="sxs-lookup"><span data-stu-id="1e885-117">When connecting sites.</span></span>                      |
| <span data-ttu-id="1e885-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-118">Attribute-Id</span></span>      | <span data-ttu-id="1e885-119">1.2.840.113556.1.4.789</span><span class="sxs-lookup"><span data-stu-id="1e885-119">1.2.840.113556.1.4.789</span></span>                      |
| <span data-ttu-id="1e885-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1e885-120">System-Id-Guid</span></span>    | <span data-ttu-id="1e885-121">26d97372-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="1e885-121">26d97372-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="1e885-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e885-122">Syntax</span></span>            | [<span data-ttu-id="1e885-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="1e885-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1e885-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1e885-124">Implementations</span></span>

-   [<span data-ttu-id="1e885-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1e885-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1e885-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1e885-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1e885-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1e885-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1e885-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1e885-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1e885-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1e885-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1e885-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1e885-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1e885-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1e885-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1e885-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e885-132">Windows 2000 Server</span></span>



| <span data-ttu-id="1e885-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-133">Entry</span></span> | <span data-ttu-id="1e885-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-134">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-135">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-136">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-137">System-Only</span></span>            | <span data-ttu-id="1e885-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-138">False</span></span>                                                           |
| <span data-ttu-id="1e885-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-139">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-140">True</span><span class="sxs-lookup"><span data-stu-id="1e885-140">True</span></span>                                                            |
| <span data-ttu-id="1e885-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-141">Is Indexed</span></span>             | <span data-ttu-id="1e885-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-142">False</span></span>                                                           |
| <span data-ttu-id="1e885-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-143">In Global Catalog</span></span>      | <span data-ttu-id="1e885-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-144">False</span></span>                                                           |
| <span data-ttu-id="1e885-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-146">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-147">Range-Lower</span></span>            | <span data-ttu-id="1e885-148">0</span><span class="sxs-lookup"><span data-stu-id="1e885-148">0</span></span>                                                               |
| <span data-ttu-id="1e885-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-149">Range-Upper</span></span>            | <span data-ttu-id="1e885-150">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-150">1024</span></span>                                                            |
| <span data-ttu-id="1e885-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-151">Search-Flags</span></span>           | <span data-ttu-id="1e885-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-152">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-153">System-Flags</span></span>           | <span data-ttu-id="1e885-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-154">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-155">Classes used in</span></span>        | [<span data-ttu-id="1e885-156">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-156">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1e885-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e885-157">Windows Server 2003</span></span>



| <span data-ttu-id="1e885-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-158">Entry</span></span> | <span data-ttu-id="1e885-159">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-160">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-161">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-162">System-Only</span></span>            | <span data-ttu-id="1e885-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-163">False</span></span>                                                           |
| <span data-ttu-id="1e885-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-164">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-165">True</span><span class="sxs-lookup"><span data-stu-id="1e885-165">True</span></span>                                                            |
| <span data-ttu-id="1e885-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-166">Is Indexed</span></span>             | <span data-ttu-id="1e885-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-167">False</span></span>                                                           |
| <span data-ttu-id="1e885-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-168">In Global Catalog</span></span>      | <span data-ttu-id="1e885-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-169">False</span></span>                                                           |
| <span data-ttu-id="1e885-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-171">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-172">Range-Lower</span></span>            | <span data-ttu-id="1e885-173">0</span><span class="sxs-lookup"><span data-stu-id="1e885-173">0</span></span>                                                               |
| <span data-ttu-id="1e885-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-174">Range-Upper</span></span>            | <span data-ttu-id="1e885-175">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-175">1024</span></span>                                                            |
| <span data-ttu-id="1e885-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-176">Search-Flags</span></span>           | <span data-ttu-id="1e885-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-177">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-178">System-Flags</span></span>           | <span data-ttu-id="1e885-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-179">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-180">Classes used in</span></span>        | [<span data-ttu-id="1e885-181">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-181">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1e885-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="1e885-182">ADAM</span></span>



| <span data-ttu-id="1e885-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-183">Entry</span></span> | <span data-ttu-id="1e885-184">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-184">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-185">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-186">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-187">System-Only</span></span>            | <span data-ttu-id="1e885-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-188">False</span></span>                                                           |
| <span data-ttu-id="1e885-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-189">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-190">True</span><span class="sxs-lookup"><span data-stu-id="1e885-190">True</span></span>                                                            |
| <span data-ttu-id="1e885-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-191">Is Indexed</span></span>             | <span data-ttu-id="1e885-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-192">False</span></span>                                                           |
| <span data-ttu-id="1e885-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-193">In Global Catalog</span></span>      | <span data-ttu-id="1e885-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-194">False</span></span>                                                           |
| <span data-ttu-id="1e885-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-196">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-197">Range-Lower</span></span>            | <span data-ttu-id="1e885-198">0</span><span class="sxs-lookup"><span data-stu-id="1e885-198">0</span></span>                                                               |
| <span data-ttu-id="1e885-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-199">Range-Upper</span></span>            | <span data-ttu-id="1e885-200">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-200">1024</span></span>                                                            |
| <span data-ttu-id="1e885-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-201">Search-Flags</span></span>           | <span data-ttu-id="1e885-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-202">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-203">System-Flags</span></span>           | <span data-ttu-id="1e885-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-204">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-205">Classes used in</span></span>        | [<span data-ttu-id="1e885-206">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-206">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1e885-207">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1e885-207">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1e885-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-208">Entry</span></span> | <span data-ttu-id="1e885-209">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-209">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-210">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-211">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-212">System-Only</span></span>            | <span data-ttu-id="1e885-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-213">False</span></span>                                                           |
| <span data-ttu-id="1e885-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-214">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-215">True</span><span class="sxs-lookup"><span data-stu-id="1e885-215">True</span></span>                                                            |
| <span data-ttu-id="1e885-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-216">Is Indexed</span></span>             | <span data-ttu-id="1e885-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-217">False</span></span>                                                           |
| <span data-ttu-id="1e885-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-218">In Global Catalog</span></span>      | <span data-ttu-id="1e885-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-219">False</span></span>                                                           |
| <span data-ttu-id="1e885-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-221">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-222">Range-Lower</span></span>            | <span data-ttu-id="1e885-223">0</span><span class="sxs-lookup"><span data-stu-id="1e885-223">0</span></span>                                                               |
| <span data-ttu-id="1e885-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-224">Range-Upper</span></span>            | <span data-ttu-id="1e885-225">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-225">1024</span></span>                                                            |
| <span data-ttu-id="1e885-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-226">Search-Flags</span></span>           | <span data-ttu-id="1e885-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-227">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-228">System-Flags</span></span>           | <span data-ttu-id="1e885-229">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-229">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-230">Classes used in</span></span>        | [<span data-ttu-id="1e885-231">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-231">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1e885-232">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e885-232">Windows Server 2008</span></span>



| <span data-ttu-id="1e885-233">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-233">Entry</span></span> | <span data-ttu-id="1e885-234">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-234">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-235">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-235">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-236">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-236">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-237">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-237">System-Only</span></span>            | <span data-ttu-id="1e885-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-238">False</span></span>                                                           |
| <span data-ttu-id="1e885-239">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-239">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-240">True</span><span class="sxs-lookup"><span data-stu-id="1e885-240">True</span></span>                                                            |
| <span data-ttu-id="1e885-241">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-241">Is Indexed</span></span>             | <span data-ttu-id="1e885-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-242">False</span></span>                                                           |
| <span data-ttu-id="1e885-243">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-243">In Global Catalog</span></span>      | <span data-ttu-id="1e885-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-244">False</span></span>                                                           |
| <span data-ttu-id="1e885-245">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-245">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-246">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-246">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-247">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-247">Range-Lower</span></span>            | <span data-ttu-id="1e885-248">0</span><span class="sxs-lookup"><span data-stu-id="1e885-248">0</span></span>                                                               |
| <span data-ttu-id="1e885-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-249">Range-Upper</span></span>            | <span data-ttu-id="1e885-250">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-250">1024</span></span>                                                            |
| <span data-ttu-id="1e885-251">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-251">Search-Flags</span></span>           | <span data-ttu-id="1e885-252">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-252">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-253">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-253">System-Flags</span></span>           | <span data-ttu-id="1e885-254">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-254">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-255">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-255">Classes used in</span></span>        | [<span data-ttu-id="1e885-256">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-256">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1e885-257">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1e885-257">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1e885-258">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-258">Entry</span></span> | <span data-ttu-id="1e885-259">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-259">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-260">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-260">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-261">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-261">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-262">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-262">System-Only</span></span>            | <span data-ttu-id="1e885-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-263">False</span></span>                                                           |
| <span data-ttu-id="1e885-264">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-264">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-265">True</span><span class="sxs-lookup"><span data-stu-id="1e885-265">True</span></span>                                                            |
| <span data-ttu-id="1e885-266">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-266">Is Indexed</span></span>             | <span data-ttu-id="1e885-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-267">False</span></span>                                                           |
| <span data-ttu-id="1e885-268">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-268">In Global Catalog</span></span>      | <span data-ttu-id="1e885-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-269">False</span></span>                                                           |
| <span data-ttu-id="1e885-270">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-270">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-271">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-271">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-272">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-272">Range-Lower</span></span>            | <span data-ttu-id="1e885-273">0</span><span class="sxs-lookup"><span data-stu-id="1e885-273">0</span></span>                                                               |
| <span data-ttu-id="1e885-274">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-274">Range-Upper</span></span>            | <span data-ttu-id="1e885-275">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-275">1024</span></span>                                                            |
| <span data-ttu-id="1e885-276">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-276">Search-Flags</span></span>           | <span data-ttu-id="1e885-277">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-277">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-278">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-278">System-Flags</span></span>           | <span data-ttu-id="1e885-279">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-279">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-280">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-280">Classes used in</span></span>        | [<span data-ttu-id="1e885-281">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-281">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1e885-282">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1e885-282">Windows Server 2012</span></span>



| <span data-ttu-id="1e885-283">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e885-283">Entry</span></span> | <span data-ttu-id="1e885-284">Значение</span><span class="sxs-lookup"><span data-stu-id="1e885-284">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="1e885-285">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1e885-285">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-286">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1e885-286">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="1e885-287">System-Only</span><span class="sxs-lookup"><span data-stu-id="1e885-287">System-Only</span></span>            | <span data-ttu-id="1e885-288">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-288">False</span></span>                                                           |
| <span data-ttu-id="1e885-289">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1e885-289">Is-Single-Valued</span></span>       | <span data-ttu-id="1e885-290">True</span><span class="sxs-lookup"><span data-stu-id="1e885-290">True</span></span>                                                            |
| <span data-ttu-id="1e885-291">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1e885-291">Is Indexed</span></span>             | <span data-ttu-id="1e885-292">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-292">False</span></span>                                                           |
| <span data-ttu-id="1e885-293">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1e885-293">In Global Catalog</span></span>      | <span data-ttu-id="1e885-294">Неверно</span><span class="sxs-lookup"><span data-stu-id="1e885-294">False</span></span>                                                           |
| <span data-ttu-id="1e885-295">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1e885-295">NT-Security-Descriptor</span></span> | <span data-ttu-id="1e885-296">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1e885-296">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="1e885-297">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1e885-297">Range-Lower</span></span>            | <span data-ttu-id="1e885-298">0</span><span class="sxs-lookup"><span data-stu-id="1e885-298">0</span></span>                                                               |
| <span data-ttu-id="1e885-299">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1e885-299">Range-Upper</span></span>            | <span data-ttu-id="1e885-300">1024</span><span class="sxs-lookup"><span data-stu-id="1e885-300">1024</span></span>                                                            |
| <span data-ttu-id="1e885-301">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-301">Search-Flags</span></span>           | <span data-ttu-id="1e885-302">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1e885-302">0x00000000</span></span>                                                      |
| <span data-ttu-id="1e885-303">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1e885-303">System-Flags</span></span>           | <span data-ttu-id="1e885-304">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1e885-304">0x00000010</span></span>                                                      |
| <span data-ttu-id="1e885-305">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1e885-305">Classes used in</span></span>        | [<span data-ttu-id="1e885-306">**Межсайтовый транспорт**</span><span class="sxs-lookup"><span data-stu-id="1e885-306">**Inter-Site-Transport**</span></span>](c-intersitetransport.md)<br/> |



 

 





