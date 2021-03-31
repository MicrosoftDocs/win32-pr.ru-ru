---
title: Атрибут Proxy-Addresses
description: Адрес прокси-сервера — это адрес, по которому объект получателя Microsoft Exchange Server распознается в внешней почтовой системе. Адреса прокси-сервера необходимы для всех объектов получателей, таких как пользовательские получатели и списки рассылки.
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Proxy-Addresses
- Схема AD атрибута proxyAddresses
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893678"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="c7377-106">Атрибут Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="c7377-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="c7377-107">Адрес прокси-сервера — это адрес, по которому объект получателя Microsoft Exchange Server распознается в внешней почтовой системе.</span><span class="sxs-lookup"><span data-stu-id="c7377-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="c7377-108">Адреса прокси-сервера необходимы для всех объектов получателей, таких как пользовательские получатели и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="c7377-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="c7377-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-109">Entry</span></span> | <span data-ttu-id="c7377-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7377-111">CN</span><span class="sxs-lookup"><span data-stu-id="c7377-111">CN</span></span>                | <span data-ttu-id="c7377-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="c7377-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="c7377-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c7377-113">Ldap-Display-Name</span></span> | <span data-ttu-id="c7377-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="c7377-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="c7377-115">Размер</span><span class="sxs-lookup"><span data-stu-id="c7377-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="c7377-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c7377-116">Update Privilege</span></span>  | <span data-ttu-id="c7377-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="c7377-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="c7377-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c7377-118">Update Frequency</span></span>  | <span data-ttu-id="c7377-119">Создается библиотекой DLL, предоставляемой объектом Address-Type Directory при установке типа адреса.</span><span class="sxs-lookup"><span data-stu-id="c7377-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="c7377-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-120">Attribute-Id</span></span>      | <span data-ttu-id="c7377-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="c7377-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="c7377-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c7377-122">System-Id-Guid</span></span>    | <span data-ttu-id="c7377-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c7377-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="c7377-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7377-124">Syntax</span></span>            | [<span data-ttu-id="c7377-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="c7377-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="c7377-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c7377-126">Implementations</span></span>

