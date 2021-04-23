---
title: Атрибут ms-DS-дополнительно-SAM-Account-Name
description: Этот атрибут используется для хранения имен учетных записей SAM, соответствующих именам узлов DNS в MS-DS-дополнительно-DNS-Host-Name.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-дополнительно-SAM-Account-Name
- Схема AD атрибута msDS-Аддитионалсамаккаунтнаме
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655463"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a><span data-ttu-id="53be5-105">Атрибут ms-DS-дополнительно-SAM-Account-Name</span><span class="sxs-lookup"><span data-stu-id="53be5-105">ms-DS-Additional-Sam-Account-Name attribute</span></span>

<span data-ttu-id="53be5-106">Этот атрибут используется для хранения имен учетных записей SAM, соответствующих именам узлов DNS в MS-DS-дополнительно-DNS-Host-Name.</span><span class="sxs-lookup"><span data-stu-id="53be5-106">This attribute is used to store the SAM account names that correspond to the DNS host names in ms-DS-Additional-Dns-Host-Name.</span></span>



| <span data-ttu-id="53be5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="53be5-107">Entry</span></span> | <span data-ttu-id="53be5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="53be5-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="53be5-109">CN</span><span class="sxs-lookup"><span data-stu-id="53be5-109">CN</span></span>                | <span data-ttu-id="53be5-110">MS-DS-дополнительно-SAM-Account-Name</span><span class="sxs-lookup"><span data-stu-id="53be5-110">ms-DS-Additional-Sam-Account-Name</span></span>           |
| <span data-ttu-id="53be5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="53be5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="53be5-112">msDS-Аддитионалсамаккаунтнаме</span><span class="sxs-lookup"><span data-stu-id="53be5-112">msDS-AdditionalSamAccountName</span></span>               |
| <span data-ttu-id="53be5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="53be5-113">Size</span></span>              | <span data-ttu-id="53be5-114">Менее 20 байт.</span><span class="sxs-lookup"><span data-stu-id="53be5-114">Less than 20 bytes.</span></span>                         |
| <span data-ttu-id="53be5-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="53be5-115">Update Privilege</span></span>  | <span data-ttu-id="53be5-116">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="53be5-116">This value is set by the system.</span></span>            |
| <span data-ttu-id="53be5-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="53be5-117">Update Frequency</span></span>  | <span data-ttu-id="53be5-118">При переименовании контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="53be5-118">When the DC is renamed.</span></span>                     |
| <span data-ttu-id="53be5-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="53be5-119">Attribute-Id</span></span>      | <span data-ttu-id="53be5-120">1.2.840.113556.1.4.1718</span><span class="sxs-lookup"><span data-stu-id="53be5-120">1.2.840.113556.1.4.1718</span></span>                     |
| <span data-ttu-id="53be5-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="53be5-121">System-Id-Guid</span></span>    | <span data-ttu-id="53be5-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span><span class="sxs-lookup"><span data-stu-id="53be5-122">975571df-a4d5-429a-9f59-cdc6581d91e6</span></span>        |
| <span data-ttu-id="53be5-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53be5-123">Syntax</span></span>            | [<span data-ttu-id="53be5-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="53be5-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="53be5-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="53be5-125">Implementations</span></span>

-   [<span data-ttu-id="53be5-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="53be5-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="53be5-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="53be5-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="53be5-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="53be5-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="53be5-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="53be5-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="53be5-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="53be5-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="53be5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="53be5-131">Windows Server 2003</span></span>



| <span data-ttu-id="53be5-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="53be5-132">Entry</span></span> | <span data-ttu-id="53be5-133">Значение</span><span class="sxs-lookup"><span data-stu-id="53be5-133">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="53be5-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="53be5-134">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53be5-135">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="53be5-136">System-Only</span></span>            | <span data-ttu-id="53be5-137">True</span><span class="sxs-lookup"><span data-stu-id="53be5-137">True</span></span>                                      |
| <span data-ttu-id="53be5-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="53be5-138">Is-Single-Valued</span></span>       | <span data-ttu-id="53be5-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-139">False</span></span>                                     |
| <span data-ttu-id="53be5-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="53be5-140">Is Indexed</span></span>             | <span data-ttu-id="53be5-141">True</span><span class="sxs-lookup"><span data-stu-id="53be5-141">True</span></span>                                      |
| <span data-ttu-id="53be5-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="53be5-142">In Global Catalog</span></span>      | <span data-ttu-id="53be5-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-143">False</span></span>                                     |
| <span data-ttu-id="53be5-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="53be5-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="53be5-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53be5-145">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="53be5-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53be5-146">Range-Lower</span></span>            | <span data-ttu-id="53be5-147">0</span><span class="sxs-lookup"><span data-stu-id="53be5-147">0</span></span>                                         |
| <span data-ttu-id="53be5-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53be5-148">Range-Upper</span></span>            | <span data-ttu-id="53be5-149">256</span><span class="sxs-lookup"><span data-stu-id="53be5-149">256</span></span>                                       |
| <span data-ttu-id="53be5-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-150">Search-Flags</span></span>           | <span data-ttu-id="53be5-151">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="53be5-151">0x0000000D</span></span>                                |
| <span data-ttu-id="53be5-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-152">System-Flags</span></span>           | <span data-ttu-id="53be5-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53be5-153">0x00000010</span></span>                                |
| <span data-ttu-id="53be5-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="53be5-154">Classes used in</span></span>        | [<span data-ttu-id="53be5-155">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="53be5-155">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="53be5-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="53be5-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="53be5-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="53be5-157">Entry</span></span> | <span data-ttu-id="53be5-158">Значение</span><span class="sxs-lookup"><span data-stu-id="53be5-158">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="53be5-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="53be5-159">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53be5-160">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="53be5-161">System-Only</span></span>            | <span data-ttu-id="53be5-162">True</span><span class="sxs-lookup"><span data-stu-id="53be5-162">True</span></span>                                      |
| <span data-ttu-id="53be5-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="53be5-163">Is-Single-Valued</span></span>       | <span data-ttu-id="53be5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-164">False</span></span>                                     |
| <span data-ttu-id="53be5-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="53be5-165">Is Indexed</span></span>             | <span data-ttu-id="53be5-166">True</span><span class="sxs-lookup"><span data-stu-id="53be5-166">True</span></span>                                      |
| <span data-ttu-id="53be5-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="53be5-167">In Global Catalog</span></span>      | <span data-ttu-id="53be5-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-168">False</span></span>                                     |
| <span data-ttu-id="53be5-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="53be5-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="53be5-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53be5-170">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="53be5-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53be5-171">Range-Lower</span></span>            | <span data-ttu-id="53be5-172">0</span><span class="sxs-lookup"><span data-stu-id="53be5-172">0</span></span>                                         |
| <span data-ttu-id="53be5-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53be5-173">Range-Upper</span></span>            | <span data-ttu-id="53be5-174">256</span><span class="sxs-lookup"><span data-stu-id="53be5-174">256</span></span>                                       |
| <span data-ttu-id="53be5-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-175">Search-Flags</span></span>           | <span data-ttu-id="53be5-176">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="53be5-176">0x0000000D</span></span>                                |
| <span data-ttu-id="53be5-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-177">System-Flags</span></span>           | <span data-ttu-id="53be5-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53be5-178">0x00000010</span></span>                                |
| <span data-ttu-id="53be5-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="53be5-179">Classes used in</span></span>        | [<span data-ttu-id="53be5-180">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="53be5-180">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="53be5-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53be5-181">Windows Server 2008</span></span>



| <span data-ttu-id="53be5-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="53be5-182">Entry</span></span> | <span data-ttu-id="53be5-183">Значение</span><span class="sxs-lookup"><span data-stu-id="53be5-183">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="53be5-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="53be5-184">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53be5-185">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="53be5-186">System-Only</span></span>            | <span data-ttu-id="53be5-187">True</span><span class="sxs-lookup"><span data-stu-id="53be5-187">True</span></span>                                      |
| <span data-ttu-id="53be5-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="53be5-188">Is-Single-Valued</span></span>       | <span data-ttu-id="53be5-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-189">False</span></span>                                     |
| <span data-ttu-id="53be5-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="53be5-190">Is Indexed</span></span>             | <span data-ttu-id="53be5-191">True</span><span class="sxs-lookup"><span data-stu-id="53be5-191">True</span></span>                                      |
| <span data-ttu-id="53be5-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="53be5-192">In Global Catalog</span></span>      | <span data-ttu-id="53be5-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-193">False</span></span>                                     |
| <span data-ttu-id="53be5-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="53be5-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="53be5-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53be5-195">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="53be5-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53be5-196">Range-Lower</span></span>            | <span data-ttu-id="53be5-197">0</span><span class="sxs-lookup"><span data-stu-id="53be5-197">0</span></span>                                         |
| <span data-ttu-id="53be5-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53be5-198">Range-Upper</span></span>            | <span data-ttu-id="53be5-199">256</span><span class="sxs-lookup"><span data-stu-id="53be5-199">256</span></span>                                       |
| <span data-ttu-id="53be5-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-200">Search-Flags</span></span>           | <span data-ttu-id="53be5-201">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="53be5-201">0x0000000D</span></span>                                |
| <span data-ttu-id="53be5-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-202">System-Flags</span></span>           | <span data-ttu-id="53be5-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53be5-203">0x00000010</span></span>                                |
| <span data-ttu-id="53be5-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="53be5-204">Classes used in</span></span>        | [<span data-ttu-id="53be5-205">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="53be5-205">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="53be5-206">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="53be5-206">Windows Server 2008 R2</span></span>



| <span data-ttu-id="53be5-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="53be5-207">Entry</span></span> | <span data-ttu-id="53be5-208">Значение</span><span class="sxs-lookup"><span data-stu-id="53be5-208">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="53be5-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="53be5-209">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53be5-210">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="53be5-211">System-Only</span></span>            | <span data-ttu-id="53be5-212">True</span><span class="sxs-lookup"><span data-stu-id="53be5-212">True</span></span>                                      |
| <span data-ttu-id="53be5-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="53be5-213">Is-Single-Valued</span></span>       | <span data-ttu-id="53be5-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-214">False</span></span>                                     |
| <span data-ttu-id="53be5-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="53be5-215">Is Indexed</span></span>             | <span data-ttu-id="53be5-216">True</span><span class="sxs-lookup"><span data-stu-id="53be5-216">True</span></span>                                      |
| <span data-ttu-id="53be5-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="53be5-217">In Global Catalog</span></span>      | <span data-ttu-id="53be5-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-218">False</span></span>                                     |
| <span data-ttu-id="53be5-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="53be5-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="53be5-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53be5-220">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="53be5-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53be5-221">Range-Lower</span></span>            | <span data-ttu-id="53be5-222">0</span><span class="sxs-lookup"><span data-stu-id="53be5-222">0</span></span>                                         |
| <span data-ttu-id="53be5-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53be5-223">Range-Upper</span></span>            | <span data-ttu-id="53be5-224">256</span><span class="sxs-lookup"><span data-stu-id="53be5-224">256</span></span>                                       |
| <span data-ttu-id="53be5-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-225">Search-Flags</span></span>           | <span data-ttu-id="53be5-226">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="53be5-226">0x0000000D</span></span>                                |
| <span data-ttu-id="53be5-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-227">System-Flags</span></span>           | <span data-ttu-id="53be5-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53be5-228">0x00000010</span></span>                                |
| <span data-ttu-id="53be5-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="53be5-229">Classes used in</span></span>        | [<span data-ttu-id="53be5-230">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="53be5-230">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="53be5-231">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="53be5-231">Windows Server 2012</span></span>



| <span data-ttu-id="53be5-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="53be5-232">Entry</span></span> | <span data-ttu-id="53be5-233">Значение</span><span class="sxs-lookup"><span data-stu-id="53be5-233">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="53be5-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="53be5-234">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="53be5-235">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="53be5-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="53be5-236">System-Only</span></span>            | <span data-ttu-id="53be5-237">True</span><span class="sxs-lookup"><span data-stu-id="53be5-237">True</span></span>                                      |
| <span data-ttu-id="53be5-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="53be5-238">Is-Single-Valued</span></span>       | <span data-ttu-id="53be5-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-239">False</span></span>                                     |
| <span data-ttu-id="53be5-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="53be5-240">Is Indexed</span></span>             | <span data-ttu-id="53be5-241">True</span><span class="sxs-lookup"><span data-stu-id="53be5-241">True</span></span>                                      |
| <span data-ttu-id="53be5-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="53be5-242">In Global Catalog</span></span>      | <span data-ttu-id="53be5-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="53be5-243">False</span></span>                                     |
| <span data-ttu-id="53be5-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="53be5-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="53be5-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="53be5-245">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="53be5-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="53be5-246">Range-Lower</span></span>            | <span data-ttu-id="53be5-247">0</span><span class="sxs-lookup"><span data-stu-id="53be5-247">0</span></span>                                         |
| <span data-ttu-id="53be5-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="53be5-248">Range-Upper</span></span>            | <span data-ttu-id="53be5-249">256</span><span class="sxs-lookup"><span data-stu-id="53be5-249">256</span></span>                                       |
| <span data-ttu-id="53be5-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-250">Search-Flags</span></span>           | <span data-ttu-id="53be5-251">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="53be5-251">0x0000000D</span></span>                                |
| <span data-ttu-id="53be5-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="53be5-252">System-Flags</span></span>           | <span data-ttu-id="53be5-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="53be5-253">0x00000010</span></span>                                |
| <span data-ttu-id="53be5-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="53be5-254">Classes used in</span></span>        | [<span data-ttu-id="53be5-255">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="53be5-255">**Computer**</span></span>](c-computer.md)<br/> |



 

 





