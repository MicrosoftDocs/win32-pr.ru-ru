---
title: Атрибут ms-DS-Supported-Encryption-Types
description: Алгоритмы шифрования, поддерживаемые учетными записями пользователя, компьютера или доверия. Примечание. в KDC эти сведения используются при создании билета службы для этой учетной записи.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- служба MS-DS-Supported-Encryption-Types Attribute AD Schema
- Схема AD атрибута msDS-Суппортеденкриптионтипес
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655418"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a><span data-ttu-id="1c59f-105">Атрибут ms-DS-Supported-Encryption-Types</span><span class="sxs-lookup"><span data-stu-id="1c59f-105">ms-DS-Supported-Encryption-Types attribute</span></span>

<span data-ttu-id="1c59f-106">Алгоритмы шифрования, поддерживаемые учетными записями пользователя, компьютера или доверия.</span><span class="sxs-lookup"><span data-stu-id="1c59f-106">The encryption algorithms supported by user, computer or trust accounts.</span></span>

> [!Note]  
> <span data-ttu-id="1c59f-107">KDC использует эти сведения при создании билета службы для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1c59f-107">The KDC uses this information while generating a service ticket for this account.</span></span> <span data-ttu-id="1c59f-108">Службы и компьютеры могут автоматически обновлять этот атрибут в соответствующих учетных записях в Active Directory и поэтому должны иметь доступ на запись к этому атрибуту.</span><span class="sxs-lookup"><span data-stu-id="1c59f-108">Services and Computers can automatically update this attribute on their respective accounts in Active Directory, and therefore need write access to this attribute.</span></span>

 



