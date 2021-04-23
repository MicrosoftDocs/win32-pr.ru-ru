---
title: ACS — атрибут Identity-Name
description: Этот атрибут содержит различающееся имя пользователя или подразделения и является идентификатором пользователя или группы пользователей, к которым применяется эта политика качества обслуживания.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- ACS-Identity — имя схемы AD
- Схема AD атрибута Аксидентитинаме
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33ef1db92b908ef8474dfb125aca678d3c22d09f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139134"
---
# <a name="acs-identity-name-attribute"></a><span data-ttu-id="195a8-105">ACS — атрибут Identity-Name</span><span class="sxs-lookup"><span data-stu-id="195a8-105">ACS-Identity-Name attribute</span></span>

<span data-ttu-id="195a8-106">Этот атрибут содержит различающееся имя пользователя или подразделения и является идентификатором пользователя или группы пользователей, к которым применяется эта политика качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="195a8-106">This attribute contains the DN of a user or OU and is the identity of a user or a group of users to which this QoS policy applies.</span></span>



| <span data-ttu-id="195a8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-107">Entry</span></span> | <span data-ttu-id="195a8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="195a8-109">CN</span><span class="sxs-lookup"><span data-stu-id="195a8-109">CN</span></span>                | <span data-ttu-id="195a8-110">ACS-Identity-Name</span><span class="sxs-lookup"><span data-stu-id="195a8-110">ACS-Identity-Name</span></span>                           |
| <span data-ttu-id="195a8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="195a8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="195a8-112">аксидентитинаме</span><span class="sxs-lookup"><span data-stu-id="195a8-112">aCSIdentityName</span></span>                             |
| <span data-ttu-id="195a8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="195a8-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="195a8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="195a8-114">Update Privilege</span></span>  | <span data-ttu-id="195a8-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="195a8-115">Domain administrator</span></span>                        |
| <span data-ttu-id="195a8-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="195a8-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="195a8-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-117">Attribute-Id</span></span>      | <span data-ttu-id="195a8-118">1.2.840.113556.1.4.784</span><span class="sxs-lookup"><span data-stu-id="195a8-118">1.2.840.113556.1.4.784</span></span>                      |
| <span data-ttu-id="195a8-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="195a8-119">System-Id-Guid</span></span>    | <span data-ttu-id="195a8-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="195a8-120">dab029b6-ddf7-11d1-90a5-00c04fd91ab1</span></span>        |
| <span data-ttu-id="195a8-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="195a8-121">Syntax</span></span>            | [<span data-ttu-id="195a8-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="195a8-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="195a8-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="195a8-123">Implementations</span></span>

