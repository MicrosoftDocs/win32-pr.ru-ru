---
title: Атрибут UAS-Compat
description: Указывает, будет ли диспетчер учетных записей безопасности применять размеры данных, чтобы сделать Active Directory совместимыми с системой учетных записей пользователей (UAS) Ланманажер.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута UAS-Compat
- Схема AD атрибута Уаскомпат
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655279"
---
# <a name="uas-compat-attribute"></a><span data-ttu-id="981f2-105">Атрибут UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="981f2-105">UAS-Compat attribute</span></span>

<span data-ttu-id="981f2-106">Указывает, будет ли диспетчер учетных записей безопасности применять размеры данных, чтобы сделать Active Directory совместимыми с системой учетных записей пользователей (UAS) Ланманажер.</span><span class="sxs-lookup"><span data-stu-id="981f2-106">Indicates if the security account manager will enforce data sizes to make Active Directory compatible with the LanManager User Account System (UAS).</span></span> <span data-ttu-id="981f2-107">Если это значение равно 0, ограничения не применяются.</span><span class="sxs-lookup"><span data-stu-id="981f2-107">If this value is 0, no limits are enforced.</span></span> <span data-ttu-id="981f2-108">Если это значение равно 1, применяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="981f2-108">If this value is 1, the following limits are enforced.</span></span>



| <span data-ttu-id="981f2-109">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-109">Value</span></span>                          | <span data-ttu-id="981f2-110">Длина</span><span class="sxs-lookup"><span data-stu-id="981f2-110">Length</span></span>                         |
|--------------------------------|--------------------------------|
| <span data-ttu-id="981f2-111">Пароль</span><span class="sxs-lookup"><span data-stu-id="981f2-111">Password</span></span><br/>            | <span data-ttu-id="981f2-112">от 0 до 14 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-112">0 to 14 characters</span></span><br/>  |
| <span data-ttu-id="981f2-113">Имя учетной записи</span><span class="sxs-lookup"><span data-stu-id="981f2-113">Account Name</span></span><br/>        | <span data-ttu-id="981f2-114">от 0 до 20 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-114">0 to 20 characters</span></span><br/>  |
| <span data-ttu-id="981f2-115">Имя домена</span><span class="sxs-lookup"><span data-stu-id="981f2-115">Domain Name</span></span><br/>         | <span data-ttu-id="981f2-116">от 0 до 15 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-116">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="981f2-117">Имя компьютера</span><span class="sxs-lookup"><span data-stu-id="981f2-117">Computer Name</span></span><br/>       | <span data-ttu-id="981f2-118">от 0 до 15 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-118">0 to 15 characters</span></span><br/>  |
| <span data-ttu-id="981f2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="981f2-119">Comments</span></span><br/>            | <span data-ttu-id="981f2-120">от 0 до 48 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-120">0 to 48 characters</span></span><br/>  |
| <span data-ttu-id="981f2-121">Домашний каталог</span><span class="sxs-lookup"><span data-stu-id="981f2-121">Home Directory</span></span><br/>      | <span data-ttu-id="981f2-122">от 0 до 256 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-122">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="981f2-123">Путь к сценарию</span><span class="sxs-lookup"><span data-stu-id="981f2-123">Script Path</span></span><br/>         | <span data-ttu-id="981f2-124">от 0 до 256 символов</span><span class="sxs-lookup"><span data-stu-id="981f2-124">0 to 256 characters</span></span><br/> |
| <span data-ttu-id="981f2-125">Единицы времени в неделю</span><span class="sxs-lookup"><span data-stu-id="981f2-125">Time Units Per Week</span></span><br/> | <span data-ttu-id="981f2-126">168 бит (21 байт)</span><span class="sxs-lookup"><span data-stu-id="981f2-126">168 bits (21 bytes)</span></span><br/> |



 



