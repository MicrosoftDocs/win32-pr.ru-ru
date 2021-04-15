---
title: Атрибут COM-typelib-ID
description: Этот атрибут хранит список идентификаторов библиотек типов, содержащихся в этом пакете приложения.
ms.assetid: 3dcd2d1f-8b6d-46f6-9707-4af006f0e610
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута COM-typelib-ID
- Схема AD атрибута Комтипелибид
topic_type:
- apiref
api_name:
- COM-Typelib-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0be116963137dcdba4d97aa3de751bdf7308c335
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655530"
---
# <a name="com-typelib-id-attribute"></a><span data-ttu-id="28b50-105">Атрибут COM-typelib-ID</span><span class="sxs-lookup"><span data-stu-id="28b50-105">COM-Typelib-Id attribute</span></span>

<span data-ttu-id="28b50-106">Этот атрибут хранит список идентификаторов библиотек типов, содержащихся в этом пакете приложения.</span><span class="sxs-lookup"><span data-stu-id="28b50-106">This attribute stores the list of type library IDs contained in this application package.</span></span>



| <span data-ttu-id="28b50-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-107">Entry</span></span> | <span data-ttu-id="28b50-108">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="28b50-109">CN</span><span class="sxs-lookup"><span data-stu-id="28b50-109">CN</span></span>                | <span data-ttu-id="28b50-110">Модель COM-typelib-ID</span><span class="sxs-lookup"><span data-stu-id="28b50-110">COM-Typelib-Id</span></span>                                                                   |
| <span data-ttu-id="28b50-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="28b50-111">Ldap-Display-Name</span></span> | <span data-ttu-id="28b50-112">комтипелибид</span><span class="sxs-lookup"><span data-stu-id="28b50-112">cOMTypelibId</span></span>                                                                     |
| <span data-ttu-id="28b50-113">Размер</span><span class="sxs-lookup"><span data-stu-id="28b50-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="28b50-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="28b50-114">Update Privilege</span></span>  | <span data-ttu-id="28b50-115">Любой пользователь может обновить этот объект на основе безопасности создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="28b50-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="28b50-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="28b50-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="28b50-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-117">Attribute-Id</span></span>      | <span data-ttu-id="28b50-118">1.2.840.113556.1.4.254</span><span class="sxs-lookup"><span data-stu-id="28b50-118">1.2.840.113556.1.4.254</span></span>                                                           |
| <span data-ttu-id="28b50-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="28b50-119">System-Id-Guid</span></span>    | <span data-ttu-id="28b50-120">281416de-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="28b50-120">281416de-1968-11d0-a28f-00aa003049e2</span></span>                                             |
| <span data-ttu-id="28b50-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28b50-121">Syntax</span></span>            | [<span data-ttu-id="28b50-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="28b50-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="28b50-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="28b50-123">Implementations</span></span>

-   [<span data-ttu-id="28b50-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="28b50-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="28b50-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="28b50-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="28b50-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="28b50-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="28b50-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="28b50-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="28b50-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="28b50-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="28b50-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="28b50-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="28b50-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28b50-130">Windows 2000 Server</span></span>



| <span data-ttu-id="28b50-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-131">Entry</span></span> | <span data-ttu-id="28b50-132">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="28b50-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b50-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b50-135">System-Only</span></span>            | <span data-ttu-id="28b50-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-136">False</span></span>                                                            |
| <span data-ttu-id="28b50-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b50-137">Is-Single-Valued</span></span>       | <span data-ttu-id="28b50-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-138">False</span></span>                                                            |
| <span data-ttu-id="28b50-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b50-139">Is Indexed</span></span>             | <span data-ttu-id="28b50-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-140">False</span></span>                                                            |
| <span data-ttu-id="28b50-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b50-141">In Global Catalog</span></span>      | <span data-ttu-id="28b50-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-142">False</span></span>                                                            |
| <span data-ttu-id="28b50-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b50-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b50-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b50-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="28b50-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b50-145">Range-Lower</span></span>            | <span data-ttu-id="28b50-146">36</span><span class="sxs-lookup"><span data-stu-id="28b50-146">36</span></span>                                                               |
| <span data-ttu-id="28b50-147">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b50-147">Range-Upper</span></span>            | <span data-ttu-id="28b50-148">36</span><span class="sxs-lookup"><span data-stu-id="28b50-148">36</span></span>                                                               |
| <span data-ttu-id="28b50-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-149">Search-Flags</span></span>           | <span data-ttu-id="28b50-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b50-150">0x00000000</span></span>                                                       |
| <span data-ttu-id="28b50-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-151">System-Flags</span></span>           | <span data-ttu-id="28b50-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b50-152">0x00000010</span></span>                                                       |
| <span data-ttu-id="28b50-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b50-153">Classes used in</span></span>        | [<span data-ttu-id="28b50-154">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="28b50-154">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="28b50-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28b50-155">Windows Server 2003</span></span>



| <span data-ttu-id="28b50-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-156">Entry</span></span> | <span data-ttu-id="28b50-157">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-157">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="28b50-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b50-158">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-159">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b50-160">System-Only</span></span>            | <span data-ttu-id="28b50-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-161">False</span></span>                                                            |
| <span data-ttu-id="28b50-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b50-162">Is-Single-Valued</span></span>       | <span data-ttu-id="28b50-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-163">False</span></span>                                                            |
| <span data-ttu-id="28b50-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b50-164">Is Indexed</span></span>             | <span data-ttu-id="28b50-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-165">False</span></span>                                                            |
| <span data-ttu-id="28b50-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b50-166">In Global Catalog</span></span>      | <span data-ttu-id="28b50-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-167">False</span></span>                                                            |
| <span data-ttu-id="28b50-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b50-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b50-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b50-169">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="28b50-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b50-170">Range-Lower</span></span>            | <span data-ttu-id="28b50-171">36</span><span class="sxs-lookup"><span data-stu-id="28b50-171">36</span></span>                                                               |
| <span data-ttu-id="28b50-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b50-172">Range-Upper</span></span>            | <span data-ttu-id="28b50-173">36</span><span class="sxs-lookup"><span data-stu-id="28b50-173">36</span></span>                                                               |
| <span data-ttu-id="28b50-174">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-174">Search-Flags</span></span>           | <span data-ttu-id="28b50-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b50-175">0x00000000</span></span>                                                       |
| <span data-ttu-id="28b50-176">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-176">System-Flags</span></span>           | <span data-ttu-id="28b50-177">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b50-177">0x00000010</span></span>                                                       |
| <span data-ttu-id="28b50-178">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b50-178">Classes used in</span></span>        | [<span data-ttu-id="28b50-179">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="28b50-179">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="28b50-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="28b50-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="28b50-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-181">Entry</span></span> | <span data-ttu-id="28b50-182">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-182">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="28b50-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b50-183">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-184">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b50-185">System-Only</span></span>            | <span data-ttu-id="28b50-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-186">False</span></span>                                                            |
| <span data-ttu-id="28b50-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b50-187">Is-Single-Valued</span></span>       | <span data-ttu-id="28b50-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-188">False</span></span>                                                            |
| <span data-ttu-id="28b50-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b50-189">Is Indexed</span></span>             | <span data-ttu-id="28b50-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-190">False</span></span>                                                            |
| <span data-ttu-id="28b50-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b50-191">In Global Catalog</span></span>      | <span data-ttu-id="28b50-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-192">False</span></span>                                                            |
| <span data-ttu-id="28b50-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b50-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b50-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b50-194">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="28b50-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b50-195">Range-Lower</span></span>            | <span data-ttu-id="28b50-196">36</span><span class="sxs-lookup"><span data-stu-id="28b50-196">36</span></span>                                                               |
| <span data-ttu-id="28b50-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b50-197">Range-Upper</span></span>            | <span data-ttu-id="28b50-198">36</span><span class="sxs-lookup"><span data-stu-id="28b50-198">36</span></span>                                                               |
| <span data-ttu-id="28b50-199">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-199">Search-Flags</span></span>           | <span data-ttu-id="28b50-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b50-200">0x00000000</span></span>                                                       |
| <span data-ttu-id="28b50-201">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-201">System-Flags</span></span>           | <span data-ttu-id="28b50-202">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b50-202">0x00000010</span></span>                                                       |
| <span data-ttu-id="28b50-203">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b50-203">Classes used in</span></span>        | [<span data-ttu-id="28b50-204">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="28b50-204">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="28b50-205">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28b50-205">Windows Server 2008</span></span>



| <span data-ttu-id="28b50-206">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-206">Entry</span></span> | <span data-ttu-id="28b50-207">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-207">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="28b50-208">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b50-208">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-209">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-209">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b50-210">System-Only</span></span>            | <span data-ttu-id="28b50-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-211">False</span></span>                                                            |
| <span data-ttu-id="28b50-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b50-212">Is-Single-Valued</span></span>       | <span data-ttu-id="28b50-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-213">False</span></span>                                                            |
| <span data-ttu-id="28b50-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b50-214">Is Indexed</span></span>             | <span data-ttu-id="28b50-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-215">False</span></span>                                                            |
| <span data-ttu-id="28b50-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b50-216">In Global Catalog</span></span>      | <span data-ttu-id="28b50-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-217">False</span></span>                                                            |
| <span data-ttu-id="28b50-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b50-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b50-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b50-219">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="28b50-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b50-220">Range-Lower</span></span>            | <span data-ttu-id="28b50-221">36</span><span class="sxs-lookup"><span data-stu-id="28b50-221">36</span></span>                                                               |
| <span data-ttu-id="28b50-222">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b50-222">Range-Upper</span></span>            | <span data-ttu-id="28b50-223">36</span><span class="sxs-lookup"><span data-stu-id="28b50-223">36</span></span>                                                               |
| <span data-ttu-id="28b50-224">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-224">Search-Flags</span></span>           | <span data-ttu-id="28b50-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b50-225">0x00000000</span></span>                                                       |
| <span data-ttu-id="28b50-226">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-226">System-Flags</span></span>           | <span data-ttu-id="28b50-227">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b50-227">0x00000010</span></span>                                                       |
| <span data-ttu-id="28b50-228">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b50-228">Classes used in</span></span>        | [<span data-ttu-id="28b50-229">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="28b50-229">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="28b50-230">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="28b50-230">Windows Server 2008 R2</span></span>



| <span data-ttu-id="28b50-231">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-231">Entry</span></span> | <span data-ttu-id="28b50-232">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-232">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="28b50-233">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b50-233">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-234">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-234">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b50-235">System-Only</span></span>            | <span data-ttu-id="28b50-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-236">False</span></span>                                                            |
| <span data-ttu-id="28b50-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b50-237">Is-Single-Valued</span></span>       | <span data-ttu-id="28b50-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-238">False</span></span>                                                            |
| <span data-ttu-id="28b50-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b50-239">Is Indexed</span></span>             | <span data-ttu-id="28b50-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-240">False</span></span>                                                            |
| <span data-ttu-id="28b50-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b50-241">In Global Catalog</span></span>      | <span data-ttu-id="28b50-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-242">False</span></span>                                                            |
| <span data-ttu-id="28b50-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b50-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b50-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b50-244">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="28b50-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b50-245">Range-Lower</span></span>            | <span data-ttu-id="28b50-246">36</span><span class="sxs-lookup"><span data-stu-id="28b50-246">36</span></span>                                                               |
| <span data-ttu-id="28b50-247">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b50-247">Range-Upper</span></span>            | <span data-ttu-id="28b50-248">36</span><span class="sxs-lookup"><span data-stu-id="28b50-248">36</span></span>                                                               |
| <span data-ttu-id="28b50-249">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-249">Search-Flags</span></span>           | <span data-ttu-id="28b50-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b50-250">0x00000000</span></span>                                                       |
| <span data-ttu-id="28b50-251">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-251">System-Flags</span></span>           | <span data-ttu-id="28b50-252">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b50-252">0x00000010</span></span>                                                       |
| <span data-ttu-id="28b50-253">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b50-253">Classes used in</span></span>        | [<span data-ttu-id="28b50-254">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="28b50-254">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="28b50-255">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28b50-255">Windows Server 2012</span></span>



| <span data-ttu-id="28b50-256">Ввод</span><span class="sxs-lookup"><span data-stu-id="28b50-256">Entry</span></span> | <span data-ttu-id="28b50-257">Значение</span><span class="sxs-lookup"><span data-stu-id="28b50-257">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="28b50-258">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="28b50-258">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-259">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="28b50-259">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="28b50-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="28b50-260">System-Only</span></span>            | <span data-ttu-id="28b50-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-261">False</span></span>                                                            |
| <span data-ttu-id="28b50-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="28b50-262">Is-Single-Valued</span></span>       | <span data-ttu-id="28b50-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-263">False</span></span>                                                            |
| <span data-ttu-id="28b50-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="28b50-264">Is Indexed</span></span>             | <span data-ttu-id="28b50-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-265">False</span></span>                                                            |
| <span data-ttu-id="28b50-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="28b50-266">In Global Catalog</span></span>      | <span data-ttu-id="28b50-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="28b50-267">False</span></span>                                                            |
| <span data-ttu-id="28b50-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="28b50-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="28b50-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="28b50-269">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="28b50-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="28b50-270">Range-Lower</span></span>            | <span data-ttu-id="28b50-271">36</span><span class="sxs-lookup"><span data-stu-id="28b50-271">36</span></span>                                                               |
| <span data-ttu-id="28b50-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="28b50-272">Range-Upper</span></span>            | <span data-ttu-id="28b50-273">36</span><span class="sxs-lookup"><span data-stu-id="28b50-273">36</span></span>                                                               |
| <span data-ttu-id="28b50-274">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-274">Search-Flags</span></span>           | <span data-ttu-id="28b50-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="28b50-275">0x00000000</span></span>                                                       |
| <span data-ttu-id="28b50-276">System-Flags</span><span class="sxs-lookup"><span data-stu-id="28b50-276">System-Flags</span></span>           | <span data-ttu-id="28b50-277">0x00000010</span><span class="sxs-lookup"><span data-stu-id="28b50-277">0x00000010</span></span>                                                       |
| <span data-ttu-id="28b50-278">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="28b50-278">Classes used in</span></span>        | [<span data-ttu-id="28b50-279">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="28b50-279">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