-   [<span data-ttu-id="c7377-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c7377-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c7377-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c7377-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c7377-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="c7377-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="c7377-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c7377-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c7377-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c7377-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c7377-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c7377-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c7377-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c7377-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c7377-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7377-134">Windows 2000 Server</span></span>



| <span data-ttu-id="c7377-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-135">Entry</span></span> | <span data-ttu-id="c7377-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-138">MAPI-Id</span></span>                | <span data-ttu-id="c7377-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-139">0x800F</span></span>                          |
| <span data-ttu-id="c7377-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-140">System-Only</span></span>            | <span data-ttu-id="c7377-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-141">False</span></span>                           |
| <span data-ttu-id="c7377-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-142">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-143">False</span></span>                           |
| <span data-ttu-id="c7377-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-144">Is Indexed</span></span>             | <span data-ttu-id="c7377-145">True</span><span class="sxs-lookup"><span data-stu-id="c7377-145">True</span></span>                            |
| <span data-ttu-id="c7377-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-146">In Global Catalog</span></span>      | <span data-ttu-id="c7377-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-147">False</span></span>                           |
| <span data-ttu-id="c7377-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-150">Range-Lower</span></span>            | <span data-ttu-id="c7377-151">1</span><span class="sxs-lookup"><span data-stu-id="c7377-151">1</span></span>                               |
| <span data-ttu-id="c7377-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-152">Range-Upper</span></span>            | <span data-ttu-id="c7377-153">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-153">1123</span></span>                            |
| <span data-ttu-id="c7377-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-154">Search-Flags</span></span>           | <span data-ttu-id="c7377-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-155">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-156">System-Flags</span></span>           | <span data-ttu-id="c7377-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-157">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-158">Classes used in</span></span>        | [<span data-ttu-id="c7377-159">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c7377-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c7377-160">Windows Server 2003</span></span>



| <span data-ttu-id="c7377-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-161">Entry</span></span> | <span data-ttu-id="c7377-162">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-164">MAPI-Id</span></span>                | <span data-ttu-id="c7377-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-165">0x800F</span></span>                          |
| <span data-ttu-id="c7377-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-166">System-Only</span></span>            | <span data-ttu-id="c7377-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-167">False</span></span>                           |
| <span data-ttu-id="c7377-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-168">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-169">False</span></span>                           |
| <span data-ttu-id="c7377-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-170">Is Indexed</span></span>             | <span data-ttu-id="c7377-171">True</span><span class="sxs-lookup"><span data-stu-id="c7377-171">True</span></span>                            |
| <span data-ttu-id="c7377-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-172">In Global Catalog</span></span>      | <span data-ttu-id="c7377-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-173">False</span></span>                           |
| <span data-ttu-id="c7377-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-176">Range-Lower</span></span>            | <span data-ttu-id="c7377-177">1</span><span class="sxs-lookup"><span data-stu-id="c7377-177">1</span></span>                               |
| <span data-ttu-id="c7377-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-178">Range-Upper</span></span>            | <span data-ttu-id="c7377-179">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-179">1123</span></span>                            |
| <span data-ttu-id="c7377-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-180">Search-Flags</span></span>           | <span data-ttu-id="c7377-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-181">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-182">System-Flags</span></span>           | <span data-ttu-id="c7377-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-183">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-184">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-184">Classes used in</span></span>        | [<span data-ttu-id="c7377-185">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="c7377-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="c7377-186">ADAM</span></span>



| <span data-ttu-id="c7377-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-187">Entry</span></span> | <span data-ttu-id="c7377-188">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-190">MAPI-Id</span></span>                | <span data-ttu-id="c7377-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-191">0x800F</span></span>                          |
| <span data-ttu-id="c7377-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-192">System-Only</span></span>            | <span data-ttu-id="c7377-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-193">False</span></span>                           |
| <span data-ttu-id="c7377-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-194">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-195">False</span></span>                           |
| <span data-ttu-id="c7377-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-196">Is Indexed</span></span>             | <span data-ttu-id="c7377-197">True</span><span class="sxs-lookup"><span data-stu-id="c7377-197">True</span></span>                            |
| <span data-ttu-id="c7377-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-198">In Global Catalog</span></span>      | <span data-ttu-id="c7377-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-199">False</span></span>                           |
| <span data-ttu-id="c7377-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-202">Range-Lower</span></span>            | <span data-ttu-id="c7377-203">1</span><span class="sxs-lookup"><span data-stu-id="c7377-203">1</span></span>                               |
| <span data-ttu-id="c7377-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-204">Range-Upper</span></span>            | <span data-ttu-id="c7377-205">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-205">1123</span></span>                            |
| <span data-ttu-id="c7377-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-206">Search-Flags</span></span>           | <span data-ttu-id="c7377-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-207">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-208">System-Flags</span></span>           | <span data-ttu-id="c7377-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-209">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-210">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-210">Classes used in</span></span>        | [<span data-ttu-id="c7377-211">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c7377-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c7377-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c7377-213">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-213">Entry</span></span> | <span data-ttu-id="c7377-214">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-215">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-216">MAPI-Id</span></span>                | <span data-ttu-id="c7377-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-217">0x800F</span></span>                          |
| <span data-ttu-id="c7377-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-218">System-Only</span></span>            | <span data-ttu-id="c7377-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-219">False</span></span>                           |
| <span data-ttu-id="c7377-220">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-220">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-221">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-221">False</span></span>                           |
| <span data-ttu-id="c7377-222">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-222">Is Indexed</span></span>             | <span data-ttu-id="c7377-223">True</span><span class="sxs-lookup"><span data-stu-id="c7377-223">True</span></span>                            |
| <span data-ttu-id="c7377-224">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-224">In Global Catalog</span></span>      | <span data-ttu-id="c7377-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-225">False</span></span>                           |
| <span data-ttu-id="c7377-226">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-227">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-228">Range-Lower</span></span>            | <span data-ttu-id="c7377-229">1</span><span class="sxs-lookup"><span data-stu-id="c7377-229">1</span></span>                               |
| <span data-ttu-id="c7377-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-230">Range-Upper</span></span>            | <span data-ttu-id="c7377-231">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-231">1123</span></span>                            |
| <span data-ttu-id="c7377-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-232">Search-Flags</span></span>           | <span data-ttu-id="c7377-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-233">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-234">System-Flags</span></span>           | <span data-ttu-id="c7377-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-235">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-236">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-236">Classes used in</span></span>        | [<span data-ttu-id="c7377-237">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c7377-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7377-238">Windows Server 2008</span></span>



| <span data-ttu-id="c7377-239">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-239">Entry</span></span> | <span data-ttu-id="c7377-240">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-241">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-242">MAPI-Id</span></span>                | <span data-ttu-id="c7377-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-243">0x800F</span></span>                          |
| <span data-ttu-id="c7377-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-244">System-Only</span></span>            | <span data-ttu-id="c7377-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-245">False</span></span>                           |
| <span data-ttu-id="c7377-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-246">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-247">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-247">False</span></span>                           |
| <span data-ttu-id="c7377-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-248">Is Indexed</span></span>             | <span data-ttu-id="c7377-249">True</span><span class="sxs-lookup"><span data-stu-id="c7377-249">True</span></span>                            |
| <span data-ttu-id="c7377-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-250">In Global Catalog</span></span>      | <span data-ttu-id="c7377-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-251">False</span></span>                           |
| <span data-ttu-id="c7377-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-254">Range-Lower</span></span>            | <span data-ttu-id="c7377-255">1</span><span class="sxs-lookup"><span data-stu-id="c7377-255">1</span></span>                               |
| <span data-ttu-id="c7377-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-256">Range-Upper</span></span>            | <span data-ttu-id="c7377-257">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-257">1123</span></span>                            |
| <span data-ttu-id="c7377-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-258">Search-Flags</span></span>           | <span data-ttu-id="c7377-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-259">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-260">System-Flags</span></span>           | <span data-ttu-id="c7377-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-261">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-262">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-262">Classes used in</span></span>        | [<span data-ttu-id="c7377-263">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c7377-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c7377-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c7377-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-265">Entry</span></span> | <span data-ttu-id="c7377-266">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-267">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-268">MAPI-Id</span></span>                | <span data-ttu-id="c7377-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-269">0x800F</span></span>                          |
| <span data-ttu-id="c7377-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-270">System-Only</span></span>            | <span data-ttu-id="c7377-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-271">False</span></span>                           |
| <span data-ttu-id="c7377-272">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-272">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-273">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-273">False</span></span>                           |
| <span data-ttu-id="c7377-274">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-274">Is Indexed</span></span>             | <span data-ttu-id="c7377-275">True</span><span class="sxs-lookup"><span data-stu-id="c7377-275">True</span></span>                            |
| <span data-ttu-id="c7377-276">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-276">In Global Catalog</span></span>      | <span data-ttu-id="c7377-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-277">False</span></span>                           |
| <span data-ttu-id="c7377-278">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-279">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-280">Range-Lower</span></span>            | <span data-ttu-id="c7377-281">1</span><span class="sxs-lookup"><span data-stu-id="c7377-281">1</span></span>                               |
| <span data-ttu-id="c7377-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-282">Range-Upper</span></span>            | <span data-ttu-id="c7377-283">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-283">1123</span></span>                            |
| <span data-ttu-id="c7377-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-284">Search-Flags</span></span>           | <span data-ttu-id="c7377-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-285">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-286">System-Flags</span></span>           | <span data-ttu-id="c7377-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-287">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-288">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-288">Classes used in</span></span>        | [<span data-ttu-id="c7377-289">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c7377-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7377-290">Windows Server 2012</span></span>



| <span data-ttu-id="c7377-291">Ввод</span><span class="sxs-lookup"><span data-stu-id="c7377-291">Entry</span></span> | <span data-ttu-id="c7377-292">Значение</span><span class="sxs-lookup"><span data-stu-id="c7377-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="c7377-293">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c7377-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="c7377-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c7377-294">MAPI-Id</span></span>                | <span data-ttu-id="c7377-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="c7377-295">0x800F</span></span>                          |
| <span data-ttu-id="c7377-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="c7377-296">System-Only</span></span>            | <span data-ttu-id="c7377-297">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-297">False</span></span>                           |
| <span data-ttu-id="c7377-298">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c7377-298">Is-Single-Valued</span></span>       | <span data-ttu-id="c7377-299">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-299">False</span></span>                           |
| <span data-ttu-id="c7377-300">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c7377-300">Is Indexed</span></span>             | <span data-ttu-id="c7377-301">True</span><span class="sxs-lookup"><span data-stu-id="c7377-301">True</span></span>                            |
| <span data-ttu-id="c7377-302">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c7377-302">In Global Catalog</span></span>      | <span data-ttu-id="c7377-303">Неверно</span><span class="sxs-lookup"><span data-stu-id="c7377-303">False</span></span>                           |
| <span data-ttu-id="c7377-304">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c7377-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="c7377-305">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c7377-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="c7377-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c7377-306">Range-Lower</span></span>            | <span data-ttu-id="c7377-307">1</span><span class="sxs-lookup"><span data-stu-id="c7377-307">1</span></span>                               |
| <span data-ttu-id="c7377-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c7377-308">Range-Upper</span></span>            | <span data-ttu-id="c7377-309">1123</span><span class="sxs-lookup"><span data-stu-id="c7377-309">1123</span></span>                            |
| <span data-ttu-id="c7377-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-310">Search-Flags</span></span>           | <span data-ttu-id="c7377-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="c7377-311">0x00000005</span></span>                      |
| <span data-ttu-id="c7377-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c7377-312">System-Flags</span></span>           | <span data-ttu-id="c7377-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c7377-313">0x00000010</span></span>                      |
| <span data-ttu-id="c7377-314">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c7377-314">Classes used in</span></span>        | [<span data-ttu-id="c7377-315">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="c7377-315">**Top**</span></span>](c-top.md)<br/> |



 

 