| <span data-ttu-id="981f2-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-127">Entry</span></span> | <span data-ttu-id="981f2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-128">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="981f2-129">CN</span><span class="sxs-lookup"><span data-stu-id="981f2-129">CN</span></span>                | <span data-ttu-id="981f2-130">UAS-Compat</span><span class="sxs-lookup"><span data-stu-id="981f2-130">UAS-Compat</span></span>                           |
| <span data-ttu-id="981f2-131">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="981f2-131">Ldap-Display-Name</span></span> | <span data-ttu-id="981f2-132">уаскомпат</span><span class="sxs-lookup"><span data-stu-id="981f2-132">uASCompat</span></span>                            |
| <span data-ttu-id="981f2-133">Размер</span><span class="sxs-lookup"><span data-stu-id="981f2-133">Size</span></span>              | \-                                   |
| <span data-ttu-id="981f2-134">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="981f2-134">Update Privilege</span></span>  | <span data-ttu-id="981f2-135">Выполняется администратором.</span><span class="sxs-lookup"><span data-stu-id="981f2-135">Performed by an administrator.</span></span>       |
| <span data-ttu-id="981f2-136">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="981f2-136">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="981f2-137">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-137">Attribute-Id</span></span>      | <span data-ttu-id="981f2-138">1.2.840.113556.1.4.155</span><span class="sxs-lookup"><span data-stu-id="981f2-138">1.2.840.113556.1.4.155</span></span>               |
| <span data-ttu-id="981f2-139">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="981f2-139">System-Id-Guid</span></span>    | <span data-ttu-id="981f2-140">bf967a61-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="981f2-140">bf967a61-0de6-11d0-a285-00aa003049e2</span></span> |
| <span data-ttu-id="981f2-141">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="981f2-141">Syntax</span></span>            | [<span data-ttu-id="981f2-142">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="981f2-142">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="981f2-143">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="981f2-143">Implementations</span></span>

-   [<span data-ttu-id="981f2-144">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="981f2-144">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="981f2-145">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="981f2-145">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="981f2-146">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="981f2-146">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="981f2-147">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="981f2-147">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="981f2-148">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="981f2-148">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="981f2-149">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="981f2-149">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="981f2-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="981f2-150">Windows 2000 Server</span></span>



| <span data-ttu-id="981f2-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-151">Entry</span></span> | <span data-ttu-id="981f2-152">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-152">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="981f2-153">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="981f2-153">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-154">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="981f2-155">System-Only</span></span>            | <span data-ttu-id="981f2-156">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-156">False</span></span>                                                 |
| <span data-ttu-id="981f2-157">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="981f2-157">Is-Single-Valued</span></span>       | <span data-ttu-id="981f2-158">True</span><span class="sxs-lookup"><span data-stu-id="981f2-158">True</span></span>                                                  |
| <span data-ttu-id="981f2-159">Индексируется</span><span class="sxs-lookup"><span data-stu-id="981f2-159">Is Indexed</span></span>             | <span data-ttu-id="981f2-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-160">False</span></span>                                                 |
| <span data-ttu-id="981f2-161">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="981f2-161">In Global Catalog</span></span>      | <span data-ttu-id="981f2-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-162">False</span></span>                                                 |
| <span data-ttu-id="981f2-163">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="981f2-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="981f2-164">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="981f2-164">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="981f2-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981f2-165">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981f2-166">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-167">Search-Flags</span></span>           | <span data-ttu-id="981f2-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981f2-168">0x00000000</span></span>                                            |
| <span data-ttu-id="981f2-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-169">System-Flags</span></span>           | <span data-ttu-id="981f2-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981f2-170">0x00000010</span></span>                                            |
| <span data-ttu-id="981f2-171">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="981f2-171">Classes used in</span></span>        | [<span data-ttu-id="981f2-172">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="981f2-172">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="981f2-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="981f2-173">Windows Server 2003</span></span>



| <span data-ttu-id="981f2-174">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-174">Entry</span></span> | <span data-ttu-id="981f2-175">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-175">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="981f2-176">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="981f2-176">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-177">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-178">System-Only</span><span class="sxs-lookup"><span data-stu-id="981f2-178">System-Only</span></span>            | <span data-ttu-id="981f2-179">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-179">False</span></span>                                                 |
| <span data-ttu-id="981f2-180">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="981f2-180">Is-Single-Valued</span></span>       | <span data-ttu-id="981f2-181">True</span><span class="sxs-lookup"><span data-stu-id="981f2-181">True</span></span>                                                  |
| <span data-ttu-id="981f2-182">Индексируется</span><span class="sxs-lookup"><span data-stu-id="981f2-182">Is Indexed</span></span>             | <span data-ttu-id="981f2-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-183">False</span></span>                                                 |
| <span data-ttu-id="981f2-184">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="981f2-184">In Global Catalog</span></span>      | <span data-ttu-id="981f2-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-185">False</span></span>                                                 |
| <span data-ttu-id="981f2-186">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="981f2-186">NT-Security-Descriptor</span></span> | <span data-ttu-id="981f2-187">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="981f2-187">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="981f2-188">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981f2-188">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-189">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981f2-189">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-190">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-190">Search-Flags</span></span>           | <span data-ttu-id="981f2-191">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981f2-191">0x00000000</span></span>                                            |
| <span data-ttu-id="981f2-192">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-192">System-Flags</span></span>           | <span data-ttu-id="981f2-193">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981f2-193">0x00000010</span></span>                                            |
| <span data-ttu-id="981f2-194">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="981f2-194">Classes used in</span></span>        | [<span data-ttu-id="981f2-195">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="981f2-195">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="981f2-196">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="981f2-196">Windows Server 2003 R2</span></span>



| <span data-ttu-id="981f2-197">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-197">Entry</span></span> | <span data-ttu-id="981f2-198">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-198">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="981f2-199">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="981f2-199">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-200">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-200">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-201">System-Only</span><span class="sxs-lookup"><span data-stu-id="981f2-201">System-Only</span></span>            | <span data-ttu-id="981f2-202">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-202">False</span></span>                                                 |
| <span data-ttu-id="981f2-203">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="981f2-203">Is-Single-Valued</span></span>       | <span data-ttu-id="981f2-204">True</span><span class="sxs-lookup"><span data-stu-id="981f2-204">True</span></span>                                                  |
| <span data-ttu-id="981f2-205">Индексируется</span><span class="sxs-lookup"><span data-stu-id="981f2-205">Is Indexed</span></span>             | <span data-ttu-id="981f2-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-206">False</span></span>                                                 |
| <span data-ttu-id="981f2-207">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="981f2-207">In Global Catalog</span></span>      | <span data-ttu-id="981f2-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-208">False</span></span>                                                 |
| <span data-ttu-id="981f2-209">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="981f2-209">NT-Security-Descriptor</span></span> | <span data-ttu-id="981f2-210">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="981f2-210">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="981f2-211">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981f2-211">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981f2-212">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-213">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-213">Search-Flags</span></span>           | <span data-ttu-id="981f2-214">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981f2-214">0x00000000</span></span>                                            |
| <span data-ttu-id="981f2-215">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-215">System-Flags</span></span>           | <span data-ttu-id="981f2-216">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981f2-216">0x00000010</span></span>                                            |
| <span data-ttu-id="981f2-217">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="981f2-217">Classes used in</span></span>        | [<span data-ttu-id="981f2-218">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="981f2-218">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="981f2-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="981f2-219">Windows Server 2008</span></span>



| <span data-ttu-id="981f2-220">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-220">Entry</span></span> | <span data-ttu-id="981f2-221">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-221">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="981f2-222">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="981f2-222">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-223">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-223">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-224">System-Only</span><span class="sxs-lookup"><span data-stu-id="981f2-224">System-Only</span></span>            | <span data-ttu-id="981f2-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-225">False</span></span>                                                 |
| <span data-ttu-id="981f2-226">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="981f2-226">Is-Single-Valued</span></span>       | <span data-ttu-id="981f2-227">True</span><span class="sxs-lookup"><span data-stu-id="981f2-227">True</span></span>                                                  |
| <span data-ttu-id="981f2-228">Индексируется</span><span class="sxs-lookup"><span data-stu-id="981f2-228">Is Indexed</span></span>             | <span data-ttu-id="981f2-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-229">False</span></span>                                                 |
| <span data-ttu-id="981f2-230">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="981f2-230">In Global Catalog</span></span>      | <span data-ttu-id="981f2-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-231">False</span></span>                                                 |
| <span data-ttu-id="981f2-232">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="981f2-232">NT-Security-Descriptor</span></span> | <span data-ttu-id="981f2-233">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="981f2-233">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="981f2-234">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981f2-234">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-235">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981f2-235">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-236">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-236">Search-Flags</span></span>           | <span data-ttu-id="981f2-237">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981f2-237">0x00000000</span></span>                                            |
| <span data-ttu-id="981f2-238">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-238">System-Flags</span></span>           | <span data-ttu-id="981f2-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981f2-239">0x00000010</span></span>                                            |
| <span data-ttu-id="981f2-240">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="981f2-240">Classes used in</span></span>        | [<span data-ttu-id="981f2-241">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="981f2-241">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="981f2-242">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="981f2-242">Windows Server 2008 R2</span></span>



| <span data-ttu-id="981f2-243">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-243">Entry</span></span> | <span data-ttu-id="981f2-244">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-244">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="981f2-245">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="981f2-245">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-246">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-246">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-247">System-Only</span><span class="sxs-lookup"><span data-stu-id="981f2-247">System-Only</span></span>            | <span data-ttu-id="981f2-248">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-248">False</span></span>                                                 |
| <span data-ttu-id="981f2-249">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="981f2-249">Is-Single-Valued</span></span>       | <span data-ttu-id="981f2-250">True</span><span class="sxs-lookup"><span data-stu-id="981f2-250">True</span></span>                                                  |
| <span data-ttu-id="981f2-251">Индексируется</span><span class="sxs-lookup"><span data-stu-id="981f2-251">Is Indexed</span></span>             | <span data-ttu-id="981f2-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-252">False</span></span>                                                 |
| <span data-ttu-id="981f2-253">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="981f2-253">In Global Catalog</span></span>      | <span data-ttu-id="981f2-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-254">False</span></span>                                                 |
| <span data-ttu-id="981f2-255">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="981f2-255">NT-Security-Descriptor</span></span> | <span data-ttu-id="981f2-256">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="981f2-256">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="981f2-257">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981f2-257">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-258">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981f2-258">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-259">Search-Flags</span></span>           | <span data-ttu-id="981f2-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981f2-260">0x00000000</span></span>                                            |
| <span data-ttu-id="981f2-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-261">System-Flags</span></span>           | <span data-ttu-id="981f2-262">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981f2-262">0x00000010</span></span>                                            |
| <span data-ttu-id="981f2-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="981f2-263">Classes used in</span></span>        | [<span data-ttu-id="981f2-264">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="981f2-264">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="981f2-265">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="981f2-265">Windows Server 2012</span></span>



| <span data-ttu-id="981f2-266">Ввод</span><span class="sxs-lookup"><span data-stu-id="981f2-266">Entry</span></span> | <span data-ttu-id="981f2-267">Значение</span><span class="sxs-lookup"><span data-stu-id="981f2-267">Value</span></span> |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="981f2-268">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="981f2-268">Link-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-269">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="981f2-269">MAPI-Id</span></span>                | \-                                                    |
| <span data-ttu-id="981f2-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="981f2-270">System-Only</span></span>            | <span data-ttu-id="981f2-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-271">False</span></span>                                                 |
| <span data-ttu-id="981f2-272">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="981f2-272">Is-Single-Valued</span></span>       | <span data-ttu-id="981f2-273">True</span><span class="sxs-lookup"><span data-stu-id="981f2-273">True</span></span>                                                  |
| <span data-ttu-id="981f2-274">Индексируется</span><span class="sxs-lookup"><span data-stu-id="981f2-274">Is Indexed</span></span>             | <span data-ttu-id="981f2-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-275">False</span></span>                                                 |
| <span data-ttu-id="981f2-276">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="981f2-276">In Global Catalog</span></span>      | <span data-ttu-id="981f2-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="981f2-277">False</span></span>                                                 |
| <span data-ttu-id="981f2-278">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="981f2-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="981f2-279">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="981f2-279">O:BAG:BAD:S:</span></span>                                          |
| <span data-ttu-id="981f2-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="981f2-280">Range-Lower</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-281">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="981f2-281">Range-Upper</span></span>            | \-                                                    |
| <span data-ttu-id="981f2-282">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-282">Search-Flags</span></span>           | <span data-ttu-id="981f2-283">0x00000000</span><span class="sxs-lookup"><span data-stu-id="981f2-283">0x00000000</span></span>                                            |
| <span data-ttu-id="981f2-284">System-Flags</span><span class="sxs-lookup"><span data-stu-id="981f2-284">System-Flags</span></span>           | <span data-ttu-id="981f2-285">0x00000010</span><span class="sxs-lookup"><span data-stu-id="981f2-285">0x00000010</span></span>                                            |
| <span data-ttu-id="981f2-286">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="981f2-286">Classes used in</span></span>        | [<span data-ttu-id="981f2-287">**SAM-домен-база**</span><span class="sxs-lookup"><span data-stu-id="981f2-287">**Sam-Domain-Base**</span></span>](c-samdomainbase.md)<br/> |



 

 





