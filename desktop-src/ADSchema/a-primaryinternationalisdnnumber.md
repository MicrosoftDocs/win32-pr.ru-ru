---
title: Phone-ISDN-первичный атрибут
description: Основной ISDN.
ms.assetid: fa92d458-8c38-4012-9170-75a51f4ed116
ms.tgt_platform: multiple
keywords:
- Телефон — схема Active Directory для атрибута ISDN
- Схема AD атрибута Примаринтернатионалисдннумбер
topic_type:
- apiref
api_name:
- Phone-ISDN-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5794643d30ff457a7b4db714d3850f0f289c0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989782"
---
# <a name="phone-isdn-primary-attribute"></a><span data-ttu-id="6226c-105">Phone-ISDN-первичный атрибут</span><span class="sxs-lookup"><span data-stu-id="6226c-105">Phone-ISDN-Primary attribute</span></span>

<span data-ttu-id="6226c-106">Основной ISDN.</span><span class="sxs-lookup"><span data-stu-id="6226c-106">The primary ISDN.</span></span>



| <span data-ttu-id="6226c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-107">Entry</span></span> | <span data-ttu-id="6226c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6226c-109">CN</span><span class="sxs-lookup"><span data-stu-id="6226c-109">CN</span></span>                | <span data-ttu-id="6226c-110">Телефон — ISDN — первичный</span><span class="sxs-lookup"><span data-stu-id="6226c-110">Phone-ISDN-Primary</span></span>                                                               |
| <span data-ttu-id="6226c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6226c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="6226c-112">примаринтернатионалисдннумбер</span><span class="sxs-lookup"><span data-stu-id="6226c-112">primaryInternationalISDNNumber</span></span>                                                   |
| <span data-ttu-id="6226c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="6226c-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="6226c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6226c-114">Update Privilege</span></span>  | <span data-ttu-id="6226c-115">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="6226c-115">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="6226c-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6226c-116">Update Frequency</span></span>  | <span data-ttu-id="6226c-117">При создании записи пользователя и при необходимости изменения номера телефона.</span><span class="sxs-lookup"><span data-stu-id="6226c-117">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="6226c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-118">Attribute-Id</span></span>      | <span data-ttu-id="6226c-119">1.2.840.113556.1.4.649</span><span class="sxs-lookup"><span data-stu-id="6226c-119">1.2.840.113556.1.4.649</span></span>                                                           |
| <span data-ttu-id="6226c-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6226c-120">System-Id-Guid</span></span>    | <span data-ttu-id="6226c-121">0296c11f-40da-11d1-a9c0-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="6226c-121">0296c11f-40da-11d1-a9c0-0000f80367c1</span></span>                                             |
| <span data-ttu-id="6226c-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6226c-122">Syntax</span></span>            | [<span data-ttu-id="6226c-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="6226c-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="6226c-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6226c-124">Implementations</span></span>

-   [<span data-ttu-id="6226c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="6226c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="6226c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="6226c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="6226c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="6226c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="6226c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="6226c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="6226c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="6226c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="6226c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6226c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="6226c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6226c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="6226c-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-132">Entry</span></span> | <span data-ttu-id="6226c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6226c-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6226c-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-135">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="6226c-136">System-Only</span></span>            | <span data-ttu-id="6226c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-137">False</span></span>                                                              |
| <span data-ttu-id="6226c-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6226c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="6226c-139">True</span><span class="sxs-lookup"><span data-stu-id="6226c-139">True</span></span>                                                               |
| <span data-ttu-id="6226c-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6226c-140">Is Indexed</span></span>             | <span data-ttu-id="6226c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-141">False</span></span>                                                              |
| <span data-ttu-id="6226c-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6226c-142">In Global Catalog</span></span>      | <span data-ttu-id="6226c-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-143">False</span></span>                                                              |
| <span data-ttu-id="6226c-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6226c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="6226c-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6226c-145">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6226c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6226c-146">Range-Lower</span></span>            | <span data-ttu-id="6226c-147">1</span><span class="sxs-lookup"><span data-stu-id="6226c-147">1</span></span>                                                                  |
| <span data-ttu-id="6226c-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6226c-148">Range-Upper</span></span>            | <span data-ttu-id="6226c-149">64</span><span class="sxs-lookup"><span data-stu-id="6226c-149">64</span></span>                                                                 |
| <span data-ttu-id="6226c-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-150">Search-Flags</span></span>           | <span data-ttu-id="6226c-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6226c-151">0x00000000</span></span>                                                         |
| <span data-ttu-id="6226c-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-152">System-Flags</span></span>           | <span data-ttu-id="6226c-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6226c-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="6226c-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6226c-154">Classes used in</span></span>        | [<span data-ttu-id="6226c-155">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6226c-155">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="6226c-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6226c-156">Windows Server 2003</span></span>



| <span data-ttu-id="6226c-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-157">Entry</span></span> | <span data-ttu-id="6226c-158">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-158">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6226c-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6226c-159">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-160">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="6226c-161">System-Only</span></span>            | <span data-ttu-id="6226c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-162">False</span></span>                                                              |
| <span data-ttu-id="6226c-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6226c-163">Is-Single-Valued</span></span>       | <span data-ttu-id="6226c-164">True</span><span class="sxs-lookup"><span data-stu-id="6226c-164">True</span></span>                                                               |
| <span data-ttu-id="6226c-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6226c-165">Is Indexed</span></span>             | <span data-ttu-id="6226c-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-166">False</span></span>                                                              |
| <span data-ttu-id="6226c-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6226c-167">In Global Catalog</span></span>      | <span data-ttu-id="6226c-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-168">False</span></span>                                                              |
| <span data-ttu-id="6226c-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6226c-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="6226c-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6226c-170">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6226c-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6226c-171">Range-Lower</span></span>            | <span data-ttu-id="6226c-172">1</span><span class="sxs-lookup"><span data-stu-id="6226c-172">1</span></span>                                                                  |
| <span data-ttu-id="6226c-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6226c-173">Range-Upper</span></span>            | <span data-ttu-id="6226c-174">64</span><span class="sxs-lookup"><span data-stu-id="6226c-174">64</span></span>                                                                 |
| <span data-ttu-id="6226c-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-175">Search-Flags</span></span>           | <span data-ttu-id="6226c-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6226c-176">0x00000000</span></span>                                                         |
| <span data-ttu-id="6226c-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-177">System-Flags</span></span>           | <span data-ttu-id="6226c-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6226c-178">0x00000010</span></span>                                                         |
| <span data-ttu-id="6226c-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6226c-179">Classes used in</span></span>        | [<span data-ttu-id="6226c-180">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6226c-180">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="6226c-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="6226c-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="6226c-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-182">Entry</span></span> | <span data-ttu-id="6226c-183">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-183">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6226c-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6226c-184">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-185">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="6226c-186">System-Only</span></span>            | <span data-ttu-id="6226c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-187">False</span></span>                                                              |
| <span data-ttu-id="6226c-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6226c-188">Is-Single-Valued</span></span>       | <span data-ttu-id="6226c-189">True</span><span class="sxs-lookup"><span data-stu-id="6226c-189">True</span></span>                                                               |
| <span data-ttu-id="6226c-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6226c-190">Is Indexed</span></span>             | <span data-ttu-id="6226c-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-191">False</span></span>                                                              |
| <span data-ttu-id="6226c-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6226c-192">In Global Catalog</span></span>      | <span data-ttu-id="6226c-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-193">False</span></span>                                                              |
| <span data-ttu-id="6226c-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6226c-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="6226c-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6226c-195">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6226c-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6226c-196">Range-Lower</span></span>            | <span data-ttu-id="6226c-197">1</span><span class="sxs-lookup"><span data-stu-id="6226c-197">1</span></span>                                                                  |
| <span data-ttu-id="6226c-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6226c-198">Range-Upper</span></span>            | <span data-ttu-id="6226c-199">64</span><span class="sxs-lookup"><span data-stu-id="6226c-199">64</span></span>                                                                 |
| <span data-ttu-id="6226c-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-200">Search-Flags</span></span>           | <span data-ttu-id="6226c-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6226c-201">0x00000000</span></span>                                                         |
| <span data-ttu-id="6226c-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-202">System-Flags</span></span>           | <span data-ttu-id="6226c-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6226c-203">0x00000010</span></span>                                                         |
| <span data-ttu-id="6226c-204">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6226c-204">Classes used in</span></span>        | [<span data-ttu-id="6226c-205">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6226c-205">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="6226c-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6226c-206">Windows Server 2008</span></span>



| <span data-ttu-id="6226c-207">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-207">Entry</span></span> | <span data-ttu-id="6226c-208">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-208">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6226c-209">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6226c-209">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-210">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="6226c-211">System-Only</span></span>            | <span data-ttu-id="6226c-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-212">False</span></span>                                                              |
| <span data-ttu-id="6226c-213">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6226c-213">Is-Single-Valued</span></span>       | <span data-ttu-id="6226c-214">True</span><span class="sxs-lookup"><span data-stu-id="6226c-214">True</span></span>                                                               |
| <span data-ttu-id="6226c-215">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6226c-215">Is Indexed</span></span>             | <span data-ttu-id="6226c-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-216">False</span></span>                                                              |
| <span data-ttu-id="6226c-217">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6226c-217">In Global Catalog</span></span>      | <span data-ttu-id="6226c-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-218">False</span></span>                                                              |
| <span data-ttu-id="6226c-219">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6226c-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="6226c-220">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6226c-220">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6226c-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6226c-221">Range-Lower</span></span>            | <span data-ttu-id="6226c-222">1</span><span class="sxs-lookup"><span data-stu-id="6226c-222">1</span></span>                                                                  |
| <span data-ttu-id="6226c-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6226c-223">Range-Upper</span></span>            | <span data-ttu-id="6226c-224">64</span><span class="sxs-lookup"><span data-stu-id="6226c-224">64</span></span>                                                                 |
| <span data-ttu-id="6226c-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-225">Search-Flags</span></span>           | <span data-ttu-id="6226c-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6226c-226">0x00000000</span></span>                                                         |
| <span data-ttu-id="6226c-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-227">System-Flags</span></span>           | <span data-ttu-id="6226c-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6226c-228">0x00000010</span></span>                                                         |
| <span data-ttu-id="6226c-229">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6226c-229">Classes used in</span></span>        | [<span data-ttu-id="6226c-230">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6226c-230">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="6226c-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="6226c-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="6226c-232">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-232">Entry</span></span> | <span data-ttu-id="6226c-233">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-233">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6226c-234">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6226c-234">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-235">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="6226c-236">System-Only</span></span>            | <span data-ttu-id="6226c-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-237">False</span></span>                                                              |
| <span data-ttu-id="6226c-238">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6226c-238">Is-Single-Valued</span></span>       | <span data-ttu-id="6226c-239">True</span><span class="sxs-lookup"><span data-stu-id="6226c-239">True</span></span>                                                               |
| <span data-ttu-id="6226c-240">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6226c-240">Is Indexed</span></span>             | <span data-ttu-id="6226c-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-241">False</span></span>                                                              |
| <span data-ttu-id="6226c-242">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6226c-242">In Global Catalog</span></span>      | <span data-ttu-id="6226c-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-243">False</span></span>                                                              |
| <span data-ttu-id="6226c-244">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6226c-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="6226c-245">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6226c-245">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6226c-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6226c-246">Range-Lower</span></span>            | <span data-ttu-id="6226c-247">1</span><span class="sxs-lookup"><span data-stu-id="6226c-247">1</span></span>                                                                  |
| <span data-ttu-id="6226c-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6226c-248">Range-Upper</span></span>            | <span data-ttu-id="6226c-249">64</span><span class="sxs-lookup"><span data-stu-id="6226c-249">64</span></span>                                                                 |
| <span data-ttu-id="6226c-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-250">Search-Flags</span></span>           | <span data-ttu-id="6226c-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6226c-251">0x00000000</span></span>                                                         |
| <span data-ttu-id="6226c-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-252">System-Flags</span></span>           | <span data-ttu-id="6226c-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6226c-253">0x00000010</span></span>                                                         |
| <span data-ttu-id="6226c-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6226c-254">Classes used in</span></span>        | [<span data-ttu-id="6226c-255">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6226c-255">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="6226c-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6226c-256">Windows Server 2012</span></span>



| <span data-ttu-id="6226c-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="6226c-257">Entry</span></span> | <span data-ttu-id="6226c-258">Значение</span><span class="sxs-lookup"><span data-stu-id="6226c-258">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="6226c-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6226c-259">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6226c-260">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="6226c-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="6226c-261">System-Only</span></span>            | <span data-ttu-id="6226c-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-262">False</span></span>                                                              |
| <span data-ttu-id="6226c-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6226c-263">Is-Single-Valued</span></span>       | <span data-ttu-id="6226c-264">True</span><span class="sxs-lookup"><span data-stu-id="6226c-264">True</span></span>                                                               |
| <span data-ttu-id="6226c-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6226c-265">Is Indexed</span></span>             | <span data-ttu-id="6226c-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-266">False</span></span>                                                              |
| <span data-ttu-id="6226c-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6226c-267">In Global Catalog</span></span>      | <span data-ttu-id="6226c-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="6226c-268">False</span></span>                                                              |
| <span data-ttu-id="6226c-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6226c-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="6226c-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6226c-270">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="6226c-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6226c-271">Range-Lower</span></span>            | <span data-ttu-id="6226c-272">1</span><span class="sxs-lookup"><span data-stu-id="6226c-272">1</span></span>                                                                  |
| <span data-ttu-id="6226c-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6226c-273">Range-Upper</span></span>            | <span data-ttu-id="6226c-274">64</span><span class="sxs-lookup"><span data-stu-id="6226c-274">64</span></span>                                                                 |
| <span data-ttu-id="6226c-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-275">Search-Flags</span></span>           | <span data-ttu-id="6226c-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6226c-276">0x00000000</span></span>                                                         |
| <span data-ttu-id="6226c-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6226c-277">System-Flags</span></span>           | <span data-ttu-id="6226c-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6226c-278">0x00000010</span></span>                                                         |
| <span data-ttu-id="6226c-279">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6226c-279">Classes used in</span></span>        | [<span data-ttu-id="6226c-280">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="6226c-280">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





