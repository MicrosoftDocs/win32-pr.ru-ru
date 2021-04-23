---
title: Атрибут ms-DS-дополнительно-DNS-Host-Name
description: Атрибут используется для хранения дополнительного имени узла DNS для объекта-компьютера. Этот атрибут используется во время переименования контроллера домена.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-дополнительно-DNS-Host-Name
- Схема AD атрибута msDS-Аддитионалдншостнаме
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989710"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a><span data-ttu-id="1ffdf-106">Атрибут ms-DS-дополнительно-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="1ffdf-106">ms-DS-Additional-Dns-Host-Name attribute</span></span>

<span data-ttu-id="1ffdf-107">Атрибут используется для хранения дополнительного имени узла DNS для объекта-компьютера.</span><span class="sxs-lookup"><span data-stu-id="1ffdf-107">The attribute is used to store the additional DNS host name of a computer object.</span></span> <span data-ttu-id="1ffdf-108">Этот атрибут используется во время переименования компьютера или управления именами с помощью "Netdom ComputerName".</span><span class="sxs-lookup"><span data-stu-id="1ffdf-108">This attribute is used at the time a computer is renamed, or names are managed with "netdom computername".</span></span>



| <span data-ttu-id="1ffdf-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ffdf-109">Entry</span></span> | <span data-ttu-id="1ffdf-110">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffdf-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1ffdf-111">CN</span><span class="sxs-lookup"><span data-stu-id="1ffdf-111">CN</span></span>                | <span data-ttu-id="1ffdf-112">MS-DS-дополнительно-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="1ffdf-112">ms-DS-Additional-Dns-Host-Name</span></span>                                              |
| <span data-ttu-id="1ffdf-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1ffdf-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1ffdf-114">msDS-Аддитионалдншостнаме</span><span class="sxs-lookup"><span data-stu-id="1ffdf-114">msDS-AdditionalDnsHostName</span></span>                                                  |
| <span data-ttu-id="1ffdf-115">Размер</span><span class="sxs-lookup"><span data-stu-id="1ffdf-115">Size</span></span>              | <span data-ttu-id="1ffdf-116">Каждое значение может содержать 2048 символов.</span><span class="sxs-lookup"><span data-stu-id="1ffdf-116">Each value can be 2048 characters.</span></span> <span data-ttu-id="1ffdf-117">Количество значений — это ограничение базы данных, равное 1200.</span><span class="sxs-lookup"><span data-stu-id="1ffdf-117">The number of value is the database limit of about 1200 values.</span></span> |
| <span data-ttu-id="1ffdf-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1ffdf-118">Update Privilege</span></span>  | <span data-ttu-id="1ffdf-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="1ffdf-119">This value is set by the system.</span></span>                                            |
| <span data-ttu-id="1ffdf-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1ffdf-120">Update Frequency</span></span>  | <span data-ttu-id="1ffdf-121">При переименовании компьютера.</span><span class="sxs-lookup"><span data-stu-id="1ffdf-121">When a computer is renamed.</span></span>                                                 |
| <span data-ttu-id="1ffdf-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1ffdf-122">Attribute-Id</span></span>      | <span data-ttu-id="1ffdf-123">1.2.840.113556.1.4.1717</span><span class="sxs-lookup"><span data-stu-id="1ffdf-123">1.2.840.113556.1.4.1717</span></span>                                                     |
| <span data-ttu-id="1ffdf-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1ffdf-124">System-Id-Guid</span></span>    | <span data-ttu-id="1ffdf-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span><span class="sxs-lookup"><span data-stu-id="1ffdf-125">80863791-dbe9-4eb8-837e-7f0ab55d9ac7</span></span>                                        |
| <span data-ttu-id="1ffdf-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ffdf-126">Syntax</span></span>            | [<span data-ttu-id="1ffdf-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                 |



## <a name="implementations"></a><span data-ttu-id="1ffdf-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1ffdf-128">Implementations</span></span>

-   [<span data-ttu-id="1ffdf-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1ffdf-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1ffdf-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1ffdf-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1ffdf-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="1ffdf-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1ffdf-134">Windows Server 2003</span></span>



| <span data-ttu-id="1ffdf-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ffdf-135">Entry</span></span> | <span data-ttu-id="1ffdf-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffdf-136">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="1ffdf-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ffdf-137">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ffdf-138">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ffdf-139">System-Only</span></span>            | <span data-ttu-id="1ffdf-140">True</span><span class="sxs-lookup"><span data-stu-id="1ffdf-140">True</span></span>                                      |
| <span data-ttu-id="1ffdf-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ffdf-141">Is-Single-Valued</span></span>       | <span data-ttu-id="1ffdf-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-142">False</span></span>                                     |
| <span data-ttu-id="1ffdf-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ffdf-143">Is Indexed</span></span>             | <span data-ttu-id="1ffdf-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-144">False</span></span>                                     |
| <span data-ttu-id="1ffdf-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ffdf-145">In Global Catalog</span></span>      | <span data-ttu-id="1ffdf-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-146">False</span></span>                                     |
| <span data-ttu-id="1ffdf-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ffdf-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ffdf-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ffdf-148">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="1ffdf-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ffdf-149">Range-Lower</span></span>            | <span data-ttu-id="1ffdf-150">0</span><span class="sxs-lookup"><span data-stu-id="1ffdf-150">0</span></span>                                         |
| <span data-ttu-id="1ffdf-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ffdf-151">Range-Upper</span></span>            | <span data-ttu-id="1ffdf-152">2048</span><span class="sxs-lookup"><span data-stu-id="1ffdf-152">2048</span></span>                                      |
| <span data-ttu-id="1ffdf-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-153">Search-Flags</span></span>           | <span data-ttu-id="1ffdf-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ffdf-154">0x00000000</span></span>                                |
| <span data-ttu-id="1ffdf-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-155">System-Flags</span></span>           | <span data-ttu-id="1ffdf-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ffdf-156">0x00000010</span></span>                                |
| <span data-ttu-id="1ffdf-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ffdf-157">Classes used in</span></span>        | [<span data-ttu-id="1ffdf-158">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-158">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1ffdf-159">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1ffdf-159">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1ffdf-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ffdf-160">Entry</span></span> | <span data-ttu-id="1ffdf-161">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffdf-161">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="1ffdf-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ffdf-162">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ffdf-163">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ffdf-164">System-Only</span></span>            | <span data-ttu-id="1ffdf-165">True</span><span class="sxs-lookup"><span data-stu-id="1ffdf-165">True</span></span>                                      |
| <span data-ttu-id="1ffdf-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ffdf-166">Is-Single-Valued</span></span>       | <span data-ttu-id="1ffdf-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-167">False</span></span>                                     |
| <span data-ttu-id="1ffdf-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ffdf-168">Is Indexed</span></span>             | <span data-ttu-id="1ffdf-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-169">False</span></span>                                     |
| <span data-ttu-id="1ffdf-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ffdf-170">In Global Catalog</span></span>      | <span data-ttu-id="1ffdf-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-171">False</span></span>                                     |
| <span data-ttu-id="1ffdf-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ffdf-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ffdf-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ffdf-173">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="1ffdf-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ffdf-174">Range-Lower</span></span>            | <span data-ttu-id="1ffdf-175">0</span><span class="sxs-lookup"><span data-stu-id="1ffdf-175">0</span></span>                                         |
| <span data-ttu-id="1ffdf-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ffdf-176">Range-Upper</span></span>            | <span data-ttu-id="1ffdf-177">2048</span><span class="sxs-lookup"><span data-stu-id="1ffdf-177">2048</span></span>                                      |
| <span data-ttu-id="1ffdf-178">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-178">Search-Flags</span></span>           | <span data-ttu-id="1ffdf-179">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ffdf-179">0x00000000</span></span>                                |
| <span data-ttu-id="1ffdf-180">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-180">System-Flags</span></span>           | <span data-ttu-id="1ffdf-181">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ffdf-181">0x00000010</span></span>                                |
| <span data-ttu-id="1ffdf-182">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ffdf-182">Classes used in</span></span>        | [<span data-ttu-id="1ffdf-183">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-183">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1ffdf-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ffdf-184">Windows Server 2008</span></span>



| <span data-ttu-id="1ffdf-185">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ffdf-185">Entry</span></span> | <span data-ttu-id="1ffdf-186">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffdf-186">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="1ffdf-187">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ffdf-187">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-188">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ffdf-188">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ffdf-189">System-Only</span></span>            | <span data-ttu-id="1ffdf-190">True</span><span class="sxs-lookup"><span data-stu-id="1ffdf-190">True</span></span>                                      |
| <span data-ttu-id="1ffdf-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ffdf-191">Is-Single-Valued</span></span>       | <span data-ttu-id="1ffdf-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-192">False</span></span>                                     |
| <span data-ttu-id="1ffdf-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ffdf-193">Is Indexed</span></span>             | <span data-ttu-id="1ffdf-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-194">False</span></span>                                     |
| <span data-ttu-id="1ffdf-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ffdf-195">In Global Catalog</span></span>      | <span data-ttu-id="1ffdf-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-196">False</span></span>                                     |
| <span data-ttu-id="1ffdf-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ffdf-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ffdf-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ffdf-198">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="1ffdf-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ffdf-199">Range-Lower</span></span>            | <span data-ttu-id="1ffdf-200">0</span><span class="sxs-lookup"><span data-stu-id="1ffdf-200">0</span></span>                                         |
| <span data-ttu-id="1ffdf-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ffdf-201">Range-Upper</span></span>            | <span data-ttu-id="1ffdf-202">2048</span><span class="sxs-lookup"><span data-stu-id="1ffdf-202">2048</span></span>                                      |
| <span data-ttu-id="1ffdf-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-203">Search-Flags</span></span>           | <span data-ttu-id="1ffdf-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ffdf-204">0x00000000</span></span>                                |
| <span data-ttu-id="1ffdf-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-205">System-Flags</span></span>           | <span data-ttu-id="1ffdf-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ffdf-206">0x00000010</span></span>                                |
| <span data-ttu-id="1ffdf-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ffdf-207">Classes used in</span></span>        | [<span data-ttu-id="1ffdf-208">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-208">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1ffdf-209">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1ffdf-209">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1ffdf-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ffdf-210">Entry</span></span> | <span data-ttu-id="1ffdf-211">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffdf-211">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="1ffdf-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ffdf-212">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ffdf-213">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ffdf-214">System-Only</span></span>            | <span data-ttu-id="1ffdf-215">True</span><span class="sxs-lookup"><span data-stu-id="1ffdf-215">True</span></span>                                      |
| <span data-ttu-id="1ffdf-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ffdf-216">Is-Single-Valued</span></span>       | <span data-ttu-id="1ffdf-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-217">False</span></span>                                     |
| <span data-ttu-id="1ffdf-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ffdf-218">Is Indexed</span></span>             | <span data-ttu-id="1ffdf-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-219">False</span></span>                                     |
| <span data-ttu-id="1ffdf-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ffdf-220">In Global Catalog</span></span>      | <span data-ttu-id="1ffdf-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-221">False</span></span>                                     |
| <span data-ttu-id="1ffdf-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ffdf-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ffdf-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ffdf-223">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="1ffdf-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ffdf-224">Range-Lower</span></span>            | <span data-ttu-id="1ffdf-225">0</span><span class="sxs-lookup"><span data-stu-id="1ffdf-225">0</span></span>                                         |
| <span data-ttu-id="1ffdf-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ffdf-226">Range-Upper</span></span>            | <span data-ttu-id="1ffdf-227">2048</span><span class="sxs-lookup"><span data-stu-id="1ffdf-227">2048</span></span>                                      |
| <span data-ttu-id="1ffdf-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-228">Search-Flags</span></span>           | <span data-ttu-id="1ffdf-229">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ffdf-229">0x00000000</span></span>                                |
| <span data-ttu-id="1ffdf-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-230">System-Flags</span></span>           | <span data-ttu-id="1ffdf-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ffdf-231">0x00000010</span></span>                                |
| <span data-ttu-id="1ffdf-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ffdf-232">Classes used in</span></span>        | [<span data-ttu-id="1ffdf-233">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-233">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1ffdf-234">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ffdf-234">Windows Server 2012</span></span>



| <span data-ttu-id="1ffdf-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="1ffdf-235">Entry</span></span> | <span data-ttu-id="1ffdf-236">Значение</span><span class="sxs-lookup"><span data-stu-id="1ffdf-236">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="1ffdf-237">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1ffdf-237">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-238">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1ffdf-238">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="1ffdf-239">System-Only</span><span class="sxs-lookup"><span data-stu-id="1ffdf-239">System-Only</span></span>            | <span data-ttu-id="1ffdf-240">True</span><span class="sxs-lookup"><span data-stu-id="1ffdf-240">True</span></span>                                      |
| <span data-ttu-id="1ffdf-241">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1ffdf-241">Is-Single-Valued</span></span>       | <span data-ttu-id="1ffdf-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-242">False</span></span>                                     |
| <span data-ttu-id="1ffdf-243">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1ffdf-243">Is Indexed</span></span>             | <span data-ttu-id="1ffdf-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-244">False</span></span>                                     |
| <span data-ttu-id="1ffdf-245">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1ffdf-245">In Global Catalog</span></span>      | <span data-ttu-id="1ffdf-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="1ffdf-246">False</span></span>                                     |
| <span data-ttu-id="1ffdf-247">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1ffdf-247">NT-Security-Descriptor</span></span> | <span data-ttu-id="1ffdf-248">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1ffdf-248">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="1ffdf-249">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1ffdf-249">Range-Lower</span></span>            | <span data-ttu-id="1ffdf-250">0</span><span class="sxs-lookup"><span data-stu-id="1ffdf-250">0</span></span>                                         |
| <span data-ttu-id="1ffdf-251">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1ffdf-251">Range-Upper</span></span>            | <span data-ttu-id="1ffdf-252">2048</span><span class="sxs-lookup"><span data-stu-id="1ffdf-252">2048</span></span>                                      |
| <span data-ttu-id="1ffdf-253">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-253">Search-Flags</span></span>           | <span data-ttu-id="1ffdf-254">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ffdf-254">0x00000000</span></span>                                |
| <span data-ttu-id="1ffdf-255">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1ffdf-255">System-Flags</span></span>           | <span data-ttu-id="1ffdf-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1ffdf-256">0x00000010</span></span>                                |
| <span data-ttu-id="1ffdf-257">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1ffdf-257">Classes used in</span></span>        | [<span data-ttu-id="1ffdf-258">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="1ffdf-258">**Computer**</span></span>](c-computer.md)<br/> |



 

 





