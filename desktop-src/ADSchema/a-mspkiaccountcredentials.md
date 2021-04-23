---
title: атрибут MS-PKI-Аккаунткредентиалс
description: Хранение зашифрованных BLOB-объектов маркера учетных данных пользователя для роуминга. | атрибут MS-PKI-Аккаунткредентиалс
ms.assetid: 08df5c7d-3aae-4cff-97df-25da6995c72e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-PKI-Аккаунткредентиалс
- Схема AD атрибута Мспкиаккаунткредентиалс
topic_type:
- apiref
api_name:
- ms-PKI-AccountCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76fb96e598b156ba5940bfb75bbfdb628f777353
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000101"
---
# <a name="ms-pki-accountcredentials-attribute"></a><span data-ttu-id="d969b-106">атрибут MS-PKI-Аккаунткредентиалс</span><span class="sxs-lookup"><span data-stu-id="d969b-106">ms-PKI-AccountCredentials attribute</span></span>

<span data-ttu-id="d969b-107">Хранение зашифрованных BLOB-объектов маркера учетных данных пользователя для роуминга.</span><span class="sxs-lookup"><span data-stu-id="d969b-107">Storage of encrypted user credential token BLOBs for roaming.</span></span>



| <span data-ttu-id="d969b-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="d969b-108">Entry</span></span> | <span data-ttu-id="d969b-109">Значение</span><span class="sxs-lookup"><span data-stu-id="d969b-109">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="d969b-110">CN</span><span class="sxs-lookup"><span data-stu-id="d969b-110">CN</span></span>                | <span data-ttu-id="d969b-111">MS-PKI-Аккаунткредентиалс</span><span class="sxs-lookup"><span data-stu-id="d969b-111">ms-PKI-AccountCredentials</span></span>                       |
| <span data-ttu-id="d969b-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d969b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="d969b-113">мспкиаккаунткредентиалс</span><span class="sxs-lookup"><span data-stu-id="d969b-113">msPKIAccountCredentials</span></span>                         |
| <span data-ttu-id="d969b-114">Размер</span><span class="sxs-lookup"><span data-stu-id="d969b-114">Size</span></span>              | \-                                              |
| <span data-ttu-id="d969b-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d969b-115">Update Privilege</span></span>  | \-                                              |
| <span data-ttu-id="d969b-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d969b-116">Update Frequency</span></span>  | \-                                              |
| <span data-ttu-id="d969b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d969b-117">Attribute-Id</span></span>      | <span data-ttu-id="d969b-118">1.2.840.113556.1.4.1894</span><span class="sxs-lookup"><span data-stu-id="d969b-118">1.2.840.113556.1.4.1894</span></span>                         |
| <span data-ttu-id="d969b-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d969b-119">System-Id-Guid</span></span>    | <span data-ttu-id="d969b-120">b8dfa744-31dc-4ef1-ac7c-84baf7ef9da7</span><span class="sxs-lookup"><span data-stu-id="d969b-120">b8dfa744-31dc-4ef1-ac7c-84baf7ef9da7</span></span>            |
| <span data-ttu-id="d969b-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d969b-121">Syntax</span></span>            | [<span data-ttu-id="d969b-122">**Object(двоичный_DN)**</span><span class="sxs-lookup"><span data-stu-id="d969b-122">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="d969b-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d969b-123">Implementations</span></span>

-   [<span data-ttu-id="d969b-124">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d969b-124">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d969b-125">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d969b-125">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d969b-126">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d969b-126">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="d969b-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d969b-127">Windows Server 2008</span></span>



| <span data-ttu-id="d969b-128">Ввод</span><span class="sxs-lookup"><span data-stu-id="d969b-128">Entry</span></span> | <span data-ttu-id="d969b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d969b-129">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d969b-130">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d969b-130">Link-Id</span></span>                | <span data-ttu-id="d969b-131">2048</span><span class="sxs-lookup"><span data-stu-id="d969b-131">2048</span></span>                              |
| <span data-ttu-id="d969b-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d969b-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d969b-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="d969b-133">System-Only</span></span>            | <span data-ttu-id="d969b-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-134">False</span></span>                             |
| <span data-ttu-id="d969b-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d969b-135">Is-Single-Valued</span></span>       | <span data-ttu-id="d969b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-136">False</span></span>                             |
| <span data-ttu-id="d969b-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d969b-137">Is Indexed</span></span>             | <span data-ttu-id="d969b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-138">False</span></span>                             |
| <span data-ttu-id="d969b-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d969b-139">In Global Catalog</span></span>      | <span data-ttu-id="d969b-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-140">False</span></span>                             |
| <span data-ttu-id="d969b-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d969b-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="d969b-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d969b-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d969b-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d969b-143">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d969b-144">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d969b-144">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d969b-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d969b-145">Search-Flags</span></span>           | <span data-ttu-id="d969b-146">0x00000280</span><span class="sxs-lookup"><span data-stu-id="d969b-146">0x00000280</span></span>                        |
| <span data-ttu-id="d969b-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d969b-147">System-Flags</span></span>           | <span data-ttu-id="d969b-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d969b-148">0x00000010</span></span>                        |
| <span data-ttu-id="d969b-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d969b-149">Classes used in</span></span>        | [<span data-ttu-id="d969b-150">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="d969b-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d969b-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d969b-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d969b-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="d969b-152">Entry</span></span> | <span data-ttu-id="d969b-153">Значение</span><span class="sxs-lookup"><span data-stu-id="d969b-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d969b-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d969b-154">Link-Id</span></span>                | <span data-ttu-id="d969b-155">2048</span><span class="sxs-lookup"><span data-stu-id="d969b-155">2048</span></span>                              |
| <span data-ttu-id="d969b-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d969b-156">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d969b-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="d969b-157">System-Only</span></span>            | <span data-ttu-id="d969b-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-158">False</span></span>                             |
| <span data-ttu-id="d969b-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d969b-159">Is-Single-Valued</span></span>       | <span data-ttu-id="d969b-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-160">False</span></span>                             |
| <span data-ttu-id="d969b-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d969b-161">Is Indexed</span></span>             | <span data-ttu-id="d969b-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-162">False</span></span>                             |
| <span data-ttu-id="d969b-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d969b-163">In Global Catalog</span></span>      | <span data-ttu-id="d969b-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-164">False</span></span>                             |
| <span data-ttu-id="d969b-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d969b-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="d969b-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d969b-166">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d969b-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d969b-167">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d969b-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d969b-168">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d969b-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d969b-169">Search-Flags</span></span>           | <span data-ttu-id="d969b-170">0x00000280</span><span class="sxs-lookup"><span data-stu-id="d969b-170">0x00000280</span></span>                        |
| <span data-ttu-id="d969b-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d969b-171">System-Flags</span></span>           | <span data-ttu-id="d969b-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d969b-172">0x00000010</span></span>                        |
| <span data-ttu-id="d969b-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d969b-173">Classes used in</span></span>        | [<span data-ttu-id="d969b-174">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="d969b-174">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d969b-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d969b-175">Windows Server 2012</span></span>



| <span data-ttu-id="d969b-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="d969b-176">Entry</span></span> | <span data-ttu-id="d969b-177">Значение</span><span class="sxs-lookup"><span data-stu-id="d969b-177">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="d969b-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d969b-178">Link-Id</span></span>                | <span data-ttu-id="d969b-179">2048</span><span class="sxs-lookup"><span data-stu-id="d969b-179">2048</span></span>                              |
| <span data-ttu-id="d969b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d969b-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="d969b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="d969b-181">System-Only</span></span>            | <span data-ttu-id="d969b-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-182">False</span></span>                             |
| <span data-ttu-id="d969b-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d969b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="d969b-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-184">False</span></span>                             |
| <span data-ttu-id="d969b-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d969b-185">Is Indexed</span></span>             | <span data-ttu-id="d969b-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-186">False</span></span>                             |
| <span data-ttu-id="d969b-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d969b-187">In Global Catalog</span></span>      | <span data-ttu-id="d969b-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="d969b-188">False</span></span>                             |
| <span data-ttu-id="d969b-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d969b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="d969b-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d969b-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="d969b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d969b-191">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="d969b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d969b-192">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="d969b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d969b-193">Search-Flags</span></span>           | <span data-ttu-id="d969b-194">0x00000280</span><span class="sxs-lookup"><span data-stu-id="d969b-194">0x00000280</span></span>                        |
| <span data-ttu-id="d969b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d969b-195">System-Flags</span></span>           | <span data-ttu-id="d969b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d969b-196">0x00000010</span></span>                        |
| <span data-ttu-id="d969b-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d969b-197">Classes used in</span></span>        | [<span data-ttu-id="d969b-198">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="d969b-198">**User**</span></span>](c-user.md)<br/> |



 

 





