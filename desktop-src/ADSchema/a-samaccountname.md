---
title: SAM-атрибут имени учетной записи
description: Имя входа, используемое для поддержки клиентов и серверов под управлением более ранних версий операционной системы, таких как Windows NT 4,0, Windows 95, Windows 98 и LAN Manager.
ms.assetid: dc661e59-9a36-4d2b-93f0-f88edf7efd66
ms.tgt_platform: multiple
keywords:
- SAM-имя учетной записи-схема AD
- Схема AD атрибута sAMAccountName
topic_type:
- apiref
api_name:
- SAM-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb64cba7825c3b4400641cdc5c62890f64bc299
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893665"
---
# <a name="sam-account-name-attribute"></a><span data-ttu-id="90e31-105">SAM-атрибут имени учетной записи</span><span class="sxs-lookup"><span data-stu-id="90e31-105">SAM-Account-Name attribute</span></span>

<span data-ttu-id="90e31-106">Имя входа, используемое для поддержки клиентов и серверов под управлением более ранних версий операционной системы, таких как Windows NT 4,0, Windows 95, Windows 98 и LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="90e31-106">The logon name used to support clients and servers running earlier versions of the operating system, such as Windows NT 4.0, Windows 95, Windows 98, and LAN Manager.</span></span>

<span data-ttu-id="90e31-107">Этот атрибут должен иметь длину не более 20 символов для поддержки более ранних версий клиентов и не может содержать следующие символы:</span><span class="sxs-lookup"><span data-stu-id="90e31-107">This attribute must be 20 characters or less to support earlier clients, and cannot contain any of these characters:</span></span>

-   <span data-ttu-id="90e31-108">"/ \\ \[ \] : ; \| = , + \* ?</span><span class="sxs-lookup"><span data-stu-id="90e31-108">"/ \\ \[ \] : ; \| = , + \* ?</span></span> <span data-ttu-id="90e31-109">< ></span><span class="sxs-lookup"><span data-stu-id="90e31-109">< ></span></span>



