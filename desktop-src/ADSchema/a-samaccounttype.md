---
title: Атрибут SAM-Account-Type
description: Этот атрибут содержит сведения о каждом объекте типа учетной записи.
ms.assetid: 00479b89-1d96-4ace-bbd8-053ca9e548b0
ms.tgt_platform: multiple
keywords:
- SAM-тип учетной записи-схема AD
- Схема AD атрибута sAMAccountType
topic_type:
- apiref
api_name:
- SAM-Account-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51de46dac0faabcc248159f7dcabafcd6060725
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989631"
---
# <a name="sam-account-type-attribute"></a><span data-ttu-id="09945-105">Атрибут SAM-Account-Type</span><span class="sxs-lookup"><span data-stu-id="09945-105">SAM-Account-Type attribute</span></span>

<span data-ttu-id="09945-106">Этот атрибут содержит сведения о каждом объекте типа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="09945-106">This attribute contains information about every account type object.</span></span> <span data-ttu-id="09945-107">Вы можете перечислить список типов учетных записей или использовать API экранной информации для создания списка.</span><span class="sxs-lookup"><span data-stu-id="09945-107">You can enumerate a list of account types or you can use the Display Information API to create a list.</span></span> <span data-ttu-id="09945-108">Так как компьютеры, обычные учетные записи пользователей и учетные записи доверия могут перечисляться как объекты пользователя, значения этих учетных записей должны быть непрерывного диапазона.</span><span class="sxs-lookup"><span data-stu-id="09945-108">Because computers, normal user accounts, and trust accounts can also be enumerated as user objects, the values for these accounts must be a contiguous range.</span></span>

<span data-ttu-id="09945-109">Ниже приведены возможные значения для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="09945-109">The possible values for this attribute are the following:</span></span>

-   <span data-ttu-id="09945-110">SAM \_ доменное \_ объект 0x0</span><span class="sxs-lookup"><span data-stu-id="09945-110">SAM\_DOMAIN\_OBJECT 0x0</span></span>
-   <span data-ttu-id="09945-111">SAM \_ Group \_ Object 0x10000000</span><span class="sxs-lookup"><span data-stu-id="09945-111">SAM\_GROUP\_OBJECT 0x10000000</span></span>
-   <span data-ttu-id="09945-112">SAM \_ : \_ \_ \_ 0x10000001 объекта группы безопасности</span><span class="sxs-lookup"><span data-stu-id="09945-112">SAM\_NON\_SECURITY\_GROUP\_OBJECT 0x10000001</span></span>
-   <span data-ttu-id="09945-113">SAM: \_ псевдоним \_ объекта 0x20000000</span><span class="sxs-lookup"><span data-stu-id="09945-113">SAM\_ALIAS\_OBJECT 0x20000000</span></span>
-   <span data-ttu-id="09945-114">SAM \_ не \_ \_ 0x20000001 объект псевдонима безопасности \_</span><span class="sxs-lookup"><span data-stu-id="09945-114">SAM\_NON\_SECURITY\_ALIAS\_OBJECT 0x20000001</span></span>
-   <span data-ttu-id="09945-115">\_ \_ 0x30000000 объект пользователя SAM</span><span class="sxs-lookup"><span data-stu-id="09945-115">SAM\_USER\_OBJECT 0x30000000</span></span>
-   <span data-ttu-id="09945-116">SAM \_ Обычная \_ \_ учетная запись пользователя 0x30000000</span><span class="sxs-lookup"><span data-stu-id="09945-116">SAM\_NORMAL\_USER\_ACCOUNT 0x30000000</span></span>
-   <span data-ttu-id="09945-117">SAM \_ \_ 0x30000001 учетной записи компьютера</span><span class="sxs-lookup"><span data-stu-id="09945-117">SAM\_MACHINE\_ACCOUNT 0x30000001</span></span>
-   <span data-ttu-id="09945-118">SAM: \_ доверие \_ учетной записи 0x30000002</span><span class="sxs-lookup"><span data-stu-id="09945-118">SAM\_TRUST\_ACCOUNT 0x30000002</span></span>
-   <span data-ttu-id="09945-119">\_ \_ 0x40000000 группы основных приложений SAM \_</span><span class="sxs-lookup"><span data-stu-id="09945-119">SAM\_APP\_BASIC\_GROUP 0x40000000</span></span>
-   <span data-ttu-id="09945-120">\_ \_ 0x40000001 группы запросов приложения SAM \_</span><span class="sxs-lookup"><span data-stu-id="09945-120">SAM\_APP\_QUERY\_GROUP 0x40000001</span></span>
-   <span data-ttu-id="09945-121">\_Тип учетной записи SAM \_ \_ Max 0x7FFFFFFF</span><span class="sxs-lookup"><span data-stu-id="09945-121">SAM\_ACCOUNT\_TYPE\_MAX 0x7fffffff</span></span>



