---
title: Control-Access-Rights, атрибут
description: Используется службой безопасности DS для определения пользователей, которые могут выполнять определенные операции с объектом узла.
ms.assetid: 5e717160-519c-4e5a-b18f-05ee767a66a3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Rights Control-Access
- Схема AD атрибута Контролакцессригхтс
topic_type:
- apiref
api_name:
- Control-Access-Rights
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3ee9075cfaf4c5bbfbf17e8e2cfef6166be032
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494097"
---
# <a name="control-access-rights-attribute"></a><span data-ttu-id="bf31b-105">Control-Access-Rights, атрибут</span><span class="sxs-lookup"><span data-stu-id="bf31b-105">Control-Access-Rights attribute</span></span>

<span data-ttu-id="bf31b-106">Используется службой безопасности DS для определения пользователей, которые могут выполнять определенные операции с объектом узла.</span><span class="sxs-lookup"><span data-stu-id="bf31b-106">Used by DS Security to determine which users can perform specific operations on the host object.</span></span>



| <span data-ttu-id="bf31b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-107">Entry</span></span> | <span data-ttu-id="bf31b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="bf31b-109">CN</span><span class="sxs-lookup"><span data-stu-id="bf31b-109">CN</span></span>                | <span data-ttu-id="bf31b-110">Управление — права доступа</span><span class="sxs-lookup"><span data-stu-id="bf31b-110">Control-Access-Rights</span></span>                                 |
| <span data-ttu-id="bf31b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bf31b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="bf31b-112">контролакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="bf31b-112">controlAccessRights</span></span>                                   |
| <span data-ttu-id="bf31b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="bf31b-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="bf31b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bf31b-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="bf31b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bf31b-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="bf31b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-116">Attribute-Id</span></span>      | <span data-ttu-id="bf31b-117">1.2.840.113556.1.4.200</span><span class="sxs-lookup"><span data-stu-id="bf31b-117">1.2.840.113556.1.4.200</span></span>                                |
| <span data-ttu-id="bf31b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bf31b-118">System-Id-Guid</span></span>    | <span data-ttu-id="bf31b-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="bf31b-119">6da8a4fc-0e52-11d0-a286-00aa003049e2</span></span>                  |
| <span data-ttu-id="bf31b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf31b-120">Syntax</span></span>            | [<span data-ttu-id="bf31b-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="bf31b-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="bf31b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bf31b-122">Implementations</span></span>

-   [<span data-ttu-id="bf31b-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="bf31b-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="bf31b-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="bf31b-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="bf31b-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="bf31b-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="bf31b-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bf31b-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bf31b-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bf31b-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bf31b-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bf31b-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="bf31b-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf31b-129">Windows 2000 Server</span></span>



| <span data-ttu-id="bf31b-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-130">Entry</span></span> | <span data-ttu-id="bf31b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-131">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31b-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf31b-132">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-133">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31b-134">System-Only</span></span>            | <span data-ttu-id="bf31b-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-135">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf31b-136">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31b-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-137">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf31b-138">Is Indexed</span></span>             | <span data-ttu-id="bf31b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-139">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf31b-140">In Global Catalog</span></span>      | <span data-ttu-id="bf31b-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-141">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf31b-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31b-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf31b-143">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="bf31b-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31b-144">Range-Lower</span></span>            | <span data-ttu-id="bf31b-145">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-145">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31b-146">Range-Upper</span></span>            | <span data-ttu-id="bf31b-147">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-147">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-148">Search-Flags</span></span>           | <span data-ttu-id="bf31b-149">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31b-149">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-150">System-Flags</span></span>           | <span data-ttu-id="bf31b-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31b-151">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf31b-152">Classes used in</span></span>        | [<span data-ttu-id="bf31b-153">**Группа**</span><span class="sxs-lookup"><span data-stu-id="bf31b-153">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="bf31b-154">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="bf31b-154">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bf31b-155">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bf31b-155">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="bf31b-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf31b-156">Windows Server 2003</span></span>



| <span data-ttu-id="bf31b-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-157">Entry</span></span> | <span data-ttu-id="bf31b-158">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31b-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf31b-159">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-160">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31b-161">System-Only</span></span>            | <span data-ttu-id="bf31b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-162">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf31b-163">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-164">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf31b-165">Is Indexed</span></span>             | <span data-ttu-id="bf31b-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-166">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf31b-167">In Global Catalog</span></span>      | <span data-ttu-id="bf31b-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-168">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf31b-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31b-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf31b-170">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="bf31b-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31b-171">Range-Lower</span></span>            | <span data-ttu-id="bf31b-172">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-172">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31b-173">Range-Upper</span></span>            | <span data-ttu-id="bf31b-174">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-174">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-175">Search-Flags</span></span>           | <span data-ttu-id="bf31b-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31b-176">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-177">System-Flags</span></span>           | <span data-ttu-id="bf31b-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31b-178">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf31b-179">Classes used in</span></span>        | [<span data-ttu-id="bf31b-180">**Группа**</span><span class="sxs-lookup"><span data-stu-id="bf31b-180">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="bf31b-181">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="bf31b-181">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bf31b-182">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bf31b-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="bf31b-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="bf31b-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="bf31b-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-184">Entry</span></span> | <span data-ttu-id="bf31b-185">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-185">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31b-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf31b-186">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-187">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31b-188">System-Only</span></span>            | <span data-ttu-id="bf31b-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-189">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf31b-190">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31b-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-191">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf31b-192">Is Indexed</span></span>             | <span data-ttu-id="bf31b-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-193">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf31b-194">In Global Catalog</span></span>      | <span data-ttu-id="bf31b-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-195">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf31b-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31b-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf31b-197">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="bf31b-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31b-198">Range-Lower</span></span>            | <span data-ttu-id="bf31b-199">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-199">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31b-200">Range-Upper</span></span>            | <span data-ttu-id="bf31b-201">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-201">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-202">Search-Flags</span></span>           | <span data-ttu-id="bf31b-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31b-203">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-204">System-Flags</span></span>           | <span data-ttu-id="bf31b-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31b-205">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-206">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf31b-206">Classes used in</span></span>        | [<span data-ttu-id="bf31b-207">**Группа**</span><span class="sxs-lookup"><span data-stu-id="bf31b-207">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="bf31b-208">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="bf31b-208">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bf31b-209">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bf31b-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="bf31b-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf31b-210">Windows Server 2008</span></span>



| <span data-ttu-id="bf31b-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-211">Entry</span></span> | <span data-ttu-id="bf31b-212">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-212">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31b-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf31b-213">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-214">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31b-215">System-Only</span></span>            | <span data-ttu-id="bf31b-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-216">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf31b-217">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31b-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-218">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf31b-219">Is Indexed</span></span>             | <span data-ttu-id="bf31b-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-220">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf31b-221">In Global Catalog</span></span>      | <span data-ttu-id="bf31b-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-222">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf31b-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31b-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf31b-224">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="bf31b-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31b-225">Range-Lower</span></span>            | <span data-ttu-id="bf31b-226">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-226">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31b-227">Range-Upper</span></span>            | <span data-ttu-id="bf31b-228">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-228">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-229">Search-Flags</span></span>           | <span data-ttu-id="bf31b-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31b-230">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-231">System-Flags</span></span>           | <span data-ttu-id="bf31b-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31b-232">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf31b-233">Classes used in</span></span>        | [<span data-ttu-id="bf31b-234">**Группа**</span><span class="sxs-lookup"><span data-stu-id="bf31b-234">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="bf31b-235">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="bf31b-235">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bf31b-236">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bf31b-236">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bf31b-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bf31b-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bf31b-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-238">Entry</span></span> | <span data-ttu-id="bf31b-239">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-239">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31b-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf31b-240">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-241">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-242">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31b-242">System-Only</span></span>            | <span data-ttu-id="bf31b-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-243">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-244">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf31b-244">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31b-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-245">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-246">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf31b-246">Is Indexed</span></span>             | <span data-ttu-id="bf31b-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-247">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-248">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf31b-248">In Global Catalog</span></span>      | <span data-ttu-id="bf31b-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-249">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-250">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf31b-250">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31b-251">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf31b-251">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="bf31b-252">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31b-252">Range-Lower</span></span>            | <span data-ttu-id="bf31b-253">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-253">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31b-254">Range-Upper</span></span>            | <span data-ttu-id="bf31b-255">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-255">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-256">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-256">Search-Flags</span></span>           | <span data-ttu-id="bf31b-257">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31b-257">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-258">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-258">System-Flags</span></span>           | <span data-ttu-id="bf31b-259">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31b-259">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-260">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf31b-260">Classes used in</span></span>        | [<span data-ttu-id="bf31b-261">**Группа**</span><span class="sxs-lookup"><span data-stu-id="bf31b-261">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="bf31b-262">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="bf31b-262">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bf31b-263">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bf31b-263">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bf31b-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf31b-264">Windows Server 2012</span></span>



| <span data-ttu-id="bf31b-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="bf31b-265">Entry</span></span> | <span data-ttu-id="bf31b-266">Значение</span><span class="sxs-lookup"><span data-stu-id="bf31b-266">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf31b-267">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bf31b-267">Link-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bf31b-268">MAPI-Id</span></span>                | \-                                                                                                                 |
| <span data-ttu-id="bf31b-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="bf31b-269">System-Only</span></span>            | <span data-ttu-id="bf31b-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-270">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-271">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bf31b-271">Is-Single-Valued</span></span>       | <span data-ttu-id="bf31b-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-272">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-273">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bf31b-273">Is Indexed</span></span>             | <span data-ttu-id="bf31b-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-274">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-275">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bf31b-275">In Global Catalog</span></span>      | <span data-ttu-id="bf31b-276">Неверно</span><span class="sxs-lookup"><span data-stu-id="bf31b-276">False</span></span>                                                                                                              |
| <span data-ttu-id="bf31b-277">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bf31b-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="bf31b-278">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bf31b-278">O:BAG:BAD:S:</span></span>                                                                                                       |
| <span data-ttu-id="bf31b-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bf31b-279">Range-Lower</span></span>            | <span data-ttu-id="bf31b-280">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-280">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bf31b-281">Range-Upper</span></span>            | <span data-ttu-id="bf31b-282">16</span><span class="sxs-lookup"><span data-stu-id="bf31b-282">16</span></span>                                                                                                                 |
| <span data-ttu-id="bf31b-283">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-283">Search-Flags</span></span>           | <span data-ttu-id="bf31b-284">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf31b-284">0x00000000</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-285">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bf31b-285">System-Flags</span></span>           | <span data-ttu-id="bf31b-286">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bf31b-286">0x00000010</span></span>                                                                                                         |
| <span data-ttu-id="bf31b-287">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bf31b-287">Classes used in</span></span>        | [<span data-ttu-id="bf31b-288">**Группа**</span><span class="sxs-lookup"><span data-stu-id="bf31b-288">**Group**</span></span>](c-group.md)<br/> [<span data-ttu-id="bf31b-289">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="bf31b-289">**Sam-Domain**</span></span>](c-samdomain.md)<br/> [<span data-ttu-id="bf31b-290">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="bf31b-290">**User**</span></span>](c-user.md)<br/> |



 

 





