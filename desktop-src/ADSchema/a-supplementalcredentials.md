---
title: Атрибут Supplemental-Credentials
description: Сохраненные учетные данные для использования при проверке подлинности. Зашифрованная версия пароля пользователя. Этот атрибут не доступен для чтения или записи.
ms.assetid: 642aa699-094e-40ed-a2f8-ec7219c85de2
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Supplemental-Credentials
- Схема AD атрибута Супплементалкредентиалс
topic_type:
- apiref
api_name:
- Supplemental-Credentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19a73b3ae3cf19745fc995a59c336b72d264e78
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535891"
---
# <a name="supplemental-credentials-attribute"></a><span data-ttu-id="c6d53-107">Атрибут Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="c6d53-107">Supplemental-Credentials attribute</span></span>

<span data-ttu-id="c6d53-108">Сохраненные учетные данные для использования при проверке подлинности.</span><span class="sxs-lookup"><span data-stu-id="c6d53-108">Stored credentials for use in authenticating.</span></span> <span data-ttu-id="c6d53-109">Зашифрованная версия пароля пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6d53-109">The encrypted version of the user's password.</span></span> <span data-ttu-id="c6d53-110">Этот атрибут не доступен для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="c6d53-110">This attribute is neither readable nor writable.</span></span>



| <span data-ttu-id="c6d53-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-111">Entry</span></span> | <span data-ttu-id="c6d53-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-112">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="c6d53-113">CN</span><span class="sxs-lookup"><span data-stu-id="c6d53-113">CN</span></span>                | <span data-ttu-id="c6d53-114">Supplemental-Credentials</span><span class="sxs-lookup"><span data-stu-id="c6d53-114">Supplemental-Credentials</span></span>                              |
| <span data-ttu-id="c6d53-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c6d53-115">Ldap-Display-Name</span></span> | <span data-ttu-id="c6d53-116">супплементалкредентиалс</span><span class="sxs-lookup"><span data-stu-id="c6d53-116">supplementalCredentials</span></span>                               |
| <span data-ttu-id="c6d53-117">Размер</span><span class="sxs-lookup"><span data-stu-id="c6d53-117">Size</span></span>              | \-                                                    |
| <span data-ttu-id="c6d53-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c6d53-118">Update Privilege</span></span>  | <span data-ttu-id="c6d53-119">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c6d53-119">This value is set by the system.</span></span>                      |
| <span data-ttu-id="c6d53-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c6d53-120">Update Frequency</span></span>  | <span data-ttu-id="c6d53-121">При изменении пароля пользователя.</span><span class="sxs-lookup"><span data-stu-id="c6d53-121">When the user's password changes.</span></span>                     |
| <span data-ttu-id="c6d53-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-122">Attribute-Id</span></span>      | <span data-ttu-id="c6d53-123">1.2.840.113556.1.4.125</span><span class="sxs-lookup"><span data-stu-id="c6d53-123">1.2.840.113556.1.4.125</span></span>                                |
| <span data-ttu-id="c6d53-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c6d53-124">System-Id-Guid</span></span>    | <span data-ttu-id="c6d53-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c6d53-125">bf967a3f-0de6-11d0-a285-00aa003049e2</span></span>                  |
| <span data-ttu-id="c6d53-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6d53-126">Syntax</span></span>            | [<span data-ttu-id="c6d53-127">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="c6d53-127">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="c6d53-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c6d53-128">Implementations</span></span>

-   [<span data-ttu-id="c6d53-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c6d53-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c6d53-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c6d53-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c6d53-131">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c6d53-131">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c6d53-132">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c6d53-132">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c6d53-133">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c6d53-133">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c6d53-134">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c6d53-134">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c6d53-135">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c6d53-135">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c6d53-136">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6d53-136">Windows 2000 Server</span></span>



| <span data-ttu-id="c6d53-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-137">Entry</span></span> | <span data-ttu-id="c6d53-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-138">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-139">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-139">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-140">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-140">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-141">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-141">System-Only</span></span>            | <span data-ttu-id="c6d53-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-142">False</span></span>                                                        |
| <span data-ttu-id="c6d53-143">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-143">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-144">False</span></span>                                                        |
| <span data-ttu-id="c6d53-145">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-145">Is Indexed</span></span>             | <span data-ttu-id="c6d53-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-146">False</span></span>                                                        |
| <span data-ttu-id="c6d53-147">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-147">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-148">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-148">False</span></span>                                                        |
| <span data-ttu-id="c6d53-149">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-149">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-150">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-150">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-151">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-151">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-152">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-153">Search-Flags</span></span>           | <span data-ttu-id="c6d53-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-154">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-155">System-Flags</span></span>           | <span data-ttu-id="c6d53-156">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-156">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-157">Classes used in</span></span>        | [<span data-ttu-id="c6d53-158">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-158">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c6d53-159">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6d53-159">Windows Server 2003</span></span>



| <span data-ttu-id="c6d53-160">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-160">Entry</span></span> | <span data-ttu-id="c6d53-161">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-161">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-162">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-162">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-163">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-164">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-164">System-Only</span></span>            | <span data-ttu-id="c6d53-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-165">False</span></span>                                                        |
| <span data-ttu-id="c6d53-166">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-166">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-167">False</span></span>                                                        |
| <span data-ttu-id="c6d53-168">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-168">Is Indexed</span></span>             | <span data-ttu-id="c6d53-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-169">False</span></span>                                                        |
| <span data-ttu-id="c6d53-170">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-170">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-171">False</span></span>                                                        |
| <span data-ttu-id="c6d53-172">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-172">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-173">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-173">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-174">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-174">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-175">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-176">Search-Flags</span></span>           | <span data-ttu-id="c6d53-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-177">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-178">System-Flags</span></span>           | <span data-ttu-id="c6d53-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-179">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-180">Classes used in</span></span>        | [<span data-ttu-id="c6d53-181">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-181">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c6d53-182">ADAM</span><span class="sxs-lookup"><span data-stu-id="c6d53-182">ADAM</span></span>



| <span data-ttu-id="c6d53-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-183">Entry</span></span> | <span data-ttu-id="c6d53-184">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-184">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-185">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-186">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-187">System-Only</span></span>            | <span data-ttu-id="c6d53-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-188">False</span></span>                                                        |
| <span data-ttu-id="c6d53-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-189">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-190">False</span></span>                                                        |
| <span data-ttu-id="c6d53-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-191">Is Indexed</span></span>             | <span data-ttu-id="c6d53-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-192">False</span></span>                                                        |
| <span data-ttu-id="c6d53-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-193">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-194">False</span></span>                                                        |
| <span data-ttu-id="c6d53-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-196">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-197">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-198">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-199">Search-Flags</span></span>           | <span data-ttu-id="c6d53-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-200">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-201">System-Flags</span></span>           | <span data-ttu-id="c6d53-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-202">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-203">Classes used in</span></span>        | [<span data-ttu-id="c6d53-204">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-204">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c6d53-205">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c6d53-205">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c6d53-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-206">Entry</span></span> | <span data-ttu-id="c6d53-207">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-207">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-208">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-209">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-210">System-Only</span></span>            | <span data-ttu-id="c6d53-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-211">False</span></span>                                                        |
| <span data-ttu-id="c6d53-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-212">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-213">False</span></span>                                                        |
| <span data-ttu-id="c6d53-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-214">Is Indexed</span></span>             | <span data-ttu-id="c6d53-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-215">False</span></span>                                                        |
| <span data-ttu-id="c6d53-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-216">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-217">False</span></span>                                                        |
| <span data-ttu-id="c6d53-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-219">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-220">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-221">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-222">Search-Flags</span></span>           | <span data-ttu-id="c6d53-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-223">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-224">System-Flags</span></span>           | <span data-ttu-id="c6d53-225">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-225">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-226">Classes used in</span></span>        | [<span data-ttu-id="c6d53-227">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-227">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c6d53-228">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6d53-228">Windows Server 2008</span></span>



| <span data-ttu-id="c6d53-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-229">Entry</span></span> | <span data-ttu-id="c6d53-230">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-230">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-231">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-232">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-233">System-Only</span></span>            | <span data-ttu-id="c6d53-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-234">False</span></span>                                                        |
| <span data-ttu-id="c6d53-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-235">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-236">False</span></span>                                                        |
| <span data-ttu-id="c6d53-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-237">Is Indexed</span></span>             | <span data-ttu-id="c6d53-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-238">False</span></span>                                                        |
| <span data-ttu-id="c6d53-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-239">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-240">False</span></span>                                                        |
| <span data-ttu-id="c6d53-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-242">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-243">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-244">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-245">Search-Flags</span></span>           | <span data-ttu-id="c6d53-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-246">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-247">System-Flags</span></span>           | <span data-ttu-id="c6d53-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-248">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-249">Classes used in</span></span>        | [<span data-ttu-id="c6d53-250">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-250">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c6d53-251">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c6d53-251">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c6d53-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-252">Entry</span></span> | <span data-ttu-id="c6d53-253">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-253">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-254">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-254">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-255">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-255">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-256">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-256">System-Only</span></span>            | <span data-ttu-id="c6d53-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-257">False</span></span>                                                        |
| <span data-ttu-id="c6d53-258">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-258">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-259">False</span></span>                                                        |
| <span data-ttu-id="c6d53-260">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-260">Is Indexed</span></span>             | <span data-ttu-id="c6d53-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-261">False</span></span>                                                        |
| <span data-ttu-id="c6d53-262">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-262">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-263">False</span></span>                                                        |
| <span data-ttu-id="c6d53-264">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-264">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-265">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-265">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-266">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-266">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-267">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-267">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-268">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-268">Search-Flags</span></span>           | <span data-ttu-id="c6d53-269">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-269">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-270">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-270">System-Flags</span></span>           | <span data-ttu-id="c6d53-271">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-271">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-272">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-272">Classes used in</span></span>        | [<span data-ttu-id="c6d53-273">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-273">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c6d53-274">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6d53-274">Windows Server 2012</span></span>



| <span data-ttu-id="c6d53-275">Ввод</span><span class="sxs-lookup"><span data-stu-id="c6d53-275">Entry</span></span> | <span data-ttu-id="c6d53-276">Значение</span><span class="sxs-lookup"><span data-stu-id="c6d53-276">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="c6d53-277">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c6d53-277">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-278">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c6d53-278">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="c6d53-279">System-Only</span><span class="sxs-lookup"><span data-stu-id="c6d53-279">System-Only</span></span>            | <span data-ttu-id="c6d53-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-280">False</span></span>                                                        |
| <span data-ttu-id="c6d53-281">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c6d53-281">Is-Single-Valued</span></span>       | <span data-ttu-id="c6d53-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-282">False</span></span>                                                        |
| <span data-ttu-id="c6d53-283">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c6d53-283">Is Indexed</span></span>             | <span data-ttu-id="c6d53-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-284">False</span></span>                                                        |
| <span data-ttu-id="c6d53-285">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c6d53-285">In Global Catalog</span></span>      | <span data-ttu-id="c6d53-286">Неверно</span><span class="sxs-lookup"><span data-stu-id="c6d53-286">False</span></span>                                                        |
| <span data-ttu-id="c6d53-287">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c6d53-287">NT-Security-Descriptor</span></span> | <span data-ttu-id="c6d53-288">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c6d53-288">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="c6d53-289">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c6d53-289">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-290">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c6d53-290">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="c6d53-291">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-291">Search-Flags</span></span>           | <span data-ttu-id="c6d53-292">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c6d53-292">0x00000000</span></span>                                                   |
| <span data-ttu-id="c6d53-293">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c6d53-293">System-Flags</span></span>           | <span data-ttu-id="c6d53-294">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c6d53-294">0x00000010</span></span>                                                   |
| <span data-ttu-id="c6d53-295">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c6d53-295">Classes used in</span></span>        | [<span data-ttu-id="c6d53-296">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="c6d53-296">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