| <span data-ttu-id="09945-122">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-122">Entry</span></span> | <span data-ttu-id="09945-123">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------|
| <span data-ttu-id="09945-124">CN</span><span class="sxs-lookup"><span data-stu-id="09945-124">CN</span></span>                | <span data-ttu-id="09945-125">SAM-тип учетной записи</span><span class="sxs-lookup"><span data-stu-id="09945-125">SAM-Account-Type</span></span>                                                |
| <span data-ttu-id="09945-126">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="09945-126">Ldap-Display-Name</span></span> | <span data-ttu-id="09945-127">sAMAccountType</span><span class="sxs-lookup"><span data-stu-id="09945-127">sAMAccountType</span></span>                                                  |
| <span data-ttu-id="09945-128">Размер</span><span class="sxs-lookup"><span data-stu-id="09945-128">Size</span></span>              | \-                                                              |
| <span data-ttu-id="09945-129">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="09945-129">Update Privilege</span></span>  | <span data-ttu-id="09945-130">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="09945-130">This value is set by the system.</span></span>                                |
| <span data-ttu-id="09945-131">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="09945-131">Update Frequency</span></span>  | <span data-ttu-id="09945-132">Это значение задается операционной системой при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="09945-132">This is set by the operating system when the object is created.</span></span> |
| <span data-ttu-id="09945-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="09945-133">Attribute-Id</span></span>      | <span data-ttu-id="09945-134">1.2.840.113556.1.4.302</span><span class="sxs-lookup"><span data-stu-id="09945-134">1.2.840.113556.1.4.302</span></span>                                          |
| <span data-ttu-id="09945-135">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="09945-135">System-Id-Guid</span></span>    | <span data-ttu-id="09945-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="09945-136">6e7b626c-64f2-11d0-afd2-00c04fd930c9</span></span>                            |
| <span data-ttu-id="09945-137">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09945-137">Syntax</span></span>            | [<span data-ttu-id="09945-138">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="09945-138">**Enumeration**</span></span>](s-enumeration.md)                            |



## <a name="implementations"></a><span data-ttu-id="09945-139">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="09945-139">Implementations</span></span>

