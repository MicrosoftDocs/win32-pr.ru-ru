---
title: Атрибут «фамилия»
description: Этот атрибут содержит семейство или фамилию пользователя.
ms.assetid: d9d53c9f-4efa-47c4-aec4-518fb8a868b3
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута фамилии
- Схема AD атрибута sn
topic_type:
- apiref
api_name:
- Surname
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453352574a7aec10c56492060ac2de6ceeca030f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989627"
---
# <a name="surname-attribute"></a><span data-ttu-id="4c1a7-105">Атрибут «фамилия»</span><span class="sxs-lookup"><span data-stu-id="4c1a7-105">Surname attribute</span></span>

<span data-ttu-id="4c1a7-106">Этот атрибут содержит семейство или фамилию пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c1a7-106">This attribute contains the family or last name for a user.</span></span>



| <span data-ttu-id="4c1a7-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-107">Entry</span></span> | <span data-ttu-id="4c1a7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4c1a7-109">CN</span><span class="sxs-lookup"><span data-stu-id="4c1a7-109">CN</span></span>                | <span data-ttu-id="4c1a7-110">Surname</span><span class="sxs-lookup"><span data-stu-id="4c1a7-110">Surname</span></span>                                                                          |
| <span data-ttu-id="4c1a7-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4c1a7-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4c1a7-112">sn</span><span class="sxs-lookup"><span data-stu-id="4c1a7-112">sn</span></span>                                                                               |
| <span data-ttu-id="4c1a7-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4c1a7-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="4c1a7-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4c1a7-114">Update Privilege</span></span>  | <span data-ttu-id="4c1a7-115">Любой пользователь может обновить этот объект на основе безопасности создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="4c1a7-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="4c1a7-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4c1a7-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="4c1a7-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-117">Attribute-Id</span></span>      | <span data-ttu-id="4c1a7-118">2.5.4.4</span><span class="sxs-lookup"><span data-stu-id="4c1a7-118">2.5.4.4</span></span>                                                                          |
| <span data-ttu-id="4c1a7-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4c1a7-119">System-Id-Guid</span></span>    | <span data-ttu-id="4c1a7-120">bf967a41-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="4c1a7-120">bf967a41-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="4c1a7-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c1a7-121">Syntax</span></span>            | [<span data-ttu-id="4c1a7-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="4c1a7-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4c1a7-123">Implementations</span></span>

-   [<span data-ttu-id="4c1a7-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="4c1a7-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4c1a7-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4c1a7-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4c1a7-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4c1a7-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="4c1a7-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c1a7-130">Windows 2000 Server</span></span>



| <span data-ttu-id="4c1a7-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-131">Entry</span></span> | <span data-ttu-id="4c1a7-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-132">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="4c1a7-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4c1a7-133">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="4c1a7-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-134">MAPI-Id</span></span>                | <span data-ttu-id="4c1a7-135">0x3A11</span><span class="sxs-lookup"><span data-stu-id="4c1a7-135">0x3A11</span></span>                                |
| <span data-ttu-id="4c1a7-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c1a7-136">System-Only</span></span>            | <span data-ttu-id="4c1a7-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="4c1a7-137">False</span></span>                                 |
| <span data-ttu-id="4c1a7-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4c1a7-138">Is-Single-Valued</span></span>       | <span data-ttu-id="4c1a7-139">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-139">True</span></span>                                  |
| <span data-ttu-id="4c1a7-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4c1a7-140">Is Indexed</span></span>             | <span data-ttu-id="4c1a7-141">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-141">True</span></span>                                  |
| <span data-ttu-id="4c1a7-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4c1a7-142">In Global Catalog</span></span>      | <span data-ttu-id="4c1a7-143">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-143">True</span></span>                                  |
| <span data-ttu-id="4c1a7-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4c1a7-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c1a7-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c1a7-145">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="4c1a7-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c1a7-146">Range-Lower</span></span>            | <span data-ttu-id="4c1a7-147">1</span><span class="sxs-lookup"><span data-stu-id="4c1a7-147">1</span></span>                                     |
| <span data-ttu-id="4c1a7-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c1a7-148">Range-Upper</span></span>            | <span data-ttu-id="4c1a7-149">64</span><span class="sxs-lookup"><span data-stu-id="4c1a7-149">64</span></span>                                    |
| <span data-ttu-id="4c1a7-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-150">Search-Flags</span></span>           | <span data-ttu-id="4c1a7-151">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c1a7-151">0x00000005</span></span>                            |
| <span data-ttu-id="4c1a7-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-152">System-Flags</span></span>           | <span data-ttu-id="4c1a7-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c1a7-153">0x00000010</span></span>                            |
| <span data-ttu-id="4c1a7-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4c1a7-154">Classes used in</span></span>        | [<span data-ttu-id="4c1a7-155">**Человек**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-155">**Person**</span></span>](c-person.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="4c1a7-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c1a7-156">Windows Server 2003</span></span>



| <span data-ttu-id="4c1a7-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-157">Entry</span></span> | <span data-ttu-id="4c1a7-158">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-158">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1a7-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4c1a7-159">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4c1a7-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-160">MAPI-Id</span></span>                | <span data-ttu-id="4c1a7-161">0x3A11</span><span class="sxs-lookup"><span data-stu-id="4c1a7-161">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="4c1a7-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c1a7-162">System-Only</span></span>            | <span data-ttu-id="4c1a7-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="4c1a7-163">False</span></span>                                                                                         |
| <span data-ttu-id="4c1a7-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4c1a7-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4c1a7-165">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-165">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4c1a7-166">Is Indexed</span></span>             | <span data-ttu-id="4c1a7-167">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-167">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4c1a7-168">In Global Catalog</span></span>      | <span data-ttu-id="4c1a7-169">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-169">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4c1a7-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c1a7-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c1a7-171">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4c1a7-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c1a7-172">Range-Lower</span></span>            | <span data-ttu-id="4c1a7-173">1</span><span class="sxs-lookup"><span data-stu-id="4c1a7-173">1</span></span>                                                                                             |
| <span data-ttu-id="4c1a7-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c1a7-174">Range-Upper</span></span>            | <span data-ttu-id="4c1a7-175">64</span><span class="sxs-lookup"><span data-stu-id="4c1a7-175">64</span></span>                                                                                            |
| <span data-ttu-id="4c1a7-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-176">Search-Flags</span></span>           | <span data-ttu-id="4c1a7-177">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c1a7-177">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-178">System-Flags</span></span>           | <span data-ttu-id="4c1a7-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c1a7-179">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4c1a7-180">Classes used in</span></span>        | [<span data-ttu-id="4c1a7-181">**Человек**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-181">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="4c1a7-182">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-182">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4c1a7-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4c1a7-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4c1a7-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-184">Entry</span></span> | <span data-ttu-id="4c1a7-185">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-185">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1a7-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4c1a7-186">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4c1a7-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-187">MAPI-Id</span></span>                | <span data-ttu-id="4c1a7-188">0x3A11</span><span class="sxs-lookup"><span data-stu-id="4c1a7-188">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="4c1a7-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c1a7-189">System-Only</span></span>            | <span data-ttu-id="4c1a7-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="4c1a7-190">False</span></span>                                                                                         |
| <span data-ttu-id="4c1a7-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4c1a7-191">Is-Single-Valued</span></span>       | <span data-ttu-id="4c1a7-192">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-192">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4c1a7-193">Is Indexed</span></span>             | <span data-ttu-id="4c1a7-194">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-194">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4c1a7-195">In Global Catalog</span></span>      | <span data-ttu-id="4c1a7-196">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-196">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4c1a7-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c1a7-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c1a7-198">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4c1a7-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c1a7-199">Range-Lower</span></span>            | <span data-ttu-id="4c1a7-200">1</span><span class="sxs-lookup"><span data-stu-id="4c1a7-200">1</span></span>                                                                                             |
| <span data-ttu-id="4c1a7-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c1a7-201">Range-Upper</span></span>            | <span data-ttu-id="4c1a7-202">64</span><span class="sxs-lookup"><span data-stu-id="4c1a7-202">64</span></span>                                                                                            |
| <span data-ttu-id="4c1a7-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-203">Search-Flags</span></span>           | <span data-ttu-id="4c1a7-204">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c1a7-204">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-205">System-Flags</span></span>           | <span data-ttu-id="4c1a7-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c1a7-206">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4c1a7-207">Classes used in</span></span>        | [<span data-ttu-id="4c1a7-208">**Человек**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-208">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="4c1a7-209">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-209">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4c1a7-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c1a7-210">Windows Server 2008</span></span>



| <span data-ttu-id="4c1a7-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-211">Entry</span></span> | <span data-ttu-id="4c1a7-212">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-212">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1a7-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4c1a7-213">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4c1a7-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-214">MAPI-Id</span></span>                | <span data-ttu-id="4c1a7-215">0x3A11</span><span class="sxs-lookup"><span data-stu-id="4c1a7-215">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="4c1a7-216">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c1a7-216">System-Only</span></span>            | <span data-ttu-id="4c1a7-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="4c1a7-217">False</span></span>                                                                                         |
| <span data-ttu-id="4c1a7-218">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4c1a7-218">Is-Single-Valued</span></span>       | <span data-ttu-id="4c1a7-219">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-219">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-220">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4c1a7-220">Is Indexed</span></span>             | <span data-ttu-id="4c1a7-221">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-221">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-222">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4c1a7-222">In Global Catalog</span></span>      | <span data-ttu-id="4c1a7-223">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-223">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-224">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4c1a7-224">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c1a7-225">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c1a7-225">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4c1a7-226">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c1a7-226">Range-Lower</span></span>            | <span data-ttu-id="4c1a7-227">1</span><span class="sxs-lookup"><span data-stu-id="4c1a7-227">1</span></span>                                                                                             |
| <span data-ttu-id="4c1a7-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c1a7-228">Range-Upper</span></span>            | <span data-ttu-id="4c1a7-229">64</span><span class="sxs-lookup"><span data-stu-id="4c1a7-229">64</span></span>                                                                                            |
| <span data-ttu-id="4c1a7-230">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-230">Search-Flags</span></span>           | <span data-ttu-id="4c1a7-231">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c1a7-231">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-232">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-232">System-Flags</span></span>           | <span data-ttu-id="4c1a7-233">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c1a7-233">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-234">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4c1a7-234">Classes used in</span></span>        | [<span data-ttu-id="4c1a7-235">**Человек**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-235">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="4c1a7-236">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-236">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4c1a7-237">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4c1a7-237">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4c1a7-238">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-238">Entry</span></span> | <span data-ttu-id="4c1a7-239">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-239">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1a7-240">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4c1a7-240">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4c1a7-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-241">MAPI-Id</span></span>                | <span data-ttu-id="4c1a7-242">0x3A11</span><span class="sxs-lookup"><span data-stu-id="4c1a7-242">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="4c1a7-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c1a7-243">System-Only</span></span>            | <span data-ttu-id="4c1a7-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="4c1a7-244">False</span></span>                                                                                         |
| <span data-ttu-id="4c1a7-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4c1a7-245">Is-Single-Valued</span></span>       | <span data-ttu-id="4c1a7-246">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-246">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4c1a7-247">Is Indexed</span></span>             | <span data-ttu-id="4c1a7-248">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-248">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4c1a7-249">In Global Catalog</span></span>      | <span data-ttu-id="4c1a7-250">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-250">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4c1a7-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c1a7-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c1a7-252">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4c1a7-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c1a7-253">Range-Lower</span></span>            | <span data-ttu-id="4c1a7-254">1</span><span class="sxs-lookup"><span data-stu-id="4c1a7-254">1</span></span>                                                                                             |
| <span data-ttu-id="4c1a7-255">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c1a7-255">Range-Upper</span></span>            | <span data-ttu-id="4c1a7-256">64</span><span class="sxs-lookup"><span data-stu-id="4c1a7-256">64</span></span>                                                                                            |
| <span data-ttu-id="4c1a7-257">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-257">Search-Flags</span></span>           | <span data-ttu-id="4c1a7-258">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c1a7-258">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-259">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-259">System-Flags</span></span>           | <span data-ttu-id="4c1a7-260">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c1a7-260">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-261">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4c1a7-261">Classes used in</span></span>        | [<span data-ttu-id="4c1a7-262">**Человек**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-262">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="4c1a7-263">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-263">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4c1a7-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c1a7-264">Windows Server 2012</span></span>



| <span data-ttu-id="4c1a7-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="4c1a7-265">Entry</span></span> | <span data-ttu-id="4c1a7-266">Значение</span><span class="sxs-lookup"><span data-stu-id="4c1a7-266">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c1a7-267">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4c1a7-267">Link-Id</span></span>                | \-                                                                                            |
| <span data-ttu-id="4c1a7-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4c1a7-268">MAPI-Id</span></span>                | <span data-ttu-id="4c1a7-269">0x3A11</span><span class="sxs-lookup"><span data-stu-id="4c1a7-269">0x3A11</span></span>                                                                                        |
| <span data-ttu-id="4c1a7-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="4c1a7-270">System-Only</span></span>            | <span data-ttu-id="4c1a7-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="4c1a7-271">False</span></span>                                                                                         |
| <span data-ttu-id="4c1a7-272">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4c1a7-272">Is-Single-Valued</span></span>       | <span data-ttu-id="4c1a7-273">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-273">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-274">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4c1a7-274">Is Indexed</span></span>             | <span data-ttu-id="4c1a7-275">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-275">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-276">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4c1a7-276">In Global Catalog</span></span>      | <span data-ttu-id="4c1a7-277">True</span><span class="sxs-lookup"><span data-stu-id="4c1a7-277">True</span></span>                                                                                          |
| <span data-ttu-id="4c1a7-278">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4c1a7-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="4c1a7-279">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4c1a7-279">O:BAG:BAD:S:</span></span>                                                                                  |
| <span data-ttu-id="4c1a7-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4c1a7-280">Range-Lower</span></span>            | <span data-ttu-id="4c1a7-281">1</span><span class="sxs-lookup"><span data-stu-id="4c1a7-281">1</span></span>                                                                                             |
| <span data-ttu-id="4c1a7-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4c1a7-282">Range-Upper</span></span>            | <span data-ttu-id="4c1a7-283">64</span><span class="sxs-lookup"><span data-stu-id="4c1a7-283">64</span></span>                                                                                            |
| <span data-ttu-id="4c1a7-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-284">Search-Flags</span></span>           | <span data-ttu-id="4c1a7-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4c1a7-285">0x00000005</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4c1a7-286">System-Flags</span></span>           | <span data-ttu-id="4c1a7-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="4c1a7-287">0x00000010</span></span>                                                                                    |
| <span data-ttu-id="4c1a7-288">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4c1a7-288">Classes used in</span></span>        | [<span data-ttu-id="4c1a7-289">**Человек**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-289">**Person**</span></span>](c-person.md)<br/> [<span data-ttu-id="4c1a7-290">**rFC822LocalPart**</span><span class="sxs-lookup"><span data-stu-id="4c1a7-290">**rFC822LocalPart**</span></span>](c-rfc822localpart.md)<br/> |



 

 





