---
title: Атрибут адреса SMTP-Mail
description: Атрибут универсального почтового адреса. Используется в поле как необязательный атрибут объектов сервера, где он используется репликацией DS на основе почты (если настроены компьютеры).
ms.assetid: 54fd710c-d140-4d46-9db3-0c72fb5fb08c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута адреса SMTP-Mail
- Схема AD атрибута mailAddress
topic_type:
- apiref
api_name:
- SMTP-Mail-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1828c59af346ab5a5741aaa03358b711484089
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138263"
---
# <a name="smtp-mail-address-attribute"></a><span data-ttu-id="a74ab-106">Атрибут адреса SMTP-Mail</span><span class="sxs-lookup"><span data-stu-id="a74ab-106">SMTP-Mail-Address attribute</span></span>

<span data-ttu-id="a74ab-107">Атрибут универсального почтового адреса.</span><span class="sxs-lookup"><span data-stu-id="a74ab-107">Generic mail address attribute.</span></span> <span data-ttu-id="a74ab-108">Используется в поле как необязательный атрибут объектов сервера, где он используется репликацией DS на основе почты (если настроены компьютеры).</span><span class="sxs-lookup"><span data-stu-id="a74ab-108">Used in the box as an optional attribute of server objects, where it is consumed by mail-based DS replication (if the computers are so configured).</span></span>