-   [<span data-ttu-id="195a8-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="195a8-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="195a8-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="195a8-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="195a8-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="195a8-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="195a8-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="195a8-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="195a8-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="195a8-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="195a8-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="195a8-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="195a8-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="195a8-130">Windows 2000 Server</span></span>



| <span data-ttu-id="195a8-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-131">Entry</span></span> | <span data-ttu-id="195a8-132">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-132">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="195a8-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="195a8-133">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-134">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="195a8-135">System-Only</span></span>            | <span data-ttu-id="195a8-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-136">False</span></span>                                        |
| <span data-ttu-id="195a8-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="195a8-137">Is-Single-Valued</span></span>       | <span data-ttu-id="195a8-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-138">False</span></span>                                        |
| <span data-ttu-id="195a8-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="195a8-139">Is Indexed</span></span>             | <span data-ttu-id="195a8-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-140">False</span></span>                                        |
| <span data-ttu-id="195a8-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="195a8-141">In Global Catalog</span></span>      | <span data-ttu-id="195a8-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-142">False</span></span>                                        |
| <span data-ttu-id="195a8-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="195a8-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="195a8-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="195a8-144">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="195a8-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="195a8-145">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="195a8-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="195a8-146">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="195a8-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-147">Search-Flags</span></span>           | <span data-ttu-id="195a8-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="195a8-148">0x00000000</span></span>                                   |
| <span data-ttu-id="195a8-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-149">System-Flags</span></span>           | <span data-ttu-id="195a8-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="195a8-150">0x00000010</span></span>                                   |
| <span data-ttu-id="195a8-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="195a8-151">Classes used in</span></span>        | [<span data-ttu-id="195a8-152">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="195a8-152">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="195a8-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="195a8-153">Windows Server 2003</span></span>



| <span data-ttu-id="195a8-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-154">Entry</span></span> | <span data-ttu-id="195a8-155">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-155">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="195a8-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="195a8-156">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-157">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="195a8-158">System-Only</span></span>            | <span data-ttu-id="195a8-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-159">False</span></span>                                        |
| <span data-ttu-id="195a8-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="195a8-160">Is-Single-Valued</span></span>       | <span data-ttu-id="195a8-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-161">False</span></span>                                        |
| <span data-ttu-id="195a8-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="195a8-162">Is Indexed</span></span>             | <span data-ttu-id="195a8-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-163">False</span></span>                                        |
| <span data-ttu-id="195a8-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="195a8-164">In Global Catalog</span></span>      | <span data-ttu-id="195a8-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-165">False</span></span>                                        |
| <span data-ttu-id="195a8-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="195a8-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="195a8-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="195a8-167">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="195a8-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="195a8-168">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="195a8-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="195a8-169">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="195a8-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-170">Search-Flags</span></span>           | <span data-ttu-id="195a8-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="195a8-171">0x00000000</span></span>                                   |
| <span data-ttu-id="195a8-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-172">System-Flags</span></span>           | <span data-ttu-id="195a8-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="195a8-173">0x00000010</span></span>                                   |
| <span data-ttu-id="195a8-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="195a8-174">Classes used in</span></span>        | [<span data-ttu-id="195a8-175">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="195a8-175">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="195a8-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="195a8-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="195a8-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-177">Entry</span></span> | <span data-ttu-id="195a8-178">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-178">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="195a8-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="195a8-179">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-180">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="195a8-181">System-Only</span></span>            | <span data-ttu-id="195a8-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-182">False</span></span>                                        |
| <span data-ttu-id="195a8-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="195a8-183">Is-Single-Valued</span></span>       | <span data-ttu-id="195a8-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-184">False</span></span>                                        |
| <span data-ttu-id="195a8-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="195a8-185">Is Indexed</span></span>             | <span data-ttu-id="195a8-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-186">False</span></span>                                        |
| <span data-ttu-id="195a8-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="195a8-187">In Global Catalog</span></span>      | <span data-ttu-id="195a8-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-188">False</span></span>                                        |
| <span data-ttu-id="195a8-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="195a8-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="195a8-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="195a8-190">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="195a8-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="195a8-191">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="195a8-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="195a8-192">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="195a8-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-193">Search-Flags</span></span>           | <span data-ttu-id="195a8-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="195a8-194">0x00000000</span></span>                                   |
| <span data-ttu-id="195a8-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-195">System-Flags</span></span>           | <span data-ttu-id="195a8-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="195a8-196">0x00000010</span></span>                                   |
| <span data-ttu-id="195a8-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="195a8-197">Classes used in</span></span>        | [<span data-ttu-id="195a8-198">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="195a8-198">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="195a8-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="195a8-199">Windows Server 2008</span></span>



| <span data-ttu-id="195a8-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-200">Entry</span></span> | <span data-ttu-id="195a8-201">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-201">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="195a8-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="195a8-202">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-203">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="195a8-204">System-Only</span></span>            | <span data-ttu-id="195a8-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-205">False</span></span>                                        |
| <span data-ttu-id="195a8-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="195a8-206">Is-Single-Valued</span></span>       | <span data-ttu-id="195a8-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-207">False</span></span>                                        |
| <span data-ttu-id="195a8-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="195a8-208">Is Indexed</span></span>             | <span data-ttu-id="195a8-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-209">False</span></span>                                        |
| <span data-ttu-id="195a8-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="195a8-210">In Global Catalog</span></span>      | <span data-ttu-id="195a8-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-211">False</span></span>                                        |
| <span data-ttu-id="195a8-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="195a8-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="195a8-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="195a8-213">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="195a8-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="195a8-214">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="195a8-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="195a8-215">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="195a8-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-216">Search-Flags</span></span>           | <span data-ttu-id="195a8-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="195a8-217">0x00000000</span></span>                                   |
| <span data-ttu-id="195a8-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-218">System-Flags</span></span>           | <span data-ttu-id="195a8-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="195a8-219">0x00000010</span></span>                                   |
| <span data-ttu-id="195a8-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="195a8-220">Classes used in</span></span>        | [<span data-ttu-id="195a8-221">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="195a8-221">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="195a8-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="195a8-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="195a8-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-223">Entry</span></span> | <span data-ttu-id="195a8-224">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-224">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="195a8-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="195a8-225">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-226">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="195a8-227">System-Only</span></span>            | <span data-ttu-id="195a8-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-228">False</span></span>                                        |
| <span data-ttu-id="195a8-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="195a8-229">Is-Single-Valued</span></span>       | <span data-ttu-id="195a8-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-230">False</span></span>                                        |
| <span data-ttu-id="195a8-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="195a8-231">Is Indexed</span></span>             | <span data-ttu-id="195a8-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-232">False</span></span>                                        |
| <span data-ttu-id="195a8-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="195a8-233">In Global Catalog</span></span>      | <span data-ttu-id="195a8-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-234">False</span></span>                                        |
| <span data-ttu-id="195a8-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="195a8-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="195a8-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="195a8-236">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="195a8-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="195a8-237">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="195a8-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="195a8-238">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="195a8-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-239">Search-Flags</span></span>           | <span data-ttu-id="195a8-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="195a8-240">0x00000000</span></span>                                   |
| <span data-ttu-id="195a8-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-241">System-Flags</span></span>           | <span data-ttu-id="195a8-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="195a8-242">0x00000010</span></span>                                   |
| <span data-ttu-id="195a8-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="195a8-243">Classes used in</span></span>        | [<span data-ttu-id="195a8-244">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="195a8-244">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="195a8-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="195a8-245">Windows Server 2012</span></span>



| <span data-ttu-id="195a8-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="195a8-246">Entry</span></span> | <span data-ttu-id="195a8-247">Значение</span><span class="sxs-lookup"><span data-stu-id="195a8-247">Value</span></span> |
|------------------------|----------------------------------------------|
| <span data-ttu-id="195a8-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="195a8-248">Link-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="195a8-249">MAPI-Id</span></span>                | \-                                           |
| <span data-ttu-id="195a8-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="195a8-250">System-Only</span></span>            | <span data-ttu-id="195a8-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-251">False</span></span>                                        |
| <span data-ttu-id="195a8-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="195a8-252">Is-Single-Valued</span></span>       | <span data-ttu-id="195a8-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-253">False</span></span>                                        |
| <span data-ttu-id="195a8-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="195a8-254">Is Indexed</span></span>             | <span data-ttu-id="195a8-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-255">False</span></span>                                        |
| <span data-ttu-id="195a8-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="195a8-256">In Global Catalog</span></span>      | <span data-ttu-id="195a8-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="195a8-257">False</span></span>                                        |
| <span data-ttu-id="195a8-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="195a8-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="195a8-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="195a8-259">O:BAG:BAD:S:</span></span>                                 |
| <span data-ttu-id="195a8-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="195a8-260">Range-Lower</span></span>            | \-                                           |
| <span data-ttu-id="195a8-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="195a8-261">Range-Upper</span></span>            | \-                                           |
| <span data-ttu-id="195a8-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-262">Search-Flags</span></span>           | <span data-ttu-id="195a8-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="195a8-263">0x00000000</span></span>                                   |
| <span data-ttu-id="195a8-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="195a8-264">System-Flags</span></span>           | <span data-ttu-id="195a8-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="195a8-265">0x00000010</span></span>                                   |
| <span data-ttu-id="195a8-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="195a8-266">Classes used in</span></span>        | [<span data-ttu-id="195a8-267">**ACS — политика**</span><span class="sxs-lookup"><span data-stu-id="195a8-267">**ACS-Policy**</span></span>](c-acspolicy.md)<br/> |



 

 





