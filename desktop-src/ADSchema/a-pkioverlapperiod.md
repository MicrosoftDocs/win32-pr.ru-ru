---
title: PKI-перекрытие-атрибут периода
description: Период времени, в течение которого сертификат должен быть продлен до истечения срока его действия.
ms.assetid: 394c78b2-7476-4c2d-9a95-f781c779ea4d
ms.tgt_platform: multiple
keywords:
- ИНФРАСТРУКТУРА AD — перекрытие с атрибутом периода
- Схема AD атрибута Пкиоверлаппериод
topic_type:
- apiref
api_name:
- PKI-Overlap-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad34a30086c4a6de8f96ae18e99c2f8a71682ef
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893313"
---
# <a name="pki-overlap-period-attribute"></a><span data-ttu-id="cf20e-105">PKI-перекрытие-атрибут периода</span><span class="sxs-lookup"><span data-stu-id="cf20e-105">PKI-Overlap-Period attribute</span></span>

<span data-ttu-id="cf20e-106">Период времени, в течение которого сертификат должен быть продлен до истечения срока его действия.</span><span class="sxs-lookup"><span data-stu-id="cf20e-106">The period by when the certificate should be renewed before it is expired.</span></span>



| <span data-ttu-id="cf20e-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-107">Entry</span></span> | <span data-ttu-id="cf20e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="cf20e-109">CN</span><span class="sxs-lookup"><span data-stu-id="cf20e-109">CN</span></span>                | <span data-ttu-id="cf20e-110">PKI — перекрытие — точка</span><span class="sxs-lookup"><span data-stu-id="cf20e-110">PKI-Overlap-Period</span></span>                                    |
| <span data-ttu-id="cf20e-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cf20e-111">Ldap-Display-Name</span></span> | <span data-ttu-id="cf20e-112">пкиоверлаппериод</span><span class="sxs-lookup"><span data-stu-id="cf20e-112">pKIOverlapPeriod</span></span>                                      |
| <span data-ttu-id="cf20e-113">Размер</span><span class="sxs-lookup"><span data-stu-id="cf20e-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="cf20e-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cf20e-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="cf20e-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cf20e-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="cf20e-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-116">Attribute-Id</span></span>      | <span data-ttu-id="cf20e-117">1.2.840.113556.1.4.1332</span><span class="sxs-lookup"><span data-stu-id="cf20e-117">1.2.840.113556.1.4.1332</span></span>                               |
| <span data-ttu-id="cf20e-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cf20e-118">System-Id-Guid</span></span>    | <span data-ttu-id="cf20e-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span><span class="sxs-lookup"><span data-stu-id="cf20e-119">1219a3ec-3b9e-11d2-90cc-00c04fd91ab1</span></span>                  |
| <span data-ttu-id="cf20e-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf20e-120">Syntax</span></span>            | [<span data-ttu-id="cf20e-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="cf20e-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="cf20e-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cf20e-122">Implementations</span></span>

-   [<span data-ttu-id="cf20e-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="cf20e-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="cf20e-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="cf20e-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="cf20e-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="cf20e-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="cf20e-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cf20e-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cf20e-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cf20e-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cf20e-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cf20e-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="cf20e-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf20e-129">Windows 2000 Server</span></span>



| <span data-ttu-id="cf20e-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-130">Entry</span></span> | <span data-ttu-id="cf20e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf20e-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf20e-132">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-133">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf20e-134">System-Only</span></span>            | <span data-ttu-id="cf20e-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-135">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf20e-136">Is-Single-Valued</span></span>       | <span data-ttu-id="cf20e-137">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-137">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf20e-138">Is Indexed</span></span>             | <span data-ttu-id="cf20e-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-139">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf20e-140">In Global Catalog</span></span>      | <span data-ttu-id="cf20e-141">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-141">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf20e-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf20e-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf20e-143">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cf20e-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf20e-144">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf20e-145">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-146">Search-Flags</span></span>           | <span data-ttu-id="cf20e-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf20e-147">0x00000000</span></span>                                                              |
| <span data-ttu-id="cf20e-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-148">System-Flags</span></span>           | <span data-ttu-id="cf20e-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf20e-149">0x00000010</span></span>                                                              |
| <span data-ttu-id="cf20e-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf20e-150">Classes used in</span></span>        | [<span data-ttu-id="cf20e-151">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="cf20e-151">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="cf20e-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf20e-152">Windows Server 2003</span></span>



| <span data-ttu-id="cf20e-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-153">Entry</span></span> | <span data-ttu-id="cf20e-154">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-154">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf20e-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf20e-155">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-156">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf20e-157">System-Only</span></span>            | <span data-ttu-id="cf20e-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-158">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf20e-159">Is-Single-Valued</span></span>       | <span data-ttu-id="cf20e-160">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-160">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf20e-161">Is Indexed</span></span>             | <span data-ttu-id="cf20e-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-162">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf20e-163">In Global Catalog</span></span>      | <span data-ttu-id="cf20e-164">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-164">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf20e-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf20e-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf20e-166">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cf20e-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf20e-167">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf20e-168">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-169">Search-Flags</span></span>           | <span data-ttu-id="cf20e-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf20e-170">0x00000000</span></span>                                                              |
| <span data-ttu-id="cf20e-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-171">System-Flags</span></span>           | <span data-ttu-id="cf20e-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf20e-172">0x00000010</span></span>                                                              |
| <span data-ttu-id="cf20e-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf20e-173">Classes used in</span></span>        | [<span data-ttu-id="cf20e-174">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="cf20e-174">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="cf20e-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="cf20e-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="cf20e-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-176">Entry</span></span> | <span data-ttu-id="cf20e-177">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-177">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf20e-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf20e-178">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-179">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf20e-180">System-Only</span></span>            | <span data-ttu-id="cf20e-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-181">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf20e-182">Is-Single-Valued</span></span>       | <span data-ttu-id="cf20e-183">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-183">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf20e-184">Is Indexed</span></span>             | <span data-ttu-id="cf20e-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-185">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf20e-186">In Global Catalog</span></span>      | <span data-ttu-id="cf20e-187">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-187">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf20e-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf20e-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf20e-189">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cf20e-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf20e-190">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf20e-191">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-192">Search-Flags</span></span>           | <span data-ttu-id="cf20e-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf20e-193">0x00000000</span></span>                                                              |
| <span data-ttu-id="cf20e-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-194">System-Flags</span></span>           | <span data-ttu-id="cf20e-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf20e-195">0x00000010</span></span>                                                              |
| <span data-ttu-id="cf20e-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf20e-196">Classes used in</span></span>        | [<span data-ttu-id="cf20e-197">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="cf20e-197">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="cf20e-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf20e-198">Windows Server 2008</span></span>



| <span data-ttu-id="cf20e-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-199">Entry</span></span> | <span data-ttu-id="cf20e-200">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-200">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf20e-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf20e-201">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-202">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf20e-203">System-Only</span></span>            | <span data-ttu-id="cf20e-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-204">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf20e-205">Is-Single-Valued</span></span>       | <span data-ttu-id="cf20e-206">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-206">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf20e-207">Is Indexed</span></span>             | <span data-ttu-id="cf20e-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-208">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf20e-209">In Global Catalog</span></span>      | <span data-ttu-id="cf20e-210">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-210">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf20e-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf20e-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf20e-212">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cf20e-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf20e-213">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf20e-214">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-215">Search-Flags</span></span>           | <span data-ttu-id="cf20e-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf20e-216">0x00000000</span></span>                                                              |
| <span data-ttu-id="cf20e-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-217">System-Flags</span></span>           | <span data-ttu-id="cf20e-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf20e-218">0x00000010</span></span>                                                              |
| <span data-ttu-id="cf20e-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf20e-219">Classes used in</span></span>        | [<span data-ttu-id="cf20e-220">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="cf20e-220">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cf20e-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cf20e-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cf20e-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-222">Entry</span></span> | <span data-ttu-id="cf20e-223">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-223">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf20e-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf20e-224">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-225">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf20e-226">System-Only</span></span>            | <span data-ttu-id="cf20e-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-227">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf20e-228">Is-Single-Valued</span></span>       | <span data-ttu-id="cf20e-229">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-229">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf20e-230">Is Indexed</span></span>             | <span data-ttu-id="cf20e-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-231">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf20e-232">In Global Catalog</span></span>      | <span data-ttu-id="cf20e-233">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-233">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf20e-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf20e-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf20e-235">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cf20e-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf20e-236">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf20e-237">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-238">Search-Flags</span></span>           | <span data-ttu-id="cf20e-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf20e-239">0x00000000</span></span>                                                              |
| <span data-ttu-id="cf20e-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-240">System-Flags</span></span>           | <span data-ttu-id="cf20e-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf20e-241">0x00000010</span></span>                                                              |
| <span data-ttu-id="cf20e-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf20e-242">Classes used in</span></span>        | [<span data-ttu-id="cf20e-243">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="cf20e-243">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cf20e-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf20e-244">Windows Server 2012</span></span>



| <span data-ttu-id="cf20e-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="cf20e-245">Entry</span></span> | <span data-ttu-id="cf20e-246">Значение</span><span class="sxs-lookup"><span data-stu-id="cf20e-246">Value</span></span> |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="cf20e-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cf20e-247">Link-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cf20e-248">MAPI-Id</span></span>                | \-                                                                      |
| <span data-ttu-id="cf20e-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="cf20e-249">System-Only</span></span>            | <span data-ttu-id="cf20e-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-250">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cf20e-251">Is-Single-Valued</span></span>       | <span data-ttu-id="cf20e-252">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-252">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cf20e-253">Is Indexed</span></span>             | <span data-ttu-id="cf20e-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="cf20e-254">False</span></span>                                                                   |
| <span data-ttu-id="cf20e-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cf20e-255">In Global Catalog</span></span>      | <span data-ttu-id="cf20e-256">True</span><span class="sxs-lookup"><span data-stu-id="cf20e-256">True</span></span>                                                                    |
| <span data-ttu-id="cf20e-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cf20e-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="cf20e-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cf20e-258">O:BAG:BAD:S:</span></span>                                                            |
| <span data-ttu-id="cf20e-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cf20e-259">Range-Lower</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cf20e-260">Range-Upper</span></span>            | \-                                                                      |
| <span data-ttu-id="cf20e-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-261">Search-Flags</span></span>           | <span data-ttu-id="cf20e-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="cf20e-262">0x00000000</span></span>                                                              |
| <span data-ttu-id="cf20e-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cf20e-263">System-Flags</span></span>           | <span data-ttu-id="cf20e-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cf20e-264">0x00000010</span></span>                                                              |
| <span data-ttu-id="cf20e-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cf20e-265">Classes used in</span></span>        | [<span data-ttu-id="cf20e-266">**PKI — шаблон сертификата**</span><span class="sxs-lookup"><span data-stu-id="cf20e-266">**PKI-Certificate-Template**</span></span>](c-pkicertificatetemplate.md)<br/> |



 

 