| <span data-ttu-id="a74ab-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-109">Entry</span></span> | <span data-ttu-id="a74ab-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="a74ab-111">CN</span><span class="sxs-lookup"><span data-stu-id="a74ab-111">CN</span></span>                | <span data-ttu-id="a74ab-112">Адрес SMTP-Mail</span><span class="sxs-lookup"><span data-stu-id="a74ab-112">SMTP-Mail-Address</span></span>                           |
| <span data-ttu-id="a74ab-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a74ab-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a74ab-114">mailAddress</span><span class="sxs-lookup"><span data-stu-id="a74ab-114">mailAddress</span></span>                                 |
| <span data-ttu-id="a74ab-115">Размер</span><span class="sxs-lookup"><span data-stu-id="a74ab-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="a74ab-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a74ab-116">Update Privilege</span></span>  | <span data-ttu-id="a74ab-117">Администратор домена</span><span class="sxs-lookup"><span data-stu-id="a74ab-117">Domain administrator</span></span>                        |
| <span data-ttu-id="a74ab-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a74ab-118">Update Frequency</span></span>  | <span data-ttu-id="a74ab-119">Почти никогда</span><span class="sxs-lookup"><span data-stu-id="a74ab-119">Almost never</span></span>                                |
| <span data-ttu-id="a74ab-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-120">Attribute-Id</span></span>      | <span data-ttu-id="a74ab-121">1.2.840.113556.1.4.786</span><span class="sxs-lookup"><span data-stu-id="a74ab-121">1.2.840.113556.1.4.786</span></span>                      |
| <span data-ttu-id="a74ab-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a74ab-122">System-Id-Guid</span></span>    | <span data-ttu-id="a74ab-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="a74ab-123">26d9736f-6070-11d1-a9c6-0000f80367c1</span></span>        |
| <span data-ttu-id="a74ab-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a74ab-124">Syntax</span></span>            | [<span data-ttu-id="a74ab-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="a74ab-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="a74ab-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a74ab-126">Implementations</span></span>

-   [<span data-ttu-id="a74ab-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a74ab-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a74ab-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a74ab-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a74ab-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="a74ab-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="a74ab-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a74ab-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a74ab-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a74ab-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a74ab-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a74ab-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a74ab-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a74ab-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a74ab-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a74ab-134">Windows 2000 Server</span></span>



| <span data-ttu-id="a74ab-135">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-135">Entry</span></span> | <span data-ttu-id="a74ab-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-136">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-137">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-137">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-138">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-139">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-139">System-Only</span></span>            | <span data-ttu-id="a74ab-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-140">False</span></span>                                 |
| <span data-ttu-id="a74ab-141">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-141">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-142">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-142">True</span></span>                                  |
| <span data-ttu-id="a74ab-143">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-143">Is Indexed</span></span>             | <span data-ttu-id="a74ab-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-144">False</span></span>                                 |
| <span data-ttu-id="a74ab-145">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-145">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-146">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-146">False</span></span>                                 |
| <span data-ttu-id="a74ab-147">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-147">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-148">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-148">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-149">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-149">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-150">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-151">Search-Flags</span></span>           | <span data-ttu-id="a74ab-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-152">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-153">System-Flags</span></span>           | <span data-ttu-id="a74ab-154">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-154">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-155">Classes used in</span></span>        | [<span data-ttu-id="a74ab-156">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-156">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a74ab-157">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a74ab-157">Windows Server 2003</span></span>



| <span data-ttu-id="a74ab-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-158">Entry</span></span> | <span data-ttu-id="a74ab-159">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-159">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-160">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-161">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-162">System-Only</span></span>            | <span data-ttu-id="a74ab-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-163">False</span></span>                                 |
| <span data-ttu-id="a74ab-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-164">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-165">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-165">True</span></span>                                  |
| <span data-ttu-id="a74ab-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-166">Is Indexed</span></span>             | <span data-ttu-id="a74ab-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-167">False</span></span>                                 |
| <span data-ttu-id="a74ab-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-168">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-169">False</span></span>                                 |
| <span data-ttu-id="a74ab-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-171">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-172">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-173">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-174">Search-Flags</span></span>           | <span data-ttu-id="a74ab-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-175">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-176">System-Flags</span></span>           | <span data-ttu-id="a74ab-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-177">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-178">Classes used in</span></span>        | [<span data-ttu-id="a74ab-179">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-179">**Server**</span></span>](c-server.md)<br/> |



## <a name="adam"></a><span data-ttu-id="a74ab-180">ADAM</span><span class="sxs-lookup"><span data-stu-id="a74ab-180">ADAM</span></span>



| <span data-ttu-id="a74ab-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-181">Entry</span></span> | <span data-ttu-id="a74ab-182">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-182">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-183">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-184">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-185">System-Only</span></span>            | <span data-ttu-id="a74ab-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-186">False</span></span>                                 |
| <span data-ttu-id="a74ab-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-187">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-188">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-188">True</span></span>                                  |
| <span data-ttu-id="a74ab-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-189">Is Indexed</span></span>             | <span data-ttu-id="a74ab-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-190">False</span></span>                                 |
| <span data-ttu-id="a74ab-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-191">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-192">False</span></span>                                 |
| <span data-ttu-id="a74ab-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-194">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-195">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-196">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-197">Search-Flags</span></span>           | <span data-ttu-id="a74ab-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-198">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-199">System-Flags</span></span>           | <span data-ttu-id="a74ab-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-200">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-201">Classes used in</span></span>        | [<span data-ttu-id="a74ab-202">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-202">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a74ab-203">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a74ab-203">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a74ab-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-204">Entry</span></span> | <span data-ttu-id="a74ab-205">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-205">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-206">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-206">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-207">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-207">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-208">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-208">System-Only</span></span>            | <span data-ttu-id="a74ab-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-209">False</span></span>                                 |
| <span data-ttu-id="a74ab-210">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-210">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-211">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-211">True</span></span>                                  |
| <span data-ttu-id="a74ab-212">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-212">Is Indexed</span></span>             | <span data-ttu-id="a74ab-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-213">False</span></span>                                 |
| <span data-ttu-id="a74ab-214">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-214">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-215">False</span></span>                                 |
| <span data-ttu-id="a74ab-216">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-216">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-217">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-217">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-218">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-218">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-219">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-219">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-220">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-220">Search-Flags</span></span>           | <span data-ttu-id="a74ab-221">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-221">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-222">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-222">System-Flags</span></span>           | <span data-ttu-id="a74ab-223">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-223">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-224">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-224">Classes used in</span></span>        | [<span data-ttu-id="a74ab-225">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-225">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a74ab-226">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a74ab-226">Windows Server 2008</span></span>



| <span data-ttu-id="a74ab-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-227">Entry</span></span> | <span data-ttu-id="a74ab-228">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-228">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-229">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-230">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-231">System-Only</span></span>            | <span data-ttu-id="a74ab-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-232">False</span></span>                                 |
| <span data-ttu-id="a74ab-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-233">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-234">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-234">True</span></span>                                  |
| <span data-ttu-id="a74ab-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-235">Is Indexed</span></span>             | <span data-ttu-id="a74ab-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-236">False</span></span>                                 |
| <span data-ttu-id="a74ab-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-237">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-238">False</span></span>                                 |
| <span data-ttu-id="a74ab-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-240">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-241">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-242">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-243">Search-Flags</span></span>           | <span data-ttu-id="a74ab-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-244">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-245">System-Flags</span></span>           | <span data-ttu-id="a74ab-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-246">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-247">Classes used in</span></span>        | [<span data-ttu-id="a74ab-248">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-248">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a74ab-249">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a74ab-249">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a74ab-250">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-250">Entry</span></span> | <span data-ttu-id="a74ab-251">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-251">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-252">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-252">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-253">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-253">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-254">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-254">System-Only</span></span>            | <span data-ttu-id="a74ab-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-255">False</span></span>                                 |
| <span data-ttu-id="a74ab-256">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-256">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-257">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-257">True</span></span>                                  |
| <span data-ttu-id="a74ab-258">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-258">Is Indexed</span></span>             | <span data-ttu-id="a74ab-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-259">False</span></span>                                 |
| <span data-ttu-id="a74ab-260">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-260">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-261">False</span></span>                                 |
| <span data-ttu-id="a74ab-262">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-262">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-263">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-263">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-264">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-264">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-265">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-265">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-266">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-266">Search-Flags</span></span>           | <span data-ttu-id="a74ab-267">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-267">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-268">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-268">System-Flags</span></span>           | <span data-ttu-id="a74ab-269">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-269">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-270">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-270">Classes used in</span></span>        | [<span data-ttu-id="a74ab-271">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-271">**Server**</span></span>](c-server.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a74ab-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a74ab-272">Windows Server 2012</span></span>



| <span data-ttu-id="a74ab-273">Ввод</span><span class="sxs-lookup"><span data-stu-id="a74ab-273">Entry</span></span> | <span data-ttu-id="a74ab-274">Значение</span><span class="sxs-lookup"><span data-stu-id="a74ab-274">Value</span></span> |
|------------------------|---------------------------------------|
| <span data-ttu-id="a74ab-275">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a74ab-275">Link-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-276">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a74ab-276">MAPI-Id</span></span>                | \-                                    |
| <span data-ttu-id="a74ab-277">System-Only</span><span class="sxs-lookup"><span data-stu-id="a74ab-277">System-Only</span></span>            | <span data-ttu-id="a74ab-278">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-278">False</span></span>                                 |
| <span data-ttu-id="a74ab-279">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a74ab-279">Is-Single-Valued</span></span>       | <span data-ttu-id="a74ab-280">True</span><span class="sxs-lookup"><span data-stu-id="a74ab-280">True</span></span>                                  |
| <span data-ttu-id="a74ab-281">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a74ab-281">Is Indexed</span></span>             | <span data-ttu-id="a74ab-282">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-282">False</span></span>                                 |
| <span data-ttu-id="a74ab-283">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a74ab-283">In Global Catalog</span></span>      | <span data-ttu-id="a74ab-284">Неверно</span><span class="sxs-lookup"><span data-stu-id="a74ab-284">False</span></span>                                 |
| <span data-ttu-id="a74ab-285">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a74ab-285">NT-Security-Descriptor</span></span> | <span data-ttu-id="a74ab-286">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a74ab-286">O:BAG:BAD:S:</span></span>                          |
| <span data-ttu-id="a74ab-287">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a74ab-287">Range-Lower</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-288">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a74ab-288">Range-Upper</span></span>            | \-                                    |
| <span data-ttu-id="a74ab-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-289">Search-Flags</span></span>           | <span data-ttu-id="a74ab-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a74ab-290">0x00000000</span></span>                            |
| <span data-ttu-id="a74ab-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a74ab-291">System-Flags</span></span>           | <span data-ttu-id="a74ab-292">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a74ab-292">0x00000010</span></span>                            |
| <span data-ttu-id="a74ab-293">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a74ab-293">Classes used in</span></span>        | [<span data-ttu-id="a74ab-294">**Сервером**</span><span class="sxs-lookup"><span data-stu-id="a74ab-294">**Server**</span></span>](c-server.md)<br/> |



 

 





