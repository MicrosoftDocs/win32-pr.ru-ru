---
title: PKI — атрибут доступа для регистрации
description: Атрибут PKI — регистрация доступа предназначен только для внутреннего использования.
ms.assetid: 09eab075-71a5-4a38-af34-dafedca9c2c6
ms.tgt_platform: multiple
keywords:
- PKI — схема AD атрибута доступа для регистрации
- Схема AD атрибута Пкиенроллментакцесс
topic_type:
- apiref
api_name:
- PKI-Enrollment-Access
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f974e1072810b902fa42d30f067a67e22236ca
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989515"
---
# <a name="pki-enrollment-access-attribute"></a><span data-ttu-id="28c0c-105">PKI — атрибут доступа для регистрации</span><span class="sxs-lookup"><span data-stu-id="28c0c-105">PKI-Enrollment-Access attribute</span></span>

<span data-ttu-id="28c0c-106">Атрибут **PKI — регистрация доступа** предназначен только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="28c0c-106">The **PKI-Enrollment-Access** attribute is for internal use only.</span></span>



| <span data-ttu-id="28c0c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-107">Entry</span></span> | <span data-ttu-id="28c0c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="28c0c-109">CN</span><span class="sxs-lookup"><span data-stu-id="28c0c-109">CN</span></span>                | <span data-ttu-id="28c0c-110">PKI — доступ к регистрации</span><span class="sxs-lookup"><span data-stu-id="28c0c-110">PKI-Enrollment-Access</span></span>                               |
| <span data-ttu-id="28c0c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="28c0c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="28c0c-112">пкиенроллментакцесс</span><span class="sxs-lookup"><span data-stu-id="28c0c-112">pKIEnrollmentAccess</span></span>                                 |
| <span data-ttu-id="28c0c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="28c0c-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="28c0c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="28c0c-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="28c0c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="28c0c-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="28c0c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-116">Attribute-Id</span></span>      | <span data-ttu-id="28c0c-117">1.2.840.113556.1.4.1335</span><span class="sxs-lookup"><span data-stu-id="28c0c-117">1.2.840.113556.1.4.1335</span></span>                             |
| <span data-ttu-id="28c0c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="28c0c-118">System-Id-Guid</span></span>    | <span data-ttu-id="28c0c-119">926be278-56f9-11d2-90d0-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="28c0c-119">926be278-56f9-11d2-90d0-00c04fd91ab1</span></span>                |
| <span data-ttu-id="28c0c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28c0c-120">Syntax</span></span>            | [<span data-ttu-id="28c0c-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="28c0c-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="28c0c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="28c0c-122">Implementations</span></span>

-   [<span data-ttu-id="28c0c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28c0c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28c0c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28c0c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28c0c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28c0c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28c0c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28c0c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28c0c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28c0c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28c0c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28c0c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28c0c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28c0c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="28c0c-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-130">Entry</span></span> | <span data-ttu-id="28c0c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c0c-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28c0c-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c0c-134">System-Only</span></span>            | <span data-ttu-id="28c0c-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-135">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28c0c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="28c0c-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-137">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28c0c-138">Is Indexed</span></span>             | <span data-ttu-id="28c0c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-139">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28c0c-140">In Global Catalog</span></span>      | <span data-ttu-id="28c0c-141">True</span><span class="sxs-lookup"><span data-stu-id="28c0c-141">True</span></span>                                                                    |
| <span data-ttu-id="28c0c-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28c0c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c0c-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28c0c-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="28c0c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c0c-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c0c-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-146">Search-Flags</span></span>           | <span data-ttu-id="28c0c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c0c-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="28c0c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-148">System-Flags</span></span>           | <span data-ttu-id="28c0c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c0c-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="28c0c-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28c0c-150">Classes used in</span></span>        | [<span data-ttu-id="28c0c-151">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="28c0c-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28c0c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28c0c-152">Windows Server 2003</span></span>



| <span data-ttu-id="28c0c-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-153">Entry</span></span> | <span data-ttu-id="28c0c-154">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c0c-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28c0c-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c0c-157">System-Only</span></span>            | <span data-ttu-id="28c0c-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-158">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28c0c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="28c0c-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-160">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28c0c-161">Is Indexed</span></span>             | <span data-ttu-id="28c0c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-162">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28c0c-163">In Global Catalog</span></span>      | <span data-ttu-id="28c0c-164">True</span><span class="sxs-lookup"><span data-stu-id="28c0c-164">True</span></span>                                                                    |
| <span data-ttu-id="28c0c-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28c0c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c0c-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28c0c-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="28c0c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c0c-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c0c-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-169">Search-Flags</span></span>           | <span data-ttu-id="28c0c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c0c-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="28c0c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-171">System-Flags</span></span>           | <span data-ttu-id="28c0c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c0c-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="28c0c-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28c0c-173">Classes used in</span></span>        | [<span data-ttu-id="28c0c-174">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="28c0c-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28c0c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28c0c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28c0c-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-176">Entry</span></span> | <span data-ttu-id="28c0c-177">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c0c-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28c0c-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c0c-180">System-Only</span></span>            | <span data-ttu-id="28c0c-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-181">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28c0c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="28c0c-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-183">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28c0c-184">Is Indexed</span></span>             | <span data-ttu-id="28c0c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-185">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28c0c-186">In Global Catalog</span></span>      | <span data-ttu-id="28c0c-187">True</span><span class="sxs-lookup"><span data-stu-id="28c0c-187">True</span></span>                                                                    |
| <span data-ttu-id="28c0c-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28c0c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c0c-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28c0c-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="28c0c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c0c-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c0c-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-192">Search-Flags</span></span>           | <span data-ttu-id="28c0c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c0c-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="28c0c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-194">System-Flags</span></span>           | <span data-ttu-id="28c0c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c0c-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="28c0c-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28c0c-196">Classes used in</span></span>        | [<span data-ttu-id="28c0c-197">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="28c0c-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28c0c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28c0c-198">Windows Server 2008</span></span>



| <span data-ttu-id="28c0c-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-199">Entry</span></span> | <span data-ttu-id="28c0c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c0c-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28c0c-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c0c-203">System-Only</span></span>            | <span data-ttu-id="28c0c-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-204">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28c0c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="28c0c-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-206">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28c0c-207">Is Indexed</span></span>             | <span data-ttu-id="28c0c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-208">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28c0c-209">In Global Catalog</span></span>      | <span data-ttu-id="28c0c-210">True</span><span class="sxs-lookup"><span data-stu-id="28c0c-210">True</span></span>                                                                    |
| <span data-ttu-id="28c0c-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28c0c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c0c-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28c0c-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="28c0c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c0c-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c0c-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-215">Search-Flags</span></span>           | <span data-ttu-id="28c0c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c0c-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="28c0c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-217">System-Flags</span></span>           | <span data-ttu-id="28c0c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c0c-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="28c0c-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28c0c-219">Classes used in</span></span>        | [<span data-ttu-id="28c0c-220">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="28c0c-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28c0c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28c0c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28c0c-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-222">Entry</span></span> | <span data-ttu-id="28c0c-223">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c0c-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28c0c-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c0c-226">System-Only</span></span>            | <span data-ttu-id="28c0c-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-227">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28c0c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="28c0c-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-229">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28c0c-230">Is Indexed</span></span>             | <span data-ttu-id="28c0c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-231">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28c0c-232">In Global Catalog</span></span>      | <span data-ttu-id="28c0c-233">True</span><span class="sxs-lookup"><span data-stu-id="28c0c-233">True</span></span>                                                                    |
| <span data-ttu-id="28c0c-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28c0c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c0c-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28c0c-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="28c0c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c0c-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c0c-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-238">Search-Flags</span></span>           | <span data-ttu-id="28c0c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c0c-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="28c0c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-240">System-Flags</span></span>           | <span data-ttu-id="28c0c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c0c-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="28c0c-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28c0c-242">Classes used in</span></span>        | [<span data-ttu-id="28c0c-243">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="28c0c-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28c0c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28c0c-244">Windows Server 2012</span></span>



| <span data-ttu-id="28c0c-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="28c0c-245">Entry</span></span> | <span data-ttu-id="28c0c-246">Значение</span><span class="sxs-lookup"><span data-stu-id="28c0c-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="28c0c-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28c0c-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28c0c-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="28c0c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="28c0c-249">System-Only</span></span>            | <span data-ttu-id="28c0c-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-250">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28c0c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="28c0c-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-252">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28c0c-253">Is Indexed</span></span>             | <span data-ttu-id="28c0c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="28c0c-254">False</span></span>                                                                   |
| <span data-ttu-id="28c0c-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28c0c-255">In Global Catalog</span></span>      | <span data-ttu-id="28c0c-256">True</span><span class="sxs-lookup"><span data-stu-id="28c0c-256">True</span></span>                                                                    |
| <span data-ttu-id="28c0c-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28c0c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="28c0c-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28c0c-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="28c0c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28c0c-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28c0c-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="28c0c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-261">Search-Flags</span></span>           | <span data-ttu-id="28c0c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28c0c-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="28c0c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28c0c-263">System-Flags</span></span>           | <span data-ttu-id="28c0c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28c0c-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="28c0c-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28c0c-265">Classes used in</span></span>        | [<span data-ttu-id="28c0c-266">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="28c0c-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





