---
title: По умолчанию — атрибут хранилища классов
description: Хранилище классов по умолчанию для данного пользователя.
ms.assetid: 9aaeb401-4c2c-4c3b-83d2-0c6044be7643
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута по умолчанию для хранения классов
- Схема AD атрибута Дефаулткласссторе
topic_type:
- apiref
api_name:
- Default-Class-Store
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5aa4e9bddcc1e9dcb0aa7de962b9c6816555482
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138207"
---
# <a name="default-class-store-attribute"></a><span data-ttu-id="8b0ed-105">По умолчанию — атрибут хранилища классов</span><span class="sxs-lookup"><span data-stu-id="8b0ed-105">Default-Class-Store attribute</span></span>

<span data-ttu-id="8b0ed-106">Хранилище классов по умолчанию для данного пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b0ed-106">The default Class Store for a given user.</span></span>



| <span data-ttu-id="8b0ed-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-107">Entry</span></span> | <span data-ttu-id="8b0ed-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="8b0ed-109">CN</span><span class="sxs-lookup"><span data-stu-id="8b0ed-109">CN</span></span>                | <span data-ttu-id="8b0ed-110">Хранилище классов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8b0ed-110">Default-Class-Store</span></span>                     |
| <span data-ttu-id="8b0ed-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8b0ed-111">Ldap-Display-Name</span></span> | <span data-ttu-id="8b0ed-112">дефаулткласссторе</span><span class="sxs-lookup"><span data-stu-id="8b0ed-112">defaultClassStore</span></span>                       |
| <span data-ttu-id="8b0ed-113">Размер</span><span class="sxs-lookup"><span data-stu-id="8b0ed-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="8b0ed-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8b0ed-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="8b0ed-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8b0ed-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="8b0ed-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-116">Attribute-Id</span></span>      | <span data-ttu-id="8b0ed-117">1.2.840.113556.1.4.213</span><span class="sxs-lookup"><span data-stu-id="8b0ed-117">1.2.840.113556.1.4.213</span></span>                  |
| <span data-ttu-id="8b0ed-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8b0ed-118">System-Id-Guid</span></span>    | <span data-ttu-id="8b0ed-119">bf967948-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="8b0ed-119">bf967948-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="8b0ed-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b0ed-120">Syntax</span></span>            | [<span data-ttu-id="8b0ed-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="8b0ed-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8b0ed-122">Implementations</span></span>

-   [<span data-ttu-id="8b0ed-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="8b0ed-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="8b0ed-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="8b0ed-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="8b0ed-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="8b0ed-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="8b0ed-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8b0ed-129">Windows 2000 Server</span></span>



| <span data-ttu-id="8b0ed-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-130">Entry</span></span> | <span data-ttu-id="8b0ed-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ed-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b0ed-132">Link-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-133">MAPI-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b0ed-134">System-Only</span></span>            | <span data-ttu-id="8b0ed-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-135">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b0ed-136">Is-Single-Valued</span></span>       | <span data-ttu-id="8b0ed-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-137">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b0ed-138">Is Indexed</span></span>             | <span data-ttu-id="8b0ed-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-139">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b0ed-140">In Global Catalog</span></span>      | <span data-ttu-id="8b0ed-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-141">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b0ed-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b0ed-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b0ed-143">O:BAG:BAD:S:</span></span>                                                                  |
| <span data-ttu-id="8b0ed-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b0ed-144">Range-Lower</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b0ed-145">Range-Upper</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-146">Search-Flags</span></span>           | <span data-ttu-id="8b0ed-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b0ed-147">0x00000000</span></span>                                                                    |
| <span data-ttu-id="8b0ed-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-148">System-Flags</span></span>           | <span data-ttu-id="8b0ed-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b0ed-149">0x00000010</span></span>                                                                    |
| <span data-ttu-id="8b0ed-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b0ed-150">Classes used in</span></span>        | [<span data-ttu-id="8b0ed-151">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-151">**Container**</span></span>](c-container.md)<br/> [<span data-ttu-id="8b0ed-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="8b0ed-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8b0ed-153">Windows Server 2003</span></span>



| <span data-ttu-id="8b0ed-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-154">Entry</span></span> | <span data-ttu-id="8b0ed-155">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-155">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ed-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b0ed-156">Link-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-157">MAPI-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b0ed-158">System-Only</span></span>            | <span data-ttu-id="8b0ed-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-159">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b0ed-160">Is-Single-Valued</span></span>       | <span data-ttu-id="8b0ed-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-161">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b0ed-162">Is Indexed</span></span>             | <span data-ttu-id="8b0ed-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-163">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b0ed-164">In Global Catalog</span></span>      | <span data-ttu-id="8b0ed-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-165">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b0ed-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b0ed-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b0ed-167">O:BAG:BAD:S:</span></span>                                                                  |
| <span data-ttu-id="8b0ed-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b0ed-168">Range-Lower</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b0ed-169">Range-Upper</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-170">Search-Flags</span></span>           | <span data-ttu-id="8b0ed-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b0ed-171">0x00000000</span></span>                                                                    |
| <span data-ttu-id="8b0ed-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-172">System-Flags</span></span>           | <span data-ttu-id="8b0ed-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b0ed-173">0x00000010</span></span>                                                                    |
| <span data-ttu-id="8b0ed-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b0ed-174">Classes used in</span></span>        | [<span data-ttu-id="8b0ed-175">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-175">**Container**</span></span>](c-container.md)<br/> [<span data-ttu-id="8b0ed-176">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-176">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="8b0ed-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="8b0ed-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="8b0ed-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-178">Entry</span></span> | <span data-ttu-id="8b0ed-179">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-179">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ed-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b0ed-180">Link-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-181">MAPI-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b0ed-182">System-Only</span></span>            | <span data-ttu-id="8b0ed-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-183">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b0ed-184">Is-Single-Valued</span></span>       | <span data-ttu-id="8b0ed-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-185">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b0ed-186">Is Indexed</span></span>             | <span data-ttu-id="8b0ed-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-187">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b0ed-188">In Global Catalog</span></span>      | <span data-ttu-id="8b0ed-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-189">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b0ed-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b0ed-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b0ed-191">O:BAG:BAD:S:</span></span>                                                                  |
| <span data-ttu-id="8b0ed-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b0ed-192">Range-Lower</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b0ed-193">Range-Upper</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-194">Search-Flags</span></span>           | <span data-ttu-id="8b0ed-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b0ed-195">0x00000000</span></span>                                                                    |
| <span data-ttu-id="8b0ed-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-196">System-Flags</span></span>           | <span data-ttu-id="8b0ed-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b0ed-197">0x00000010</span></span>                                                                    |
| <span data-ttu-id="8b0ed-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b0ed-198">Classes used in</span></span>        | [<span data-ttu-id="8b0ed-199">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-199">**Container**</span></span>](c-container.md)<br/> [<span data-ttu-id="8b0ed-200">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-200">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="8b0ed-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b0ed-201">Windows Server 2008</span></span>



| <span data-ttu-id="8b0ed-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-202">Entry</span></span> | <span data-ttu-id="8b0ed-203">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-203">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ed-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b0ed-204">Link-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-205">MAPI-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b0ed-206">System-Only</span></span>            | <span data-ttu-id="8b0ed-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-207">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b0ed-208">Is-Single-Valued</span></span>       | <span data-ttu-id="8b0ed-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-209">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b0ed-210">Is Indexed</span></span>             | <span data-ttu-id="8b0ed-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-211">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b0ed-212">In Global Catalog</span></span>      | <span data-ttu-id="8b0ed-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-213">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b0ed-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b0ed-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b0ed-215">O:BAG:BAD:S:</span></span>                                                                  |
| <span data-ttu-id="8b0ed-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b0ed-216">Range-Lower</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b0ed-217">Range-Upper</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-218">Search-Flags</span></span>           | <span data-ttu-id="8b0ed-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b0ed-219">0x00000000</span></span>                                                                    |
| <span data-ttu-id="8b0ed-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-220">System-Flags</span></span>           | <span data-ttu-id="8b0ed-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b0ed-221">0x00000010</span></span>                                                                    |
| <span data-ttu-id="8b0ed-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b0ed-222">Classes used in</span></span>        | [<span data-ttu-id="8b0ed-223">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-223">**Container**</span></span>](c-container.md)<br/> [<span data-ttu-id="8b0ed-224">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-224">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="8b0ed-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8b0ed-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="8b0ed-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-226">Entry</span></span> | <span data-ttu-id="8b0ed-227">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ed-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b0ed-228">Link-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-229">MAPI-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b0ed-230">System-Only</span></span>            | <span data-ttu-id="8b0ed-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-231">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b0ed-232">Is-Single-Valued</span></span>       | <span data-ttu-id="8b0ed-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-233">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b0ed-234">Is Indexed</span></span>             | <span data-ttu-id="8b0ed-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-235">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b0ed-236">In Global Catalog</span></span>      | <span data-ttu-id="8b0ed-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-237">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b0ed-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b0ed-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b0ed-239">O:BAG:BAD:S:</span></span>                                                                  |
| <span data-ttu-id="8b0ed-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b0ed-240">Range-Lower</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b0ed-241">Range-Upper</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-242">Search-Flags</span></span>           | <span data-ttu-id="8b0ed-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b0ed-243">0x00000000</span></span>                                                                    |
| <span data-ttu-id="8b0ed-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-244">System-Flags</span></span>           | <span data-ttu-id="8b0ed-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b0ed-245">0x00000010</span></span>                                                                    |
| <span data-ttu-id="8b0ed-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b0ed-246">Classes used in</span></span>        | [<span data-ttu-id="8b0ed-247">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-247">**Container**</span></span>](c-container.md)<br/> [<span data-ttu-id="8b0ed-248">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-248">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="8b0ed-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8b0ed-249">Windows Server 2012</span></span>



| <span data-ttu-id="8b0ed-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="8b0ed-250">Entry</span></span> | <span data-ttu-id="8b0ed-251">Значение</span><span class="sxs-lookup"><span data-stu-id="8b0ed-251">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="8b0ed-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8b0ed-252">Link-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8b0ed-253">MAPI-Id</span></span>                | \-                                                                            |
| <span data-ttu-id="8b0ed-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="8b0ed-254">System-Only</span></span>            | <span data-ttu-id="8b0ed-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-255">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8b0ed-256">Is-Single-Valued</span></span>       | <span data-ttu-id="8b0ed-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-257">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8b0ed-258">Is Indexed</span></span>             | <span data-ttu-id="8b0ed-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-259">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8b0ed-260">In Global Catalog</span></span>      | <span data-ttu-id="8b0ed-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="8b0ed-261">False</span></span>                                                                         |
| <span data-ttu-id="8b0ed-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8b0ed-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="8b0ed-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8b0ed-263">O:BAG:BAD:S:</span></span>                                                                  |
| <span data-ttu-id="8b0ed-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8b0ed-264">Range-Lower</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8b0ed-265">Range-Upper</span></span>            | \-                                                                            |
| <span data-ttu-id="8b0ed-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-266">Search-Flags</span></span>           | <span data-ttu-id="8b0ed-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8b0ed-267">0x00000000</span></span>                                                                    |
| <span data-ttu-id="8b0ed-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8b0ed-268">System-Flags</span></span>           | <span data-ttu-id="8b0ed-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8b0ed-269">0x00000010</span></span>                                                                    |
| <span data-ttu-id="8b0ed-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8b0ed-270">Classes used in</span></span>        | [<span data-ttu-id="8b0ed-271">**Контейнер**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-271">**Container**</span></span>](c-container.md)<br/> [<span data-ttu-id="8b0ed-272">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="8b0ed-272">**User**</span></span>](c-user.md)<br/> |



 

 





