---
title: атрибут MS-PKI-Template-минор-Revision
description: Отслеживает атрибуты в изменяемом классе. Однако это не вызовет автоматическую регистрацию.
ms.assetid: ff08b621-9a77-48a9-847d-f390ffb41326
ms.tgt_platform: multiple
keywords:
- Схема Active Directory для атрибута MS-PKI-Template-Minor-редакция
- Мспки-Template — незначительная версия-схема AD для атрибута
topic_type:
- apiref
api_name:
- ms-PKI-Template-Minor-Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c44e80fa634067ea8b0336cbc63cbf33c09ab2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493977"
---
# <a name="ms-pki-template-minor-revision-attribute"></a><span data-ttu-id="f4953-106">атрибут MS-PKI-Template-минор-Revision</span><span class="sxs-lookup"><span data-stu-id="f4953-106">ms-PKI-Template-Minor-Revision attribute</span></span>

<span data-ttu-id="f4953-107">Отслеживает атрибуты в изменяемом классе.</span><span class="sxs-lookup"><span data-stu-id="f4953-107">Keeps track of attributes in the class changing.</span></span> <span data-ttu-id="f4953-108">Однако это не вызовет автоматическую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="f4953-108">However, this will not trigger auto-enrollment.</span></span>



| <span data-ttu-id="f4953-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4953-109">Entry</span></span> | <span data-ttu-id="f4953-110">Значение</span><span class="sxs-lookup"><span data-stu-id="f4953-110">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4953-111">CN</span><span class="sxs-lookup"><span data-stu-id="f4953-111">CN</span></span>                | <span data-ttu-id="f4953-112">MS-PKI-Template — дополнительный номер редакции</span><span class="sxs-lookup"><span data-stu-id="f4953-112">ms-PKI-Template-Minor-Revision</span></span>                                                                    |
| <span data-ttu-id="f4953-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f4953-113">Ldap-Display-Name</span></span> | <span data-ttu-id="f4953-114">Мспки-Template — дополнительный номер редакции</span><span class="sxs-lookup"><span data-stu-id="f4953-114">msPKI-Template-Minor-Revision</span></span>                                                                     |
| <span data-ttu-id="f4953-115">Размер</span><span class="sxs-lookup"><span data-stu-id="f4953-115">Size</span></span>              | <span data-ttu-id="f4953-116">4 байта</span><span class="sxs-lookup"><span data-stu-id="f4953-116">4 bytes</span></span>                                                                                           |
| <span data-ttu-id="f4953-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f4953-117">Update Privilege</span></span>  | <span data-ttu-id="f4953-118">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="f4953-118">Domain administrator</span></span>                                                                              |
| <span data-ttu-id="f4953-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f4953-119">Update Frequency</span></span>  | <span data-ttu-id="f4953-120">При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template).</span><span class="sxs-lookup"><span data-stu-id="f4953-120">When the certificate template (ms-PKI-Certificate-Template) object is edited, created, or cloned.</span></span> |
| <span data-ttu-id="f4953-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f4953-121">Attribute-Id</span></span>      | <span data-ttu-id="f4953-122">1.2.840.113556.1.4.1435</span><span class="sxs-lookup"><span data-stu-id="f4953-122">1.2.840.113556.1.4.1435</span></span>                                                                           |
| <span data-ttu-id="f4953-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f4953-123">System-Id-Guid</span></span>    | <span data-ttu-id="f4953-124">13f5236c-1884-46b1-b5d0-484e38990d58</span><span class="sxs-lookup"><span data-stu-id="f4953-124">13f5236c-1884-46b1-b5d0-484e38990d58</span></span>                                                              |
| <span data-ttu-id="f4953-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4953-125">Syntax</span></span>            | [<span data-ttu-id="f4953-126">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="f4953-126">**Enumeration**</span></span>](s-enumeration.md)                                                              |



## <a name="implementations"></a><span data-ttu-id="f4953-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f4953-127">Implementations</span></span>

