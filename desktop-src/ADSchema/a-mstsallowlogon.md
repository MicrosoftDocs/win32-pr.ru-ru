---
title: атрибут MS-TS-Allow-logon
description: Указывает, разрешено ли пользователю входить на сервер терминалов. Значение равно 1, если вход разрешен, и 0, если вход запрещен.
ms.assetid: 9cd6edbc-f8e7-4933-9f62-1e34e3d31fb7
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута MS-TS-Allow-logon
- Схема AD атрибута Мстсалловлогон
topic_type:
- apiref
api_name:
- ms-TS-Allow-Logon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd78662167e281ea720f2ad5d98f25c2f5c4ae
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893390"
---
# <a name="ms-ts-allow-logon-attribute"></a><span data-ttu-id="294ef-106">атрибут MS-TS-Allow-logon</span><span class="sxs-lookup"><span data-stu-id="294ef-106">ms-TS-Allow-Logon attribute</span></span>

<span data-ttu-id="294ef-107">Указывает, разрешено ли пользователю входить на сервер терминалов.</span><span class="sxs-lookup"><span data-stu-id="294ef-107">Specifies whether the user is allowed to log on to the Terminal Server.</span></span> <span data-ttu-id="294ef-108">Значение равно 1, если вход разрешен, и 0, если вход запрещен.</span><span class="sxs-lookup"><span data-stu-id="294ef-108">The value is 1 if logon is allowed, and 0 if logon is not allowed.</span></span>



| <span data-ttu-id="294ef-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="294ef-109">Entry</span></span> | <span data-ttu-id="294ef-110">Значение</span><span class="sxs-lookup"><span data-stu-id="294ef-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="294ef-111">CN</span><span class="sxs-lookup"><span data-stu-id="294ef-111">CN</span></span>                | <span data-ttu-id="294ef-112">MS-TS-Allow-logon</span><span class="sxs-lookup"><span data-stu-id="294ef-112">ms-TS-Allow-Logon</span></span>                    |
| <span data-ttu-id="294ef-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="294ef-113">Ldap-Display-Name</span></span> | <span data-ttu-id="294ef-114">мстсалловлогон</span><span class="sxs-lookup"><span data-stu-id="294ef-114">msTSAllowLogon</span></span>                       |
| <span data-ttu-id="294ef-115">Размер</span><span class="sxs-lookup"><span data-stu-id="294ef-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="294ef-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="294ef-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="294ef-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="294ef-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="294ef-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="294ef-118">Attribute-Id</span></span>      | <span data-ttu-id="294ef-119">1.2.840.113556.1.4.1979</span><span class="sxs-lookup"><span data-stu-id="294ef-119">1.2.840.113556.1.4.1979</span></span>              |
| <span data-ttu-id="294ef-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="294ef-120">System-Id-Guid</span></span>    | <span data-ttu-id="294ef-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span><span class="sxs-lookup"><span data-stu-id="294ef-121">3a0cd464-bc54-40e7-93ae-a646a6ecc4b4</span></span> |
| <span data-ttu-id="294ef-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="294ef-122">Syntax</span></span>            | [<span data-ttu-id="294ef-123">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="294ef-123">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="294ef-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="294ef-124">Implementations</span></span>

