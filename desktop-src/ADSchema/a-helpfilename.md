---
title: Help-File-Name, атрибут
description: Этот атрибут использовался для Exchange 4,0. Он содержал имя, которое должно использоваться для файла, когда поставщик загрузил данные справки на клиентский компьютер. Он не используется для других версий Exchange.
ms.assetid: 3383b953-8a5c-4dfd-9d06-c35d29d6ea2d
ms.tgt_platform: multiple
keywords:
- Help-имя файла-схема атрибута AD
- Схема AD атрибута Хелпфиленаме
topic_type:
- apiref
api_name:
- Help-File-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e049e34fe43cb17314f8483a2a77bd680a4e7fa
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893594"
---
# <a name="help-file-name-attribute"></a><span data-ttu-id="d0719-107">Help-File-Name, атрибут</span><span class="sxs-lookup"><span data-stu-id="d0719-107">Help-File-Name attribute</span></span>

<span data-ttu-id="d0719-108">Этот атрибут использовался для Exchange 4,0.</span><span class="sxs-lookup"><span data-stu-id="d0719-108">This attribute was used for Exchange 4.0.</span></span> <span data-ttu-id="d0719-109">Он содержал имя, которое должно использоваться для файла, когда поставщик загрузил данные справки на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="d0719-109">It contained the name that should be used for the file when the provider downloaded help data to a client computer.</span></span> <span data-ttu-id="d0719-110">Он не используется для других версий Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0719-110">It is not used for any other versions of Exchange.</span></span>