| <span data-ttu-id="90e31-110">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-110">Entry</span></span> | <span data-ttu-id="90e31-111">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e31-112">CN</span><span class="sxs-lookup"><span data-stu-id="90e31-112">CN</span></span>                | <span data-ttu-id="90e31-113">SAM-имя учетной записи</span><span class="sxs-lookup"><span data-stu-id="90e31-113">SAM-Account-Name</span></span>                                                                         |
| <span data-ttu-id="90e31-114">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="90e31-114">Ldap-Display-Name</span></span> | <span data-ttu-id="90e31-115">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="90e31-115">sAMAccountName</span></span>                                                                           |
| <span data-ttu-id="90e31-116">Размер</span><span class="sxs-lookup"><span data-stu-id="90e31-116">Size</span></span>              | <span data-ttu-id="90e31-117">не более 20 символов.</span><span class="sxs-lookup"><span data-stu-id="90e31-117">20 characters or less.</span></span>                                                                   |
| <span data-ttu-id="90e31-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="90e31-118">Update Privilege</span></span>  | <span data-ttu-id="90e31-119">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="90e31-119">Domain administrator</span></span>                                                                     |
| <span data-ttu-id="90e31-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="90e31-120">Update Frequency</span></span>  | <span data-ttu-id="90e31-121">Это значение должно быть назначено при создании записи учетной записи и не должно изменяться.</span><span class="sxs-lookup"><span data-stu-id="90e31-121">This value should be assigned when the account record is created, and should not change.</span></span> |
| <span data-ttu-id="90e31-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-122">Attribute-Id</span></span>      | <span data-ttu-id="90e31-123">1.2.840.113556.1.4.221</span><span class="sxs-lookup"><span data-stu-id="90e31-123">1.2.840.113556.1.4.221</span></span>                                                                   |
| <span data-ttu-id="90e31-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="90e31-124">System-Id-Guid</span></span>    | <span data-ttu-id="90e31-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="90e31-125">3e0abfd0-126a-11d0-a060-00aa006c33ed</span></span>                                                     |
| <span data-ttu-id="90e31-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90e31-126">Syntax</span></span>            | [<span data-ttu-id="90e31-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="90e31-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                              |



## <a name="implementations"></a><span data-ttu-id="90e31-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="90e31-128">Implementations</span></span>

-   [<span data-ttu-id="90e31-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="90e31-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="90e31-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="90e31-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="90e31-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="90e31-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="90e31-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="90e31-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="90e31-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="90e31-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="90e31-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="90e31-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="90e31-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90e31-135">Windows 2000 Server</span></span>



| <span data-ttu-id="90e31-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-136">Entry</span></span> | <span data-ttu-id="90e31-137">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-137">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="90e31-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90e31-138">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-139">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e31-140">System-Only</span></span>            | <span data-ttu-id="90e31-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="90e31-141">False</span></span>                                                        |
| <span data-ttu-id="90e31-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90e31-142">Is-Single-Valued</span></span>       | <span data-ttu-id="90e31-143">True</span><span class="sxs-lookup"><span data-stu-id="90e31-143">True</span></span>                                                         |
| <span data-ttu-id="90e31-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90e31-144">Is Indexed</span></span>             | <span data-ttu-id="90e31-145">True</span><span class="sxs-lookup"><span data-stu-id="90e31-145">True</span></span>                                                         |
| <span data-ttu-id="90e31-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90e31-146">In Global Catalog</span></span>      | <span data-ttu-id="90e31-147">True</span><span class="sxs-lookup"><span data-stu-id="90e31-147">True</span></span>                                                         |
| <span data-ttu-id="90e31-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90e31-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e31-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90e31-149">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="90e31-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e31-150">Range-Lower</span></span>            | <span data-ttu-id="90e31-151">0</span><span class="sxs-lookup"><span data-stu-id="90e31-151">0</span></span>                                                            |
| <span data-ttu-id="90e31-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e31-152">Range-Upper</span></span>            | <span data-ttu-id="90e31-153">256</span><span class="sxs-lookup"><span data-stu-id="90e31-153">256</span></span>                                                          |
| <span data-ttu-id="90e31-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-154">Search-Flags</span></span>           | <span data-ttu-id="90e31-155">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90e31-155">0x0000000D</span></span>                                                   |
| <span data-ttu-id="90e31-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-156">System-Flags</span></span>           | <span data-ttu-id="90e31-157">0x00000012</span><span class="sxs-lookup"><span data-stu-id="90e31-157">0x00000012</span></span>                                                   |
| <span data-ttu-id="90e31-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90e31-158">Classes used in</span></span>        | [<span data-ttu-id="90e31-159">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="90e31-159">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="90e31-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90e31-160">Windows Server 2003</span></span>



| <span data-ttu-id="90e31-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-161">Entry</span></span> | <span data-ttu-id="90e31-162">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-162">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="90e31-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90e31-163">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-164">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e31-165">System-Only</span></span>            | <span data-ttu-id="90e31-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="90e31-166">False</span></span>                                                        |
| <span data-ttu-id="90e31-167">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90e31-167">Is-Single-Valued</span></span>       | <span data-ttu-id="90e31-168">True</span><span class="sxs-lookup"><span data-stu-id="90e31-168">True</span></span>                                                         |
| <span data-ttu-id="90e31-169">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90e31-169">Is Indexed</span></span>             | <span data-ttu-id="90e31-170">True</span><span class="sxs-lookup"><span data-stu-id="90e31-170">True</span></span>                                                         |
| <span data-ttu-id="90e31-171">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90e31-171">In Global Catalog</span></span>      | <span data-ttu-id="90e31-172">True</span><span class="sxs-lookup"><span data-stu-id="90e31-172">True</span></span>                                                         |
| <span data-ttu-id="90e31-173">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90e31-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e31-174">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90e31-174">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="90e31-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e31-175">Range-Lower</span></span>            | <span data-ttu-id="90e31-176">0</span><span class="sxs-lookup"><span data-stu-id="90e31-176">0</span></span>                                                            |
| <span data-ttu-id="90e31-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e31-177">Range-Upper</span></span>            | <span data-ttu-id="90e31-178">256</span><span class="sxs-lookup"><span data-stu-id="90e31-178">256</span></span>                                                          |
| <span data-ttu-id="90e31-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-179">Search-Flags</span></span>           | <span data-ttu-id="90e31-180">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90e31-180">0x0000000D</span></span>                                                   |
| <span data-ttu-id="90e31-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-181">System-Flags</span></span>           | <span data-ttu-id="90e31-182">0x00000012</span><span class="sxs-lookup"><span data-stu-id="90e31-182">0x00000012</span></span>                                                   |
| <span data-ttu-id="90e31-183">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90e31-183">Classes used in</span></span>        | [<span data-ttu-id="90e31-184">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="90e31-184">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="90e31-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="90e31-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="90e31-186">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-186">Entry</span></span> | <span data-ttu-id="90e31-187">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-187">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="90e31-188">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90e31-188">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-189">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e31-190">System-Only</span></span>            | <span data-ttu-id="90e31-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="90e31-191">False</span></span>                                                        |
| <span data-ttu-id="90e31-192">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90e31-192">Is-Single-Valued</span></span>       | <span data-ttu-id="90e31-193">True</span><span class="sxs-lookup"><span data-stu-id="90e31-193">True</span></span>                                                         |
| <span data-ttu-id="90e31-194">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90e31-194">Is Indexed</span></span>             | <span data-ttu-id="90e31-195">True</span><span class="sxs-lookup"><span data-stu-id="90e31-195">True</span></span>                                                         |
| <span data-ttu-id="90e31-196">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90e31-196">In Global Catalog</span></span>      | <span data-ttu-id="90e31-197">True</span><span class="sxs-lookup"><span data-stu-id="90e31-197">True</span></span>                                                         |
| <span data-ttu-id="90e31-198">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90e31-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e31-199">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90e31-199">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="90e31-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e31-200">Range-Lower</span></span>            | <span data-ttu-id="90e31-201">0</span><span class="sxs-lookup"><span data-stu-id="90e31-201">0</span></span>                                                            |
| <span data-ttu-id="90e31-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e31-202">Range-Upper</span></span>            | <span data-ttu-id="90e31-203">256</span><span class="sxs-lookup"><span data-stu-id="90e31-203">256</span></span>                                                          |
| <span data-ttu-id="90e31-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-204">Search-Flags</span></span>           | <span data-ttu-id="90e31-205">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90e31-205">0x0000000D</span></span>                                                   |
| <span data-ttu-id="90e31-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-206">System-Flags</span></span>           | <span data-ttu-id="90e31-207">0x00000012</span><span class="sxs-lookup"><span data-stu-id="90e31-207">0x00000012</span></span>                                                   |
| <span data-ttu-id="90e31-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90e31-208">Classes used in</span></span>        | [<span data-ttu-id="90e31-209">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="90e31-209">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="90e31-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90e31-210">Windows Server 2008</span></span>



| <span data-ttu-id="90e31-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-211">Entry</span></span> | <span data-ttu-id="90e31-212">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-212">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="90e31-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90e31-213">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-214">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e31-215">System-Only</span></span>            | <span data-ttu-id="90e31-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="90e31-216">False</span></span>                                                        |
| <span data-ttu-id="90e31-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90e31-217">Is-Single-Valued</span></span>       | <span data-ttu-id="90e31-218">True</span><span class="sxs-lookup"><span data-stu-id="90e31-218">True</span></span>                                                         |
| <span data-ttu-id="90e31-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90e31-219">Is Indexed</span></span>             | <span data-ttu-id="90e31-220">True</span><span class="sxs-lookup"><span data-stu-id="90e31-220">True</span></span>                                                         |
| <span data-ttu-id="90e31-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90e31-221">In Global Catalog</span></span>      | <span data-ttu-id="90e31-222">True</span><span class="sxs-lookup"><span data-stu-id="90e31-222">True</span></span>                                                         |
| <span data-ttu-id="90e31-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90e31-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e31-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90e31-224">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="90e31-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e31-225">Range-Lower</span></span>            | <span data-ttu-id="90e31-226">0</span><span class="sxs-lookup"><span data-stu-id="90e31-226">0</span></span>                                                            |
| <span data-ttu-id="90e31-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e31-227">Range-Upper</span></span>            | <span data-ttu-id="90e31-228">256</span><span class="sxs-lookup"><span data-stu-id="90e31-228">256</span></span>                                                          |
| <span data-ttu-id="90e31-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-229">Search-Flags</span></span>           | <span data-ttu-id="90e31-230">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90e31-230">0x0000000D</span></span>                                                   |
| <span data-ttu-id="90e31-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-231">System-Flags</span></span>           | <span data-ttu-id="90e31-232">0x00000012</span><span class="sxs-lookup"><span data-stu-id="90e31-232">0x00000012</span></span>                                                   |
| <span data-ttu-id="90e31-233">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90e31-233">Classes used in</span></span>        | [<span data-ttu-id="90e31-234">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="90e31-234">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="90e31-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="90e31-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="90e31-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-236">Entry</span></span> | <span data-ttu-id="90e31-237">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-237">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="90e31-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90e31-238">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-239">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e31-240">System-Only</span></span>            | <span data-ttu-id="90e31-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="90e31-241">False</span></span>                                                        |
| <span data-ttu-id="90e31-242">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90e31-242">Is-Single-Valued</span></span>       | <span data-ttu-id="90e31-243">True</span><span class="sxs-lookup"><span data-stu-id="90e31-243">True</span></span>                                                         |
| <span data-ttu-id="90e31-244">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90e31-244">Is Indexed</span></span>             | <span data-ttu-id="90e31-245">True</span><span class="sxs-lookup"><span data-stu-id="90e31-245">True</span></span>                                                         |
| <span data-ttu-id="90e31-246">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90e31-246">In Global Catalog</span></span>      | <span data-ttu-id="90e31-247">True</span><span class="sxs-lookup"><span data-stu-id="90e31-247">True</span></span>                                                         |
| <span data-ttu-id="90e31-248">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90e31-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e31-249">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90e31-249">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="90e31-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e31-250">Range-Lower</span></span>            | <span data-ttu-id="90e31-251">0</span><span class="sxs-lookup"><span data-stu-id="90e31-251">0</span></span>                                                            |
| <span data-ttu-id="90e31-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e31-252">Range-Upper</span></span>            | <span data-ttu-id="90e31-253">256</span><span class="sxs-lookup"><span data-stu-id="90e31-253">256</span></span>                                                          |
| <span data-ttu-id="90e31-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-254">Search-Flags</span></span>           | <span data-ttu-id="90e31-255">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90e31-255">0x0000000D</span></span>                                                   |
| <span data-ttu-id="90e31-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-256">System-Flags</span></span>           | <span data-ttu-id="90e31-257">0x00000012</span><span class="sxs-lookup"><span data-stu-id="90e31-257">0x00000012</span></span>                                                   |
| <span data-ttu-id="90e31-258">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90e31-258">Classes used in</span></span>        | [<span data-ttu-id="90e31-259">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="90e31-259">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="90e31-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="90e31-260">Windows Server 2012</span></span>



| <span data-ttu-id="90e31-261">Ввод</span><span class="sxs-lookup"><span data-stu-id="90e31-261">Entry</span></span> | <span data-ttu-id="90e31-262">Значение</span><span class="sxs-lookup"><span data-stu-id="90e31-262">Value</span></span> |
|------------------------|--------------------------------------------------------------|
| <span data-ttu-id="90e31-263">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="90e31-263">Link-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="90e31-264">MAPI-Id</span></span>                | \-                                                           |
| <span data-ttu-id="90e31-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="90e31-265">System-Only</span></span>            | <span data-ttu-id="90e31-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="90e31-266">False</span></span>                                                        |
| <span data-ttu-id="90e31-267">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="90e31-267">Is-Single-Valued</span></span>       | <span data-ttu-id="90e31-268">True</span><span class="sxs-lookup"><span data-stu-id="90e31-268">True</span></span>                                                         |
| <span data-ttu-id="90e31-269">Индексируется</span><span class="sxs-lookup"><span data-stu-id="90e31-269">Is Indexed</span></span>             | <span data-ttu-id="90e31-270">True</span><span class="sxs-lookup"><span data-stu-id="90e31-270">True</span></span>                                                         |
| <span data-ttu-id="90e31-271">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="90e31-271">In Global Catalog</span></span>      | <span data-ttu-id="90e31-272">True</span><span class="sxs-lookup"><span data-stu-id="90e31-272">True</span></span>                                                         |
| <span data-ttu-id="90e31-273">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="90e31-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="90e31-274">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="90e31-274">O:BAG:BAD:S:</span></span>                                                 |
| <span data-ttu-id="90e31-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="90e31-275">Range-Lower</span></span>            | <span data-ttu-id="90e31-276">0</span><span class="sxs-lookup"><span data-stu-id="90e31-276">0</span></span>                                                            |
| <span data-ttu-id="90e31-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="90e31-277">Range-Upper</span></span>            | <span data-ttu-id="90e31-278">256</span><span class="sxs-lookup"><span data-stu-id="90e31-278">256</span></span>                                                          |
| <span data-ttu-id="90e31-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-279">Search-Flags</span></span>           | <span data-ttu-id="90e31-280">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="90e31-280">0x0000000D</span></span>                                                   |
| <span data-ttu-id="90e31-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="90e31-281">System-Flags</span></span>           | <span data-ttu-id="90e31-282">0x00000012</span><span class="sxs-lookup"><span data-stu-id="90e31-282">0x00000012</span></span>                                                   |
| <span data-ttu-id="90e31-283">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="90e31-283">Classes used in</span></span>        | [<span data-ttu-id="90e31-284">**Безопасность — участник**</span><span class="sxs-lookup"><span data-stu-id="90e31-284">**Security-Principal**</span></span>](c-securityprincipal.md)<br/> |



 

 