-   [<span data-ttu-id="294ef-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="294ef-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="294ef-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="294ef-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="294ef-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="294ef-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="294ef-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="294ef-128">Windows Server 2008</span></span>



| <span data-ttu-id="294ef-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="294ef-129">Entry</span></span> | <span data-ttu-id="294ef-130">Значение</span><span class="sxs-lookup"><span data-stu-id="294ef-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="294ef-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="294ef-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="294ef-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294ef-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="294ef-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="294ef-133">System-Only</span></span>            | <span data-ttu-id="294ef-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-134">False</span></span>                             |
| <span data-ttu-id="294ef-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="294ef-135">Is-Single-Valued</span></span>       | <span data-ttu-id="294ef-136">True</span><span class="sxs-lookup"><span data-stu-id="294ef-136">True</span></span>                              |
| <span data-ttu-id="294ef-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="294ef-137">Is Indexed</span></span>             | <span data-ttu-id="294ef-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-138">False</span></span>                             |
| <span data-ttu-id="294ef-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="294ef-139">In Global Catalog</span></span>      | <span data-ttu-id="294ef-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-140">False</span></span>                             |
| <span data-ttu-id="294ef-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="294ef-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="294ef-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="294ef-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="294ef-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294ef-143">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="294ef-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294ef-144">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="294ef-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294ef-145">Search-Flags</span></span>           | <span data-ttu-id="294ef-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294ef-146">0x00000000</span></span>                        |
| <span data-ttu-id="294ef-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294ef-147">System-Flags</span></span>           | <span data-ttu-id="294ef-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294ef-148">0x00000010</span></span>                        |
| <span data-ttu-id="294ef-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="294ef-149">Classes used in</span></span>        | [<span data-ttu-id="294ef-150">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="294ef-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="294ef-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="294ef-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="294ef-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="294ef-152">Entry</span></span> | <span data-ttu-id="294ef-153">Значение</span><span class="sxs-lookup"><span data-stu-id="294ef-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="294ef-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="294ef-154">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="294ef-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294ef-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="294ef-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="294ef-156">System-Only</span></span>            | <span data-ttu-id="294ef-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-157">False</span></span>                             |
| <span data-ttu-id="294ef-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="294ef-158">Is-Single-Valued</span></span>       | <span data-ttu-id="294ef-159">True</span><span class="sxs-lookup"><span data-stu-id="294ef-159">True</span></span>                              |
| <span data-ttu-id="294ef-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="294ef-160">Is Indexed</span></span>             | <span data-ttu-id="294ef-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-161">False</span></span>                             |
| <span data-ttu-id="294ef-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="294ef-162">In Global Catalog</span></span>      | <span data-ttu-id="294ef-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-163">False</span></span>                             |
| <span data-ttu-id="294ef-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="294ef-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="294ef-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="294ef-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="294ef-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294ef-166">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="294ef-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294ef-167">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="294ef-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294ef-168">Search-Flags</span></span>           | <span data-ttu-id="294ef-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294ef-169">0x00000000</span></span>                        |
| <span data-ttu-id="294ef-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294ef-170">System-Flags</span></span>           | <span data-ttu-id="294ef-171">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294ef-171">0x00000010</span></span>                        |
| <span data-ttu-id="294ef-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="294ef-172">Classes used in</span></span>        | [<span data-ttu-id="294ef-173">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="294ef-173">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="294ef-174">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="294ef-174">Windows Server 2012</span></span>



| <span data-ttu-id="294ef-175">Ввод</span><span class="sxs-lookup"><span data-stu-id="294ef-175">Entry</span></span> | <span data-ttu-id="294ef-176">Значение</span><span class="sxs-lookup"><span data-stu-id="294ef-176">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="294ef-177">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="294ef-177">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="294ef-178">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="294ef-178">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="294ef-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="294ef-179">System-Only</span></span>            | <span data-ttu-id="294ef-180">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-180">False</span></span>                             |
| <span data-ttu-id="294ef-181">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="294ef-181">Is-Single-Valued</span></span>       | <span data-ttu-id="294ef-182">True</span><span class="sxs-lookup"><span data-stu-id="294ef-182">True</span></span>                              |
| <span data-ttu-id="294ef-183">Индексируется</span><span class="sxs-lookup"><span data-stu-id="294ef-183">Is Indexed</span></span>             | <span data-ttu-id="294ef-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-184">False</span></span>                             |
| <span data-ttu-id="294ef-185">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="294ef-185">In Global Catalog</span></span>      | <span data-ttu-id="294ef-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="294ef-186">False</span></span>                             |
| <span data-ttu-id="294ef-187">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="294ef-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="294ef-188">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="294ef-188">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="294ef-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="294ef-189">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="294ef-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="294ef-190">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="294ef-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="294ef-191">Search-Flags</span></span>           | <span data-ttu-id="294ef-192">0x00000000</span><span class="sxs-lookup"><span data-stu-id="294ef-192">0x00000000</span></span>                        |
| <span data-ttu-id="294ef-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="294ef-193">System-Flags</span></span>           | <span data-ttu-id="294ef-194">0x00000010</span><span class="sxs-lookup"><span data-stu-id="294ef-194">0x00000010</span></span>                        |
| <span data-ttu-id="294ef-195">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="294ef-195">Classes used in</span></span>        | [<span data-ttu-id="294ef-196">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="294ef-196">**User**</span></span>](c-user.md)<br/> |



 

 





