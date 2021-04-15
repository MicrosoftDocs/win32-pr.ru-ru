---
title: Атрибут моникера
description: Имя или путь для COM-объекта.
ms.assetid: e1ddcf9e-f8db-4aa0-a387-352a467a5b2c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута моникера
- Схема AD атрибута моникера
topic_type:
- apiref
api_name:
- Moniker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef9d1eeb5d4c635379704a7dc250c3c80a2f9c07
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655231"
---
# <a name="moniker-attribute"></a><span data-ttu-id="6c7a2-105">Атрибут моникера</span><span class="sxs-lookup"><span data-stu-id="6c7a2-105">Moniker attribute</span></span>

<span data-ttu-id="6c7a2-106">Имя или путь для COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="6c7a2-106">The name or path for a COM object.</span></span>



| <span data-ttu-id="6c7a2-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-107">Entry</span></span> | <span data-ttu-id="6c7a2-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="6c7a2-109">CN</span><span class="sxs-lookup"><span data-stu-id="6c7a2-109">CN</span></span>                | <span data-ttu-id="6c7a2-110">Moniker</span><span class="sxs-lookup"><span data-stu-id="6c7a2-110">Moniker</span></span>                                               |
| <span data-ttu-id="6c7a2-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6c7a2-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6c7a2-112">моникер</span><span class="sxs-lookup"><span data-stu-id="6c7a2-112">moniker</span></span>                                               |
| <span data-ttu-id="6c7a2-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6c7a2-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="6c7a2-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6c7a2-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="6c7a2-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6c7a2-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="6c7a2-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-116">Attribute-Id</span></span>      | <span data-ttu-id="6c7a2-117">1.2.840.113556.1.4.82</span><span class="sxs-lookup"><span data-stu-id="6c7a2-117">1.2.840.113556.1.4.82</span></span>                                 |
| <span data-ttu-id="6c7a2-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6c7a2-118">System-Id-Guid</span></span>    | <span data-ttu-id="6c7a2-119">bf9679c7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="6c7a2-119">bf9679c7-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="6c7a2-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c7a2-120">Syntax</span></span>            | [<span data-ttu-id="6c7a2-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="6c7a2-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6c7a2-122">Implementations</span></span>

-   [<span data-ttu-id="6c7a2-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6c7a2-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6c7a2-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6c7a2-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6c7a2-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6c7a2-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6c7a2-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6c7a2-129">Windows 2000 Server</span></span>



| <span data-ttu-id="6c7a2-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-130">Entry</span></span> | <span data-ttu-id="6c7a2-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-131">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a2-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c7a2-132">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-133">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c7a2-134">System-Only</span></span>            | <span data-ttu-id="6c7a2-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-135">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c7a2-136">Is-Single-Valued</span></span>       | <span data-ttu-id="6c7a2-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-137">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c7a2-138">Is Indexed</span></span>             | <span data-ttu-id="6c7a2-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-139">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c7a2-140">In Global Catalog</span></span>      | <span data-ttu-id="6c7a2-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-141">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c7a2-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c7a2-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c7a2-143">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="6c7a2-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c7a2-144">Range-Lower</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c7a2-145">Range-Upper</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-146">Search-Flags</span></span>           | <span data-ttu-id="6c7a2-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c7a2-147">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-148">System-Flags</span></span>           | <span data-ttu-id="6c7a2-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c7a2-149">0x00000010</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c7a2-150">Classes used in</span></span>        | [<span data-ttu-id="6c7a2-151">**Точка подключения COM**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-151">**Com-Connection-Point**</span></span>](c-comconnectionpoint.md)<br/> [<span data-ttu-id="6c7a2-152">**Память**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-152">**Storage**</span></span>](c-storage.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6c7a2-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6c7a2-153">Windows Server 2003</span></span>



| <span data-ttu-id="6c7a2-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-154">Entry</span></span> | <span data-ttu-id="6c7a2-155">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-155">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a2-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c7a2-156">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-157">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c7a2-158">System-Only</span></span>            | <span data-ttu-id="6c7a2-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-159">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c7a2-160">Is-Single-Valued</span></span>       | <span data-ttu-id="6c7a2-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-161">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c7a2-162">Is Indexed</span></span>             | <span data-ttu-id="6c7a2-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-163">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c7a2-164">In Global Catalog</span></span>      | <span data-ttu-id="6c7a2-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-165">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c7a2-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c7a2-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c7a2-167">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="6c7a2-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c7a2-168">Range-Lower</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c7a2-169">Range-Upper</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-170">Search-Flags</span></span>           | <span data-ttu-id="6c7a2-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c7a2-171">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-172">System-Flags</span></span>           | <span data-ttu-id="6c7a2-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c7a2-173">0x00000010</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c7a2-174">Classes used in</span></span>        | [<span data-ttu-id="6c7a2-175">**Точка подключения COM**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-175">**Com-Connection-Point**</span></span>](c-comconnectionpoint.md)<br/> [<span data-ttu-id="6c7a2-176">**Память**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-176">**Storage**</span></span>](c-storage.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6c7a2-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6c7a2-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6c7a2-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-178">Entry</span></span> | <span data-ttu-id="6c7a2-179">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-179">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a2-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c7a2-180">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-181">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c7a2-182">System-Only</span></span>            | <span data-ttu-id="6c7a2-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-183">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c7a2-184">Is-Single-Valued</span></span>       | <span data-ttu-id="6c7a2-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-185">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c7a2-186">Is Indexed</span></span>             | <span data-ttu-id="6c7a2-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-187">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c7a2-188">In Global Catalog</span></span>      | <span data-ttu-id="6c7a2-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-189">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c7a2-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c7a2-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c7a2-191">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="6c7a2-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c7a2-192">Range-Lower</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c7a2-193">Range-Upper</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-194">Search-Flags</span></span>           | <span data-ttu-id="6c7a2-195">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c7a2-195">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-196">System-Flags</span></span>           | <span data-ttu-id="6c7a2-197">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c7a2-197">0x00000010</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c7a2-198">Classes used in</span></span>        | [<span data-ttu-id="6c7a2-199">**Точка подключения COM**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-199">**Com-Connection-Point**</span></span>](c-comconnectionpoint.md)<br/> [<span data-ttu-id="6c7a2-200">**Память**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-200">**Storage**</span></span>](c-storage.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6c7a2-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c7a2-201">Windows Server 2008</span></span>



| <span data-ttu-id="6c7a2-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-202">Entry</span></span> | <span data-ttu-id="6c7a2-203">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a2-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c7a2-204">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-205">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c7a2-206">System-Only</span></span>            | <span data-ttu-id="6c7a2-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-207">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c7a2-208">Is-Single-Valued</span></span>       | <span data-ttu-id="6c7a2-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-209">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c7a2-210">Is Indexed</span></span>             | <span data-ttu-id="6c7a2-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-211">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c7a2-212">In Global Catalog</span></span>      | <span data-ttu-id="6c7a2-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-213">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c7a2-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c7a2-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c7a2-215">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="6c7a2-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c7a2-216">Range-Lower</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c7a2-217">Range-Upper</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-218">Search-Flags</span></span>           | <span data-ttu-id="6c7a2-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c7a2-219">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-220">System-Flags</span></span>           | <span data-ttu-id="6c7a2-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c7a2-221">0x00000010</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c7a2-222">Classes used in</span></span>        | [<span data-ttu-id="6c7a2-223">**Точка подключения COM**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-223">**Com-Connection-Point**</span></span>](c-comconnectionpoint.md)<br/> [<span data-ttu-id="6c7a2-224">**Память**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-224">**Storage**</span></span>](c-storage.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6c7a2-225">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6c7a2-225">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6c7a2-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-226">Entry</span></span> | <span data-ttu-id="6c7a2-227">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-227">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a2-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c7a2-228">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-229">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c7a2-230">System-Only</span></span>            | <span data-ttu-id="6c7a2-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-231">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c7a2-232">Is-Single-Valued</span></span>       | <span data-ttu-id="6c7a2-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-233">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c7a2-234">Is Indexed</span></span>             | <span data-ttu-id="6c7a2-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-235">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c7a2-236">In Global Catalog</span></span>      | <span data-ttu-id="6c7a2-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-237">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c7a2-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c7a2-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c7a2-239">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="6c7a2-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c7a2-240">Range-Lower</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c7a2-241">Range-Upper</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-242">Search-Flags</span></span>           | <span data-ttu-id="6c7a2-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c7a2-243">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-244">System-Flags</span></span>           | <span data-ttu-id="6c7a2-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c7a2-245">0x00000010</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c7a2-246">Classes used in</span></span>        | [<span data-ttu-id="6c7a2-247">**Точка подключения COM**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-247">**Com-Connection-Point**</span></span>](c-comconnectionpoint.md)<br/> [<span data-ttu-id="6c7a2-248">**Память**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-248">**Storage**</span></span>](c-storage.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6c7a2-249">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6c7a2-249">Windows Server 2012</span></span>



| <span data-ttu-id="6c7a2-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="6c7a2-250">Entry</span></span> | <span data-ttu-id="6c7a2-251">Значение</span><span class="sxs-lookup"><span data-stu-id="6c7a2-251">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7a2-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6c7a2-252">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6c7a2-253">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="6c7a2-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="6c7a2-254">System-Only</span></span>            | <span data-ttu-id="6c7a2-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-255">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6c7a2-256">Is-Single-Valued</span></span>       | <span data-ttu-id="6c7a2-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-257">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6c7a2-258">Is Indexed</span></span>             | <span data-ttu-id="6c7a2-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-259">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6c7a2-260">In Global Catalog</span></span>      | <span data-ttu-id="6c7a2-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="6c7a2-261">False</span></span>                                                                                                   |
| <span data-ttu-id="6c7a2-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6c7a2-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="6c7a2-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6c7a2-263">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="6c7a2-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6c7a2-264">Range-Lower</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6c7a2-265">Range-Upper</span></span>            | \-                                                                                                      |
| <span data-ttu-id="6c7a2-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-266">Search-Flags</span></span>           | <span data-ttu-id="6c7a2-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c7a2-267">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6c7a2-268">System-Flags</span></span>           | <span data-ttu-id="6c7a2-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6c7a2-269">0x00000010</span></span>                                                                                              |
| <span data-ttu-id="6c7a2-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6c7a2-270">Classes used in</span></span>        | [<span data-ttu-id="6c7a2-271">**Точка подключения COM**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-271">**Com-Connection-Point**</span></span>](c-comconnectionpoint.md)<br/> [<span data-ttu-id="6c7a2-272">**Память**</span><span class="sxs-lookup"><span data-stu-id="6c7a2-272">**Storage**</span></span>](c-storage.md)<br/> |



 

 





