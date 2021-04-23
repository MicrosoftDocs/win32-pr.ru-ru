---
title: MSI-файл-атрибут списка
description: Этот атрибут содержит список файлов установщика Microsoft, таких как базовый MSI-файл (MSI) и файлы преобразования MST (. MST).
ms.assetid: 259a13a2-bb34-49aa-862e-4159e887310c
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута списка файлов MSI
- Схема AD атрибута Мсифилелист
topic_type:
- apiref
api_name:
- Msi-File-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05608cdf443ab053549fde7db509ca79be08b3a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138930"
---
# <a name="msi-file-list-attribute"></a><span data-ttu-id="29453-105">MSI-файл-атрибут списка</span><span class="sxs-lookup"><span data-stu-id="29453-105">Msi-File-List attribute</span></span>

<span data-ttu-id="29453-106">Этот атрибут содержит список файлов установщика Microsoft, таких как базовый MSI-файл (MSI) и файлы преобразования MST (. MST).</span><span class="sxs-lookup"><span data-stu-id="29453-106">This attribute contains a list of Microsoft installer files, such as the base MSI file (.msi) and MST transform files (.mst).</span></span>



| <span data-ttu-id="29453-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-107">Entry</span></span> | <span data-ttu-id="29453-108">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="29453-109">CN</span><span class="sxs-lookup"><span data-stu-id="29453-109">CN</span></span>                | <span data-ttu-id="29453-110">MSI-файл-список</span><span class="sxs-lookup"><span data-stu-id="29453-110">Msi-File-List</span></span>                               |
| <span data-ttu-id="29453-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="29453-111">Ldap-Display-Name</span></span> | <span data-ttu-id="29453-112">мсифилелист</span><span class="sxs-lookup"><span data-stu-id="29453-112">msiFileList</span></span>                                 |
| <span data-ttu-id="29453-113">Размер</span><span class="sxs-lookup"><span data-stu-id="29453-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="29453-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="29453-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="29453-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="29453-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="29453-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="29453-116">Attribute-Id</span></span>      | <span data-ttu-id="29453-117">1.2.840.113556.1.4.671</span><span class="sxs-lookup"><span data-stu-id="29453-117">1.2.840.113556.1.4.671</span></span>                      |
| <span data-ttu-id="29453-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="29453-118">System-Id-Guid</span></span>    | <span data-ttu-id="29453-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="29453-119">7bfdcb7d-4807-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="29453-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29453-120">Syntax</span></span>            | [<span data-ttu-id="29453-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="29453-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="29453-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="29453-122">Implementations</span></span>

-   [<span data-ttu-id="29453-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="29453-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="29453-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="29453-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="29453-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="29453-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="29453-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="29453-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="29453-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="29453-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="29453-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="29453-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="29453-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29453-129">Windows 2000 Server</span></span>



| <span data-ttu-id="29453-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-130">Entry</span></span> | <span data-ttu-id="29453-131">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-131">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29453-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29453-132">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29453-133">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="29453-134">System-Only</span></span>            | <span data-ttu-id="29453-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-135">False</span></span>                                                            |
| <span data-ttu-id="29453-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29453-136">Is-Single-Valued</span></span>       | <span data-ttu-id="29453-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-137">False</span></span>                                                            |
| <span data-ttu-id="29453-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29453-138">Is Indexed</span></span>             | <span data-ttu-id="29453-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-139">False</span></span>                                                            |
| <span data-ttu-id="29453-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29453-140">In Global Catalog</span></span>      | <span data-ttu-id="29453-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-141">False</span></span>                                                            |
| <span data-ttu-id="29453-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29453-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="29453-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29453-143">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29453-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29453-144">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29453-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29453-145">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29453-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-146">Search-Flags</span></span>           | <span data-ttu-id="29453-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29453-147">0x00000000</span></span>                                                       |
| <span data-ttu-id="29453-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-148">System-Flags</span></span>           | <span data-ttu-id="29453-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29453-149">0x00000010</span></span>                                                       |
| <span data-ttu-id="29453-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29453-150">Classes used in</span></span>        | [<span data-ttu-id="29453-151">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="29453-151">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="29453-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29453-152">Windows Server 2003</span></span>



| <span data-ttu-id="29453-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-153">Entry</span></span> | <span data-ttu-id="29453-154">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-154">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29453-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29453-155">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29453-156">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="29453-157">System-Only</span></span>            | <span data-ttu-id="29453-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-158">False</span></span>                                                            |
| <span data-ttu-id="29453-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29453-159">Is-Single-Valued</span></span>       | <span data-ttu-id="29453-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-160">False</span></span>                                                            |
| <span data-ttu-id="29453-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29453-161">Is Indexed</span></span>             | <span data-ttu-id="29453-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-162">False</span></span>                                                            |
| <span data-ttu-id="29453-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29453-163">In Global Catalog</span></span>      | <span data-ttu-id="29453-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-164">False</span></span>                                                            |
| <span data-ttu-id="29453-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29453-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="29453-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29453-166">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29453-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29453-167">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29453-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29453-168">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29453-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-169">Search-Flags</span></span>           | <span data-ttu-id="29453-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29453-170">0x00000000</span></span>                                                       |
| <span data-ttu-id="29453-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-171">System-Flags</span></span>           | <span data-ttu-id="29453-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29453-172">0x00000010</span></span>                                                       |
| <span data-ttu-id="29453-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29453-173">Classes used in</span></span>        | [<span data-ttu-id="29453-174">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="29453-174">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="29453-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="29453-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="29453-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-176">Entry</span></span> | <span data-ttu-id="29453-177">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-177">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29453-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29453-178">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29453-179">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="29453-180">System-Only</span></span>            | <span data-ttu-id="29453-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-181">False</span></span>                                                            |
| <span data-ttu-id="29453-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29453-182">Is-Single-Valued</span></span>       | <span data-ttu-id="29453-183">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-183">False</span></span>                                                            |
| <span data-ttu-id="29453-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29453-184">Is Indexed</span></span>             | <span data-ttu-id="29453-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-185">False</span></span>                                                            |
| <span data-ttu-id="29453-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29453-186">In Global Catalog</span></span>      | <span data-ttu-id="29453-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-187">False</span></span>                                                            |
| <span data-ttu-id="29453-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29453-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="29453-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29453-189">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29453-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29453-190">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29453-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29453-191">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29453-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-192">Search-Flags</span></span>           | <span data-ttu-id="29453-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29453-193">0x00000000</span></span>                                                       |
| <span data-ttu-id="29453-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-194">System-Flags</span></span>           | <span data-ttu-id="29453-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29453-195">0x00000010</span></span>                                                       |
| <span data-ttu-id="29453-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29453-196">Classes used in</span></span>        | [<span data-ttu-id="29453-197">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="29453-197">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="29453-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29453-198">Windows Server 2008</span></span>



| <span data-ttu-id="29453-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-199">Entry</span></span> | <span data-ttu-id="29453-200">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-200">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29453-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29453-201">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29453-202">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="29453-203">System-Only</span></span>            | <span data-ttu-id="29453-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-204">False</span></span>                                                            |
| <span data-ttu-id="29453-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29453-205">Is-Single-Valued</span></span>       | <span data-ttu-id="29453-206">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-206">False</span></span>                                                            |
| <span data-ttu-id="29453-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29453-207">Is Indexed</span></span>             | <span data-ttu-id="29453-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-208">False</span></span>                                                            |
| <span data-ttu-id="29453-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29453-209">In Global Catalog</span></span>      | <span data-ttu-id="29453-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-210">False</span></span>                                                            |
| <span data-ttu-id="29453-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29453-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="29453-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29453-212">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29453-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29453-213">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29453-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29453-214">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29453-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-215">Search-Flags</span></span>           | <span data-ttu-id="29453-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29453-216">0x00000000</span></span>                                                       |
| <span data-ttu-id="29453-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-217">System-Flags</span></span>           | <span data-ttu-id="29453-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29453-218">0x00000010</span></span>                                                       |
| <span data-ttu-id="29453-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29453-219">Classes used in</span></span>        | [<span data-ttu-id="29453-220">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="29453-220">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="29453-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="29453-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="29453-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-222">Entry</span></span> | <span data-ttu-id="29453-223">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-223">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29453-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29453-224">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29453-225">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="29453-226">System-Only</span></span>            | <span data-ttu-id="29453-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-227">False</span></span>                                                            |
| <span data-ttu-id="29453-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29453-228">Is-Single-Valued</span></span>       | <span data-ttu-id="29453-229">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-229">False</span></span>                                                            |
| <span data-ttu-id="29453-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29453-230">Is Indexed</span></span>             | <span data-ttu-id="29453-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-231">False</span></span>                                                            |
| <span data-ttu-id="29453-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29453-232">In Global Catalog</span></span>      | <span data-ttu-id="29453-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-233">False</span></span>                                                            |
| <span data-ttu-id="29453-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29453-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="29453-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29453-235">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29453-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29453-236">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29453-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29453-237">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29453-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-238">Search-Flags</span></span>           | <span data-ttu-id="29453-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29453-239">0x00000000</span></span>                                                       |
| <span data-ttu-id="29453-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-240">System-Flags</span></span>           | <span data-ttu-id="29453-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29453-241">0x00000010</span></span>                                                       |
| <span data-ttu-id="29453-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29453-242">Classes used in</span></span>        | [<span data-ttu-id="29453-243">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="29453-243">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="29453-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29453-244">Windows Server 2012</span></span>



| <span data-ttu-id="29453-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="29453-245">Entry</span></span> | <span data-ttu-id="29453-246">Значение</span><span class="sxs-lookup"><span data-stu-id="29453-246">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="29453-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="29453-247">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="29453-248">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="29453-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="29453-249">System-Only</span></span>            | <span data-ttu-id="29453-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-250">False</span></span>                                                            |
| <span data-ttu-id="29453-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="29453-251">Is-Single-Valued</span></span>       | <span data-ttu-id="29453-252">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-252">False</span></span>                                                            |
| <span data-ttu-id="29453-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="29453-253">Is Indexed</span></span>             | <span data-ttu-id="29453-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-254">False</span></span>                                                            |
| <span data-ttu-id="29453-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="29453-255">In Global Catalog</span></span>      | <span data-ttu-id="29453-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="29453-256">False</span></span>                                                            |
| <span data-ttu-id="29453-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="29453-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="29453-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="29453-258">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="29453-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="29453-259">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="29453-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="29453-260">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="29453-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-261">Search-Flags</span></span>           | <span data-ttu-id="29453-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="29453-262">0x00000000</span></span>                                                       |
| <span data-ttu-id="29453-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="29453-263">System-Flags</span></span>           | <span data-ttu-id="29453-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="29453-264">0x00000010</span></span>                                                       |
| <span data-ttu-id="29453-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="29453-265">Classes used in</span></span>        | [<span data-ttu-id="29453-266">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="29453-266">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





