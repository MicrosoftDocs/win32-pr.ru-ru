---
title: Атрибут Domain-Component
description: Атрибут именования для объектов Domain и DNS. Обычно отображается как DC имя_домена.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Domain-Component
- Схема AD атрибута контроллера домена
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138211"
---
# <a name="domain-component-attribute"></a><span data-ttu-id="881b3-106">Атрибут Domain-Component</span><span class="sxs-lookup"><span data-stu-id="881b3-106">Domain-Component attribute</span></span>

<span data-ttu-id="881b3-107">Атрибут именования для объектов Domain и DNS.</span><span class="sxs-lookup"><span data-stu-id="881b3-107">The naming attribute for Domain and DNS objects.</span></span> <span data-ttu-id="881b3-108">Обычно отображается как DC = имя_домена.</span><span class="sxs-lookup"><span data-stu-id="881b3-108">Usually displayed as dc=DomainName.</span></span>



| <span data-ttu-id="881b3-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-109">Entry</span></span> | <span data-ttu-id="881b3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="881b3-111">CN</span><span class="sxs-lookup"><span data-stu-id="881b3-111">CN</span></span>                | <span data-ttu-id="881b3-112">Domain-Component</span><span class="sxs-lookup"><span data-stu-id="881b3-112">Domain-Component</span></span>                            |
| <span data-ttu-id="881b3-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="881b3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="881b3-114">dc</span><span class="sxs-lookup"><span data-stu-id="881b3-114">dc</span></span>                                          |
| <span data-ttu-id="881b3-115">Размер</span><span class="sxs-lookup"><span data-stu-id="881b3-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="881b3-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="881b3-116">Update Privilege</span></span>  | <span data-ttu-id="881b3-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="881b3-117">Domain administrator</span></span>                        |
| <span data-ttu-id="881b3-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="881b3-118">Update Frequency</span></span>  | <span data-ttu-id="881b3-119">При создании домена.</span><span class="sxs-lookup"><span data-stu-id="881b3-119">When the domain is created.</span></span>                 |
| <span data-ttu-id="881b3-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-120">Attribute-Id</span></span>      | <span data-ttu-id="881b3-121">0.9.2342.19200300.100.1.25</span><span class="sxs-lookup"><span data-stu-id="881b3-121">0.9.2342.19200300.100.1.25</span></span>                  |
| <span data-ttu-id="881b3-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="881b3-122">System-Id-Guid</span></span>    | <span data-ttu-id="881b3-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="881b3-123">19195a55-6da0-11d0-afd3-00c04fd930c9</span></span>        |
| <span data-ttu-id="881b3-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="881b3-124">Syntax</span></span>            | [<span data-ttu-id="881b3-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="881b3-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="881b3-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="881b3-126">Implementations</span></span>