| <span data-ttu-id="d0719-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-111">Entry</span></span> | <span data-ttu-id="d0719-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-112">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="d0719-113">CN</span><span class="sxs-lookup"><span data-stu-id="d0719-113">CN</span></span>                | <span data-ttu-id="d0719-114">Help-File-Name</span><span class="sxs-lookup"><span data-stu-id="d0719-114">Help-File-Name</span></span>                              |
| <span data-ttu-id="d0719-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="d0719-115">Ldap-Display-Name</span></span> | <span data-ttu-id="d0719-116">хелпфиленаме</span><span class="sxs-lookup"><span data-stu-id="d0719-116">helpFileName</span></span>                                |
| <span data-ttu-id="d0719-117">Размер</span><span class="sxs-lookup"><span data-stu-id="d0719-117">Size</span></span>              | \-                                          |
| <span data-ttu-id="d0719-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="d0719-118">Update Privilege</span></span>  | <span data-ttu-id="d0719-119">Используется системой.</span><span class="sxs-lookup"><span data-stu-id="d0719-119">This is used by the system.</span></span>                 |
| <span data-ttu-id="d0719-120">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="d0719-120">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="d0719-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-121">Attribute-Id</span></span>      | <span data-ttu-id="d0719-122">1.2.840.113556.1.2.327</span><span class="sxs-lookup"><span data-stu-id="d0719-122">1.2.840.113556.1.2.327</span></span>                      |
| <span data-ttu-id="d0719-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="d0719-123">System-Id-Guid</span></span>    | <span data-ttu-id="d0719-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span><span class="sxs-lookup"><span data-stu-id="d0719-124">5fd424a9-1262-11d0-a060-00aa006c33ed</span></span>        |
| <span data-ttu-id="d0719-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0719-125">Syntax</span></span>            | [<span data-ttu-id="d0719-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="d0719-126">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="d0719-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="d0719-127">Implementations</span></span>

-   [<span data-ttu-id="d0719-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d0719-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d0719-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d0719-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d0719-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d0719-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d0719-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d0719-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d0719-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d0719-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d0719-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d0719-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d0719-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0719-134">Windows 2000 Server</span></span>



| <span data-ttu-id="d0719-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-135">Entry</span></span> | <span data-ttu-id="d0719-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-136">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0719-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0719-137">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d0719-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-138">MAPI-Id</span></span>                | <span data-ttu-id="d0719-139">0x803B</span><span class="sxs-lookup"><span data-stu-id="d0719-139">0x803B</span></span>                                                   |
| <span data-ttu-id="d0719-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0719-140">System-Only</span></span>            | <span data-ttu-id="d0719-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-141">False</span></span>                                                    |
| <span data-ttu-id="d0719-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0719-142">Is-Single-Valued</span></span>       | <span data-ttu-id="d0719-143">True</span><span class="sxs-lookup"><span data-stu-id="d0719-143">True</span></span>                                                     |
| <span data-ttu-id="d0719-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0719-144">Is Indexed</span></span>             | <span data-ttu-id="d0719-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-145">False</span></span>                                                    |
| <span data-ttu-id="d0719-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0719-146">In Global Catalog</span></span>      | <span data-ttu-id="d0719-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-147">False</span></span>                                                    |
| <span data-ttu-id="d0719-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0719-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0719-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0719-149">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d0719-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0719-150">Range-Lower</span></span>            | <span data-ttu-id="d0719-151">1</span><span class="sxs-lookup"><span data-stu-id="d0719-151">1</span></span>                                                        |
| <span data-ttu-id="d0719-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0719-152">Range-Upper</span></span>            | <span data-ttu-id="d0719-153">13</span><span class="sxs-lookup"><span data-stu-id="d0719-153">13</span></span>                                                       |
| <span data-ttu-id="d0719-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-154">Search-Flags</span></span>           | <span data-ttu-id="d0719-155">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0719-155">0x00000000</span></span>                                               |
| <span data-ttu-id="d0719-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-156">System-Flags</span></span>           | <span data-ttu-id="d0719-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0719-157">0x00000010</span></span>                                               |
| <span data-ttu-id="d0719-158">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0719-158">Classes used in</span></span>        | [<span data-ttu-id="d0719-159">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0719-159">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d0719-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d0719-160">Windows Server 2003</span></span>



| <span data-ttu-id="d0719-161">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-161">Entry</span></span> | <span data-ttu-id="d0719-162">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-162">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0719-163">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0719-163">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d0719-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-164">MAPI-Id</span></span>                | <span data-ttu-id="d0719-165">0x803B</span><span class="sxs-lookup"><span data-stu-id="d0719-165">0x803B</span></span>                                                   |
| <span data-ttu-id="d0719-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0719-166">System-Only</span></span>            | <span data-ttu-id="d0719-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-167">False</span></span>                                                    |
| <span data-ttu-id="d0719-168">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0719-168">Is-Single-Valued</span></span>       | <span data-ttu-id="d0719-169">True</span><span class="sxs-lookup"><span data-stu-id="d0719-169">True</span></span>                                                     |
| <span data-ttu-id="d0719-170">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0719-170">Is Indexed</span></span>             | <span data-ttu-id="d0719-171">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-171">False</span></span>                                                    |
| <span data-ttu-id="d0719-172">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0719-172">In Global Catalog</span></span>      | <span data-ttu-id="d0719-173">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-173">False</span></span>                                                    |
| <span data-ttu-id="d0719-174">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0719-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0719-175">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0719-175">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d0719-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0719-176">Range-Lower</span></span>            | <span data-ttu-id="d0719-177">1</span><span class="sxs-lookup"><span data-stu-id="d0719-177">1</span></span>                                                        |
| <span data-ttu-id="d0719-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0719-178">Range-Upper</span></span>            | <span data-ttu-id="d0719-179">13</span><span class="sxs-lookup"><span data-stu-id="d0719-179">13</span></span>                                                       |
| <span data-ttu-id="d0719-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-180">Search-Flags</span></span>           | <span data-ttu-id="d0719-181">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0719-181">0x00000000</span></span>                                               |
| <span data-ttu-id="d0719-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-182">System-Flags</span></span>           | <span data-ttu-id="d0719-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0719-183">0x00000010</span></span>                                               |
| <span data-ttu-id="d0719-184">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0719-184">Classes used in</span></span>        | [<span data-ttu-id="d0719-185">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0719-185">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d0719-186">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d0719-186">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d0719-187">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-187">Entry</span></span> | <span data-ttu-id="d0719-188">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-188">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0719-189">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0719-189">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d0719-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-190">MAPI-Id</span></span>                | <span data-ttu-id="d0719-191">0x803B</span><span class="sxs-lookup"><span data-stu-id="d0719-191">0x803B</span></span>                                                   |
| <span data-ttu-id="d0719-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0719-192">System-Only</span></span>            | <span data-ttu-id="d0719-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-193">False</span></span>                                                    |
| <span data-ttu-id="d0719-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0719-194">Is-Single-Valued</span></span>       | <span data-ttu-id="d0719-195">True</span><span class="sxs-lookup"><span data-stu-id="d0719-195">True</span></span>                                                     |
| <span data-ttu-id="d0719-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0719-196">Is Indexed</span></span>             | <span data-ttu-id="d0719-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-197">False</span></span>                                                    |
| <span data-ttu-id="d0719-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0719-198">In Global Catalog</span></span>      | <span data-ttu-id="d0719-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-199">False</span></span>                                                    |
| <span data-ttu-id="d0719-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0719-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0719-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0719-201">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d0719-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0719-202">Range-Lower</span></span>            | <span data-ttu-id="d0719-203">1</span><span class="sxs-lookup"><span data-stu-id="d0719-203">1</span></span>                                                        |
| <span data-ttu-id="d0719-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0719-204">Range-Upper</span></span>            | <span data-ttu-id="d0719-205">13</span><span class="sxs-lookup"><span data-stu-id="d0719-205">13</span></span>                                                       |
| <span data-ttu-id="d0719-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-206">Search-Flags</span></span>           | <span data-ttu-id="d0719-207">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0719-207">0x00000000</span></span>                                               |
| <span data-ttu-id="d0719-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-208">System-Flags</span></span>           | <span data-ttu-id="d0719-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0719-209">0x00000010</span></span>                                               |
| <span data-ttu-id="d0719-210">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0719-210">Classes used in</span></span>        | [<span data-ttu-id="d0719-211">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0719-211">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d0719-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0719-212">Windows Server 2008</span></span>



| <span data-ttu-id="d0719-213">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-213">Entry</span></span> | <span data-ttu-id="d0719-214">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-214">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0719-215">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0719-215">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d0719-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-216">MAPI-Id</span></span>                | <span data-ttu-id="d0719-217">0x803B</span><span class="sxs-lookup"><span data-stu-id="d0719-217">0x803B</span></span>                                                   |
| <span data-ttu-id="d0719-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0719-218">System-Only</span></span>            | <span data-ttu-id="d0719-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-219">False</span></span>                                                    |
| <span data-ttu-id="d0719-220">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0719-220">Is-Single-Valued</span></span>       | <span data-ttu-id="d0719-221">True</span><span class="sxs-lookup"><span data-stu-id="d0719-221">True</span></span>                                                     |
| <span data-ttu-id="d0719-222">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0719-222">Is Indexed</span></span>             | <span data-ttu-id="d0719-223">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-223">False</span></span>                                                    |
| <span data-ttu-id="d0719-224">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0719-224">In Global Catalog</span></span>      | <span data-ttu-id="d0719-225">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-225">False</span></span>                                                    |
| <span data-ttu-id="d0719-226">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0719-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0719-227">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0719-227">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d0719-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0719-228">Range-Lower</span></span>            | <span data-ttu-id="d0719-229">1</span><span class="sxs-lookup"><span data-stu-id="d0719-229">1</span></span>                                                        |
| <span data-ttu-id="d0719-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0719-230">Range-Upper</span></span>            | <span data-ttu-id="d0719-231">13</span><span class="sxs-lookup"><span data-stu-id="d0719-231">13</span></span>                                                       |
| <span data-ttu-id="d0719-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-232">Search-Flags</span></span>           | <span data-ttu-id="d0719-233">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0719-233">0x00000000</span></span>                                               |
| <span data-ttu-id="d0719-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-234">System-Flags</span></span>           | <span data-ttu-id="d0719-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0719-235">0x00000010</span></span>                                               |
| <span data-ttu-id="d0719-236">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0719-236">Classes used in</span></span>        | [<span data-ttu-id="d0719-237">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0719-237">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d0719-238">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0719-238">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d0719-239">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-239">Entry</span></span> | <span data-ttu-id="d0719-240">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-240">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0719-241">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0719-241">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d0719-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-242">MAPI-Id</span></span>                | <span data-ttu-id="d0719-243">0x803B</span><span class="sxs-lookup"><span data-stu-id="d0719-243">0x803B</span></span>                                                   |
| <span data-ttu-id="d0719-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0719-244">System-Only</span></span>            | <span data-ttu-id="d0719-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-245">False</span></span>                                                    |
| <span data-ttu-id="d0719-246">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0719-246">Is-Single-Valued</span></span>       | <span data-ttu-id="d0719-247">True</span><span class="sxs-lookup"><span data-stu-id="d0719-247">True</span></span>                                                     |
| <span data-ttu-id="d0719-248">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0719-248">Is Indexed</span></span>             | <span data-ttu-id="d0719-249">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-249">False</span></span>                                                    |
| <span data-ttu-id="d0719-250">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0719-250">In Global Catalog</span></span>      | <span data-ttu-id="d0719-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-251">False</span></span>                                                    |
| <span data-ttu-id="d0719-252">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0719-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0719-253">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0719-253">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d0719-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0719-254">Range-Lower</span></span>            | <span data-ttu-id="d0719-255">1</span><span class="sxs-lookup"><span data-stu-id="d0719-255">1</span></span>                                                        |
| <span data-ttu-id="d0719-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0719-256">Range-Upper</span></span>            | <span data-ttu-id="d0719-257">13</span><span class="sxs-lookup"><span data-stu-id="d0719-257">13</span></span>                                                       |
| <span data-ttu-id="d0719-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-258">Search-Flags</span></span>           | <span data-ttu-id="d0719-259">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0719-259">0x00000000</span></span>                                               |
| <span data-ttu-id="d0719-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-260">System-Flags</span></span>           | <span data-ttu-id="d0719-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0719-261">0x00000010</span></span>                                               |
| <span data-ttu-id="d0719-262">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0719-262">Classes used in</span></span>        | [<span data-ttu-id="d0719-263">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0719-263">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d0719-264">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0719-264">Windows Server 2012</span></span>



| <span data-ttu-id="d0719-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="d0719-265">Entry</span></span> | <span data-ttu-id="d0719-266">Значение</span><span class="sxs-lookup"><span data-stu-id="d0719-266">Value</span></span> |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="d0719-267">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="d0719-267">Link-Id</span></span>                | \-                                                       |
| <span data-ttu-id="d0719-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d0719-268">MAPI-Id</span></span>                | <span data-ttu-id="d0719-269">0x803B</span><span class="sxs-lookup"><span data-stu-id="d0719-269">0x803B</span></span>                                                   |
| <span data-ttu-id="d0719-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="d0719-270">System-Only</span></span>            | <span data-ttu-id="d0719-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-271">False</span></span>                                                    |
| <span data-ttu-id="d0719-272">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="d0719-272">Is-Single-Valued</span></span>       | <span data-ttu-id="d0719-273">True</span><span class="sxs-lookup"><span data-stu-id="d0719-273">True</span></span>                                                     |
| <span data-ttu-id="d0719-274">Индексируется</span><span class="sxs-lookup"><span data-stu-id="d0719-274">Is Indexed</span></span>             | <span data-ttu-id="d0719-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-275">False</span></span>                                                    |
| <span data-ttu-id="d0719-276">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="d0719-276">In Global Catalog</span></span>      | <span data-ttu-id="d0719-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="d0719-277">False</span></span>                                                    |
| <span data-ttu-id="d0719-278">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="d0719-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="d0719-279">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="d0719-279">O:BAG:BAD:S:</span></span>                                             |
| <span data-ttu-id="d0719-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d0719-280">Range-Lower</span></span>            | <span data-ttu-id="d0719-281">1</span><span class="sxs-lookup"><span data-stu-id="d0719-281">1</span></span>                                                        |
| <span data-ttu-id="d0719-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d0719-282">Range-Upper</span></span>            | <span data-ttu-id="d0719-283">13</span><span class="sxs-lookup"><span data-stu-id="d0719-283">13</span></span>                                                       |
| <span data-ttu-id="d0719-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-284">Search-Flags</span></span>           | <span data-ttu-id="d0719-285">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0719-285">0x00000000</span></span>                                               |
| <span data-ttu-id="d0719-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d0719-286">System-Flags</span></span>           | <span data-ttu-id="d0719-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0719-287">0x00000010</span></span>                                               |
| <span data-ttu-id="d0719-288">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="d0719-288">Classes used in</span></span>        | [<span data-ttu-id="d0719-289">**Отображение шаблона**</span><span class="sxs-lookup"><span data-stu-id="d0719-289">**Display-Template**</span></span>](c-displaytemplate.md)<br/> |



 

 





