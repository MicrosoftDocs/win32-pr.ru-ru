---
title: Атрибут ms-DS-"-User-кэшируемые-at-RODC"
description: Для Read-Only контроллера домена (RODC) определяет, можно ли кэшировать секреты указанного пользователя.
ms.assetid: 1118d0a9-2219-478a-82b0-8ea4bbeae47d
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS--User-кэшируемые-at-RODC
- Схема AD атрибута msDS-Исусеркачаблеатродк
topic_type:
- apiref
api_name:
- ms-DS-Is-User-Cachable-At-Rodc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5699208cebe4c49321186813a64611f79ec52f4b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103805015"
---
# <a name="ms-ds-is-user-cachable-at-rodc-attribute"></a><span data-ttu-id="de357-105">Атрибут ms-DS-"-User-кэшируемые-at-RODC"</span><span class="sxs-lookup"><span data-stu-id="de357-105">ms-DS-Is-User-Cachable-At-Rodc attribute</span></span>

<span data-ttu-id="de357-106">Для Read-Only контроллера домена (RODC) определяет, можно ли кэшировать секреты указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="de357-106">For a Read-Only Domain Controller (RODC), identifies whether the specified user's secrets can be cached.</span></span>



| <span data-ttu-id="de357-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="de357-107">Entry</span></span> | <span data-ttu-id="de357-108">Значение</span><span class="sxs-lookup"><span data-stu-id="de357-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="de357-109">CN</span><span class="sxs-lookup"><span data-stu-id="de357-109">CN</span></span>                | <span data-ttu-id="de357-110">MS-DS-"-пользователь-кэшируемые-at-RODC"</span><span class="sxs-lookup"><span data-stu-id="de357-110">ms-DS-Is-User-Cachable-At-Rodc</span></span>       |
| <span data-ttu-id="de357-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="de357-111">Ldap-Display-Name</span></span> | <span data-ttu-id="de357-112">msDS-Исусеркачаблеатродк</span><span class="sxs-lookup"><span data-stu-id="de357-112">msDS-IsUserCachableAtRodc</span></span>            |
| <span data-ttu-id="de357-113">Размер</span><span class="sxs-lookup"><span data-stu-id="de357-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="de357-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="de357-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="de357-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="de357-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="de357-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="de357-116">Attribute-Id</span></span>      | <span data-ttu-id="de357-117">1.2.840.113556.1.4.2025</span><span class="sxs-lookup"><span data-stu-id="de357-117">1.2.840.113556.1.4.2025</span></span>              |
| <span data-ttu-id="de357-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="de357-118">System-Id-Guid</span></span>    | <span data-ttu-id="de357-119">fe01245a-341f-4556-951f-48c033a89050</span><span class="sxs-lookup"><span data-stu-id="de357-119">fe01245a-341f-4556-951f-48c033a89050</span></span> |
| <span data-ttu-id="de357-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de357-120">Syntax</span></span>            | [<span data-ttu-id="de357-121">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="de357-121">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="de357-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="de357-122">Implementations</span></span>

-   [<span data-ttu-id="de357-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="de357-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="de357-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="de357-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="de357-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="de357-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="de357-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de357-126">Windows Server 2008</span></span>



| <span data-ttu-id="de357-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="de357-127">Entry</span></span> | <span data-ttu-id="de357-128">Значение</span><span class="sxs-lookup"><span data-stu-id="de357-128">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de357-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de357-129">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="de357-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de357-130">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="de357-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="de357-131">System-Only</span></span>            | <span data-ttu-id="de357-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-132">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de357-133">Is-Single-Valued</span></span>       | <span data-ttu-id="de357-134">True</span><span class="sxs-lookup"><span data-stu-id="de357-134">True</span></span>                                                                                                                     |
| <span data-ttu-id="de357-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de357-135">Is Indexed</span></span>             | <span data-ttu-id="de357-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-136">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de357-137">In Global Catalog</span></span>      | <span data-ttu-id="de357-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-138">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de357-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="de357-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de357-140">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="de357-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de357-141">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="de357-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de357-142">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="de357-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de357-143">Search-Flags</span></span>           | <span data-ttu-id="de357-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de357-144">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="de357-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de357-145">System-Flags</span></span>           | <span data-ttu-id="de357-146">0x00000014</span><span class="sxs-lookup"><span data-stu-id="de357-146">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="de357-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de357-147">Classes used in</span></span>        | [<span data-ttu-id="de357-148">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="de357-148">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="de357-149">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="de357-149">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="de357-150">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="de357-150">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="de357-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="de357-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="de357-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="de357-152">Entry</span></span> | <span data-ttu-id="de357-153">Значение</span><span class="sxs-lookup"><span data-stu-id="de357-153">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de357-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de357-154">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="de357-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de357-155">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="de357-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="de357-156">System-Only</span></span>            | <span data-ttu-id="de357-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-157">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de357-158">Is-Single-Valued</span></span>       | <span data-ttu-id="de357-159">True</span><span class="sxs-lookup"><span data-stu-id="de357-159">True</span></span>                                                                                                                     |
| <span data-ttu-id="de357-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de357-160">Is Indexed</span></span>             | <span data-ttu-id="de357-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-161">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de357-162">In Global Catalog</span></span>      | <span data-ttu-id="de357-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-163">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de357-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="de357-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de357-165">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="de357-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de357-166">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="de357-167">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de357-167">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="de357-168">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de357-168">Search-Flags</span></span>           | <span data-ttu-id="de357-169">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de357-169">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="de357-170">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de357-170">System-Flags</span></span>           | <span data-ttu-id="de357-171">0x00000014</span><span class="sxs-lookup"><span data-stu-id="de357-171">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="de357-172">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de357-172">Classes used in</span></span>        | [<span data-ttu-id="de357-173">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="de357-173">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="de357-174">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="de357-174">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="de357-175">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="de357-175">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="de357-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de357-176">Windows Server 2012</span></span>



| <span data-ttu-id="de357-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="de357-177">Entry</span></span> | <span data-ttu-id="de357-178">Значение</span><span class="sxs-lookup"><span data-stu-id="de357-178">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de357-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="de357-179">Link-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="de357-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="de357-180">MAPI-Id</span></span>                | \-                                                                                                                       |
| <span data-ttu-id="de357-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="de357-181">System-Only</span></span>            | <span data-ttu-id="de357-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-182">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="de357-183">Is-Single-Valued</span></span>       | <span data-ttu-id="de357-184">True</span><span class="sxs-lookup"><span data-stu-id="de357-184">True</span></span>                                                                                                                     |
| <span data-ttu-id="de357-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="de357-185">Is Indexed</span></span>             | <span data-ttu-id="de357-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-186">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="de357-187">In Global Catalog</span></span>      | <span data-ttu-id="de357-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="de357-188">False</span></span>                                                                                                                    |
| <span data-ttu-id="de357-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="de357-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="de357-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="de357-190">O:BAG:BAD:S:</span></span>                                                                                                             |
| <span data-ttu-id="de357-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="de357-191">Range-Lower</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="de357-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="de357-192">Range-Upper</span></span>            | \-                                                                                                                       |
| <span data-ttu-id="de357-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="de357-193">Search-Flags</span></span>           | <span data-ttu-id="de357-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="de357-194">0x00000000</span></span>                                                                                                               |
| <span data-ttu-id="de357-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="de357-195">System-Flags</span></span>           | <span data-ttu-id="de357-196">0x00000014</span><span class="sxs-lookup"><span data-stu-id="de357-196">0x00000014</span></span>                                                                                                               |
| <span data-ttu-id="de357-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="de357-197">Classes used in</span></span>        | [<span data-ttu-id="de357-198">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="de357-198">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="de357-199">**NTDS-DSA**</span><span class="sxs-lookup"><span data-stu-id="de357-199">**NTDS-DSA**</span></span>](c-ntdsdsa.md)<br/> [<span data-ttu-id="de357-200">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="de357-200">**Server**</span></span>](c-server.md)<br/> |



 

 





