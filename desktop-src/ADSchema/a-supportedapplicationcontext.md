---
title: Поддерживается — атрибут контекста приложения
description: Указывает идентификаторы объектов контекстов приложений, поддерживаемых приложением OSI.
ms.assetid: 803d68bc-4537-4a45-bd86-b0558076e4df
ms.tgt_platform: multiple
keywords:
- Поддерживается — схема AD атрибута приложения-контекста
- Схема AD атрибута Суппортедаппликатионконтекст
topic_type:
- apiref
api_name:
- Supported-Application-Context
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29512a4d9588a8097ca531acd477c08b0e316876
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536128"
---
# <a name="supported-application-context-attribute"></a><span data-ttu-id="b7dde-105">Поддерживается — атрибут контекста приложения</span><span class="sxs-lookup"><span data-stu-id="b7dde-105">Supported-Application-Context attribute</span></span>

<span data-ttu-id="b7dde-106">Указывает идентификаторы объектов контекстов приложений, поддерживаемых приложением OSI.</span><span class="sxs-lookup"><span data-stu-id="b7dde-106">Specifies the object identifiers of application contexts that an OSI application supports.</span></span>



| <span data-ttu-id="b7dde-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-107">Entry</span></span> | <span data-ttu-id="b7dde-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b7dde-109">CN</span><span class="sxs-lookup"><span data-stu-id="b7dde-109">CN</span></span>                | <span data-ttu-id="b7dde-110">Поддерживается — контекст приложения</span><span class="sxs-lookup"><span data-stu-id="b7dde-110">Supported-Application-Context</span></span>                         |
| <span data-ttu-id="b7dde-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="b7dde-111">Ldap-Display-Name</span></span> | <span data-ttu-id="b7dde-112">суппортедаппликатионконтекст</span><span class="sxs-lookup"><span data-stu-id="b7dde-112">supportedApplicationContext</span></span>                           |
| <span data-ttu-id="b7dde-113">Размер</span><span class="sxs-lookup"><span data-stu-id="b7dde-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="b7dde-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="b7dde-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="b7dde-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="b7dde-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="b7dde-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-116">Attribute-Id</span></span>      | <span data-ttu-id="b7dde-117">2.5.4.30</span><span class="sxs-lookup"><span data-stu-id="b7dde-117">2.5.4.30</span></span>                                              |
| <span data-ttu-id="b7dde-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="b7dde-118">System-Id-Guid</span></span>    | <span data-ttu-id="b7dde-119">1677588f-47f3-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="b7dde-119">1677588f-47f3-11d1-a9c3-0000f80367c1</span></span>                  |
| <span data-ttu-id="b7dde-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7dde-120">Syntax</span></span>            | [<span data-ttu-id="b7dde-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="b7dde-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="b7dde-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="b7dde-122">Implementations</span></span>

-   [<span data-ttu-id="b7dde-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="b7dde-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="b7dde-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="b7dde-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="b7dde-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="b7dde-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="b7dde-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="b7dde-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="b7dde-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="b7dde-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="b7dde-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="b7dde-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="b7dde-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b7dde-129">Windows 2000 Server</span></span>



| <span data-ttu-id="b7dde-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-130">Entry</span></span> | <span data-ttu-id="b7dde-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dde-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7dde-132">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-133">MAPI-Id</span></span>                | <span data-ttu-id="b7dde-134">0x813D</span><span class="sxs-lookup"><span data-stu-id="b7dde-134">0x813D</span></span>                                                                                                                              |
| <span data-ttu-id="b7dde-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7dde-135">System-Only</span></span>            | <span data-ttu-id="b7dde-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-136">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7dde-137">Is-Single-Valued</span></span>       | <span data-ttu-id="b7dde-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-138">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7dde-139">Is Indexed</span></span>             | <span data-ttu-id="b7dde-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-140">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7dde-141">In Global Catalog</span></span>      | <span data-ttu-id="b7dde-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-142">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7dde-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7dde-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7dde-144">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="b7dde-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7dde-145">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7dde-146">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-147">Search-Flags</span></span>           | <span data-ttu-id="b7dde-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-148">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-149">System-Flags</span></span>           | <span data-ttu-id="b7dde-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-150">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7dde-151">Classes used in</span></span>        | [<span data-ttu-id="b7dde-152">**Сущность приложения**</span><span class="sxs-lookup"><span data-stu-id="b7dde-152">**Application-Entity**</span></span>](c-applicationentity.md)<br/> [<span data-ttu-id="b7dde-153">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="b7dde-153">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="b7dde-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7dde-154">Windows Server 2003</span></span>



| <span data-ttu-id="b7dde-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-155">Entry</span></span> | <span data-ttu-id="b7dde-156">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dde-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7dde-157">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-158">MAPI-Id</span></span>                | <span data-ttu-id="b7dde-159">0x813D</span><span class="sxs-lookup"><span data-stu-id="b7dde-159">0x813D</span></span>                                                                                                                              |
| <span data-ttu-id="b7dde-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7dde-160">System-Only</span></span>            | <span data-ttu-id="b7dde-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-161">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7dde-162">Is-Single-Valued</span></span>       | <span data-ttu-id="b7dde-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-163">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7dde-164">Is Indexed</span></span>             | <span data-ttu-id="b7dde-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-165">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7dde-166">In Global Catalog</span></span>      | <span data-ttu-id="b7dde-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-167">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7dde-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7dde-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7dde-169">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="b7dde-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7dde-170">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7dde-171">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-172">Search-Flags</span></span>           | <span data-ttu-id="b7dde-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-173">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-174">System-Flags</span></span>           | <span data-ttu-id="b7dde-175">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-175">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7dde-176">Classes used in</span></span>        | [<span data-ttu-id="b7dde-177">**Сущность приложения**</span><span class="sxs-lookup"><span data-stu-id="b7dde-177">**Application-Entity**</span></span>](c-applicationentity.md)<br/> [<span data-ttu-id="b7dde-178">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="b7dde-178">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="b7dde-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="b7dde-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="b7dde-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-180">Entry</span></span> | <span data-ttu-id="b7dde-181">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dde-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7dde-182">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-183">MAPI-Id</span></span>                | <span data-ttu-id="b7dde-184">0x813D</span><span class="sxs-lookup"><span data-stu-id="b7dde-184">0x813D</span></span>                                                                                                                              |
| <span data-ttu-id="b7dde-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7dde-185">System-Only</span></span>            | <span data-ttu-id="b7dde-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-186">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7dde-187">Is-Single-Valued</span></span>       | <span data-ttu-id="b7dde-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-188">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7dde-189">Is Indexed</span></span>             | <span data-ttu-id="b7dde-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-190">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7dde-191">In Global Catalog</span></span>      | <span data-ttu-id="b7dde-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-192">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7dde-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7dde-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7dde-194">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="b7dde-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7dde-195">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7dde-196">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-197">Search-Flags</span></span>           | <span data-ttu-id="b7dde-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-198">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-199">System-Flags</span></span>           | <span data-ttu-id="b7dde-200">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-200">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7dde-201">Classes used in</span></span>        | [<span data-ttu-id="b7dde-202">**Сущность приложения**</span><span class="sxs-lookup"><span data-stu-id="b7dde-202">**Application-Entity**</span></span>](c-applicationentity.md)<br/> [<span data-ttu-id="b7dde-203">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="b7dde-203">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="b7dde-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7dde-204">Windows Server 2008</span></span>



| <span data-ttu-id="b7dde-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-205">Entry</span></span> | <span data-ttu-id="b7dde-206">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dde-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7dde-207">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-208">MAPI-Id</span></span>                | <span data-ttu-id="b7dde-209">0x813D</span><span class="sxs-lookup"><span data-stu-id="b7dde-209">0x813D</span></span>                                                                                                                              |
| <span data-ttu-id="b7dde-210">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7dde-210">System-Only</span></span>            | <span data-ttu-id="b7dde-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-211">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-212">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7dde-212">Is-Single-Valued</span></span>       | <span data-ttu-id="b7dde-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-213">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-214">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7dde-214">Is Indexed</span></span>             | <span data-ttu-id="b7dde-215">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-215">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-216">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7dde-216">In Global Catalog</span></span>      | <span data-ttu-id="b7dde-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-217">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-218">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7dde-218">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7dde-219">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7dde-219">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="b7dde-220">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7dde-220">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-221">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7dde-221">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-222">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-222">Search-Flags</span></span>           | <span data-ttu-id="b7dde-223">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-223">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-224">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-224">System-Flags</span></span>           | <span data-ttu-id="b7dde-225">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-225">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-226">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7dde-226">Classes used in</span></span>        | [<span data-ttu-id="b7dde-227">**Сущность приложения**</span><span class="sxs-lookup"><span data-stu-id="b7dde-227">**Application-Entity**</span></span>](c-applicationentity.md)<br/> [<span data-ttu-id="b7dde-228">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="b7dde-228">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="b7dde-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7dde-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="b7dde-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-230">Entry</span></span> | <span data-ttu-id="b7dde-231">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dde-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7dde-232">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-233">MAPI-Id</span></span>                | <span data-ttu-id="b7dde-234">0x813D</span><span class="sxs-lookup"><span data-stu-id="b7dde-234">0x813D</span></span>                                                                                                                              |
| <span data-ttu-id="b7dde-235">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7dde-235">System-Only</span></span>            | <span data-ttu-id="b7dde-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-236">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-237">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7dde-237">Is-Single-Valued</span></span>       | <span data-ttu-id="b7dde-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-238">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-239">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7dde-239">Is Indexed</span></span>             | <span data-ttu-id="b7dde-240">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-240">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-241">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7dde-241">In Global Catalog</span></span>      | <span data-ttu-id="b7dde-242">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-242">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-243">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7dde-243">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7dde-244">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7dde-244">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="b7dde-245">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7dde-245">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-246">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7dde-246">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-247">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-247">Search-Flags</span></span>           | <span data-ttu-id="b7dde-248">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-248">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-249">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-249">System-Flags</span></span>           | <span data-ttu-id="b7dde-250">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-250">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-251">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7dde-251">Classes used in</span></span>        | [<span data-ttu-id="b7dde-252">**Сущность приложения**</span><span class="sxs-lookup"><span data-stu-id="b7dde-252">**Application-Entity**</span></span>](c-applicationentity.md)<br/> [<span data-ttu-id="b7dde-253">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="b7dde-253">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="b7dde-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7dde-254">Windows Server 2012</span></span>



| <span data-ttu-id="b7dde-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="b7dde-255">Entry</span></span> | <span data-ttu-id="b7dde-256">Значение</span><span class="sxs-lookup"><span data-stu-id="b7dde-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dde-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="b7dde-257">Link-Id</span></span>                | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="b7dde-258">MAPI-Id</span></span>                | <span data-ttu-id="b7dde-259">0x813D</span><span class="sxs-lookup"><span data-stu-id="b7dde-259">0x813D</span></span>                                                                                                                              |
| <span data-ttu-id="b7dde-260">System-Only</span><span class="sxs-lookup"><span data-stu-id="b7dde-260">System-Only</span></span>            | <span data-ttu-id="b7dde-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-261">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-262">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="b7dde-262">Is-Single-Valued</span></span>       | <span data-ttu-id="b7dde-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-263">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-264">Индексируется</span><span class="sxs-lookup"><span data-stu-id="b7dde-264">Is Indexed</span></span>             | <span data-ttu-id="b7dde-265">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-265">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-266">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="b7dde-266">In Global Catalog</span></span>      | <span data-ttu-id="b7dde-267">Неверно</span><span class="sxs-lookup"><span data-stu-id="b7dde-267">False</span></span>                                                                                                                               |
| <span data-ttu-id="b7dde-268">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="b7dde-268">NT-Security-Descriptor</span></span> | <span data-ttu-id="b7dde-269">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="b7dde-269">O:BAG:BAD:S:</span></span>                                                                                                                        |
| <span data-ttu-id="b7dde-270">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="b7dde-270">Range-Lower</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-271">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="b7dde-271">Range-Upper</span></span>            | \-                                                                                                                                  |
| <span data-ttu-id="b7dde-272">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-272">Search-Flags</span></span>           | <span data-ttu-id="b7dde-273">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-273">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-274">System-Flags</span><span class="sxs-lookup"><span data-stu-id="b7dde-274">System-Flags</span></span>           | <span data-ttu-id="b7dde-275">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b7dde-275">0x00000000</span></span>                                                                                                                          |
| <span data-ttu-id="b7dde-276">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="b7dde-276">Classes used in</span></span>        | [<span data-ttu-id="b7dde-277">**Сущность приложения**</span><span class="sxs-lookup"><span data-stu-id="b7dde-277">**Application-Entity**</span></span>](c-applicationentity.md)<br/> [<span data-ttu-id="b7dde-278">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="b7dde-278">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





