---
title: Phone — Главная — другие атрибуты
description: Список альтернативных номеров домашнего телефона.
ms.assetid: 502e0a9d-301c-4c2e-98c3-8efe75c8b0cf
ms.tgt_platform: multiple
keywords:
- Телефон — Главная — другая схема AD атрибутов
- Схема AD атрибута Осерхомефоне
topic_type:
- apiref
api_name:
- Phone-Home-Other
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ed3aa026a1e60bb644ddab81293921ac9b8271
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893322"
---
# <a name="phone-home-other-attribute"></a><span data-ttu-id="ffb8f-105">Phone — Главная — другие атрибуты</span><span class="sxs-lookup"><span data-stu-id="ffb8f-105">Phone-Home-Other attribute</span></span>

<span data-ttu-id="ffb8f-106">Список альтернативных номеров домашнего телефона.</span><span class="sxs-lookup"><span data-stu-id="ffb8f-106">A list of alternate home phone numbers.</span></span>



| <span data-ttu-id="ffb8f-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-107">Entry</span></span> | <span data-ttu-id="ffb8f-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-109">CN</span><span class="sxs-lookup"><span data-stu-id="ffb8f-109">CN</span></span>                | <span data-ttu-id="ffb8f-110">Телефон — Главная страница — другие</span><span class="sxs-lookup"><span data-stu-id="ffb8f-110">Phone-Home-Other</span></span>                                                                 |
| <span data-ttu-id="ffb8f-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ffb8f-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ffb8f-112">otherHomePhone</span><span class="sxs-lookup"><span data-stu-id="ffb8f-112">otherHomePhone</span></span>                                                                   |
| <span data-ttu-id="ffb8f-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ffb8f-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="ffb8f-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ffb8f-114">Update Privilege</span></span>  | <span data-ttu-id="ffb8f-115">Администратор домена или владелец учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ffb8f-115">Domain administrator or account owner.</span></span>                                           |
| <span data-ttu-id="ffb8f-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ffb8f-116">Update Frequency</span></span>  | <span data-ttu-id="ffb8f-117">При создании записи пользователя и при необходимости изменения номера телефона.</span><span class="sxs-lookup"><span data-stu-id="ffb8f-117">When the user's record is created and whenever the phone number needs to change.</span></span> |
| <span data-ttu-id="ffb8f-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-118">Attribute-Id</span></span>      | <span data-ttu-id="ffb8f-119">1.2.840.113556.1.2.277</span><span class="sxs-lookup"><span data-stu-id="ffb8f-119">1.2.840.113556.1.2.277</span></span>                                                           |
| <span data-ttu-id="ffb8f-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ffb8f-120">System-Id-Guid</span></span>    | <span data-ttu-id="ffb8f-121">f0f8ffa2-1191-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="ffb8f-121">f0f8ffa2-1191-11d0-a060-00aa006c33ed</span></span>                                             |
| <span data-ttu-id="ffb8f-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffb8f-122">Syntax</span></span>            | [<span data-ttu-id="ffb8f-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-123">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="ffb8f-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ffb8f-124">Implementations</span></span>

-   [<span data-ttu-id="ffb8f-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="ffb8f-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="ffb8f-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="ffb8f-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="ffb8f-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="ffb8f-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="ffb8f-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ffb8f-131">Windows 2000 Server</span></span>



| <span data-ttu-id="ffb8f-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-132">Entry</span></span> | <span data-ttu-id="ffb8f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-133">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffb8f-134">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ffb8f-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-135">MAPI-Id</span></span>                | <span data-ttu-id="ffb8f-136">0x3A2F</span><span class="sxs-lookup"><span data-stu-id="ffb8f-136">0x3A2F</span></span>                                                             |
| <span data-ttu-id="ffb8f-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb8f-137">System-Only</span></span>            | <span data-ttu-id="ffb8f-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-138">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffb8f-139">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb8f-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-140">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffb8f-141">Is Indexed</span></span>             | <span data-ttu-id="ffb8f-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-142">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffb8f-143">In Global Catalog</span></span>      | <span data-ttu-id="ffb8f-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-144">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffb8f-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb8f-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffb8f-146">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ffb8f-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb8f-147">Range-Lower</span></span>            | <span data-ttu-id="ffb8f-148">1</span><span class="sxs-lookup"><span data-stu-id="ffb8f-148">1</span></span>                                                                  |
| <span data-ttu-id="ffb8f-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb8f-149">Range-Upper</span></span>            | <span data-ttu-id="ffb8f-150">64</span><span class="sxs-lookup"><span data-stu-id="ffb8f-150">64</span></span>                                                                 |
| <span data-ttu-id="ffb8f-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-151">Search-Flags</span></span>           | <span data-ttu-id="ffb8f-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb8f-152">0x00000000</span></span>                                                         |
| <span data-ttu-id="ffb8f-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-153">System-Flags</span></span>           | <span data-ttu-id="ffb8f-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb8f-154">0x00000010</span></span>                                                         |
| <span data-ttu-id="ffb8f-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffb8f-155">Classes used in</span></span>        | [<span data-ttu-id="ffb8f-156">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-156">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="ffb8f-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ffb8f-157">Windows Server 2003</span></span>



| <span data-ttu-id="ffb8f-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-158">Entry</span></span> | <span data-ttu-id="ffb8f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-159">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffb8f-160">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ffb8f-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-161">MAPI-Id</span></span>                | <span data-ttu-id="ffb8f-162">0x3A2F</span><span class="sxs-lookup"><span data-stu-id="ffb8f-162">0x3A2F</span></span>                                                             |
| <span data-ttu-id="ffb8f-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb8f-163">System-Only</span></span>            | <span data-ttu-id="ffb8f-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-164">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffb8f-165">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb8f-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-166">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffb8f-167">Is Indexed</span></span>             | <span data-ttu-id="ffb8f-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-168">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffb8f-169">In Global Catalog</span></span>      | <span data-ttu-id="ffb8f-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-170">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffb8f-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb8f-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffb8f-172">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ffb8f-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb8f-173">Range-Lower</span></span>            | <span data-ttu-id="ffb8f-174">1</span><span class="sxs-lookup"><span data-stu-id="ffb8f-174">1</span></span>                                                                  |
| <span data-ttu-id="ffb8f-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb8f-175">Range-Upper</span></span>            | <span data-ttu-id="ffb8f-176">64</span><span class="sxs-lookup"><span data-stu-id="ffb8f-176">64</span></span>                                                                 |
| <span data-ttu-id="ffb8f-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-177">Search-Flags</span></span>           | <span data-ttu-id="ffb8f-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb8f-178">0x00000000</span></span>                                                         |
| <span data-ttu-id="ffb8f-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-179">System-Flags</span></span>           | <span data-ttu-id="ffb8f-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb8f-180">0x00000010</span></span>                                                         |
| <span data-ttu-id="ffb8f-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffb8f-181">Classes used in</span></span>        | [<span data-ttu-id="ffb8f-182">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-182">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="ffb8f-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="ffb8f-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="ffb8f-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-184">Entry</span></span> | <span data-ttu-id="ffb8f-185">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-185">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffb8f-186">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ffb8f-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-187">MAPI-Id</span></span>                | <span data-ttu-id="ffb8f-188">0x3A2F</span><span class="sxs-lookup"><span data-stu-id="ffb8f-188">0x3A2F</span></span>                                                             |
| <span data-ttu-id="ffb8f-189">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb8f-189">System-Only</span></span>            | <span data-ttu-id="ffb8f-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-190">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-191">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffb8f-191">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb8f-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-192">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-193">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffb8f-193">Is Indexed</span></span>             | <span data-ttu-id="ffb8f-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-194">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-195">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffb8f-195">In Global Catalog</span></span>      | <span data-ttu-id="ffb8f-196">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-196">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-197">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffb8f-197">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb8f-198">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffb8f-198">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ffb8f-199">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb8f-199">Range-Lower</span></span>            | <span data-ttu-id="ffb8f-200">1</span><span class="sxs-lookup"><span data-stu-id="ffb8f-200">1</span></span>                                                                  |
| <span data-ttu-id="ffb8f-201">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb8f-201">Range-Upper</span></span>            | <span data-ttu-id="ffb8f-202">64</span><span class="sxs-lookup"><span data-stu-id="ffb8f-202">64</span></span>                                                                 |
| <span data-ttu-id="ffb8f-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-203">Search-Flags</span></span>           | <span data-ttu-id="ffb8f-204">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb8f-204">0x00000000</span></span>                                                         |
| <span data-ttu-id="ffb8f-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-205">System-Flags</span></span>           | <span data-ttu-id="ffb8f-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb8f-206">0x00000010</span></span>                                                         |
| <span data-ttu-id="ffb8f-207">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffb8f-207">Classes used in</span></span>        | [<span data-ttu-id="ffb8f-208">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-208">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="ffb8f-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffb8f-209">Windows Server 2008</span></span>



| <span data-ttu-id="ffb8f-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-210">Entry</span></span> | <span data-ttu-id="ffb8f-211">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-211">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffb8f-212">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ffb8f-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-213">MAPI-Id</span></span>                | <span data-ttu-id="ffb8f-214">0x3A2F</span><span class="sxs-lookup"><span data-stu-id="ffb8f-214">0x3A2F</span></span>                                                             |
| <span data-ttu-id="ffb8f-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb8f-215">System-Only</span></span>            | <span data-ttu-id="ffb8f-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-216">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffb8f-217">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb8f-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-218">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffb8f-219">Is Indexed</span></span>             | <span data-ttu-id="ffb8f-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-220">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffb8f-221">In Global Catalog</span></span>      | <span data-ttu-id="ffb8f-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-222">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffb8f-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb8f-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffb8f-224">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ffb8f-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb8f-225">Range-Lower</span></span>            | <span data-ttu-id="ffb8f-226">1</span><span class="sxs-lookup"><span data-stu-id="ffb8f-226">1</span></span>                                                                  |
| <span data-ttu-id="ffb8f-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb8f-227">Range-Upper</span></span>            | <span data-ttu-id="ffb8f-228">64</span><span class="sxs-lookup"><span data-stu-id="ffb8f-228">64</span></span>                                                                 |
| <span data-ttu-id="ffb8f-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-229">Search-Flags</span></span>           | <span data-ttu-id="ffb8f-230">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb8f-230">0x00000000</span></span>                                                         |
| <span data-ttu-id="ffb8f-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-231">System-Flags</span></span>           | <span data-ttu-id="ffb8f-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb8f-232">0x00000010</span></span>                                                         |
| <span data-ttu-id="ffb8f-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffb8f-233">Classes used in</span></span>        | [<span data-ttu-id="ffb8f-234">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-234">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="ffb8f-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ffb8f-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="ffb8f-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-236">Entry</span></span> | <span data-ttu-id="ffb8f-237">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-237">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffb8f-238">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ffb8f-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-239">MAPI-Id</span></span>                | <span data-ttu-id="ffb8f-240">0x3A2F</span><span class="sxs-lookup"><span data-stu-id="ffb8f-240">0x3A2F</span></span>                                                             |
| <span data-ttu-id="ffb8f-241">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb8f-241">System-Only</span></span>            | <span data-ttu-id="ffb8f-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-242">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-243">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffb8f-243">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb8f-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-244">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-245">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffb8f-245">Is Indexed</span></span>             | <span data-ttu-id="ffb8f-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-246">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-247">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffb8f-247">In Global Catalog</span></span>      | <span data-ttu-id="ffb8f-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-248">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-249">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffb8f-249">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb8f-250">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffb8f-250">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ffb8f-251">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb8f-251">Range-Lower</span></span>            | <span data-ttu-id="ffb8f-252">1</span><span class="sxs-lookup"><span data-stu-id="ffb8f-252">1</span></span>                                                                  |
| <span data-ttu-id="ffb8f-253">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb8f-253">Range-Upper</span></span>            | <span data-ttu-id="ffb8f-254">64</span><span class="sxs-lookup"><span data-stu-id="ffb8f-254">64</span></span>                                                                 |
| <span data-ttu-id="ffb8f-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-255">Search-Flags</span></span>           | <span data-ttu-id="ffb8f-256">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb8f-256">0x00000000</span></span>                                                         |
| <span data-ttu-id="ffb8f-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-257">System-Flags</span></span>           | <span data-ttu-id="ffb8f-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb8f-258">0x00000010</span></span>                                                         |
| <span data-ttu-id="ffb8f-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffb8f-259">Classes used in</span></span>        | [<span data-ttu-id="ffb8f-260">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-260">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="ffb8f-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffb8f-261">Windows Server 2012</span></span>



| <span data-ttu-id="ffb8f-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="ffb8f-262">Entry</span></span> | <span data-ttu-id="ffb8f-263">Значение</span><span class="sxs-lookup"><span data-stu-id="ffb8f-263">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ffb8f-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ffb8f-264">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ffb8f-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ffb8f-265">MAPI-Id</span></span>                | <span data-ttu-id="ffb8f-266">0x3A2F</span><span class="sxs-lookup"><span data-stu-id="ffb8f-266">0x3A2F</span></span>                                                             |
| <span data-ttu-id="ffb8f-267">System-Only</span><span class="sxs-lookup"><span data-stu-id="ffb8f-267">System-Only</span></span>            | <span data-ttu-id="ffb8f-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-268">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-269">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ffb8f-269">Is-Single-Valued</span></span>       | <span data-ttu-id="ffb8f-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-270">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-271">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ffb8f-271">Is Indexed</span></span>             | <span data-ttu-id="ffb8f-272">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-272">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-273">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ffb8f-273">In Global Catalog</span></span>      | <span data-ttu-id="ffb8f-274">Неверно</span><span class="sxs-lookup"><span data-stu-id="ffb8f-274">False</span></span>                                                              |
| <span data-ttu-id="ffb8f-275">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ffb8f-275">NT-Security-Descriptor</span></span> | <span data-ttu-id="ffb8f-276">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ffb8f-276">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ffb8f-277">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ffb8f-277">Range-Lower</span></span>            | <span data-ttu-id="ffb8f-278">1</span><span class="sxs-lookup"><span data-stu-id="ffb8f-278">1</span></span>                                                                  |
| <span data-ttu-id="ffb8f-279">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ffb8f-279">Range-Upper</span></span>            | <span data-ttu-id="ffb8f-280">64</span><span class="sxs-lookup"><span data-stu-id="ffb8f-280">64</span></span>                                                                 |
| <span data-ttu-id="ffb8f-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-281">Search-Flags</span></span>           | <span data-ttu-id="ffb8f-282">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ffb8f-282">0x00000000</span></span>                                                         |
| <span data-ttu-id="ffb8f-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ffb8f-283">System-Flags</span></span>           | <span data-ttu-id="ffb8f-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ffb8f-284">0x00000010</span></span>                                                         |
| <span data-ttu-id="ffb8f-285">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ffb8f-285">Classes used in</span></span>        | [<span data-ttu-id="ffb8f-286">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ffb8f-286">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





