---
title: Атрибут Address-Type
description: Символьная строка, описывающая формат адреса пользователя. Типы адресов сопоставляются с форматами адресов. То есть, просмотрев тип адреса получателя, клиентские приложения могут определить, как отформатировать адрес, подходящий для получателя.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Address-Type
- Схема AD атрибута addressType
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece3b396d619272c616ff1a959d01efb64ccd46
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655546"
---
# <a name="address-type-attribute"></a><span data-ttu-id="0ad61-107">Атрибут Address-Type</span><span class="sxs-lookup"><span data-stu-id="0ad61-107">Address-Type attribute</span></span>

<span data-ttu-id="0ad61-108">Символьная строка, описывающая формат адреса пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ad61-108">A character string that describes the format of the user's address.</span></span> <span data-ttu-id="0ad61-109">Типы адресов сопоставляются с форматами адресов.</span><span class="sxs-lookup"><span data-stu-id="0ad61-109">Address types map to address formats.</span></span> <span data-ttu-id="0ad61-110">То есть, просмотрев тип адреса получателя, клиентские приложения могут определить, как отформатировать адрес, подходящий для получателя.</span><span class="sxs-lookup"><span data-stu-id="0ad61-110">That is, by looking at a recipient's address type, client applications can determine how to format an address that is appropriate for the recipient.</span></span>



| <span data-ttu-id="0ad61-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-111">Entry</span></span> | <span data-ttu-id="0ad61-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-112">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad61-113">CN</span><span class="sxs-lookup"><span data-stu-id="0ad61-113">CN</span></span>                | <span data-ttu-id="0ad61-114">Address-Type</span><span class="sxs-lookup"><span data-stu-id="0ad61-114">Address-Type</span></span>                                                                                                              |
| <span data-ttu-id="0ad61-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0ad61-115">Ldap-Display-Name</span></span> | <span data-ttu-id="0ad61-116">addressType</span><span class="sxs-lookup"><span data-stu-id="0ad61-116">addressType</span></span>                                                                                                               |
| <span data-ttu-id="0ad61-117">Размер</span><span class="sxs-lookup"><span data-stu-id="0ad61-117">Size</span></span>              | <span data-ttu-id="0ad61-118">Типы адресов: 3COM, АТРИ, ККМАИЛ, COMPUSERVE, EX, FAX, MSFAX, MCI, МХС, MS, MSA, MSN, ПРОФС, SMTP, СНАДС, ТЕЛЕКСА, X400, X500</span><span class="sxs-lookup"><span data-stu-id="0ad61-118">Address types: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN,PROFS,SMTP, SNADS, TELEX, X400, X500</span></span> |
| <span data-ttu-id="0ad61-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0ad61-119">Update Privilege</span></span>  | <span data-ttu-id="0ad61-120">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="0ad61-120">This value is set by the system.</span></span>                                                                                          |
| <span data-ttu-id="0ad61-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0ad61-121">Update Frequency</span></span>  | <span data-ttu-id="0ad61-122">Задается при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="0ad61-122">Set when the object is created.</span></span>                                                                                           |
| <span data-ttu-id="0ad61-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-123">Attribute-Id</span></span>      | <span data-ttu-id="0ad61-124">1.2.840.113556.1.2.350</span><span class="sxs-lookup"><span data-stu-id="0ad61-124">1.2.840.113556.1.2.350</span></span>                                                                                                    |
| <span data-ttu-id="0ad61-125">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0ad61-125">System-Id-Guid</span></span>    | <span data-ttu-id="0ad61-126">5fd42464-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="0ad61-126">5fd42464-1262-11d0-a060-00aa006c33ed</span></span>                                                                                      |
| <span data-ttu-id="0ad61-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ad61-127">Syntax</span></span>            | [<span data-ttu-id="0ad61-128">**String(Teletex)**</span><span class="sxs-lookup"><span data-stu-id="0ad61-128">**String(Teletex)**</span></span>](s-string-teletex.md)                                                                               |



## <a name="implementations"></a><span data-ttu-id="0ad61-129">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0ad61-129">Implementations</span></span>

