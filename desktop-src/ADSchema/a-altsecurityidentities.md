---
title: Атрибут "Alt-Security-identitys"
description: Содержит сопоставления для сертификатов X. 509 или внешних учетных записей пользователей Kerberos этому пользователю в целях проверки подлинности.
ms.assetid: 40b2af9c-fd4f-4883-8494-2b64682ee50c
ms.tgt_platform: multiple
keywords:
- Alt — безопасность — схема AD атрибутов удостоверений
- Схема AD атрибута Алтсекуритидентитиес
topic_type:
- apiref
api_name:
- Alt-Security-Identities
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2548e337f29778400bb173a8c15d928d7b06d988
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989579"
---
# <a name="alt-security-identities-attribute"></a><span data-ttu-id="e7e5c-105">Атрибут "Alt-Security-identitys"</span><span class="sxs-lookup"><span data-stu-id="e7e5c-105">Alt-Security-Identities attribute</span></span>

<span data-ttu-id="e7e5c-106">Содержит сопоставления для сертификатов X. 509 или внешних учетных записей пользователей Kerberos этому пользователю в целях проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e7e5c-106">Contains mappings for X.509 certificates or external Kerberos user accounts to this user for the purpose of authentication.</span></span>



| <span data-ttu-id="e7e5c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-107">Entry</span></span> | <span data-ttu-id="e7e5c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="e7e5c-109">CN</span><span class="sxs-lookup"><span data-stu-id="e7e5c-109">CN</span></span>                | <span data-ttu-id="e7e5c-110">Alt-Security — удостоверения</span><span class="sxs-lookup"><span data-stu-id="e7e5c-110">Alt-Security-Identities</span></span>                             |
| <span data-ttu-id="e7e5c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="e7e5c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e7e5c-112">altSecurityIdentities</span><span class="sxs-lookup"><span data-stu-id="e7e5c-112">altSecurityIdentities</span></span>                               |
| <span data-ttu-id="e7e5c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="e7e5c-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="e7e5c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="e7e5c-114">Update Privilege</span></span>  | <span data-ttu-id="e7e5c-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="e7e5c-115">Domain administrator</span></span>                                |
| <span data-ttu-id="e7e5c-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="e7e5c-116">Update Frequency</span></span>  | <span data-ttu-id="e7e5c-117">Каждый раз, когда требуется новый механизм проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="e7e5c-117">Each time a new authentication mechanism is needed.</span></span> |
| <span data-ttu-id="e7e5c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-118">Attribute-Id</span></span>      | <span data-ttu-id="e7e5c-119">1.2.840.113556.1.4.867</span><span class="sxs-lookup"><span data-stu-id="e7e5c-119">1.2.840.113556.1.4.867</span></span>                              |
| <span data-ttu-id="e7e5c-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="e7e5c-120">System-Id-Guid</span></span>    | <span data-ttu-id="e7e5c-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="e7e5c-121">00fbf30c-91fe-11d1-aebc-0000f80367c1</span></span>                |
| <span data-ttu-id="e7e5c-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7e5c-122">Syntax</span></span>            | [<span data-ttu-id="e7e5c-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-123">**String(Unicode)**</span></span>](s-string-unicode.md)         |



## <a name="implementations"></a><span data-ttu-id="e7e5c-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="e7e5c-124">Implementations</span></span>

