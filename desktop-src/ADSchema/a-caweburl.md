---
title: Атрибут CA-WEB-URL
description: URL-адрес для HTTP-подключения к центру сертификации.
ms.assetid: 148bab57-25ae-467a-86a2-dbf83e69979e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута CA-WEB-URL
- Схема AD атрибута Кавебурл
topic_type:
- apiref
api_name:
- CA-WEB-URL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42b49efb851b0720499f5b641770279c12cb9563
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138291"
---
# <a name="ca-web-url-attribute"></a><span data-ttu-id="3d40a-105">Атрибут CA-WEB-URL</span><span class="sxs-lookup"><span data-stu-id="3d40a-105">CA-WEB-URL attribute</span></span>

<span data-ttu-id="3d40a-106">URL-адрес для HTTP-подключения к центру сертификации.</span><span class="sxs-lookup"><span data-stu-id="3d40a-106">URL for http connection to a certification authority.</span></span>



| <span data-ttu-id="3d40a-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-107">Entry</span></span> | <span data-ttu-id="3d40a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="3d40a-109">CN</span><span class="sxs-lookup"><span data-stu-id="3d40a-109">CN</span></span>                | <span data-ttu-id="3d40a-110">CA-WEB-URL</span><span class="sxs-lookup"><span data-stu-id="3d40a-110">CA-WEB-URL</span></span>                                  |
| <span data-ttu-id="3d40a-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="3d40a-111">Ldap-Display-Name</span></span> | <span data-ttu-id="3d40a-112">кавебурл</span><span class="sxs-lookup"><span data-stu-id="3d40a-112">cAWEBURL</span></span>                                    |
| <span data-ttu-id="3d40a-113">Размер</span><span class="sxs-lookup"><span data-stu-id="3d40a-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="3d40a-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="3d40a-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="3d40a-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="3d40a-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="3d40a-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-116">Attribute-Id</span></span>      | <span data-ttu-id="3d40a-117">1.2.840.113556.1.4.688</span><span class="sxs-lookup"><span data-stu-id="3d40a-117">1.2.840.113556.1.4.688</span></span>                      |
| <span data-ttu-id="3d40a-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="3d40a-118">System-Id-Guid</span></span>    | <span data-ttu-id="3d40a-119">963d2736-48be-11d1-a9c3-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="3d40a-119">963d2736-48be-11d1-a9c3-0000f80367c1</span></span>        |
| <span data-ttu-id="3d40a-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d40a-120">Syntax</span></span>            | [<span data-ttu-id="3d40a-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="3d40a-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="3d40a-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="3d40a-122">Implementations</span></span>

-   [<span data-ttu-id="3d40a-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="3d40a-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="3d40a-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="3d40a-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="3d40a-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="3d40a-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="3d40a-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="3d40a-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="3d40a-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="3d40a-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="3d40a-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3d40a-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="3d40a-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d40a-129">Windows 2000 Server</span></span>



| <span data-ttu-id="3d40a-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-130">Entry</span></span> | <span data-ttu-id="3d40a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-131">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3d40a-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d40a-132">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-133">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d40a-134">System-Only</span></span>            | <span data-ttu-id="3d40a-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-135">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d40a-136">Is-Single-Valued</span></span>       | <span data-ttu-id="3d40a-137">True</span><span class="sxs-lookup"><span data-stu-id="3d40a-137">True</span></span>                                                                   |
| <span data-ttu-id="3d40a-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d40a-138">Is Indexed</span></span>             | <span data-ttu-id="3d40a-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-139">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d40a-140">In Global Catalog</span></span>      | <span data-ttu-id="3d40a-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-141">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d40a-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d40a-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d40a-143">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3d40a-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d40a-144">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d40a-145">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-146">Search-Flags</span></span>           | <span data-ttu-id="3d40a-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d40a-147">0x00000000</span></span>                                                             |
| <span data-ttu-id="3d40a-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-148">System-Flags</span></span>           | <span data-ttu-id="3d40a-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d40a-149">0x00000010</span></span>                                                             |
| <span data-ttu-id="3d40a-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d40a-150">Classes used in</span></span>        | [<span data-ttu-id="3d40a-151">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3d40a-151">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="3d40a-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d40a-152">Windows Server 2003</span></span>



| <span data-ttu-id="3d40a-153">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-153">Entry</span></span> | <span data-ttu-id="3d40a-154">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-154">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3d40a-155">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d40a-155">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-156">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-156">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-157">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d40a-157">System-Only</span></span>            | <span data-ttu-id="3d40a-158">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-158">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-159">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d40a-159">Is-Single-Valued</span></span>       | <span data-ttu-id="3d40a-160">True</span><span class="sxs-lookup"><span data-stu-id="3d40a-160">True</span></span>                                                                   |
| <span data-ttu-id="3d40a-161">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d40a-161">Is Indexed</span></span>             | <span data-ttu-id="3d40a-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-162">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-163">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d40a-163">In Global Catalog</span></span>      | <span data-ttu-id="3d40a-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-164">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-165">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d40a-165">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d40a-166">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d40a-166">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3d40a-167">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d40a-167">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d40a-168">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-169">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-169">Search-Flags</span></span>           | <span data-ttu-id="3d40a-170">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d40a-170">0x00000000</span></span>                                                             |
| <span data-ttu-id="3d40a-171">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-171">System-Flags</span></span>           | <span data-ttu-id="3d40a-172">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d40a-172">0x00000010</span></span>                                                             |
| <span data-ttu-id="3d40a-173">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d40a-173">Classes used in</span></span>        | [<span data-ttu-id="3d40a-174">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3d40a-174">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="3d40a-175">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="3d40a-175">Windows Server 2003 R2</span></span>



| <span data-ttu-id="3d40a-176">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-176">Entry</span></span> | <span data-ttu-id="3d40a-177">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-177">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3d40a-178">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d40a-178">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-179">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-179">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-180">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d40a-180">System-Only</span></span>            | <span data-ttu-id="3d40a-181">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-181">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-182">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d40a-182">Is-Single-Valued</span></span>       | <span data-ttu-id="3d40a-183">True</span><span class="sxs-lookup"><span data-stu-id="3d40a-183">True</span></span>                                                                   |
| <span data-ttu-id="3d40a-184">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d40a-184">Is Indexed</span></span>             | <span data-ttu-id="3d40a-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-185">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-186">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d40a-186">In Global Catalog</span></span>      | <span data-ttu-id="3d40a-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-187">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-188">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d40a-188">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d40a-189">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d40a-189">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3d40a-190">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d40a-190">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-191">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d40a-191">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-192">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-192">Search-Flags</span></span>           | <span data-ttu-id="3d40a-193">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d40a-193">0x00000000</span></span>                                                             |
| <span data-ttu-id="3d40a-194">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-194">System-Flags</span></span>           | <span data-ttu-id="3d40a-195">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d40a-195">0x00000010</span></span>                                                             |
| <span data-ttu-id="3d40a-196">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d40a-196">Classes used in</span></span>        | [<span data-ttu-id="3d40a-197">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3d40a-197">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="3d40a-198">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d40a-198">Windows Server 2008</span></span>



| <span data-ttu-id="3d40a-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-199">Entry</span></span> | <span data-ttu-id="3d40a-200">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-200">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3d40a-201">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d40a-201">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-202">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-202">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d40a-203">System-Only</span></span>            | <span data-ttu-id="3d40a-204">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-204">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d40a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="3d40a-206">True</span><span class="sxs-lookup"><span data-stu-id="3d40a-206">True</span></span>                                                                   |
| <span data-ttu-id="3d40a-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d40a-207">Is Indexed</span></span>             | <span data-ttu-id="3d40a-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-208">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d40a-209">In Global Catalog</span></span>      | <span data-ttu-id="3d40a-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-210">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d40a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d40a-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d40a-212">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3d40a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d40a-213">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d40a-214">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-215">Search-Flags</span></span>           | <span data-ttu-id="3d40a-216">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d40a-216">0x00000000</span></span>                                                             |
| <span data-ttu-id="3d40a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-217">System-Flags</span></span>           | <span data-ttu-id="3d40a-218">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d40a-218">0x00000010</span></span>                                                             |
| <span data-ttu-id="3d40a-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d40a-219">Classes used in</span></span>        | [<span data-ttu-id="3d40a-220">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3d40a-220">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="3d40a-221">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3d40a-221">Windows Server 2008 R2</span></span>



| <span data-ttu-id="3d40a-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-222">Entry</span></span> | <span data-ttu-id="3d40a-223">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-223">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3d40a-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d40a-224">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-225">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-226">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d40a-226">System-Only</span></span>            | <span data-ttu-id="3d40a-227">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-227">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-228">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d40a-228">Is-Single-Valued</span></span>       | <span data-ttu-id="3d40a-229">True</span><span class="sxs-lookup"><span data-stu-id="3d40a-229">True</span></span>                                                                   |
| <span data-ttu-id="3d40a-230">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d40a-230">Is Indexed</span></span>             | <span data-ttu-id="3d40a-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-231">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-232">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d40a-232">In Global Catalog</span></span>      | <span data-ttu-id="3d40a-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-233">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-234">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d40a-234">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d40a-235">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d40a-235">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3d40a-236">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d40a-236">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d40a-237">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-238">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-238">Search-Flags</span></span>           | <span data-ttu-id="3d40a-239">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d40a-239">0x00000000</span></span>                                                             |
| <span data-ttu-id="3d40a-240">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-240">System-Flags</span></span>           | <span data-ttu-id="3d40a-241">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d40a-241">0x00000010</span></span>                                                             |
| <span data-ttu-id="3d40a-242">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d40a-242">Classes used in</span></span>        | [<span data-ttu-id="3d40a-243">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3d40a-243">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="3d40a-244">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3d40a-244">Windows Server 2012</span></span>



| <span data-ttu-id="3d40a-245">Ввод</span><span class="sxs-lookup"><span data-stu-id="3d40a-245">Entry</span></span> | <span data-ttu-id="3d40a-246">Значение</span><span class="sxs-lookup"><span data-stu-id="3d40a-246">Value</span></span> |
|------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="3d40a-247">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="3d40a-247">Link-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-248">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="3d40a-248">MAPI-Id</span></span>                | \-                                                                     |
| <span data-ttu-id="3d40a-249">System-Only</span><span class="sxs-lookup"><span data-stu-id="3d40a-249">System-Only</span></span>            | <span data-ttu-id="3d40a-250">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-250">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-251">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="3d40a-251">Is-Single-Valued</span></span>       | <span data-ttu-id="3d40a-252">True</span><span class="sxs-lookup"><span data-stu-id="3d40a-252">True</span></span>                                                                   |
| <span data-ttu-id="3d40a-253">Индексируется</span><span class="sxs-lookup"><span data-stu-id="3d40a-253">Is Indexed</span></span>             | <span data-ttu-id="3d40a-254">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-254">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-255">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="3d40a-255">In Global Catalog</span></span>      | <span data-ttu-id="3d40a-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="3d40a-256">False</span></span>                                                                  |
| <span data-ttu-id="3d40a-257">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="3d40a-257">NT-Security-Descriptor</span></span> | <span data-ttu-id="3d40a-258">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="3d40a-258">O:BAG:BAD:S:</span></span>                                                           |
| <span data-ttu-id="3d40a-259">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="3d40a-259">Range-Lower</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-260">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="3d40a-260">Range-Upper</span></span>            | \-                                                                     |
| <span data-ttu-id="3d40a-261">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-261">Search-Flags</span></span>           | <span data-ttu-id="3d40a-262">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3d40a-262">0x00000000</span></span>                                                             |
| <span data-ttu-id="3d40a-263">System-Flags</span><span class="sxs-lookup"><span data-stu-id="3d40a-263">System-Flags</span></span>           | <span data-ttu-id="3d40a-264">0x00000010</span><span class="sxs-lookup"><span data-stu-id="3d40a-264">0x00000010</span></span>                                                             |
| <span data-ttu-id="3d40a-265">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="3d40a-265">Classes used in</span></span>        | [<span data-ttu-id="3d40a-266">**Центр сертификации**</span><span class="sxs-lookup"><span data-stu-id="3d40a-266">**Certification-Authority**</span></span>](c-certificationauthority.md)<br/> |



 

 