-   [<span data-ttu-id="0ad61-130">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="0ad61-130">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="0ad61-131">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="0ad61-131">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="0ad61-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="0ad61-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="0ad61-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="0ad61-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="0ad61-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="0ad61-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="0ad61-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0ad61-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="0ad61-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ad61-136">Windows 2000 Server</span></span>



| <span data-ttu-id="0ad61-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-137">Entry</span></span> | <span data-ttu-id="0ad61-138">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-138">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ad61-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ad61-139">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ad61-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-140">MAPI-Id</span></span>                | <span data-ttu-id="0ad61-141">0x8048</span><span class="sxs-lookup"><span data-stu-id="0ad61-141">0x8048</span></span>                                                   |
| <span data-ttu-id="0ad61-142">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad61-142">System-Only</span></span>            | <span data-ttu-id="0ad61-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-143">False</span></span>                                                    |
| <span data-ttu-id="0ad61-144">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ad61-144">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad61-145">True</span><span class="sxs-lookup"><span data-stu-id="0ad61-145">True</span></span>                                                     |
| <span data-ttu-id="0ad61-146">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ad61-146">Is Indexed</span></span>             | <span data-ttu-id="0ad61-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-147">False</span></span>                                                    |
| <span data-ttu-id="0ad61-148">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ad61-148">In Global Catalog</span></span>      | <span data-ttu-id="0ad61-149">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-149">False</span></span>                                                    |
| <span data-ttu-id="0ad61-150">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ad61-150">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad61-151">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ad61-151">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ad61-152">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad61-152">Range-Lower</span></span>            | <span data-ttu-id="0ad61-153">1</span><span class="sxs-lookup"><span data-stu-id="0ad61-153">1</span></span>                                                        |
| <span data-ttu-id="0ad61-154">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad61-154">Range-Upper</span></span>            | <span data-ttu-id="0ad61-155">32</span><span class="sxs-lookup"><span data-stu-id="0ad61-155">32</span></span>                                                       |
| <span data-ttu-id="0ad61-156">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-156">Search-Flags</span></span>           | <span data-ttu-id="0ad61-157">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad61-157">0x00000000</span></span>                                               |
| <span data-ttu-id="0ad61-158">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-158">System-Flags</span></span>           | <span data-ttu-id="0ad61-159">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad61-159">0x00000010</span></span>                                               |
| <span data-ttu-id="0ad61-160">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ad61-160">Classes used in</span></span>        | [<span data-ttu-id="0ad61-161">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="0ad61-161">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="0ad61-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0ad61-162">Windows Server 2003</span></span>



| <span data-ttu-id="0ad61-163">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-163">Entry</span></span> | <span data-ttu-id="0ad61-164">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-164">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ad61-165">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ad61-165">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ad61-166">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-166">MAPI-Id</span></span>                | <span data-ttu-id="0ad61-167">0x8048</span><span class="sxs-lookup"><span data-stu-id="0ad61-167">0x8048</span></span>                                                   |
| <span data-ttu-id="0ad61-168">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad61-168">System-Only</span></span>            | <span data-ttu-id="0ad61-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-169">False</span></span>                                                    |
| <span data-ttu-id="0ad61-170">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ad61-170">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad61-171">True</span><span class="sxs-lookup"><span data-stu-id="0ad61-171">True</span></span>                                                     |
| <span data-ttu-id="0ad61-172">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ad61-172">Is Indexed</span></span>             | <span data-ttu-id="0ad61-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-173">False</span></span>                                                    |
| <span data-ttu-id="0ad61-174">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ad61-174">In Global Catalog</span></span>      | <span data-ttu-id="0ad61-175">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-175">False</span></span>                                                    |
| <span data-ttu-id="0ad61-176">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ad61-176">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad61-177">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ad61-177">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ad61-178">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad61-178">Range-Lower</span></span>            | <span data-ttu-id="0ad61-179">1</span><span class="sxs-lookup"><span data-stu-id="0ad61-179">1</span></span>                                                        |
| <span data-ttu-id="0ad61-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad61-180">Range-Upper</span></span>            | <span data-ttu-id="0ad61-181">32</span><span class="sxs-lookup"><span data-stu-id="0ad61-181">32</span></span>                                                       |
| <span data-ttu-id="0ad61-182">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-182">Search-Flags</span></span>           | <span data-ttu-id="0ad61-183">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad61-183">0x00000000</span></span>                                               |
| <span data-ttu-id="0ad61-184">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-184">System-Flags</span></span>           | <span data-ttu-id="0ad61-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad61-185">0x00000010</span></span>                                               |
| <span data-ttu-id="0ad61-186">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ad61-186">Classes used in</span></span>        | [<span data-ttu-id="0ad61-187">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="0ad61-187">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="0ad61-188">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="0ad61-188">Windows Server 2003 R2</span></span>



| <span data-ttu-id="0ad61-189">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-189">Entry</span></span> | <span data-ttu-id="0ad61-190">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-190">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ad61-191">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ad61-191">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ad61-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-192">MAPI-Id</span></span>                | <span data-ttu-id="0ad61-193">0x8048</span><span class="sxs-lookup"><span data-stu-id="0ad61-193">0x8048</span></span>                                                   |
| <span data-ttu-id="0ad61-194">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad61-194">System-Only</span></span>            | <span data-ttu-id="0ad61-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-195">False</span></span>                                                    |
| <span data-ttu-id="0ad61-196">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ad61-196">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad61-197">True</span><span class="sxs-lookup"><span data-stu-id="0ad61-197">True</span></span>                                                     |
| <span data-ttu-id="0ad61-198">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ad61-198">Is Indexed</span></span>             | <span data-ttu-id="0ad61-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-199">False</span></span>                                                    |
| <span data-ttu-id="0ad61-200">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ad61-200">In Global Catalog</span></span>      | <span data-ttu-id="0ad61-201">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-201">False</span></span>                                                    |
| <span data-ttu-id="0ad61-202">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ad61-202">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad61-203">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ad61-203">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ad61-204">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad61-204">Range-Lower</span></span>            | <span data-ttu-id="0ad61-205">1</span><span class="sxs-lookup"><span data-stu-id="0ad61-205">1</span></span>                                                        |
| <span data-ttu-id="0ad61-206">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad61-206">Range-Upper</span></span>            | <span data-ttu-id="0ad61-207">32</span><span class="sxs-lookup"><span data-stu-id="0ad61-207">32</span></span>                                                       |
| <span data-ttu-id="0ad61-208">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-208">Search-Flags</span></span>           | <span data-ttu-id="0ad61-209">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad61-209">0x00000000</span></span>                                               |
| <span data-ttu-id="0ad61-210">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-210">System-Flags</span></span>           | <span data-ttu-id="0ad61-211">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad61-211">0x00000010</span></span>                                               |
| <span data-ttu-id="0ad61-212">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ad61-212">Classes used in</span></span>        | [<span data-ttu-id="0ad61-213">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="0ad61-213">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="0ad61-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ad61-214">Windows Server 2008</span></span>



| <span data-ttu-id="0ad61-215">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-215">Entry</span></span> | <span data-ttu-id="0ad61-216">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-216">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ad61-217">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ad61-217">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ad61-218">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-218">MAPI-Id</span></span>                | <span data-ttu-id="0ad61-219">0x8048</span><span class="sxs-lookup"><span data-stu-id="0ad61-219">0x8048</span></span>                                                   |
| <span data-ttu-id="0ad61-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad61-220">System-Only</span></span>            | <span data-ttu-id="0ad61-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-221">False</span></span>                                                    |
| <span data-ttu-id="0ad61-222">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ad61-222">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad61-223">True</span><span class="sxs-lookup"><span data-stu-id="0ad61-223">True</span></span>                                                     |
| <span data-ttu-id="0ad61-224">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ad61-224">Is Indexed</span></span>             | <span data-ttu-id="0ad61-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-225">False</span></span>                                                    |
| <span data-ttu-id="0ad61-226">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ad61-226">In Global Catalog</span></span>      | <span data-ttu-id="0ad61-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-227">False</span></span>                                                    |
| <span data-ttu-id="0ad61-228">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ad61-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad61-229">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ad61-229">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ad61-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad61-230">Range-Lower</span></span>            | <span data-ttu-id="0ad61-231">1</span><span class="sxs-lookup"><span data-stu-id="0ad61-231">1</span></span>                                                        |
| <span data-ttu-id="0ad61-232">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad61-232">Range-Upper</span></span>            | <span data-ttu-id="0ad61-233">32</span><span class="sxs-lookup"><span data-stu-id="0ad61-233">32</span></span>                                                       |
| <span data-ttu-id="0ad61-234">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-234">Search-Flags</span></span>           | <span data-ttu-id="0ad61-235">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad61-235">0x00000000</span></span>                                               |
| <span data-ttu-id="0ad61-236">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-236">System-Flags</span></span>           | <span data-ttu-id="0ad61-237">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad61-237">0x00000010</span></span>                                               |
| <span data-ttu-id="0ad61-238">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ad61-238">Classes used in</span></span>        | [<span data-ttu-id="0ad61-239">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="0ad61-239">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="0ad61-240">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0ad61-240">Windows Server 2008 R2</span></span>



| <span data-ttu-id="0ad61-241">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-241">Entry</span></span> | <span data-ttu-id="0ad61-242">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-242">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ad61-243">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ad61-243">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ad61-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-244">MAPI-Id</span></span>                | <span data-ttu-id="0ad61-245">0x8048</span><span class="sxs-lookup"><span data-stu-id="0ad61-245">0x8048</span></span>                                                   |
| <span data-ttu-id="0ad61-246">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad61-246">System-Only</span></span>            | <span data-ttu-id="0ad61-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-247">False</span></span>                                                    |
| <span data-ttu-id="0ad61-248">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ad61-248">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad61-249">True</span><span class="sxs-lookup"><span data-stu-id="0ad61-249">True</span></span>                                                     |
| <span data-ttu-id="0ad61-250">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ad61-250">Is Indexed</span></span>             | <span data-ttu-id="0ad61-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-251">False</span></span>                                                    |
| <span data-ttu-id="0ad61-252">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ad61-252">In Global Catalog</span></span>      | <span data-ttu-id="0ad61-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-253">False</span></span>                                                    |
| <span data-ttu-id="0ad61-254">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ad61-254">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad61-255">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ad61-255">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ad61-256">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad61-256">Range-Lower</span></span>            | <span data-ttu-id="0ad61-257">1</span><span class="sxs-lookup"><span data-stu-id="0ad61-257">1</span></span>                                                        |
| <span data-ttu-id="0ad61-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad61-258">Range-Upper</span></span>            | <span data-ttu-id="0ad61-259">32</span><span class="sxs-lookup"><span data-stu-id="0ad61-259">32</span></span>                                                       |
| <span data-ttu-id="0ad61-260">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-260">Search-Flags</span></span>           | <span data-ttu-id="0ad61-261">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad61-261">0x00000000</span></span>                                               |
| <span data-ttu-id="0ad61-262">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-262">System-Flags</span></span>           | <span data-ttu-id="0ad61-263">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad61-263">0x00000010</span></span>                                               |
| <span data-ttu-id="0ad61-264">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ad61-264">Classes used in</span></span>        | [<span data-ttu-id="0ad61-265">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="0ad61-265">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="0ad61-266">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0ad61-266">Windows Server 2012</span></span>



| <span data-ttu-id="0ad61-267">Ввод</span><span class="sxs-lookup"><span data-stu-id="0ad61-267">Entry</span></span> | <span data-ttu-id="0ad61-268">Значение</span><span class="sxs-lookup"><span data-stu-id="0ad61-268">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="0ad61-269">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0ad61-269">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="0ad61-270">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0ad61-270">MAPI-Id</span></span>                | <span data-ttu-id="0ad61-271">0x8048</span><span class="sxs-lookup"><span data-stu-id="0ad61-271">0x8048</span></span>                                                   |
| <span data-ttu-id="0ad61-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="0ad61-272">System-Only</span></span>            | <span data-ttu-id="0ad61-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-273">False</span></span>                                                    |
| <span data-ttu-id="0ad61-274">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0ad61-274">Is-Single-Valued</span></span>       | <span data-ttu-id="0ad61-275">True</span><span class="sxs-lookup"><span data-stu-id="0ad61-275">True</span></span>                                                     |
| <span data-ttu-id="0ad61-276">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0ad61-276">Is Indexed</span></span>             | <span data-ttu-id="0ad61-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-277">False</span></span>                                                    |
| <span data-ttu-id="0ad61-278">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0ad61-278">In Global Catalog</span></span>      | <span data-ttu-id="0ad61-279">Неверно</span><span class="sxs-lookup"><span data-stu-id="0ad61-279">False</span></span>                                                    |
| <span data-ttu-id="0ad61-280">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0ad61-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="0ad61-281">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0ad61-281">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="0ad61-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0ad61-282">Range-Lower</span></span>            | <span data-ttu-id="0ad61-283">1</span><span class="sxs-lookup"><span data-stu-id="0ad61-283">1</span></span>                                                        |
| <span data-ttu-id="0ad61-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0ad61-284">Range-Upper</span></span>            | <span data-ttu-id="0ad61-285">32</span><span class="sxs-lookup"><span data-stu-id="0ad61-285">32</span></span>                                                       |
| <span data-ttu-id="0ad61-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-286">Search-Flags</span></span>           | <span data-ttu-id="0ad61-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0ad61-287">0x00000000</span></span>                                               |
| <span data-ttu-id="0ad61-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0ad61-288">System-Flags</span></span>           | <span data-ttu-id="0ad61-289">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0ad61-289">0x00000010</span></span>                                               |
| <span data-ttu-id="0ad61-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0ad61-290">Classes used in</span></span>        | [<span data-ttu-id="0ad61-291">**Адрес — шаблон**</span><span class="sxs-lookup"><span data-stu-id="0ad61-291">**Address-Template**</span></span>](c-addresstemplate.md)<br/> |



 

 