-   [<span data-ttu-id="f4953-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f4953-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f4953-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f4953-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f4953-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f4953-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f4953-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f4953-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f4953-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f4953-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="f4953-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4953-133">Windows Server 2003</span></span>



| <span data-ttu-id="f4953-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4953-134">Entry</span></span> | <span data-ttu-id="f4953-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f4953-135">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f4953-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4953-136">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4953-137">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4953-138">System-Only</span></span>            | <span data-ttu-id="f4953-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-139">False</span></span>                                                                   |
| <span data-ttu-id="f4953-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4953-140">Is-Single-Valued</span></span>       | <span data-ttu-id="f4953-141">True</span><span class="sxs-lookup"><span data-stu-id="f4953-141">True</span></span>                                                                    |
| <span data-ttu-id="f4953-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4953-142">Is Indexed</span></span>             | <span data-ttu-id="f4953-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-143">False</span></span>                                                                   |
| <span data-ttu-id="f4953-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4953-144">In Global Catalog</span></span>      | <span data-ttu-id="f4953-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-145">False</span></span>                                                                   |
| <span data-ttu-id="f4953-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4953-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4953-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4953-147">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="f4953-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4953-148">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4953-149">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-150">Search-Flags</span></span>           | <span data-ttu-id="f4953-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4953-151">0x00000000</span></span>                                                              |
| <span data-ttu-id="f4953-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-152">System-Flags</span></span>           | <span data-ttu-id="f4953-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4953-153">0x00000010</span></span>                                                              |
| <span data-ttu-id="f4953-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4953-154">Classes used in</span></span>        | [<span data-ttu-id="f4953-155">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="f4953-155">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f4953-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f4953-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f4953-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4953-157">Entry</span></span> | <span data-ttu-id="f4953-158">Значение</span><span class="sxs-lookup"><span data-stu-id="f4953-158">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f4953-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4953-159">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4953-160">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4953-161">System-Only</span></span>            | <span data-ttu-id="f4953-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-162">False</span></span>                                                                   |
| <span data-ttu-id="f4953-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4953-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f4953-164">True</span><span class="sxs-lookup"><span data-stu-id="f4953-164">True</span></span>                                                                    |
| <span data-ttu-id="f4953-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4953-165">Is Indexed</span></span>             | <span data-ttu-id="f4953-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-166">False</span></span>                                                                   |
| <span data-ttu-id="f4953-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4953-167">In Global Catalog</span></span>      | <span data-ttu-id="f4953-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-168">False</span></span>                                                                   |
| <span data-ttu-id="f4953-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4953-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4953-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4953-170">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="f4953-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4953-171">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4953-172">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-173">Search-Flags</span></span>           | <span data-ttu-id="f4953-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4953-174">0x00000000</span></span>                                                              |
| <span data-ttu-id="f4953-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-175">System-Flags</span></span>           | <span data-ttu-id="f4953-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4953-176">0x00000010</span></span>                                                              |
| <span data-ttu-id="f4953-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4953-177">Classes used in</span></span>        | [<span data-ttu-id="f4953-178">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="f4953-178">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f4953-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4953-179">Windows Server 2008</span></span>



| <span data-ttu-id="f4953-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4953-180">Entry</span></span> | <span data-ttu-id="f4953-181">Значение</span><span class="sxs-lookup"><span data-stu-id="f4953-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f4953-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4953-182">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4953-183">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4953-184">System-Only</span></span>            | <span data-ttu-id="f4953-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-185">False</span></span>                                                                   |
| <span data-ttu-id="f4953-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4953-186">Is-Single-Valued</span></span>       | <span data-ttu-id="f4953-187">True</span><span class="sxs-lookup"><span data-stu-id="f4953-187">True</span></span>                                                                    |
| <span data-ttu-id="f4953-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4953-188">Is Indexed</span></span>             | <span data-ttu-id="f4953-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-189">False</span></span>                                                                   |
| <span data-ttu-id="f4953-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4953-190">In Global Catalog</span></span>      | <span data-ttu-id="f4953-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-191">False</span></span>                                                                   |
| <span data-ttu-id="f4953-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4953-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4953-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4953-193">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="f4953-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4953-194">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4953-195">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-196">Search-Flags</span></span>           | <span data-ttu-id="f4953-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4953-197">0x00000000</span></span>                                                              |
| <span data-ttu-id="f4953-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-198">System-Flags</span></span>           | <span data-ttu-id="f4953-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4953-199">0x00000010</span></span>                                                              |
| <span data-ttu-id="f4953-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4953-200">Classes used in</span></span>        | [<span data-ttu-id="f4953-201">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="f4953-201">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f4953-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f4953-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f4953-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4953-203">Entry</span></span> | <span data-ttu-id="f4953-204">Значение</span><span class="sxs-lookup"><span data-stu-id="f4953-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f4953-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4953-205">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4953-206">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4953-207">System-Only</span></span>            | <span data-ttu-id="f4953-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-208">False</span></span>                                                                   |
| <span data-ttu-id="f4953-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4953-209">Is-Single-Valued</span></span>       | <span data-ttu-id="f4953-210">True</span><span class="sxs-lookup"><span data-stu-id="f4953-210">True</span></span>                                                                    |
| <span data-ttu-id="f4953-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4953-211">Is Indexed</span></span>             | <span data-ttu-id="f4953-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-212">False</span></span>                                                                   |
| <span data-ttu-id="f4953-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4953-213">In Global Catalog</span></span>      | <span data-ttu-id="f4953-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-214">False</span></span>                                                                   |
| <span data-ttu-id="f4953-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4953-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4953-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4953-216">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="f4953-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4953-217">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4953-218">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-219">Search-Flags</span></span>           | <span data-ttu-id="f4953-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4953-220">0x00000000</span></span>                                                              |
| <span data-ttu-id="f4953-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-221">System-Flags</span></span>           | <span data-ttu-id="f4953-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4953-222">0x00000010</span></span>                                                              |
| <span data-ttu-id="f4953-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4953-223">Classes used in</span></span>        | [<span data-ttu-id="f4953-224">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="f4953-224">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f4953-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4953-225">Windows Server 2012</span></span>



| <span data-ttu-id="f4953-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="f4953-226">Entry</span></span> | <span data-ttu-id="f4953-227">Значение</span><span class="sxs-lookup"><span data-stu-id="f4953-227">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f4953-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f4953-228">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f4953-229">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="f4953-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="f4953-230">System-Only</span></span>            | <span data-ttu-id="f4953-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-231">False</span></span>                                                                   |
| <span data-ttu-id="f4953-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f4953-232">Is-Single-Valued</span></span>       | <span data-ttu-id="f4953-233">True</span><span class="sxs-lookup"><span data-stu-id="f4953-233">True</span></span>                                                                    |
| <span data-ttu-id="f4953-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f4953-234">Is Indexed</span></span>             | <span data-ttu-id="f4953-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-235">False</span></span>                                                                   |
| <span data-ttu-id="f4953-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f4953-236">In Global Catalog</span></span>      | <span data-ttu-id="f4953-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="f4953-237">False</span></span>                                                                   |
| <span data-ttu-id="f4953-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f4953-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="f4953-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f4953-239">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="f4953-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f4953-240">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f4953-241">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="f4953-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-242">Search-Flags</span></span>           | <span data-ttu-id="f4953-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f4953-243">0x00000000</span></span>                                                              |
| <span data-ttu-id="f4953-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f4953-244">System-Flags</span></span>           | <span data-ttu-id="f4953-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f4953-245">0x00000010</span></span>                                                              |
| <span data-ttu-id="f4953-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f4953-246">Classes used in</span></span>        | [<span data-ttu-id="f4953-247">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="f4953-247">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