-   [<span data-ttu-id="09945-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="09945-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="09945-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="09945-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="09945-142">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="09945-142">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="09945-143">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="09945-143">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="09945-144">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="09945-144">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="09945-145">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="09945-145">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="09945-146">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09945-146">Windows 2000 Server</span></span>



| <span data-ttu-id="09945-147">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-147">Entry</span></span> | <span data-ttu-id="09945-148">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-148">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09945-149">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09945-149">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-150">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09945-150">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-151">System-Only</span><span class="sxs-lookup"><span data-stu-id="09945-151">System-Only</span></span>            | <span data-ttu-id="09945-152">Неверно</span><span class="sxs-lookup"><span data-stu-id="09945-152">False</span></span>                                                        |
| <span data-ttu-id="09945-153">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09945-153">Is-Single-Valued</span></span>       | <span data-ttu-id="09945-154">True</span><span class="sxs-lookup"><span data-stu-id="09945-154">True</span></span>                                                         |
| <span data-ttu-id="09945-155">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09945-155">Is Indexed</span></span>             | <span data-ttu-id="09945-156">True</span><span class="sxs-lookup"><span data-stu-id="09945-156">True</span></span>                                                         |
| <span data-ttu-id="09945-157">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09945-157">In Global Catalog</span></span>      | <span data-ttu-id="09945-158">True</span><span class="sxs-lookup"><span data-stu-id="09945-158">True</span></span>                                                         |
| <span data-ttu-id="09945-159">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09945-159">NT-Security-Descriptor</span></span> | <span data-ttu-id="09945-160">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09945-160">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="09945-161">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09945-161">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="09945-162">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09945-162">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="09945-163">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-163">Search-Flags</span></span>           | <span data-ttu-id="09945-164">0x00000001</span><span class="sxs-lookup"><span data-stu-id="09945-164">0x00000001</span></span>                                                   |
| <span data-ttu-id="09945-165">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-165">System-Flags</span></span>           | <span data-ttu-id="09945-166">0x00000012</span><span class="sxs-lookup"><span data-stu-id="09945-166">0x00000012</span></span>                                                   |
| <span data-ttu-id="09945-167">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09945-167">Classes used in</span></span>        | [<span data-ttu-id="09945-168">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="09945-168">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="09945-169">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09945-169">Windows Server 2003</span></span>



| <span data-ttu-id="09945-170">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-170">Entry</span></span> | <span data-ttu-id="09945-171">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-171">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09945-172">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09945-172">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-173">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09945-173">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-174">System-Only</span><span class="sxs-lookup"><span data-stu-id="09945-174">System-Only</span></span>            | <span data-ttu-id="09945-175">Неверно</span><span class="sxs-lookup"><span data-stu-id="09945-175">False</span></span>                                                        |
| <span data-ttu-id="09945-176">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09945-176">Is-Single-Valued</span></span>       | <span data-ttu-id="09945-177">True</span><span class="sxs-lookup"><span data-stu-id="09945-177">True</span></span>                                                         |
| <span data-ttu-id="09945-178">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09945-178">Is Indexed</span></span>             | <span data-ttu-id="09945-179">True</span><span class="sxs-lookup"><span data-stu-id="09945-179">True</span></span>                                                         |
| <span data-ttu-id="09945-180">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09945-180">In Global Catalog</span></span>      | <span data-ttu-id="09945-181">True</span><span class="sxs-lookup"><span data-stu-id="09945-181">True</span></span>                                                         |
| <span data-ttu-id="09945-182">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09945-182">NT-Security-Descriptor</span></span> | <span data-ttu-id="09945-183">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09945-183">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="09945-184">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09945-184">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="09945-185">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09945-185">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="09945-186">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-186">Search-Flags</span></span>           | <span data-ttu-id="09945-187">0x00000001</span><span class="sxs-lookup"><span data-stu-id="09945-187">0x00000001</span></span>                                                   |
| <span data-ttu-id="09945-188">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-188">System-Flags</span></span>           | <span data-ttu-id="09945-189">0x00000012</span><span class="sxs-lookup"><span data-stu-id="09945-189">0x00000012</span></span>                                                   |
| <span data-ttu-id="09945-190">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09945-190">Classes used in</span></span>        | [<span data-ttu-id="09945-191">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="09945-191">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="09945-192">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="09945-192">Windows Server 2003 R2</span></span>



| <span data-ttu-id="09945-193">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-193">Entry</span></span> | <span data-ttu-id="09945-194">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-194">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09945-195">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09945-195">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-196">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09945-196">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-197">System-Only</span><span class="sxs-lookup"><span data-stu-id="09945-197">System-Only</span></span>            | <span data-ttu-id="09945-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="09945-198">False</span></span>                                                        |
| <span data-ttu-id="09945-199">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09945-199">Is-Single-Valued</span></span>       | <span data-ttu-id="09945-200">True</span><span class="sxs-lookup"><span data-stu-id="09945-200">True</span></span>                                                         |
| <span data-ttu-id="09945-201">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09945-201">Is Indexed</span></span>             | <span data-ttu-id="09945-202">True</span><span class="sxs-lookup"><span data-stu-id="09945-202">True</span></span>                                                         |
| <span data-ttu-id="09945-203">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09945-203">In Global Catalog</span></span>      | <span data-ttu-id="09945-204">True</span><span class="sxs-lookup"><span data-stu-id="09945-204">True</span></span>                                                         |
| <span data-ttu-id="09945-205">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09945-205">NT-Security-Descriptor</span></span> | <span data-ttu-id="09945-206">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09945-206">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="09945-207">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09945-207">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="09945-208">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09945-208">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="09945-209">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-209">Search-Flags</span></span>           | <span data-ttu-id="09945-210">0x00000001</span><span class="sxs-lookup"><span data-stu-id="09945-210">0x00000001</span></span>                                                   |
| <span data-ttu-id="09945-211">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-211">System-Flags</span></span>           | <span data-ttu-id="09945-212">0x00000012</span><span class="sxs-lookup"><span data-stu-id="09945-212">0x00000012</span></span>                                                   |
| <span data-ttu-id="09945-213">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09945-213">Classes used in</span></span>        | [<span data-ttu-id="09945-214">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="09945-214">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="09945-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09945-215">Windows Server 2008</span></span>



| <span data-ttu-id="09945-216">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-216">Entry</span></span> | <span data-ttu-id="09945-217">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-217">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09945-218">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09945-218">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-219">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09945-219">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-220">System-Only</span><span class="sxs-lookup"><span data-stu-id="09945-220">System-Only</span></span>            | <span data-ttu-id="09945-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="09945-221">False</span></span>                                                        |
| <span data-ttu-id="09945-222">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09945-222">Is-Single-Valued</span></span>       | <span data-ttu-id="09945-223">True</span><span class="sxs-lookup"><span data-stu-id="09945-223">True</span></span>                                                         |
| <span data-ttu-id="09945-224">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09945-224">Is Indexed</span></span>             | <span data-ttu-id="09945-225">True</span><span class="sxs-lookup"><span data-stu-id="09945-225">True</span></span>                                                         |
| <span data-ttu-id="09945-226">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09945-226">In Global Catalog</span></span>      | <span data-ttu-id="09945-227">True</span><span class="sxs-lookup"><span data-stu-id="09945-227">True</span></span>                                                         |
| <span data-ttu-id="09945-228">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09945-228">NT-Security-Descriptor</span></span> | <span data-ttu-id="09945-229">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09945-229">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="09945-230">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09945-230">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="09945-231">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09945-231">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="09945-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-232">Search-Flags</span></span>           | <span data-ttu-id="09945-233">0x00000001</span><span class="sxs-lookup"><span data-stu-id="09945-233">0x00000001</span></span>                                                   |
| <span data-ttu-id="09945-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-234">System-Flags</span></span>           | <span data-ttu-id="09945-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="09945-235">0x00000012</span></span>                                                   |
| <span data-ttu-id="09945-236">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09945-236">Classes used in</span></span>        | [<span data-ttu-id="09945-237">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="09945-237">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="09945-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09945-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="09945-239">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-239">Entry</span></span> | <span data-ttu-id="09945-240">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-240">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09945-241">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09945-241">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09945-242">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="09945-243">System-Only</span></span>            | <span data-ttu-id="09945-244">Неверно</span><span class="sxs-lookup"><span data-stu-id="09945-244">False</span></span>                                                        |
| <span data-ttu-id="09945-245">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09945-245">Is-Single-Valued</span></span>       | <span data-ttu-id="09945-246">True</span><span class="sxs-lookup"><span data-stu-id="09945-246">True</span></span>                                                         |
| <span data-ttu-id="09945-247">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09945-247">Is Indexed</span></span>             | <span data-ttu-id="09945-248">True</span><span class="sxs-lookup"><span data-stu-id="09945-248">True</span></span>                                                         |
| <span data-ttu-id="09945-249">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09945-249">In Global Catalog</span></span>      | <span data-ttu-id="09945-250">True</span><span class="sxs-lookup"><span data-stu-id="09945-250">True</span></span>                                                         |
| <span data-ttu-id="09945-251">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09945-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="09945-252">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09945-252">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="09945-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09945-253">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="09945-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09945-254">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="09945-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-255">Search-Flags</span></span>           | <span data-ttu-id="09945-256">0x00000001</span><span class="sxs-lookup"><span data-stu-id="09945-256">0x00000001</span></span>                                                   |
| <span data-ttu-id="09945-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-257">System-Flags</span></span>           | <span data-ttu-id="09945-258">0x00000012</span><span class="sxs-lookup"><span data-stu-id="09945-258">0x00000012</span></span>                                                   |
| <span data-ttu-id="09945-259">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09945-259">Classes used in</span></span>        | [<span data-ttu-id="09945-260">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="09945-260">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="09945-261">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="09945-261">Windows Server 2012</span></span>



| <span data-ttu-id="09945-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="09945-262">Entry</span></span> | <span data-ttu-id="09945-263">Значение</span><span class="sxs-lookup"><span data-stu-id="09945-263">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09945-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="09945-264">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="09945-265">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="09945-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="09945-266">System-Only</span></span>            | <span data-ttu-id="09945-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="09945-267">False</span></span>                                                        |
| <span data-ttu-id="09945-268">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="09945-268">Is-Single-Valued</span></span>       | <span data-ttu-id="09945-269">True</span><span class="sxs-lookup"><span data-stu-id="09945-269">True</span></span>                                                         |
| <span data-ttu-id="09945-270">Индексируется</span><span class="sxs-lookup"><span data-stu-id="09945-270">Is Indexed</span></span>             | <span data-ttu-id="09945-271">True</span><span class="sxs-lookup"><span data-stu-id="09945-271">True</span></span>                                                         |
| <span data-ttu-id="09945-272">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="09945-272">In Global Catalog</span></span>      | <span data-ttu-id="09945-273">True</span><span class="sxs-lookup"><span data-stu-id="09945-273">True</span></span>                                                         |
| <span data-ttu-id="09945-274">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="09945-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="09945-275">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="09945-275">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="09945-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="09945-276">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="09945-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="09945-277">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="09945-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-278">Search-Flags</span></span>           | <span data-ttu-id="09945-279">0x00000001</span><span class="sxs-lookup"><span data-stu-id="09945-279">0x00000001</span></span>                                                   |
| <span data-ttu-id="09945-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="09945-280">System-Flags</span></span>           | <span data-ttu-id="09945-281">0x00000012</span><span class="sxs-lookup"><span data-stu-id="09945-281">0x00000012</span></span>                                                   |
| <span data-ttu-id="09945-282">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="09945-282">Classes used in</span></span>        | [<span data-ttu-id="09945-283">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="09945-283">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