-   [<span data-ttu-id="881b3-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="881b3-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="881b3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="881b3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="881b3-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="881b3-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="881b3-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="881b3-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="881b3-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="881b3-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="881b3-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="881b3-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="881b3-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="881b3-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="881b3-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="881b3-134">Windows 2000 Server</span></span>



| <span data-ttu-id="881b3-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-135">Entry</span></span> | <span data-ttu-id="881b3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-136">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b3-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-137">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-138">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-139">System-Only</span></span>            | <span data-ttu-id="881b3-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-140">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-141">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-142">True</span><span class="sxs-lookup"><span data-stu-id="881b3-142">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-143">Is Indexed</span></span>             | <span data-ttu-id="881b3-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-144">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-145">In Global Catalog</span></span>      | <span data-ttu-id="881b3-146">True</span><span class="sxs-lookup"><span data-stu-id="881b3-146">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-148">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="881b3-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-149">Range-Lower</span></span>            | <span data-ttu-id="881b3-150">1</span><span class="sxs-lookup"><span data-stu-id="881b3-150">1</span></span>                                                                                                                       |
| <span data-ttu-id="881b3-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-151">Range-Upper</span></span>            | <span data-ttu-id="881b3-152">255</span><span class="sxs-lookup"><span data-stu-id="881b3-152">255</span></span>                                                                                                                     |
| <span data-ttu-id="881b3-153">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-153">Search-Flags</span></span>           | <span data-ttu-id="881b3-154">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-154">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="881b3-155">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-155">System-Flags</span></span>           | <span data-ttu-id="881b3-156">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-156">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="881b3-157">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-157">Classes used in</span></span>        | [<span data-ttu-id="881b3-158">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="881b3-158">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="881b3-159">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="881b3-159">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="881b3-160">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-160">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="881b3-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="881b3-161">Windows Server 2003</span></span>



| <span data-ttu-id="881b3-162">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-162">Entry</span></span> | <span data-ttu-id="881b3-163">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-163">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b3-164">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-164">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-165">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-165">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-166">System-Only</span></span>            | <span data-ttu-id="881b3-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-167">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-168">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-169">True</span><span class="sxs-lookup"><span data-stu-id="881b3-169">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-170">Is Indexed</span></span>             | <span data-ttu-id="881b3-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-171">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-172">In Global Catalog</span></span>      | <span data-ttu-id="881b3-173">True</span><span class="sxs-lookup"><span data-stu-id="881b3-173">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-175">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="881b3-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-176">Range-Lower</span></span>            | <span data-ttu-id="881b3-177">1</span><span class="sxs-lookup"><span data-stu-id="881b3-177">1</span></span>                                                                                                                       |
| <span data-ttu-id="881b3-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-178">Range-Upper</span></span>            | <span data-ttu-id="881b3-179">255</span><span class="sxs-lookup"><span data-stu-id="881b3-179">255</span></span>                                                                                                                     |
| <span data-ttu-id="881b3-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-180">Search-Flags</span></span>           | <span data-ttu-id="881b3-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-181">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="881b3-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-182">System-Flags</span></span>           | <span data-ttu-id="881b3-183">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-183">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="881b3-184">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-184">Classes used in</span></span>        | [<span data-ttu-id="881b3-185">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="881b3-185">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="881b3-186">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="881b3-186">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="881b3-187">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-187">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="adam"></a><span data-ttu-id="881b3-188">ADAM</span><span class="sxs-lookup"><span data-stu-id="881b3-188">ADAM</span></span>



| <span data-ttu-id="881b3-189">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-189">Entry</span></span> | <span data-ttu-id="881b3-190">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-190">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="881b3-191">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-191">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="881b3-192">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-192">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="881b3-193">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-193">System-Only</span></span>            | <span data-ttu-id="881b3-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-194">False</span></span>                                 |
| <span data-ttu-id="881b3-195">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-195">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-196">True</span><span class="sxs-lookup"><span data-stu-id="881b3-196">True</span></span>                                  |
| <span data-ttu-id="881b3-197">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-197">Is Indexed</span></span>             | <span data-ttu-id="881b3-198">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-198">False</span></span>                                 |
| <span data-ttu-id="881b3-199">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-199">In Global Catalog</span></span>      | <span data-ttu-id="881b3-200">True</span><span class="sxs-lookup"><span data-stu-id="881b3-200">True</span></span>                                  |
| <span data-ttu-id="881b3-201">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-201">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-202">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-202">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="881b3-203">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-203">Range-Lower</span></span>            | <span data-ttu-id="881b3-204">1</span><span class="sxs-lookup"><span data-stu-id="881b3-204">1</span></span>                                     |
| <span data-ttu-id="881b3-205">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-205">Range-Upper</span></span>            | <span data-ttu-id="881b3-206">255</span><span class="sxs-lookup"><span data-stu-id="881b3-206">255</span></span>                                   |
| <span data-ttu-id="881b3-207">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-207">Search-Flags</span></span>           | <span data-ttu-id="881b3-208">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-208">0x00000000</span></span>                            |
| <span data-ttu-id="881b3-209">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-209">System-Flags</span></span>           | <span data-ttu-id="881b3-210">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-210">0x00000012</span></span>                            |
| <span data-ttu-id="881b3-211">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-211">Classes used in</span></span>        | [<span data-ttu-id="881b3-212">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-212">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="881b3-213">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="881b3-213">Windows Server 2003 R2</span></span>



| <span data-ttu-id="881b3-214">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-214">Entry</span></span> | <span data-ttu-id="881b3-215">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-215">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b3-216">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-216">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-217">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-217">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-218">System-Only</span></span>            | <span data-ttu-id="881b3-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-219">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-220">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-220">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-221">True</span><span class="sxs-lookup"><span data-stu-id="881b3-221">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-222">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-222">Is Indexed</span></span>             | <span data-ttu-id="881b3-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-223">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-224">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-224">In Global Catalog</span></span>      | <span data-ttu-id="881b3-225">True</span><span class="sxs-lookup"><span data-stu-id="881b3-225">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-226">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-227">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-227">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="881b3-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-228">Range-Lower</span></span>            | <span data-ttu-id="881b3-229">1</span><span class="sxs-lookup"><span data-stu-id="881b3-229">1</span></span>                                                                                                                       |
| <span data-ttu-id="881b3-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-230">Range-Upper</span></span>            | <span data-ttu-id="881b3-231">255</span><span class="sxs-lookup"><span data-stu-id="881b3-231">255</span></span>                                                                                                                     |
| <span data-ttu-id="881b3-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-232">Search-Flags</span></span>           | <span data-ttu-id="881b3-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-233">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="881b3-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-234">System-Flags</span></span>           | <span data-ttu-id="881b3-235">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-235">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="881b3-236">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-236">Classes used in</span></span>        | [<span data-ttu-id="881b3-237">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="881b3-237">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="881b3-238">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="881b3-238">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="881b3-239">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-239">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="881b3-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="881b3-240">Windows Server 2008</span></span>



| <span data-ttu-id="881b3-241">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-241">Entry</span></span> | <span data-ttu-id="881b3-242">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-242">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b3-243">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-243">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-244">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-244">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-245">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-245">System-Only</span></span>            | <span data-ttu-id="881b3-246">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-246">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-247">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-247">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-248">True</span><span class="sxs-lookup"><span data-stu-id="881b3-248">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-249">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-249">Is Indexed</span></span>             | <span data-ttu-id="881b3-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-250">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-251">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-251">In Global Catalog</span></span>      | <span data-ttu-id="881b3-252">True</span><span class="sxs-lookup"><span data-stu-id="881b3-252">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-253">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-253">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-254">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-254">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="881b3-255">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-255">Range-Lower</span></span>            | <span data-ttu-id="881b3-256">1</span><span class="sxs-lookup"><span data-stu-id="881b3-256">1</span></span>                                                                                                                       |
| <span data-ttu-id="881b3-257">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-257">Range-Upper</span></span>            | <span data-ttu-id="881b3-258">255</span><span class="sxs-lookup"><span data-stu-id="881b3-258">255</span></span>                                                                                                                     |
| <span data-ttu-id="881b3-259">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-259">Search-Flags</span></span>           | <span data-ttu-id="881b3-260">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-260">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="881b3-261">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-261">System-Flags</span></span>           | <span data-ttu-id="881b3-262">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-262">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="881b3-263">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-263">Classes used in</span></span>        | [<span data-ttu-id="881b3-264">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="881b3-264">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="881b3-265">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="881b3-265">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="881b3-266">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-266">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="881b3-267">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="881b3-267">Windows Server 2008 R2</span></span>



| <span data-ttu-id="881b3-268">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-268">Entry</span></span> | <span data-ttu-id="881b3-269">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-269">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b3-270">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-270">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-271">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-271">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-272">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-272">System-Only</span></span>            | <span data-ttu-id="881b3-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-273">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-274">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-274">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-275">True</span><span class="sxs-lookup"><span data-stu-id="881b3-275">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-276">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-276">Is Indexed</span></span>             | <span data-ttu-id="881b3-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-277">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-278">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-278">In Global Catalog</span></span>      | <span data-ttu-id="881b3-279">True</span><span class="sxs-lookup"><span data-stu-id="881b3-279">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-280">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-280">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-281">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-281">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="881b3-282">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-282">Range-Lower</span></span>            | <span data-ttu-id="881b3-283">1</span><span class="sxs-lookup"><span data-stu-id="881b3-283">1</span></span>                                                                                                                       |
| <span data-ttu-id="881b3-284">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-284">Range-Upper</span></span>            | <span data-ttu-id="881b3-285">255</span><span class="sxs-lookup"><span data-stu-id="881b3-285">255</span></span>                                                                                                                     |
| <span data-ttu-id="881b3-286">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-286">Search-Flags</span></span>           | <span data-ttu-id="881b3-287">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-287">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="881b3-288">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-288">System-Flags</span></span>           | <span data-ttu-id="881b3-289">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-289">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="881b3-290">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-290">Classes used in</span></span>        | [<span data-ttu-id="881b3-291">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="881b3-291">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="881b3-292">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="881b3-292">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="881b3-293">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-293">**Domain**</span></span>](c-domain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="881b3-294">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="881b3-294">Windows Server 2012</span></span>



| <span data-ttu-id="881b3-295">Ввод</span><span class="sxs-lookup"><span data-stu-id="881b3-295">Entry</span></span> | <span data-ttu-id="881b3-296">Значение</span><span class="sxs-lookup"><span data-stu-id="881b3-296">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="881b3-297">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="881b3-297">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-298">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="881b3-298">MAPI-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="881b3-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="881b3-299">System-Only</span></span>            | <span data-ttu-id="881b3-300">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-300">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-301">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="881b3-301">Is-Single-Valued</span></span>       | <span data-ttu-id="881b3-302">True</span><span class="sxs-lookup"><span data-stu-id="881b3-302">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-303">Индексируется</span><span class="sxs-lookup"><span data-stu-id="881b3-303">Is Indexed</span></span>             | <span data-ttu-id="881b3-304">Неверно</span><span class="sxs-lookup"><span data-stu-id="881b3-304">False</span></span>                                                                                                                   |
| <span data-ttu-id="881b3-305">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="881b3-305">In Global Catalog</span></span>      | <span data-ttu-id="881b3-306">True</span><span class="sxs-lookup"><span data-stu-id="881b3-306">True</span></span>                                                                                                                    |
| <span data-ttu-id="881b3-307">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="881b3-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="881b3-308">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="881b3-308">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="881b3-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="881b3-309">Range-Lower</span></span>            | <span data-ttu-id="881b3-310">1</span><span class="sxs-lookup"><span data-stu-id="881b3-310">1</span></span>                                                                                                                       |
| <span data-ttu-id="881b3-311">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="881b3-311">Range-Upper</span></span>            | <span data-ttu-id="881b3-312">255</span><span class="sxs-lookup"><span data-stu-id="881b3-312">255</span></span>                                                                                                                     |
| <span data-ttu-id="881b3-313">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-313">Search-Flags</span></span>           | <span data-ttu-id="881b3-314">0x00000000</span><span class="sxs-lookup"><span data-stu-id="881b3-314">0x00000000</span></span>                                                                                                              |
| <span data-ttu-id="881b3-315">System-Flags</span><span class="sxs-lookup"><span data-stu-id="881b3-315">System-Flags</span></span>           | <span data-ttu-id="881b3-316">0x00000012</span><span class="sxs-lookup"><span data-stu-id="881b3-316">0x00000012</span></span>                                                                                                              |
| <span data-ttu-id="881b3-317">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="881b3-317">Classes used in</span></span>        | [<span data-ttu-id="881b3-318">**DNS-узел**</span><span class="sxs-lookup"><span data-stu-id="881b3-318">**Dns-Node**</span></span>](c-dnsnode.md)<br/> [<span data-ttu-id="881b3-319">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="881b3-319">**Dns-Zone**</span></span>](c-dnszone.md)<br/> [<span data-ttu-id="881b3-320">**Домен**</span><span class="sxs-lookup"><span data-stu-id="881b3-320">**Domain**</span></span>](c-domain.md)<br/> |



 

 





