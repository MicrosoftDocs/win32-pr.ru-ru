---
title: Can-Upgrade-атрибут скрипта
description: Этот атрибут хранит список пакетов приложений, которые могут быть обновлены, или которые могут обновить этот пакет приложения.
ms.assetid: 95dea9c7-dbbd-42fb-ab32-6b89490aa5d6
ms.tgt_platform: multiple
keywords:
- Can-Upgrade — схема AD атрибута Script
- Схема AD атрибута Канупградескрипт
topic_type:
- apiref
api_name:
- Can-Upgrade-Script
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e5b90c45d124a8647dd5d3a0af9c4a2ca6c4f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655536"
---
# <a name="can-upgrade-script-attribute"></a><span data-ttu-id="f9bcb-105">Can-Upgrade-атрибут скрипта</span><span class="sxs-lookup"><span data-stu-id="f9bcb-105">Can-Upgrade-Script attribute</span></span>

<span data-ttu-id="f9bcb-106">Этот атрибут хранит список пакетов приложений, которые могут быть обновлены, или которые могут обновить этот пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="f9bcb-106">This attribute stores the list of application packages that can be upgraded by or which can upgrade this application package.</span></span>



| <span data-ttu-id="f9bcb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-107">Entry</span></span> | <span data-ttu-id="f9bcb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="f9bcb-109">CN</span><span class="sxs-lookup"><span data-stu-id="f9bcb-109">CN</span></span>                | <span data-ttu-id="f9bcb-110">Can-Upgrade-Скрипт</span><span class="sxs-lookup"><span data-stu-id="f9bcb-110">Can-Upgrade-Script</span></span>                          |
| <span data-ttu-id="f9bcb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="f9bcb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f9bcb-112">канупградескрипт</span><span class="sxs-lookup"><span data-stu-id="f9bcb-112">canUpgradeScript</span></span>                            |
| <span data-ttu-id="f9bcb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="f9bcb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="f9bcb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="f9bcb-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="f9bcb-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="f9bcb-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="f9bcb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-116">Attribute-Id</span></span>      | <span data-ttu-id="f9bcb-117">1.2.840.113556.1.4.815</span><span class="sxs-lookup"><span data-stu-id="f9bcb-117">1.2.840.113556.1.4.815</span></span>                      |
| <span data-ttu-id="f9bcb-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="f9bcb-118">System-Id-Guid</span></span>    | <span data-ttu-id="f9bcb-119">d9e18314-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="f9bcb-119">d9e18314-8939-11d1-aebc-0000f80367c1</span></span>        |
| <span data-ttu-id="f9bcb-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9bcb-120">Syntax</span></span>            | [<span data-ttu-id="f9bcb-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="f9bcb-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="f9bcb-122">Implementations</span></span>

-   [<span data-ttu-id="f9bcb-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f9bcb-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f9bcb-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f9bcb-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f9bcb-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f9bcb-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f9bcb-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f9bcb-129">Windows 2000 Server</span></span>



| <span data-ttu-id="f9bcb-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-130">Entry</span></span> | <span data-ttu-id="f9bcb-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f9bcb-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f9bcb-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9bcb-134">System-Only</span></span>            | <span data-ttu-id="f9bcb-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-135">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f9bcb-136">Is-Single-Valued</span></span>       | <span data-ttu-id="f9bcb-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-137">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f9bcb-138">Is Indexed</span></span>             | <span data-ttu-id="f9bcb-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-139">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f9bcb-140">In Global Catalog</span></span>      | <span data-ttu-id="f9bcb-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-141">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f9bcb-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9bcb-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9bcb-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f9bcb-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9bcb-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9bcb-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-146">Search-Flags</span></span>           | <span data-ttu-id="f9bcb-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="f9bcb-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-148">System-Flags</span></span>           | <span data-ttu-id="f9bcb-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9bcb-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="f9bcb-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f9bcb-150">Classes used in</span></span>        | [<span data-ttu-id="f9bcb-151">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f9bcb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9bcb-152">Windows Server 2003</span></span>



| <span data-ttu-id="f9bcb-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-153">Entry</span></span> | <span data-ttu-id="f9bcb-154">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f9bcb-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f9bcb-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9bcb-157">System-Only</span></span>            | <span data-ttu-id="f9bcb-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-158">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f9bcb-159">Is-Single-Valued</span></span>       | <span data-ttu-id="f9bcb-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-160">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f9bcb-161">Is Indexed</span></span>             | <span data-ttu-id="f9bcb-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-162">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f9bcb-163">In Global Catalog</span></span>      | <span data-ttu-id="f9bcb-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-164">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f9bcb-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9bcb-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9bcb-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f9bcb-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9bcb-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9bcb-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-169">Search-Flags</span></span>           | <span data-ttu-id="f9bcb-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="f9bcb-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-171">System-Flags</span></span>           | <span data-ttu-id="f9bcb-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9bcb-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="f9bcb-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f9bcb-173">Classes used in</span></span>        | [<span data-ttu-id="f9bcb-174">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f9bcb-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f9bcb-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f9bcb-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-176">Entry</span></span> | <span data-ttu-id="f9bcb-177">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f9bcb-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f9bcb-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9bcb-180">System-Only</span></span>            | <span data-ttu-id="f9bcb-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-181">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f9bcb-182">Is-Single-Valued</span></span>       | <span data-ttu-id="f9bcb-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-183">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f9bcb-184">Is Indexed</span></span>             | <span data-ttu-id="f9bcb-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-185">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f9bcb-186">In Global Catalog</span></span>      | <span data-ttu-id="f9bcb-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-187">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f9bcb-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9bcb-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9bcb-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f9bcb-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9bcb-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9bcb-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-192">Search-Flags</span></span>           | <span data-ttu-id="f9bcb-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="f9bcb-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-194">System-Flags</span></span>           | <span data-ttu-id="f9bcb-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9bcb-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="f9bcb-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f9bcb-196">Classes used in</span></span>        | [<span data-ttu-id="f9bcb-197">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f9bcb-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9bcb-198">Windows Server 2008</span></span>



| <span data-ttu-id="f9bcb-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-199">Entry</span></span> | <span data-ttu-id="f9bcb-200">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f9bcb-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f9bcb-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9bcb-203">System-Only</span></span>            | <span data-ttu-id="f9bcb-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-204">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f9bcb-205">Is-Single-Valued</span></span>       | <span data-ttu-id="f9bcb-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-206">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f9bcb-207">Is Indexed</span></span>             | <span data-ttu-id="f9bcb-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-208">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f9bcb-209">In Global Catalog</span></span>      | <span data-ttu-id="f9bcb-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-210">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f9bcb-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9bcb-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9bcb-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f9bcb-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9bcb-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9bcb-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-215">Search-Flags</span></span>           | <span data-ttu-id="f9bcb-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="f9bcb-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-217">System-Flags</span></span>           | <span data-ttu-id="f9bcb-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9bcb-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="f9bcb-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f9bcb-219">Classes used in</span></span>        | [<span data-ttu-id="f9bcb-220">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f9bcb-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9bcb-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f9bcb-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-222">Entry</span></span> | <span data-ttu-id="f9bcb-223">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f9bcb-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f9bcb-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9bcb-226">System-Only</span></span>            | <span data-ttu-id="f9bcb-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-227">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f9bcb-228">Is-Single-Valued</span></span>       | <span data-ttu-id="f9bcb-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-229">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f9bcb-230">Is Indexed</span></span>             | <span data-ttu-id="f9bcb-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-231">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f9bcb-232">In Global Catalog</span></span>      | <span data-ttu-id="f9bcb-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-233">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f9bcb-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9bcb-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9bcb-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f9bcb-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9bcb-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9bcb-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-238">Search-Flags</span></span>           | <span data-ttu-id="f9bcb-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="f9bcb-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-240">System-Flags</span></span>           | <span data-ttu-id="f9bcb-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9bcb-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="f9bcb-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f9bcb-242">Classes used in</span></span>        | [<span data-ttu-id="f9bcb-243">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f9bcb-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9bcb-244">Windows Server 2012</span></span>



| <span data-ttu-id="f9bcb-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="f9bcb-245">Entry</span></span> | <span data-ttu-id="f9bcb-246">Значение</span><span class="sxs-lookup"><span data-stu-id="f9bcb-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="f9bcb-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="f9bcb-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f9bcb-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="f9bcb-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="f9bcb-249">System-Only</span></span>            | <span data-ttu-id="f9bcb-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-250">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="f9bcb-251">Is-Single-Valued</span></span>       | <span data-ttu-id="f9bcb-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-252">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="f9bcb-253">Is Indexed</span></span>             | <span data-ttu-id="f9bcb-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-254">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="f9bcb-255">In Global Catalog</span></span>      | <span data-ttu-id="f9bcb-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="f9bcb-256">False</span></span>                                                            |
| <span data-ttu-id="f9bcb-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="f9bcb-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="f9bcb-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="f9bcb-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="f9bcb-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f9bcb-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f9bcb-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="f9bcb-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-261">Search-Flags</span></span>           | <span data-ttu-id="f9bcb-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f9bcb-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="f9bcb-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f9bcb-263">System-Flags</span></span>           | <span data-ttu-id="f9bcb-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f9bcb-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="f9bcb-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="f9bcb-265">Classes used in</span></span>        | [<span data-ttu-id="f9bcb-266">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="f9bcb-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





