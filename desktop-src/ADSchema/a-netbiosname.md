---
title: Атрибут NETBIOS-Name
description: Имя объекта, который будет использоваться по протоколу NetBIOS.
ms.assetid: 03cbfa61-b747-4f3e-9bf5-17fd6da2e7be
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута NETBIOS-Name
- Схема AD атрибута nETBIOSName
topic_type:
- apiref
api_name:
- NETBIOS-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4063b842200bf99910a3652b8f3bea9419c2728f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138551"
---
# <a name="netbios-name-attribute"></a><span data-ttu-id="1f920-105">Атрибут NETBIOS-Name</span><span class="sxs-lookup"><span data-stu-id="1f920-105">NETBIOS-Name attribute</span></span>

<span data-ttu-id="1f920-106">Имя объекта, который будет использоваться по протоколу NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="1f920-106">The name of the object to be used over NetBIOS.</span></span>



| <span data-ttu-id="1f920-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-107">Entry</span></span> | <span data-ttu-id="1f920-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="1f920-109">CN</span><span class="sxs-lookup"><span data-stu-id="1f920-109">CN</span></span>                | <span data-ttu-id="1f920-110">NETBIOS-Name</span><span class="sxs-lookup"><span data-stu-id="1f920-110">NETBIOS-Name</span></span>                                |
| <span data-ttu-id="1f920-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="1f920-111">Ldap-Display-Name</span></span> | <span data-ttu-id="1f920-112">nETBIOSName</span><span class="sxs-lookup"><span data-stu-id="1f920-112">nETBIOSName</span></span>                                 |
| <span data-ttu-id="1f920-113">Размер</span><span class="sxs-lookup"><span data-stu-id="1f920-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="1f920-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="1f920-114">Update Privilege</span></span>  | <span data-ttu-id="1f920-115">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="1f920-115">Domain administrator</span></span>                        |
| <span data-ttu-id="1f920-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="1f920-116">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="1f920-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-117">Attribute-Id</span></span>      | <span data-ttu-id="1f920-118">1.2.840.113556.1.4.87</span><span class="sxs-lookup"><span data-stu-id="1f920-118">1.2.840.113556.1.4.87</span></span>                       |
| <span data-ttu-id="1f920-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="1f920-119">System-Id-Guid</span></span>    | <span data-ttu-id="1f920-120">bf9679d8-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1f920-120">bf9679d8-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="1f920-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f920-121">Syntax</span></span>            | [<span data-ttu-id="1f920-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="1f920-122">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="1f920-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="1f920-123">Implementations</span></span>

-   [<span data-ttu-id="1f920-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1f920-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1f920-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1f920-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1f920-126">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1f920-126">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1f920-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1f920-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1f920-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1f920-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1f920-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1f920-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1f920-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1f920-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1f920-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f920-131">Windows 2000 Server</span></span>



| <span data-ttu-id="1f920-132">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-132">Entry</span></span> | <span data-ttu-id="1f920-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-133">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-134">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-134">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-135">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-136">System-Only</span></span>            | <span data-ttu-id="1f920-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-137">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-138">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-138">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-139">True</span><span class="sxs-lookup"><span data-stu-id="1f920-139">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-140">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-140">Is Indexed</span></span>             | <span data-ttu-id="1f920-141">True</span><span class="sxs-lookup"><span data-stu-id="1f920-141">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-142">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-142">In Global Catalog</span></span>      | <span data-ttu-id="1f920-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-143">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-144">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-145">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-145">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="1f920-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-146">Range-Lower</span></span>            | <span data-ttu-id="1f920-147">1</span><span class="sxs-lookup"><span data-stu-id="1f920-147">1</span></span>                                                                                       |
| <span data-ttu-id="1f920-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-148">Range-Upper</span></span>            | <span data-ttu-id="1f920-149">16</span><span class="sxs-lookup"><span data-stu-id="1f920-149">16</span></span>                                                                                      |
| <span data-ttu-id="1f920-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-150">Search-Flags</span></span>           | <span data-ttu-id="1f920-151">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-151">0x00000001</span></span>                                                                              |
| <span data-ttu-id="1f920-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-152">System-Flags</span></span>           | <span data-ttu-id="1f920-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-153">0x00000010</span></span>                                                                              |
| <span data-ttu-id="1f920-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-154">Classes used in</span></span>        | [<span data-ttu-id="1f920-155">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-155">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-156">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="1f920-156">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1f920-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f920-157">Windows Server 2003</span></span>



| <span data-ttu-id="1f920-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-158">Entry</span></span> | <span data-ttu-id="1f920-159">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-159">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-160">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-161">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-162">System-Only</span></span>            | <span data-ttu-id="1f920-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-163">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-164">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-165">True</span><span class="sxs-lookup"><span data-stu-id="1f920-165">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-166">Is Indexed</span></span>             | <span data-ttu-id="1f920-167">True</span><span class="sxs-lookup"><span data-stu-id="1f920-167">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-168">In Global Catalog</span></span>      | <span data-ttu-id="1f920-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-169">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-171">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="1f920-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-172">Range-Lower</span></span>            | <span data-ttu-id="1f920-173">1</span><span class="sxs-lookup"><span data-stu-id="1f920-173">1</span></span>                                                                                       |
| <span data-ttu-id="1f920-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-174">Range-Upper</span></span>            | <span data-ttu-id="1f920-175">16</span><span class="sxs-lookup"><span data-stu-id="1f920-175">16</span></span>                                                                                      |
| <span data-ttu-id="1f920-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-176">Search-Flags</span></span>           | <span data-ttu-id="1f920-177">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-177">0x00000001</span></span>                                                                              |
| <span data-ttu-id="1f920-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-178">System-Flags</span></span>           | <span data-ttu-id="1f920-179">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-179">0x00000010</span></span>                                                                              |
| <span data-ttu-id="1f920-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-180">Classes used in</span></span>        | [<span data-ttu-id="1f920-181">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-181">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-182">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="1f920-182">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1f920-183">ADAM</span><span class="sxs-lookup"><span data-stu-id="1f920-183">ADAM</span></span>



| <span data-ttu-id="1f920-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-184">Entry</span></span> | <span data-ttu-id="1f920-185">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-185">Value</span></span> |
|------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-186">Link-Id</span></span>                | \-                                                                               |
| <span data-ttu-id="1f920-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-187">MAPI-Id</span></span>                | \-                                                                               |
| <span data-ttu-id="1f920-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-188">System-Only</span></span>            | <span data-ttu-id="1f920-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-189">False</span></span>                                                                            |
| <span data-ttu-id="1f920-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-190">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-191">True</span><span class="sxs-lookup"><span data-stu-id="1f920-191">True</span></span>                                                                             |
| <span data-ttu-id="1f920-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-192">Is Indexed</span></span>             | <span data-ttu-id="1f920-193">True</span><span class="sxs-lookup"><span data-stu-id="1f920-193">True</span></span>                                                                             |
| <span data-ttu-id="1f920-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-194">In Global Catalog</span></span>      | <span data-ttu-id="1f920-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-195">False</span></span>                                                                            |
| <span data-ttu-id="1f920-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-197">O:BAG:BAD:S:</span></span>                                                                     |
| <span data-ttu-id="1f920-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-198">Range-Lower</span></span>            | <span data-ttu-id="1f920-199">1</span><span class="sxs-lookup"><span data-stu-id="1f920-199">1</span></span>                                                                                |
| <span data-ttu-id="1f920-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-200">Range-Upper</span></span>            | <span data-ttu-id="1f920-201">16</span><span class="sxs-lookup"><span data-stu-id="1f920-201">16</span></span>                                                                               |
| <span data-ttu-id="1f920-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-202">Search-Flags</span></span>           | <span data-ttu-id="1f920-203">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-203">0x00000001</span></span>                                                                       |
| <span data-ttu-id="1f920-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-204">System-Flags</span></span>           | <span data-ttu-id="1f920-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-205">0x00000010</span></span>                                                                       |
| <span data-ttu-id="1f920-206">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-206">Classes used in</span></span>        | [<span data-ttu-id="1f920-207">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-207">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-208">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="1f920-208">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1f920-209">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1f920-209">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1f920-210">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-210">Entry</span></span> | <span data-ttu-id="1f920-211">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-211">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-212">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-212">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-213">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-213">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-214">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-214">System-Only</span></span>            | <span data-ttu-id="1f920-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-215">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-216">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-216">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-217">True</span><span class="sxs-lookup"><span data-stu-id="1f920-217">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-218">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-218">Is Indexed</span></span>             | <span data-ttu-id="1f920-219">True</span><span class="sxs-lookup"><span data-stu-id="1f920-219">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-220">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-220">In Global Catalog</span></span>      | <span data-ttu-id="1f920-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-221">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-222">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-222">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-223">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-223">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="1f920-224">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-224">Range-Lower</span></span>            | <span data-ttu-id="1f920-225">1</span><span class="sxs-lookup"><span data-stu-id="1f920-225">1</span></span>                                                                                       |
| <span data-ttu-id="1f920-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-226">Range-Upper</span></span>            | <span data-ttu-id="1f920-227">16</span><span class="sxs-lookup"><span data-stu-id="1f920-227">16</span></span>                                                                                      |
| <span data-ttu-id="1f920-228">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-228">Search-Flags</span></span>           | <span data-ttu-id="1f920-229">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-229">0x00000001</span></span>                                                                              |
| <span data-ttu-id="1f920-230">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-230">System-Flags</span></span>           | <span data-ttu-id="1f920-231">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-231">0x00000010</span></span>                                                                              |
| <span data-ttu-id="1f920-232">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-232">Classes used in</span></span>        | [<span data-ttu-id="1f920-233">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-233">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-234">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="1f920-234">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1f920-235">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f920-235">Windows Server 2008</span></span>



| <span data-ttu-id="1f920-236">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-236">Entry</span></span> | <span data-ttu-id="1f920-237">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-237">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-238">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-238">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-239">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-240">System-Only</span></span>            | <span data-ttu-id="1f920-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-241">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-242">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-242">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-243">True</span><span class="sxs-lookup"><span data-stu-id="1f920-243">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-244">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-244">Is Indexed</span></span>             | <span data-ttu-id="1f920-245">True</span><span class="sxs-lookup"><span data-stu-id="1f920-245">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-246">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-246">In Global Catalog</span></span>      | <span data-ttu-id="1f920-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-247">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-248">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-249">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-249">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="1f920-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-250">Range-Lower</span></span>            | <span data-ttu-id="1f920-251">1</span><span class="sxs-lookup"><span data-stu-id="1f920-251">1</span></span>                                                                                       |
| <span data-ttu-id="1f920-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-252">Range-Upper</span></span>            | <span data-ttu-id="1f920-253">16</span><span class="sxs-lookup"><span data-stu-id="1f920-253">16</span></span>                                                                                      |
| <span data-ttu-id="1f920-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-254">Search-Flags</span></span>           | <span data-ttu-id="1f920-255">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-255">0x00000001</span></span>                                                                              |
| <span data-ttu-id="1f920-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-256">System-Flags</span></span>           | <span data-ttu-id="1f920-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-257">0x00000010</span></span>                                                                              |
| <span data-ttu-id="1f920-258">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-258">Classes used in</span></span>        | [<span data-ttu-id="1f920-259">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-259">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-260">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="1f920-260">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1f920-261">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f920-261">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1f920-262">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-262">Entry</span></span> | <span data-ttu-id="1f920-263">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-263">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-264">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-264">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-265">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-265">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-266">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-266">System-Only</span></span>            | <span data-ttu-id="1f920-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-267">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-268">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-268">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-269">True</span><span class="sxs-lookup"><span data-stu-id="1f920-269">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-270">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-270">Is Indexed</span></span>             | <span data-ttu-id="1f920-271">True</span><span class="sxs-lookup"><span data-stu-id="1f920-271">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-272">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-272">In Global Catalog</span></span>      | <span data-ttu-id="1f920-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-273">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-274">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-274">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-275">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-275">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="1f920-276">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-276">Range-Lower</span></span>            | <span data-ttu-id="1f920-277">1</span><span class="sxs-lookup"><span data-stu-id="1f920-277">1</span></span>                                                                                       |
| <span data-ttu-id="1f920-278">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-278">Range-Upper</span></span>            | <span data-ttu-id="1f920-279">16</span><span class="sxs-lookup"><span data-stu-id="1f920-279">16</span></span>                                                                                      |
| <span data-ttu-id="1f920-280">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-280">Search-Flags</span></span>           | <span data-ttu-id="1f920-281">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-281">0x00000001</span></span>                                                                              |
| <span data-ttu-id="1f920-282">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-282">System-Flags</span></span>           | <span data-ttu-id="1f920-283">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-283">0x00000010</span></span>                                                                              |
| <span data-ttu-id="1f920-284">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-284">Classes used in</span></span>        | [<span data-ttu-id="1f920-285">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-285">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-286">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="1f920-286">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1f920-287">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1f920-287">Windows Server 2012</span></span>



| <span data-ttu-id="1f920-288">Ввод</span><span class="sxs-lookup"><span data-stu-id="1f920-288">Entry</span></span> | <span data-ttu-id="1f920-289">Значение</span><span class="sxs-lookup"><span data-stu-id="1f920-289">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f920-290">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="1f920-290">Link-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-291">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1f920-291">MAPI-Id</span></span>                | \-                                                                                      |
| <span data-ttu-id="1f920-292">System-Only</span><span class="sxs-lookup"><span data-stu-id="1f920-292">System-Only</span></span>            | <span data-ttu-id="1f920-293">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-293">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-294">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="1f920-294">Is-Single-Valued</span></span>       | <span data-ttu-id="1f920-295">True</span><span class="sxs-lookup"><span data-stu-id="1f920-295">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-296">Индексируется</span><span class="sxs-lookup"><span data-stu-id="1f920-296">Is Indexed</span></span>             | <span data-ttu-id="1f920-297">True</span><span class="sxs-lookup"><span data-stu-id="1f920-297">True</span></span>                                                                                    |
| <span data-ttu-id="1f920-298">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="1f920-298">In Global Catalog</span></span>      | <span data-ttu-id="1f920-299">Неверно</span><span class="sxs-lookup"><span data-stu-id="1f920-299">False</span></span>                                                                                   |
| <span data-ttu-id="1f920-300">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="1f920-300">NT-Security-Descriptor</span></span> | <span data-ttu-id="1f920-301">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="1f920-301">O:BAG:BAD:S:</span></span>                                                                            |
| <span data-ttu-id="1f920-302">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1f920-302">Range-Lower</span></span>            | <span data-ttu-id="1f920-303">1</span><span class="sxs-lookup"><span data-stu-id="1f920-303">1</span></span>                                                                                       |
| <span data-ttu-id="1f920-304">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1f920-304">Range-Upper</span></span>            | <span data-ttu-id="1f920-305">16</span><span class="sxs-lookup"><span data-stu-id="1f920-305">16</span></span>                                                                                      |
| <span data-ttu-id="1f920-306">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-306">Search-Flags</span></span>           | <span data-ttu-id="1f920-307">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1f920-307">0x00000001</span></span>                                                                              |
| <span data-ttu-id="1f920-308">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1f920-308">System-Flags</span></span>           | <span data-ttu-id="1f920-309">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1f920-309">0x00000010</span></span>                                                                              |
| <span data-ttu-id="1f920-310">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="1f920-310">Classes used in</span></span>        | [<span data-ttu-id="1f920-311">**Перекрестная ссылка**</span><span class="sxs-lookup"><span data-stu-id="1f920-311">**Cross-Ref**</span></span>](c-crossref.md)<br/> [<span data-ttu-id="1f920-312">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="1f920-312">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





