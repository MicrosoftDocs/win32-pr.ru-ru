---
title: Атрибут Куерипоинт
description: URL-адрес или UNC страницы запроса или другой внешний интерфейс для доступа к каталогу.
ms.assetid: 8e23d8d0-e35a-4a2c-befb-696b037e8c91
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Куерипоинт
- Схема AD атрибута Куерипоинт
topic_type:
- apiref
api_name:
- QueryPoint
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbd3e1cb56bd07c97ecbaff9a1802f5af68d5ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804294"
---
# <a name="querypoint-attribute"></a><span data-ttu-id="eafe7-105">Атрибут Куерипоинт</span><span class="sxs-lookup"><span data-stu-id="eafe7-105">QueryPoint attribute</span></span>

<span data-ttu-id="eafe7-106">URL-адрес или UNC страницы запроса или другой внешний интерфейс для доступа к каталогу.</span><span class="sxs-lookup"><span data-stu-id="eafe7-106">The URL or UNC of a query page or other front end for accessing a catalog.</span></span>



| <span data-ttu-id="eafe7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-107">Entry</span></span> | <span data-ttu-id="eafe7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="eafe7-109">CN</span><span class="sxs-lookup"><span data-stu-id="eafe7-109">CN</span></span>                | <span data-ttu-id="eafe7-110">куерипоинт</span><span class="sxs-lookup"><span data-stu-id="eafe7-110">QueryPoint</span></span>                                  |
| <span data-ttu-id="eafe7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="eafe7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="eafe7-112">куерипоинт</span><span class="sxs-lookup"><span data-stu-id="eafe7-112">queryPoint</span></span>                                  |
| <span data-ttu-id="eafe7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="eafe7-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="eafe7-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="eafe7-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="eafe7-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="eafe7-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="eafe7-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-116">Attribute-Id</span></span>      | <span data-ttu-id="eafe7-117">1.2.840.113556.1.4.680</span><span class="sxs-lookup"><span data-stu-id="eafe7-117">1.2.840.113556.1.4.680</span></span>                      |
| <span data-ttu-id="eafe7-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="eafe7-118">System-Id-Guid</span></span>    | <span data-ttu-id="eafe7-119">7bfdcb86-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="eafe7-119">7bfdcb86-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="eafe7-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eafe7-120">Syntax</span></span>            | [<span data-ttu-id="eafe7-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="eafe7-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="eafe7-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="eafe7-122">Implementations</span></span>

