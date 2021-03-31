---
title: MS-TS-повторное подключение — атрибут действия
description: Действие повторного подключения сеанса служб терминалов указывает, разрешено ли повторное подключение к отключенному сеансу служб терминалов с любого клиентского компьютера.
ms.assetid: 093c2477-aed6-4736-9c8a-05aeca539cf8
ms.tgt_platform: multiple
keywords:
- Active-TS-повторное подключение — схема AD атрибута действия
- Схема AD атрибута Мстсреконнектионактион
topic_type:
- apiref
api_name:
- ms-TS-Reconnection-Action
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e09931ec652f2fdd1e9ae6c6cec71e7a896a9f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893754"
---
# <a name="ms-ts-reconnection-action-attribute"></a><span data-ttu-id="1c221-105">MS-TS-повторное подключение — атрибут действия</span><span class="sxs-lookup"><span data-stu-id="1c221-105">ms-TS-Reconnection-Action attribute</span></span>

<span data-ttu-id="1c221-106">Действие повторного подключения сеанса служб терминалов указывает, разрешено ли повторное подключение к отключенному сеансу служб терминалов с любого клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c221-106">Terminal Services session Reconnection Action specifies whether to allow reconnection to a disconnected Terminal Services session from any client computer.</span></span>



| <span data-ttu-id="1c221-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c221-107">Entry</span></span> | <span data-ttu-id="1c221-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1c221-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1c221-109">CN</span><span class="sxs-lookup"><span data-stu-id="1c221-109">CN</span></span>                | <span data-ttu-id="1c221-110">MS-TS-повторное подключение — действие</span><span class="sxs-lookup"><span data-stu-id="1c221-110">ms-TS-Reconnection-Action</span></span>            |
| <span data-ttu-id="1c221-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1c221-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1c221-112">мстсреконнектионактион</span><span class="sxs-lookup"><span data-stu-id="1c221-112">msTSReconnectionAction</span></span>               |
| <span data-ttu-id="1c221-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1c221-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="1c221-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1c221-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1c221-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1c221-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1c221-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1c221-116">Attribute-Id</span></span>      | <span data-ttu-id="1c221-117">1.2.840.113556.1.4.1984</span><span class="sxs-lookup"><span data-stu-id="1c221-117">1.2.840.113556.1.4.1984</span></span>              |
| <span data-ttu-id="1c221-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1c221-118">System-Id-Guid</span></span>    | <span data-ttu-id="1c221-119">366ed7ca-3e18-4c7f-abae-351a01e4b4f7</span><span class="sxs-lookup"><span data-stu-id="1c221-119">366ed7ca-3e18-4c7f-abae-351a01e4b4f7</span></span> |
| <span data-ttu-id="1c221-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c221-120">Syntax</span></span>            | [<span data-ttu-id="1c221-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="1c221-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="1c221-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1c221-122">Implementations</span></span>

-   [<span data-ttu-id="1c221-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1c221-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1c221-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1c221-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1c221-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1c221-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="1c221-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c221-126">Windows Server 2008</span></span>



| <span data-ttu-id="1c221-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c221-127">Entry</span></span> | <span data-ttu-id="1c221-128">Значение</span><span class="sxs-lookup"><span data-stu-id="1c221-128">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1c221-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c221-129">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1c221-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c221-130">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1c221-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c221-131">System-Only</span></span>            | <span data-ttu-id="1c221-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-132">False</span></span>                             |
| <span data-ttu-id="1c221-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c221-133">Is-Single-Valued</span></span>       | <span data-ttu-id="1c221-134">True</span><span class="sxs-lookup"><span data-stu-id="1c221-134">True</span></span>                              |
| <span data-ttu-id="1c221-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c221-135">Is Indexed</span></span>             | <span data-ttu-id="1c221-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-136">False</span></span>                             |
| <span data-ttu-id="1c221-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c221-137">In Global Catalog</span></span>      | <span data-ttu-id="1c221-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-138">False</span></span>                             |
| <span data-ttu-id="1c221-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c221-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c221-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c221-140">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1c221-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c221-141">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1c221-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c221-142">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1c221-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c221-143">Search-Flags</span></span>           | <span data-ttu-id="1c221-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c221-144">0x00000000</span></span>                        |
| <span data-ttu-id="1c221-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c221-145">System-Flags</span></span>           | <span data-ttu-id="1c221-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c221-146">0x00000010</span></span>                        |
| <span data-ttu-id="1c221-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c221-147">Classes used in</span></span>        | [<span data-ttu-id="1c221-148">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1c221-148">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1c221-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c221-149">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1c221-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c221-150">Entry</span></span> | <span data-ttu-id="1c221-151">Значение</span><span class="sxs-lookup"><span data-stu-id="1c221-151">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1c221-152">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c221-152">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1c221-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c221-153">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1c221-154">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c221-154">System-Only</span></span>            | <span data-ttu-id="1c221-155">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-155">False</span></span>                             |
| <span data-ttu-id="1c221-156">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c221-156">Is-Single-Valued</span></span>       | <span data-ttu-id="1c221-157">True</span><span class="sxs-lookup"><span data-stu-id="1c221-157">True</span></span>                              |
| <span data-ttu-id="1c221-158">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c221-158">Is Indexed</span></span>             | <span data-ttu-id="1c221-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-159">False</span></span>                             |
| <span data-ttu-id="1c221-160">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c221-160">In Global Catalog</span></span>      | <span data-ttu-id="1c221-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-161">False</span></span>                             |
| <span data-ttu-id="1c221-162">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c221-162">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c221-163">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c221-163">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1c221-164">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c221-164">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1c221-165">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c221-165">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1c221-166">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c221-166">Search-Flags</span></span>           | <span data-ttu-id="1c221-167">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c221-167">0x00000000</span></span>                        |
| <span data-ttu-id="1c221-168">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c221-168">System-Flags</span></span>           | <span data-ttu-id="1c221-169">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c221-169">0x00000010</span></span>                        |
| <span data-ttu-id="1c221-170">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c221-170">Classes used in</span></span>        | [<span data-ttu-id="1c221-171">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1c221-171">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1c221-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c221-172">Windows Server 2012</span></span>



| <span data-ttu-id="1c221-173">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c221-173">Entry</span></span> | <span data-ttu-id="1c221-174">Значение</span><span class="sxs-lookup"><span data-stu-id="1c221-174">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1c221-175">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c221-175">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1c221-176">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c221-176">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1c221-177">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c221-177">System-Only</span></span>            | <span data-ttu-id="1c221-178">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-178">False</span></span>                             |
| <span data-ttu-id="1c221-179">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c221-179">Is-Single-Valued</span></span>       | <span data-ttu-id="1c221-180">True</span><span class="sxs-lookup"><span data-stu-id="1c221-180">True</span></span>                              |
| <span data-ttu-id="1c221-181">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c221-181">Is Indexed</span></span>             | <span data-ttu-id="1c221-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-182">False</span></span>                             |
| <span data-ttu-id="1c221-183">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c221-183">In Global Catalog</span></span>      | <span data-ttu-id="1c221-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c221-184">False</span></span>                             |
| <span data-ttu-id="1c221-185">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c221-185">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c221-186">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c221-186">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1c221-187">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c221-187">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="1c221-188">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c221-188">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="1c221-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c221-189">Search-Flags</span></span>           | <span data-ttu-id="1c221-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c221-190">0x00000000</span></span>                        |
| <span data-ttu-id="1c221-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c221-191">System-Flags</span></span>           | <span data-ttu-id="1c221-192">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c221-192">0x00000010</span></span>                        |
| <span data-ttu-id="1c221-193">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c221-193">Classes used in</span></span>        | [<span data-ttu-id="1c221-194">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="1c221-194">**User**</span></span>](c-user.md)<br/> |



 

 