| <span data-ttu-id="1c59f-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c59f-109">Entry</span></span> | <span data-ttu-id="1c59f-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1c59f-110">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="1c59f-111">CN</span><span class="sxs-lookup"><span data-stu-id="1c59f-111">CN</span></span>                | <span data-ttu-id="1c59f-112">MS-DS-Supported-Encryption-Types</span><span class="sxs-lookup"><span data-stu-id="1c59f-112">ms-DS-Supported-Encryption-Types</span></span>     |
| <span data-ttu-id="1c59f-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1c59f-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1c59f-114">msDS-Суппортеденкриптионтипес</span><span class="sxs-lookup"><span data-stu-id="1c59f-114">msDS-SupportedEncryptionTypes</span></span>        |
| <span data-ttu-id="1c59f-115">Размер</span><span class="sxs-lookup"><span data-stu-id="1c59f-115">Size</span></span>              | \-                                   |
| <span data-ttu-id="1c59f-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1c59f-116">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="1c59f-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1c59f-117">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="1c59f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1c59f-118">Attribute-Id</span></span>      | <span data-ttu-id="1c59f-119">1.2.840.113556.1.4.1963</span><span class="sxs-lookup"><span data-stu-id="1c59f-119">1.2.840.113556.1.4.1963</span></span>              |
| <span data-ttu-id="1c59f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1c59f-120">System-Id-Guid</span></span>    | <span data-ttu-id="1c59f-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span><span class="sxs-lookup"><span data-stu-id="1c59f-121">20119867-1d04-4ab7-9371-cfc3d5df0afd</span></span> |
| <span data-ttu-id="1c59f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c59f-122">Syntax</span></span>            | [<span data-ttu-id="1c59f-123">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="1c59f-123">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="1c59f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1c59f-124">Implementations</span></span>

-   [<span data-ttu-id="1c59f-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1c59f-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1c59f-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1c59f-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1c59f-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1c59f-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="1c59f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c59f-128">Windows Server 2008</span></span>



| <span data-ttu-id="1c59f-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c59f-129">Entry</span></span> | <span data-ttu-id="1c59f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1c59f-130">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c59f-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c59f-131">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="1c59f-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c59f-132">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="1c59f-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c59f-133">System-Only</span></span>            | <span data-ttu-id="1c59f-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-134">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c59f-135">Is-Single-Valued</span></span>       | <span data-ttu-id="1c59f-136">True</span><span class="sxs-lookup"><span data-stu-id="1c59f-136">True</span></span>                                                                                   |
| <span data-ttu-id="1c59f-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c59f-137">Is Indexed</span></span>             | <span data-ttu-id="1c59f-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-138">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c59f-139">In Global Catalog</span></span>      | <span data-ttu-id="1c59f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-140">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c59f-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c59f-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c59f-142">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="1c59f-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c59f-143">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="1c59f-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c59f-144">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="1c59f-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c59f-145">Search-Flags</span></span>           | <span data-ttu-id="1c59f-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c59f-146">0x00000000</span></span>                                                                             |
| <span data-ttu-id="1c59f-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c59f-147">System-Flags</span></span>           | <span data-ttu-id="1c59f-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c59f-148">0x00000010</span></span>                                                                             |
| <span data-ttu-id="1c59f-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c59f-149">Classes used in</span></span>        | [<span data-ttu-id="1c59f-150">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1c59f-150">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="1c59f-151">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1c59f-151">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1c59f-152">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c59f-152">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1c59f-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c59f-153">Entry</span></span> | <span data-ttu-id="1c59f-154">Значение</span><span class="sxs-lookup"><span data-stu-id="1c59f-154">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c59f-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c59f-155">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="1c59f-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c59f-156">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="1c59f-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c59f-157">System-Only</span></span>            | <span data-ttu-id="1c59f-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-158">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c59f-159">Is-Single-Valued</span></span>       | <span data-ttu-id="1c59f-160">True</span><span class="sxs-lookup"><span data-stu-id="1c59f-160">True</span></span>                                                                                   |
| <span data-ttu-id="1c59f-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c59f-161">Is Indexed</span></span>             | <span data-ttu-id="1c59f-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-162">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c59f-163">In Global Catalog</span></span>      | <span data-ttu-id="1c59f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-164">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c59f-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c59f-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c59f-166">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="1c59f-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c59f-167">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="1c59f-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c59f-168">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="1c59f-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c59f-169">Search-Flags</span></span>           | <span data-ttu-id="1c59f-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c59f-170">0x00000000</span></span>                                                                             |
| <span data-ttu-id="1c59f-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c59f-171">System-Flags</span></span>           | <span data-ttu-id="1c59f-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c59f-172">0x00000010</span></span>                                                                             |
| <span data-ttu-id="1c59f-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c59f-173">Classes used in</span></span>        | [<span data-ttu-id="1c59f-174">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1c59f-174">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="1c59f-175">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="1c59f-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1c59f-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c59f-176">Windows Server 2012</span></span>



| <span data-ttu-id="1c59f-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="1c59f-177">Entry</span></span> | <span data-ttu-id="1c59f-178">Значение</span><span class="sxs-lookup"><span data-stu-id="1c59f-178">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c59f-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1c59f-179">Link-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="1c59f-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1c59f-180">MAPI-Id</span></span>                | \-                                                                                     |
| <span data-ttu-id="1c59f-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="1c59f-181">System-Only</span></span>            | <span data-ttu-id="1c59f-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-182">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1c59f-183">Is-Single-Valued</span></span>       | <span data-ttu-id="1c59f-184">True</span><span class="sxs-lookup"><span data-stu-id="1c59f-184">True</span></span>                                                                                   |
| <span data-ttu-id="1c59f-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1c59f-185">Is Indexed</span></span>             | <span data-ttu-id="1c59f-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-186">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1c59f-187">In Global Catalog</span></span>      | <span data-ttu-id="1c59f-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="1c59f-188">False</span></span>                                                                                  |
| <span data-ttu-id="1c59f-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1c59f-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="1c59f-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1c59f-190">O:BAG:BAD:S:</span></span>                                                                           |
| <span data-ttu-id="1c59f-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1c59f-191">Range-Lower</span></span>            | \-                                                                                     |
| <span data-ttu-id="1c59f-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1c59f-192">Range-Upper</span></span>            | \-                                                                                     |
| <span data-ttu-id="1c59f-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1c59f-193">Search-Flags</span></span>           | <span data-ttu-id="1c59f-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1c59f-194">0x00000000</span></span>                                                                             |
| <span data-ttu-id="1c59f-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1c59f-195">System-Flags</span></span>           | <span data-ttu-id="1c59f-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1c59f-196">0x00000010</span></span>                                                                             |
| <span data-ttu-id="1c59f-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1c59f-197">Classes used in</span></span>        | [<span data-ttu-id="1c59f-198">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="1c59f-198">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> [<span data-ttu-id="1c59f-199">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="1c59f-199">**User**</span></span>](c-user.md)<br/> |



 

 