-   [<span data-ttu-id="eafe7-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="eafe7-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="eafe7-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="eafe7-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="eafe7-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="eafe7-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="eafe7-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="eafe7-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="eafe7-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="eafe7-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="eafe7-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="eafe7-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="eafe7-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="eafe7-129">Windows 2000 Server</span></span>



| <span data-ttu-id="eafe7-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-130">Entry</span></span> | <span data-ttu-id="eafe7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-131">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="eafe7-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eafe7-132">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-133">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="eafe7-134">System-Only</span></span>            | <span data-ttu-id="eafe7-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-135">False</span></span>                                                           |
| <span data-ttu-id="eafe7-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eafe7-136">Is-Single-Valued</span></span>       | <span data-ttu-id="eafe7-137">True</span><span class="sxs-lookup"><span data-stu-id="eafe7-137">True</span></span>                                                            |
| <span data-ttu-id="eafe7-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eafe7-138">Is Indexed</span></span>             | <span data-ttu-id="eafe7-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-139">False</span></span>                                                           |
| <span data-ttu-id="eafe7-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eafe7-140">In Global Catalog</span></span>      | <span data-ttu-id="eafe7-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-141">False</span></span>                                                           |
| <span data-ttu-id="eafe7-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eafe7-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="eafe7-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eafe7-143">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="eafe7-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eafe7-144">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eafe7-145">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-146">Search-Flags</span></span>           | <span data-ttu-id="eafe7-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eafe7-147">0x00000000</span></span>                                                      |
| <span data-ttu-id="eafe7-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-148">System-Flags</span></span>           | <span data-ttu-id="eafe7-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafe7-149">0x00000010</span></span>                                                      |
| <span data-ttu-id="eafe7-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eafe7-150">Classes used in</span></span>        | [<span data-ttu-id="eafe7-151">**Каталог индекс-сервер**</span><span class="sxs-lookup"><span data-stu-id="eafe7-151">**Index-Server-Catalog**</span></span>](c-indexservercatalog.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="eafe7-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eafe7-152">Windows Server 2003</span></span>



| <span data-ttu-id="eafe7-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-153">Entry</span></span> | <span data-ttu-id="eafe7-154">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-154">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="eafe7-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eafe7-155">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-156">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="eafe7-157">System-Only</span></span>            | <span data-ttu-id="eafe7-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-158">False</span></span>                                                           |
| <span data-ttu-id="eafe7-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eafe7-159">Is-Single-Valued</span></span>       | <span data-ttu-id="eafe7-160">True</span><span class="sxs-lookup"><span data-stu-id="eafe7-160">True</span></span>                                                            |
| <span data-ttu-id="eafe7-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eafe7-161">Is Indexed</span></span>             | <span data-ttu-id="eafe7-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-162">False</span></span>                                                           |
| <span data-ttu-id="eafe7-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eafe7-163">In Global Catalog</span></span>      | <span data-ttu-id="eafe7-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-164">False</span></span>                                                           |
| <span data-ttu-id="eafe7-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eafe7-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="eafe7-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eafe7-166">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="eafe7-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eafe7-167">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eafe7-168">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-169">Search-Flags</span></span>           | <span data-ttu-id="eafe7-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eafe7-170">0x00000000</span></span>                                                      |
| <span data-ttu-id="eafe7-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-171">System-Flags</span></span>           | <span data-ttu-id="eafe7-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafe7-172">0x00000010</span></span>                                                      |
| <span data-ttu-id="eafe7-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eafe7-173">Classes used in</span></span>        | [<span data-ttu-id="eafe7-174">**Каталог индекс-сервер**</span><span class="sxs-lookup"><span data-stu-id="eafe7-174">**Index-Server-Catalog**</span></span>](c-indexservercatalog.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="eafe7-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="eafe7-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="eafe7-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-176">Entry</span></span> | <span data-ttu-id="eafe7-177">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-177">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="eafe7-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eafe7-178">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-179">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="eafe7-180">System-Only</span></span>            | <span data-ttu-id="eafe7-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-181">False</span></span>                                                           |
| <span data-ttu-id="eafe7-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eafe7-182">Is-Single-Valued</span></span>       | <span data-ttu-id="eafe7-183">True</span><span class="sxs-lookup"><span data-stu-id="eafe7-183">True</span></span>                                                            |
| <span data-ttu-id="eafe7-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eafe7-184">Is Indexed</span></span>             | <span data-ttu-id="eafe7-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-185">False</span></span>                                                           |
| <span data-ttu-id="eafe7-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eafe7-186">In Global Catalog</span></span>      | <span data-ttu-id="eafe7-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-187">False</span></span>                                                           |
| <span data-ttu-id="eafe7-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eafe7-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="eafe7-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eafe7-189">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="eafe7-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eafe7-190">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eafe7-191">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-192">Search-Flags</span></span>           | <span data-ttu-id="eafe7-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eafe7-193">0x00000000</span></span>                                                      |
| <span data-ttu-id="eafe7-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-194">System-Flags</span></span>           | <span data-ttu-id="eafe7-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafe7-195">0x00000010</span></span>                                                      |
| <span data-ttu-id="eafe7-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eafe7-196">Classes used in</span></span>        | [<span data-ttu-id="eafe7-197">**Каталог индекс-сервер**</span><span class="sxs-lookup"><span data-stu-id="eafe7-197">**Index-Server-Catalog**</span></span>](c-indexservercatalog.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="eafe7-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eafe7-198">Windows Server 2008</span></span>



| <span data-ttu-id="eafe7-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-199">Entry</span></span> | <span data-ttu-id="eafe7-200">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-200">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="eafe7-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eafe7-201">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-202">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="eafe7-203">System-Only</span></span>            | <span data-ttu-id="eafe7-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-204">False</span></span>                                                           |
| <span data-ttu-id="eafe7-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eafe7-205">Is-Single-Valued</span></span>       | <span data-ttu-id="eafe7-206">True</span><span class="sxs-lookup"><span data-stu-id="eafe7-206">True</span></span>                                                            |
| <span data-ttu-id="eafe7-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eafe7-207">Is Indexed</span></span>             | <span data-ttu-id="eafe7-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-208">False</span></span>                                                           |
| <span data-ttu-id="eafe7-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eafe7-209">In Global Catalog</span></span>      | <span data-ttu-id="eafe7-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-210">False</span></span>                                                           |
| <span data-ttu-id="eafe7-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eafe7-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="eafe7-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eafe7-212">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="eafe7-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eafe7-213">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eafe7-214">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-215">Search-Flags</span></span>           | <span data-ttu-id="eafe7-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eafe7-216">0x00000000</span></span>                                                      |
| <span data-ttu-id="eafe7-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-217">System-Flags</span></span>           | <span data-ttu-id="eafe7-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafe7-218">0x00000010</span></span>                                                      |
| <span data-ttu-id="eafe7-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eafe7-219">Classes used in</span></span>        | [<span data-ttu-id="eafe7-220">**Каталог индекс-сервер**</span><span class="sxs-lookup"><span data-stu-id="eafe7-220">**Index-Server-Catalog**</span></span>](c-indexservercatalog.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="eafe7-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eafe7-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="eafe7-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-222">Entry</span></span> | <span data-ttu-id="eafe7-223">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-223">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="eafe7-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eafe7-224">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-225">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="eafe7-226">System-Only</span></span>            | <span data-ttu-id="eafe7-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-227">False</span></span>                                                           |
| <span data-ttu-id="eafe7-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eafe7-228">Is-Single-Valued</span></span>       | <span data-ttu-id="eafe7-229">True</span><span class="sxs-lookup"><span data-stu-id="eafe7-229">True</span></span>                                                            |
| <span data-ttu-id="eafe7-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eafe7-230">Is Indexed</span></span>             | <span data-ttu-id="eafe7-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-231">False</span></span>                                                           |
| <span data-ttu-id="eafe7-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eafe7-232">In Global Catalog</span></span>      | <span data-ttu-id="eafe7-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-233">False</span></span>                                                           |
| <span data-ttu-id="eafe7-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eafe7-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="eafe7-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eafe7-235">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="eafe7-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eafe7-236">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eafe7-237">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-238">Search-Flags</span></span>           | <span data-ttu-id="eafe7-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eafe7-239">0x00000000</span></span>                                                      |
| <span data-ttu-id="eafe7-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-240">System-Flags</span></span>           | <span data-ttu-id="eafe7-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafe7-241">0x00000010</span></span>                                                      |
| <span data-ttu-id="eafe7-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eafe7-242">Classes used in</span></span>        | [<span data-ttu-id="eafe7-243">**Каталог индекс-сервер**</span><span class="sxs-lookup"><span data-stu-id="eafe7-243">**Index-Server-Catalog**</span></span>](c-indexservercatalog.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="eafe7-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eafe7-244">Windows Server 2012</span></span>



| <span data-ttu-id="eafe7-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="eafe7-245">Entry</span></span> | <span data-ttu-id="eafe7-246">Значение</span><span class="sxs-lookup"><span data-stu-id="eafe7-246">Value</span></span> |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="eafe7-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="eafe7-247">Link-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="eafe7-248">MAPI-Id</span></span>                | \-                                                              |
| <span data-ttu-id="eafe7-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="eafe7-249">System-Only</span></span>            | <span data-ttu-id="eafe7-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-250">False</span></span>                                                           |
| <span data-ttu-id="eafe7-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="eafe7-251">Is-Single-Valued</span></span>       | <span data-ttu-id="eafe7-252">True</span><span class="sxs-lookup"><span data-stu-id="eafe7-252">True</span></span>                                                            |
| <span data-ttu-id="eafe7-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="eafe7-253">Is Indexed</span></span>             | <span data-ttu-id="eafe7-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-254">False</span></span>                                                           |
| <span data-ttu-id="eafe7-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="eafe7-255">In Global Catalog</span></span>      | <span data-ttu-id="eafe7-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="eafe7-256">False</span></span>                                                           |
| <span data-ttu-id="eafe7-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="eafe7-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="eafe7-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="eafe7-258">O:BAG:BAD:S:</span></span>                                                    |
| <span data-ttu-id="eafe7-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="eafe7-259">Range-Lower</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="eafe7-260">Range-Upper</span></span>            | \-                                                              |
| <span data-ttu-id="eafe7-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-261">Search-Flags</span></span>           | <span data-ttu-id="eafe7-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="eafe7-262">0x00000000</span></span>                                                      |
| <span data-ttu-id="eafe7-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="eafe7-263">System-Flags</span></span>           | <span data-ttu-id="eafe7-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="eafe7-264">0x00000010</span></span>                                                      |
| <span data-ttu-id="eafe7-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="eafe7-265">Classes used in</span></span>        | [<span data-ttu-id="eafe7-266">**Каталог индекс-сервер**</span><span class="sxs-lookup"><span data-stu-id="eafe7-266">**Index-Server-Catalog**</span></span>](c-indexservercatalog.md)<br/> |



 

 