-   [<span data-ttu-id="e7e5c-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e7e5c-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e7e5c-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e7e5c-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e7e5c-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e7e5c-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e7e5c-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e7e5c-131">Windows 2000 Server</span></span>



| <span data-ttu-id="e7e5c-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-132">Entry</span></span> | <span data-ttu-id="e7e5c-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-133">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e7e5c-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7e5c-134">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-135">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7e5c-136">System-Only</span></span>            | <span data-ttu-id="e7e5c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-137">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7e5c-138">Is-Single-Valued</span></span>       | <span data-ttu-id="e7e5c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-139">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7e5c-140">Is Indexed</span></span>             | <span data-ttu-id="e7e5c-141">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-141">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7e5c-142">In Global Catalog</span></span>      | <span data-ttu-id="e7e5c-143">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-143">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7e5c-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7e5c-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7e5c-145">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="e7e5c-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7e5c-146">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7e5c-147">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-148">Search-Flags</span></span>           | <span data-ttu-id="e7e5c-149">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7e5c-149">0x00000001</span></span>                                                   |
| <span data-ttu-id="e7e5c-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-150">System-Flags</span></span>           | <span data-ttu-id="e7e5c-151">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-151">0x00000012</span></span>                                                   |
| <span data-ttu-id="e7e5c-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7e5c-152">Classes used in</span></span>        | [<span data-ttu-id="e7e5c-153">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-153">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e7e5c-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7e5c-154">Windows Server 2003</span></span>



| <span data-ttu-id="e7e5c-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-155">Entry</span></span> | <span data-ttu-id="e7e5c-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-156">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e7e5c-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7e5c-157">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-158">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7e5c-159">System-Only</span></span>            | <span data-ttu-id="e7e5c-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-160">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7e5c-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e7e5c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-162">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7e5c-163">Is Indexed</span></span>             | <span data-ttu-id="e7e5c-164">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-164">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7e5c-165">In Global Catalog</span></span>      | <span data-ttu-id="e7e5c-166">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-166">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7e5c-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7e5c-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7e5c-168">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="e7e5c-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7e5c-169">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7e5c-170">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-171">Search-Flags</span></span>           | <span data-ttu-id="e7e5c-172">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7e5c-172">0x00000001</span></span>                                                   |
| <span data-ttu-id="e7e5c-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-173">System-Flags</span></span>           | <span data-ttu-id="e7e5c-174">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-174">0x00000012</span></span>                                                   |
| <span data-ttu-id="e7e5c-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7e5c-175">Classes used in</span></span>        | [<span data-ttu-id="e7e5c-176">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-176">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e7e5c-177">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e7e5c-177">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e7e5c-178">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-178">Entry</span></span> | <span data-ttu-id="e7e5c-179">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-179">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e7e5c-180">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7e5c-180">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-181">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-181">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-182">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7e5c-182">System-Only</span></span>            | <span data-ttu-id="e7e5c-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-183">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-184">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7e5c-184">Is-Single-Valued</span></span>       | <span data-ttu-id="e7e5c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-185">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-186">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7e5c-186">Is Indexed</span></span>             | <span data-ttu-id="e7e5c-187">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-187">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-188">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7e5c-188">In Global Catalog</span></span>      | <span data-ttu-id="e7e5c-189">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-189">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-190">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7e5c-190">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7e5c-191">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7e5c-191">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="e7e5c-192">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7e5c-192">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7e5c-193">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-194">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-194">Search-Flags</span></span>           | <span data-ttu-id="e7e5c-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7e5c-195">0x00000001</span></span>                                                   |
| <span data-ttu-id="e7e5c-196">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-196">System-Flags</span></span>           | <span data-ttu-id="e7e5c-197">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-197">0x00000012</span></span>                                                   |
| <span data-ttu-id="e7e5c-198">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7e5c-198">Classes used in</span></span>        | [<span data-ttu-id="e7e5c-199">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-199">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e7e5c-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7e5c-200">Windows Server 2008</span></span>



| <span data-ttu-id="e7e5c-201">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-201">Entry</span></span> | <span data-ttu-id="e7e5c-202">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-202">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e7e5c-203">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7e5c-203">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-204">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-204">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-205">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7e5c-205">System-Only</span></span>            | <span data-ttu-id="e7e5c-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-206">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-207">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7e5c-207">Is-Single-Valued</span></span>       | <span data-ttu-id="e7e5c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-208">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-209">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7e5c-209">Is Indexed</span></span>             | <span data-ttu-id="e7e5c-210">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-210">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-211">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7e5c-211">In Global Catalog</span></span>      | <span data-ttu-id="e7e5c-212">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-212">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-213">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7e5c-213">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7e5c-214">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7e5c-214">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="e7e5c-215">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7e5c-215">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-216">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7e5c-216">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-217">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-217">Search-Flags</span></span>           | <span data-ttu-id="e7e5c-218">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7e5c-218">0x00000001</span></span>                                                   |
| <span data-ttu-id="e7e5c-219">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-219">System-Flags</span></span>           | <span data-ttu-id="e7e5c-220">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-220">0x00000012</span></span>                                                   |
| <span data-ttu-id="e7e5c-221">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7e5c-221">Classes used in</span></span>        | [<span data-ttu-id="e7e5c-222">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-222">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e7e5c-223">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e7e5c-223">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e7e5c-224">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-224">Entry</span></span> | <span data-ttu-id="e7e5c-225">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-225">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e7e5c-226">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7e5c-226">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-227">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-227">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-228">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7e5c-228">System-Only</span></span>            | <span data-ttu-id="e7e5c-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-229">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-230">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7e5c-230">Is-Single-Valued</span></span>       | <span data-ttu-id="e7e5c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-231">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-232">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7e5c-232">Is Indexed</span></span>             | <span data-ttu-id="e7e5c-233">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-233">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-234">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7e5c-234">In Global Catalog</span></span>      | <span data-ttu-id="e7e5c-235">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-235">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-236">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7e5c-236">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7e5c-237">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7e5c-237">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="e7e5c-238">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7e5c-238">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-239">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7e5c-239">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-240">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-240">Search-Flags</span></span>           | <span data-ttu-id="e7e5c-241">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7e5c-241">0x00000001</span></span>                                                   |
| <span data-ttu-id="e7e5c-242">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-242">System-Flags</span></span>           | <span data-ttu-id="e7e5c-243">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-243">0x00000012</span></span>                                                   |
| <span data-ttu-id="e7e5c-244">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7e5c-244">Classes used in</span></span>        | [<span data-ttu-id="e7e5c-245">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-245">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e7e5c-246">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-246">Windows Server 2012</span></span>



| <span data-ttu-id="e7e5c-247">Ввод</span><span class="sxs-lookup"><span data-stu-id="e7e5c-247">Entry</span></span> | <span data-ttu-id="e7e5c-248">Значение</span><span class="sxs-lookup"><span data-stu-id="e7e5c-248">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="e7e5c-249">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="e7e5c-249">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-250">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e7e5c-250">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="e7e5c-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="e7e5c-251">System-Only</span></span>            | <span data-ttu-id="e7e5c-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-252">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="e7e5c-253">Is-Single-Valued</span></span>       | <span data-ttu-id="e7e5c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="e7e5c-254">False</span></span>                                                        |
| <span data-ttu-id="e7e5c-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="e7e5c-255">Is Indexed</span></span>             | <span data-ttu-id="e7e5c-256">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-256">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="e7e5c-257">In Global Catalog</span></span>      | <span data-ttu-id="e7e5c-258">True</span><span class="sxs-lookup"><span data-stu-id="e7e5c-258">True</span></span>                                                         |
| <span data-ttu-id="e7e5c-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="e7e5c-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="e7e5c-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="e7e5c-260">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="e7e5c-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e7e5c-261">Range-Lower</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e7e5c-262">Range-Upper</span></span>            | \-                                                           |
| <span data-ttu-id="e7e5c-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-263">Search-Flags</span></span>           | <span data-ttu-id="e7e5c-264">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e7e5c-264">0x00000001</span></span>                                                   |
| <span data-ttu-id="e7e5c-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e7e5c-265">System-Flags</span></span>           | <span data-ttu-id="e7e5c-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="e7e5c-266">0x00000012</span></span>                                                   |
| <span data-ttu-id="e7e5c-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="e7e5c-267">Classes used in</span></span>        | [<span data-ttu-id="e7e5c-268">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="e7e5c-268">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





