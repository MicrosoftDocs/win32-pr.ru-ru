---
title: Атрибут ms-DS-Other-Settings
description: Этот атрибут с несколькими значениями используется для хранения любого настраиваемого параметра для DS, хранимого в формате значения имени.
ms.assetid: e7d17c8e-6264-43d1-9010-9d589f93a086
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Other-Settings
- msDS — схема AD атрибутов других параметров
topic_type:
- apiref
api_name:
- ms-DS-Other-Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3699ac7983f33730cb73bb0f1eab0c13e72cbce
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893498"
---
# <a name="ms-ds-other-settings-attribute"></a><span data-ttu-id="27380-105">Атрибут ms-DS-Other-Settings</span><span class="sxs-lookup"><span data-stu-id="27380-105">ms-DS-Other-Settings attribute</span></span>

<span data-ttu-id="27380-106">Этот атрибут с несколькими значениями используется для хранения любых настраиваемых параметров для DS, хранимых в формате NAME = VALUE.</span><span class="sxs-lookup"><span data-stu-id="27380-106">This multiple-valued attribute is used to store any configurable setting for the DS stored in the NAME=VALUE format.</span></span>



| <span data-ttu-id="27380-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-107">Entry</span></span> | <span data-ttu-id="27380-108">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="27380-109">CN</span><span class="sxs-lookup"><span data-stu-id="27380-109">CN</span></span>                | <span data-ttu-id="27380-110">MS-DS-Other-Settings</span><span class="sxs-lookup"><span data-stu-id="27380-110">ms-DS-Other-Settings</span></span>                        |
| <span data-ttu-id="27380-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="27380-111">Ldap-Display-Name</span></span> | <span data-ttu-id="27380-112">msDS-Other-Settings</span><span class="sxs-lookup"><span data-stu-id="27380-112">msDS-Other-Settings</span></span>                         |
| <span data-ttu-id="27380-113">Размер</span><span class="sxs-lookup"><span data-stu-id="27380-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="27380-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="27380-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="27380-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="27380-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="27380-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="27380-116">Attribute-Id</span></span>      | <span data-ttu-id="27380-117">1.2.840.113556.1.4.1621</span><span class="sxs-lookup"><span data-stu-id="27380-117">1.2.840.113556.1.4.1621</span></span>                     |
| <span data-ttu-id="27380-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="27380-118">System-Id-Guid</span></span>    | <span data-ttu-id="27380-119">79d2f34c-9d7d-42bb-838f-866b3e4400e2</span><span class="sxs-lookup"><span data-stu-id="27380-119">79d2f34c-9d7d-42bb-838f-866b3e4400e2</span></span>        |
| <span data-ttu-id="27380-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27380-120">Syntax</span></span>            | [<span data-ttu-id="27380-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="27380-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="27380-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="27380-122">Implementations</span></span>

-   [<span data-ttu-id="27380-123">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="27380-123">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="27380-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="27380-124">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="27380-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="27380-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="27380-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="27380-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="27380-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="27380-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="27380-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="27380-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="27380-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27380-129">Windows Server 2003</span></span>



| <span data-ttu-id="27380-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-130">Entry</span></span> | <span data-ttu-id="27380-131">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-131">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27380-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27380-132">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27380-133">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="27380-134">System-Only</span></span>            | <span data-ttu-id="27380-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-135">False</span></span>                                            |
| <span data-ttu-id="27380-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27380-136">Is-Single-Valued</span></span>       | <span data-ttu-id="27380-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-137">False</span></span>                                            |
| <span data-ttu-id="27380-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27380-138">Is Indexed</span></span>             | <span data-ttu-id="27380-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-139">False</span></span>                                            |
| <span data-ttu-id="27380-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27380-140">In Global Catalog</span></span>      | <span data-ttu-id="27380-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-141">False</span></span>                                            |
| <span data-ttu-id="27380-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27380-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="27380-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27380-143">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27380-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27380-144">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27380-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27380-145">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27380-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-146">Search-Flags</span></span>           | <span data-ttu-id="27380-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27380-147">0x00000000</span></span>                                       |
| <span data-ttu-id="27380-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-148">System-Flags</span></span>           | <span data-ttu-id="27380-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27380-149">0x00000010</span></span>                                       |
| <span data-ttu-id="27380-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27380-150">Classes used in</span></span>        | [<span data-ttu-id="27380-151">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="27380-151">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="adam"></a><span data-ttu-id="27380-152">ADAM</span><span class="sxs-lookup"><span data-stu-id="27380-152">ADAM</span></span>



| <span data-ttu-id="27380-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-153">Entry</span></span> | <span data-ttu-id="27380-154">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-154">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27380-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27380-155">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27380-156">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="27380-157">System-Only</span></span>            | <span data-ttu-id="27380-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-158">False</span></span>                                            |
| <span data-ttu-id="27380-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27380-159">Is-Single-Valued</span></span>       | <span data-ttu-id="27380-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-160">False</span></span>                                            |
| <span data-ttu-id="27380-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27380-161">Is Indexed</span></span>             | <span data-ttu-id="27380-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-162">False</span></span>                                            |
| <span data-ttu-id="27380-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27380-163">In Global Catalog</span></span>      | <span data-ttu-id="27380-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-164">False</span></span>                                            |
| <span data-ttu-id="27380-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27380-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="27380-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27380-166">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27380-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27380-167">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27380-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27380-168">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27380-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-169">Search-Flags</span></span>           | <span data-ttu-id="27380-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27380-170">0x00000000</span></span>                                       |
| <span data-ttu-id="27380-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-171">System-Flags</span></span>           | <span data-ttu-id="27380-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27380-172">0x00000010</span></span>                                       |
| <span data-ttu-id="27380-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27380-173">Classes used in</span></span>        | [<span data-ttu-id="27380-174">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="27380-174">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="27380-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="27380-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="27380-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-176">Entry</span></span> | <span data-ttu-id="27380-177">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-177">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27380-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27380-178">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27380-179">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="27380-180">System-Only</span></span>            | <span data-ttu-id="27380-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-181">False</span></span>                                            |
| <span data-ttu-id="27380-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27380-182">Is-Single-Valued</span></span>       | <span data-ttu-id="27380-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-183">False</span></span>                                            |
| <span data-ttu-id="27380-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27380-184">Is Indexed</span></span>             | <span data-ttu-id="27380-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-185">False</span></span>                                            |
| <span data-ttu-id="27380-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27380-186">In Global Catalog</span></span>      | <span data-ttu-id="27380-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-187">False</span></span>                                            |
| <span data-ttu-id="27380-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27380-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="27380-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27380-189">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27380-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27380-190">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27380-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27380-191">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27380-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-192">Search-Flags</span></span>           | <span data-ttu-id="27380-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27380-193">0x00000000</span></span>                                       |
| <span data-ttu-id="27380-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-194">System-Flags</span></span>           | <span data-ttu-id="27380-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27380-195">0x00000010</span></span>                                       |
| <span data-ttu-id="27380-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27380-196">Classes used in</span></span>        | [<span data-ttu-id="27380-197">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="27380-197">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="27380-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27380-198">Windows Server 2008</span></span>



| <span data-ttu-id="27380-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-199">Entry</span></span> | <span data-ttu-id="27380-200">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-200">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27380-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27380-201">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27380-202">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="27380-203">System-Only</span></span>            | <span data-ttu-id="27380-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-204">False</span></span>                                            |
| <span data-ttu-id="27380-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27380-205">Is-Single-Valued</span></span>       | <span data-ttu-id="27380-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-206">False</span></span>                                            |
| <span data-ttu-id="27380-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27380-207">Is Indexed</span></span>             | <span data-ttu-id="27380-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-208">False</span></span>                                            |
| <span data-ttu-id="27380-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27380-209">In Global Catalog</span></span>      | <span data-ttu-id="27380-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-210">False</span></span>                                            |
| <span data-ttu-id="27380-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27380-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="27380-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27380-212">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27380-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27380-213">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27380-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27380-214">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27380-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-215">Search-Flags</span></span>           | <span data-ttu-id="27380-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27380-216">0x00000000</span></span>                                       |
| <span data-ttu-id="27380-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-217">System-Flags</span></span>           | <span data-ttu-id="27380-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27380-218">0x00000010</span></span>                                       |
| <span data-ttu-id="27380-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27380-219">Classes used in</span></span>        | [<span data-ttu-id="27380-220">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="27380-220">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="27380-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27380-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="27380-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-222">Entry</span></span> | <span data-ttu-id="27380-223">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-223">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27380-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27380-224">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27380-225">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="27380-226">System-Only</span></span>            | <span data-ttu-id="27380-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-227">False</span></span>                                            |
| <span data-ttu-id="27380-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27380-228">Is-Single-Valued</span></span>       | <span data-ttu-id="27380-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-229">False</span></span>                                            |
| <span data-ttu-id="27380-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27380-230">Is Indexed</span></span>             | <span data-ttu-id="27380-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-231">False</span></span>                                            |
| <span data-ttu-id="27380-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27380-232">In Global Catalog</span></span>      | <span data-ttu-id="27380-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-233">False</span></span>                                            |
| <span data-ttu-id="27380-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27380-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="27380-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27380-235">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27380-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27380-236">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27380-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27380-237">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27380-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-238">Search-Flags</span></span>           | <span data-ttu-id="27380-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27380-239">0x00000000</span></span>                                       |
| <span data-ttu-id="27380-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-240">System-Flags</span></span>           | <span data-ttu-id="27380-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27380-241">0x00000010</span></span>                                       |
| <span data-ttu-id="27380-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27380-242">Classes used in</span></span>        | [<span data-ttu-id="27380-243">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="27380-243">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="27380-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27380-244">Windows Server 2012</span></span>



| <span data-ttu-id="27380-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="27380-245">Entry</span></span> | <span data-ttu-id="27380-246">Значение</span><span class="sxs-lookup"><span data-stu-id="27380-246">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="27380-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="27380-247">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="27380-248">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="27380-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="27380-249">System-Only</span></span>            | <span data-ttu-id="27380-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-250">False</span></span>                                            |
| <span data-ttu-id="27380-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="27380-251">Is-Single-Valued</span></span>       | <span data-ttu-id="27380-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-252">False</span></span>                                            |
| <span data-ttu-id="27380-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="27380-253">Is Indexed</span></span>             | <span data-ttu-id="27380-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-254">False</span></span>                                            |
| <span data-ttu-id="27380-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="27380-255">In Global Catalog</span></span>      | <span data-ttu-id="27380-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="27380-256">False</span></span>                                            |
| <span data-ttu-id="27380-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="27380-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="27380-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="27380-258">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="27380-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="27380-259">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="27380-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="27380-260">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="27380-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-261">Search-Flags</span></span>           | <span data-ttu-id="27380-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="27380-262">0x00000000</span></span>                                       |
| <span data-ttu-id="27380-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="27380-263">System-Flags</span></span>           | <span data-ttu-id="27380-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="27380-264">0x00000010</span></span>                                       |
| <span data-ttu-id="27380-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="27380-265">Classes used in</span></span>        | [<span data-ttu-id="27380-266">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="27380-266">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





