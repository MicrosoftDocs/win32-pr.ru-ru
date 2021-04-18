---
title: Атрибут COM-ProgID
description: Этот атрибут хранит список идентификаторов программных объектов COM, реализованных в этом пакете приложения.
ms.assetid: 9d2945e4-f236-48f6-bed3-145d445ff653
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута COM-ProgID
- Схема AD атрибута Компрогид
topic_type:
- apiref
api_name:
- COM-ProgID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686976732bedf2c4ba486186634720568d3b6c3c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655532"
---
# <a name="com-progid-attribute"></a><span data-ttu-id="536a5-105">Атрибут COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="536a5-105">COM-ProgID attribute</span></span>

<span data-ttu-id="536a5-106">Этот атрибут хранит список идентификаторов программных объектов COM, реализованных в этом пакете приложения.</span><span class="sxs-lookup"><span data-stu-id="536a5-106">This attribute stores the list of COM object program IDs that are implemented in this application package.</span></span>



| <span data-ttu-id="536a5-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-107">Entry</span></span> | <span data-ttu-id="536a5-108">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-109">CN</span><span class="sxs-lookup"><span data-stu-id="536a5-109">CN</span></span>                | <span data-ttu-id="536a5-110">COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="536a5-110">COM-ProgID</span></span>                                                                       |
| <span data-ttu-id="536a5-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="536a5-111">Ldap-Display-Name</span></span> | <span data-ttu-id="536a5-112">компрогид</span><span class="sxs-lookup"><span data-stu-id="536a5-112">cOMProgID</span></span>                                                                        |
| <span data-ttu-id="536a5-113">Размер</span><span class="sxs-lookup"><span data-stu-id="536a5-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="536a5-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="536a5-114">Update Privilege</span></span>  | <span data-ttu-id="536a5-115">Любой пользователь может обновить этот объект на основе безопасности создаваемого объекта.</span><span class="sxs-lookup"><span data-stu-id="536a5-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="536a5-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="536a5-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="536a5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-117">Attribute-Id</span></span>      | <span data-ttu-id="536a5-118">1.2.840.113556.1.4.21</span><span class="sxs-lookup"><span data-stu-id="536a5-118">1.2.840.113556.1.4.21</span></span>                                                            |
| <span data-ttu-id="536a5-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="536a5-119">System-Id-Guid</span></span>    | <span data-ttu-id="536a5-120">bf96793d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="536a5-120">bf96793d-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="536a5-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="536a5-121">Syntax</span></span>            | [<span data-ttu-id="536a5-122">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="536a5-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="536a5-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="536a5-123">Implementations</span></span>

-   [<span data-ttu-id="536a5-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="536a5-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="536a5-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="536a5-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="536a5-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="536a5-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="536a5-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="536a5-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="536a5-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="536a5-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="536a5-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="536a5-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="536a5-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="536a5-130">Windows 2000 Server</span></span>



| <span data-ttu-id="536a5-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-131">Entry</span></span> | <span data-ttu-id="536a5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="536a5-133">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-134">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="536a5-135">System-Only</span></span>            | <span data-ttu-id="536a5-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-136">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="536a5-137">Is-Single-Valued</span></span>       | <span data-ttu-id="536a5-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-138">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="536a5-139">Is Indexed</span></span>             | <span data-ttu-id="536a5-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-140">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="536a5-141">In Global Catalog</span></span>      | <span data-ttu-id="536a5-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-142">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="536a5-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="536a5-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="536a5-144">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="536a5-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="536a5-145">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="536a5-146">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-147">Search-Flags</span></span>           | <span data-ttu-id="536a5-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536a5-148">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-149">System-Flags</span></span>           | <span data-ttu-id="536a5-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="536a5-150">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="536a5-151">Classes used in</span></span>        | [<span data-ttu-id="536a5-152">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="536a5-152">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="536a5-153">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="536a5-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="536a5-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="536a5-154">Windows Server 2003</span></span>



| <span data-ttu-id="536a5-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-155">Entry</span></span> | <span data-ttu-id="536a5-156">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="536a5-157">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-158">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="536a5-159">System-Only</span></span>            | <span data-ttu-id="536a5-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-160">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="536a5-161">Is-Single-Valued</span></span>       | <span data-ttu-id="536a5-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-162">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="536a5-163">Is Indexed</span></span>             | <span data-ttu-id="536a5-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-164">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="536a5-165">In Global Catalog</span></span>      | <span data-ttu-id="536a5-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-166">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="536a5-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="536a5-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="536a5-168">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="536a5-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="536a5-169">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="536a5-170">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-171">Search-Flags</span></span>           | <span data-ttu-id="536a5-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536a5-172">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-173">System-Flags</span></span>           | <span data-ttu-id="536a5-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="536a5-174">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="536a5-175">Classes used in</span></span>        | [<span data-ttu-id="536a5-176">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="536a5-176">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="536a5-177">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="536a5-177">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="536a5-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="536a5-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="536a5-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-179">Entry</span></span> | <span data-ttu-id="536a5-180">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="536a5-181">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-182">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="536a5-183">System-Only</span></span>            | <span data-ttu-id="536a5-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-184">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="536a5-185">Is-Single-Valued</span></span>       | <span data-ttu-id="536a5-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-186">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="536a5-187">Is Indexed</span></span>             | <span data-ttu-id="536a5-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-188">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="536a5-189">In Global Catalog</span></span>      | <span data-ttu-id="536a5-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-190">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="536a5-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="536a5-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="536a5-192">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="536a5-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="536a5-193">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="536a5-194">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-195">Search-Flags</span></span>           | <span data-ttu-id="536a5-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536a5-196">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-197">System-Flags</span></span>           | <span data-ttu-id="536a5-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="536a5-198">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="536a5-199">Classes used in</span></span>        | [<span data-ttu-id="536a5-200">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="536a5-200">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="536a5-201">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="536a5-201">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="536a5-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="536a5-202">Windows Server 2008</span></span>



| <span data-ttu-id="536a5-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-203">Entry</span></span> | <span data-ttu-id="536a5-204">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="536a5-205">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-206">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="536a5-207">System-Only</span></span>            | <span data-ttu-id="536a5-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-208">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="536a5-209">Is-Single-Valued</span></span>       | <span data-ttu-id="536a5-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-210">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="536a5-211">Is Indexed</span></span>             | <span data-ttu-id="536a5-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-212">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="536a5-213">In Global Catalog</span></span>      | <span data-ttu-id="536a5-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-214">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="536a5-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="536a5-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="536a5-216">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="536a5-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="536a5-217">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="536a5-218">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-219">Search-Flags</span></span>           | <span data-ttu-id="536a5-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536a5-220">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-221">System-Flags</span></span>           | <span data-ttu-id="536a5-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="536a5-222">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="536a5-223">Classes used in</span></span>        | [<span data-ttu-id="536a5-224">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="536a5-224">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="536a5-225">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="536a5-225">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="536a5-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="536a5-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="536a5-227">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-227">Entry</span></span> | <span data-ttu-id="536a5-228">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-229">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="536a5-229">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-230">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="536a5-231">System-Only</span></span>            | <span data-ttu-id="536a5-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-232">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-233">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="536a5-233">Is-Single-Valued</span></span>       | <span data-ttu-id="536a5-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-234">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-235">Индексируется</span><span class="sxs-lookup"><span data-stu-id="536a5-235">Is Indexed</span></span>             | <span data-ttu-id="536a5-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-236">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-237">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="536a5-237">In Global Catalog</span></span>      | <span data-ttu-id="536a5-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-238">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-239">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="536a5-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="536a5-240">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="536a5-240">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="536a5-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="536a5-241">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="536a5-242">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-243">Search-Flags</span></span>           | <span data-ttu-id="536a5-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536a5-244">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-245">System-Flags</span></span>           | <span data-ttu-id="536a5-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="536a5-246">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-247">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="536a5-247">Classes used in</span></span>        | [<span data-ttu-id="536a5-248">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="536a5-248">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="536a5-249">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="536a5-249">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="536a5-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="536a5-250">Windows Server 2012</span></span>



| <span data-ttu-id="536a5-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="536a5-251">Entry</span></span> | <span data-ttu-id="536a5-252">Значение</span><span class="sxs-lookup"><span data-stu-id="536a5-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536a5-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="536a5-253">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="536a5-254">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="536a5-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="536a5-255">System-Only</span></span>            | <span data-ttu-id="536a5-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-256">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="536a5-257">Is-Single-Valued</span></span>       | <span data-ttu-id="536a5-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-258">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="536a5-259">Is Indexed</span></span>             | <span data-ttu-id="536a5-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-260">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="536a5-261">In Global Catalog</span></span>      | <span data-ttu-id="536a5-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="536a5-262">False</span></span>                                                                                                                         |
| <span data-ttu-id="536a5-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="536a5-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="536a5-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="536a5-264">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="536a5-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="536a5-265">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="536a5-266">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="536a5-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-267">Search-Flags</span></span>           | <span data-ttu-id="536a5-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="536a5-268">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="536a5-269">System-Flags</span></span>           | <span data-ttu-id="536a5-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="536a5-270">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="536a5-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="536a5-271">Classes used in</span></span>        | [<span data-ttu-id="536a5-272">**Регистрация класса**</span><span class="sxs-lookup"><span data-stu-id="536a5-272">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="536a5-273">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="536a5-273">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





