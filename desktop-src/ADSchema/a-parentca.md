---
title: Атрибут parent — CA
description: Различающееся имя объекта центра сертификации (ЦС) для родительского ЦС.
ms.assetid: ccb5b338-e67d-4f1b-b13c-257746ab39d1
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута родительского ЦС
- Схема AD атрибута Парентка
topic_type:
- apiref
api_name:
- Parent-CA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4c065c86548769ab8643a561c7aec3132728d5d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138802"
---
# <a name="parent-ca-attribute"></a><span data-ttu-id="adf6c-105">Атрибут parent — CA</span><span class="sxs-lookup"><span data-stu-id="adf6c-105">Parent-CA attribute</span></span>

<span data-ttu-id="adf6c-106">Различающееся имя объекта центра сертификации (ЦС) для родительского ЦС.</span><span class="sxs-lookup"><span data-stu-id="adf6c-106">The distinguished name of a certification authority (CA) object for a parent CA.</span></span>



| <span data-ttu-id="adf6c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-107">Entry</span></span> | <span data-ttu-id="adf6c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="adf6c-109">CN</span><span class="sxs-lookup"><span data-stu-id="adf6c-109">CN</span></span>                | <span data-ttu-id="adf6c-110">Родительский ЦС</span><span class="sxs-lookup"><span data-stu-id="adf6c-110">Parent-CA</span></span>                               |
| <span data-ttu-id="adf6c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="adf6c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="adf6c-112">парентка</span><span class="sxs-lookup"><span data-stu-id="adf6c-112">parentCA</span></span>                                |
| <span data-ttu-id="adf6c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="adf6c-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="adf6c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="adf6c-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="adf6c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="adf6c-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="adf6c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-116">Attribute-Id</span></span>      | <span data-ttu-id="adf6c-117">1.2.840.113556.1.4.557</span><span class="sxs-lookup"><span data-stu-id="adf6c-117">1.2.840.113556.1.4.557</span></span>                  |
| <span data-ttu-id="adf6c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="adf6c-118">System-Id-Guid</span></span>    | <span data-ttu-id="adf6c-119">5245801b-ca6a-11d0-afff-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="adf6c-119">5245801b-ca6a-11d0-afff-0000f80367c1</span></span>    |
| <span data-ttu-id="adf6c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adf6c-120">Syntax</span></span>            | [<span data-ttu-id="adf6c-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="adf6c-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="adf6c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="adf6c-122">Implementations</span></span>

-   [<span data-ttu-id="adf6c-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="adf6c-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="adf6c-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="adf6c-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="adf6c-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="adf6c-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="adf6c-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="adf6c-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="adf6c-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="adf6c-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="adf6c-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="adf6c-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="adf6c-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="adf6c-129">Windows 2000 Server</span></span>



| <span data-ttu-id="adf6c-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-130">Entry</span></span> | <span data-ttu-id="adf6c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="adf6c-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="adf6c-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf6c-134">System-Only</span></span>            | <span data-ttu-id="adf6c-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-135">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="adf6c-136">Is-Single-Valued</span></span>       | <span data-ttu-id="adf6c-137">True</span><span class="sxs-lookup"><span data-stu-id="adf6c-137">True</span></span>                                                                   |
| <span data-ttu-id="adf6c-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="adf6c-138">Is Indexed</span></span>             | <span data-ttu-id="adf6c-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-139">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="adf6c-140">In Global Catalog</span></span>      | <span data-ttu-id="adf6c-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-141">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="adf6c-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf6c-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf6c-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="adf6c-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf6c-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf6c-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-146">Search-Flags</span></span>           | <span data-ttu-id="adf6c-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf6c-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="adf6c-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-148">System-Flags</span></span>           | <span data-ttu-id="adf6c-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf6c-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="adf6c-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="adf6c-150">Classes used in</span></span>        | [<span data-ttu-id="adf6c-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="adf6c-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="adf6c-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="adf6c-152">Windows Server 2003</span></span>



| <span data-ttu-id="adf6c-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-153">Entry</span></span> | <span data-ttu-id="adf6c-154">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="adf6c-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="adf6c-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf6c-157">System-Only</span></span>            | <span data-ttu-id="adf6c-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-158">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="adf6c-159">Is-Single-Valued</span></span>       | <span data-ttu-id="adf6c-160">True</span><span class="sxs-lookup"><span data-stu-id="adf6c-160">True</span></span>                                                                   |
| <span data-ttu-id="adf6c-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="adf6c-161">Is Indexed</span></span>             | <span data-ttu-id="adf6c-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-162">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="adf6c-163">In Global Catalog</span></span>      | <span data-ttu-id="adf6c-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-164">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="adf6c-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf6c-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf6c-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="adf6c-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf6c-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf6c-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-169">Search-Flags</span></span>           | <span data-ttu-id="adf6c-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf6c-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="adf6c-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-171">System-Flags</span></span>           | <span data-ttu-id="adf6c-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf6c-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="adf6c-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="adf6c-173">Classes used in</span></span>        | [<span data-ttu-id="adf6c-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="adf6c-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="adf6c-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="adf6c-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="adf6c-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-176">Entry</span></span> | <span data-ttu-id="adf6c-177">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="adf6c-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="adf6c-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf6c-180">System-Only</span></span>            | <span data-ttu-id="adf6c-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-181">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="adf6c-182">Is-Single-Valued</span></span>       | <span data-ttu-id="adf6c-183">True</span><span class="sxs-lookup"><span data-stu-id="adf6c-183">True</span></span>                                                                   |
| <span data-ttu-id="adf6c-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="adf6c-184">Is Indexed</span></span>             | <span data-ttu-id="adf6c-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-185">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="adf6c-186">In Global Catalog</span></span>      | <span data-ttu-id="adf6c-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-187">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="adf6c-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf6c-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf6c-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="adf6c-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf6c-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf6c-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-192">Search-Flags</span></span>           | <span data-ttu-id="adf6c-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf6c-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="adf6c-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-194">System-Flags</span></span>           | <span data-ttu-id="adf6c-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf6c-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="adf6c-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="adf6c-196">Classes used in</span></span>        | [<span data-ttu-id="adf6c-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="adf6c-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="adf6c-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adf6c-198">Windows Server 2008</span></span>



| <span data-ttu-id="adf6c-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-199">Entry</span></span> | <span data-ttu-id="adf6c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="adf6c-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="adf6c-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf6c-203">System-Only</span></span>            | <span data-ttu-id="adf6c-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-204">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="adf6c-205">Is-Single-Valued</span></span>       | <span data-ttu-id="adf6c-206">True</span><span class="sxs-lookup"><span data-stu-id="adf6c-206">True</span></span>                                                                   |
| <span data-ttu-id="adf6c-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="adf6c-207">Is Indexed</span></span>             | <span data-ttu-id="adf6c-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-208">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="adf6c-209">In Global Catalog</span></span>      | <span data-ttu-id="adf6c-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-210">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="adf6c-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf6c-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf6c-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="adf6c-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf6c-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf6c-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-215">Search-Flags</span></span>           | <span data-ttu-id="adf6c-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf6c-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="adf6c-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-217">System-Flags</span></span>           | <span data-ttu-id="adf6c-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf6c-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="adf6c-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="adf6c-219">Classes used in</span></span>        | [<span data-ttu-id="adf6c-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="adf6c-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="adf6c-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="adf6c-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="adf6c-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-222">Entry</span></span> | <span data-ttu-id="adf6c-223">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="adf6c-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="adf6c-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf6c-226">System-Only</span></span>            | <span data-ttu-id="adf6c-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-227">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="adf6c-228">Is-Single-Valued</span></span>       | <span data-ttu-id="adf6c-229">True</span><span class="sxs-lookup"><span data-stu-id="adf6c-229">True</span></span>                                                                   |
| <span data-ttu-id="adf6c-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="adf6c-230">Is Indexed</span></span>             | <span data-ttu-id="adf6c-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-231">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="adf6c-232">In Global Catalog</span></span>      | <span data-ttu-id="adf6c-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-233">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="adf6c-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf6c-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf6c-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="adf6c-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf6c-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf6c-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-238">Search-Flags</span></span>           | <span data-ttu-id="adf6c-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf6c-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="adf6c-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-240">System-Flags</span></span>           | <span data-ttu-id="adf6c-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf6c-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="adf6c-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="adf6c-242">Classes used in</span></span>        | [<span data-ttu-id="adf6c-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="adf6c-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="adf6c-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="adf6c-244">Windows Server 2012</span></span>



| <span data-ttu-id="adf6c-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="adf6c-245">Entry</span></span> | <span data-ttu-id="adf6c-246">Значение</span><span class="sxs-lookup"><span data-stu-id="adf6c-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="adf6c-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="adf6c-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="adf6c-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="adf6c-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="adf6c-249">System-Only</span></span>            | <span data-ttu-id="adf6c-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-250">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="adf6c-251">Is-Single-Valued</span></span>       | <span data-ttu-id="adf6c-252">True</span><span class="sxs-lookup"><span data-stu-id="adf6c-252">True</span></span>                                                                   |
| <span data-ttu-id="adf6c-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="adf6c-253">Is Indexed</span></span>             | <span data-ttu-id="adf6c-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-254">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="adf6c-255">In Global Catalog</span></span>      | <span data-ttu-id="adf6c-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="adf6c-256">False</span></span>                                                                  |
| <span data-ttu-id="adf6c-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="adf6c-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="adf6c-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="adf6c-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="adf6c-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="adf6c-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="adf6c-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="adf6c-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-261">Search-Flags</span></span>           | <span data-ttu-id="adf6c-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="adf6c-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="adf6c-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="adf6c-263">System-Flags</span></span>           | <span data-ttu-id="adf6c-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="adf6c-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="adf6c-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="adf6c-265">Classes used in</span></span>        | [<span data-ttu-id="adf6c-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="adf6c-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





