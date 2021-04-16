---
title: Атрибут ГПК-User-Extension-Names
description: Используется объектом групповая политика для политик пользователя.
ms.assetid: 3c6fa679-7597-4286-bd79-7a0030212810
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ГПК-User-Extension-Names
- Схема AD атрибута Гпкусерекстенсионнамес
topic_type:
- apiref
api_name:
- GPC-User-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12de39539af6ee523838f8081aa04a5d21b8a1d3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493515"
---
# <a name="gpc-user-extension-names-attribute"></a><span data-ttu-id="61ee6-105">Атрибут ГПК-User-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="61ee6-105">GPC-User-Extension-Names attribute</span></span>

<span data-ttu-id="61ee6-106">Используется объектом групповая политика для политик пользователя.</span><span class="sxs-lookup"><span data-stu-id="61ee6-106">Used by the Group Policy Object for user policies.</span></span>



| <span data-ttu-id="61ee6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-107">Entry</span></span> | <span data-ttu-id="61ee6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="61ee6-109">CN</span><span class="sxs-lookup"><span data-stu-id="61ee6-109">CN</span></span>                | <span data-ttu-id="61ee6-110">ГПК-User-Extensions-Names</span><span class="sxs-lookup"><span data-stu-id="61ee6-110">GPC-User-Extension-Names</span></span>                                                        |
| <span data-ttu-id="61ee6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="61ee6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="61ee6-112">гпкусерекстенсионнамес</span><span class="sxs-lookup"><span data-stu-id="61ee6-112">gPCUserExtensionNames</span></span>                                                           |
| <span data-ttu-id="61ee6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="61ee6-113">Size</span></span>              | <span data-ttu-id="61ee6-114">Зависит от числа клиентских расширений, имеющих политику в этом объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="61ee6-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="61ee6-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="61ee6-115">Update Privilege</span></span>  | <span data-ttu-id="61ee6-116">Администратор домена или политики.</span><span class="sxs-lookup"><span data-stu-id="61ee6-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="61ee6-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="61ee6-117">Update Frequency</span></span>  | <span data-ttu-id="61ee6-118">Каждый раз при обновлении объекта групповой политики с помощью ГПЕ.</span><span class="sxs-lookup"><span data-stu-id="61ee6-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="61ee6-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-119">Attribute-Id</span></span>      | <span data-ttu-id="61ee6-120">1.2.840.113556.1.4.1349</span><span class="sxs-lookup"><span data-stu-id="61ee6-120">1.2.840.113556.1.4.1349</span></span>                                                         |
| <span data-ttu-id="61ee6-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="61ee6-121">System-Id-Guid</span></span>    | <span data-ttu-id="61ee6-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="61ee6-122">42a75fc6-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="61ee6-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61ee6-123">Syntax</span></span>            | [<span data-ttu-id="61ee6-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="61ee6-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="61ee6-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="61ee6-125">Implementations</span></span>

-   [<span data-ttu-id="61ee6-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="61ee6-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="61ee6-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="61ee6-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="61ee6-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="61ee6-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="61ee6-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="61ee6-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="61ee6-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="61ee6-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="61ee6-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="61ee6-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="61ee6-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61ee6-132">Windows 2000 Server</span></span>



| <span data-ttu-id="61ee6-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-133">Entry</span></span> | <span data-ttu-id="61ee6-134">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="61ee6-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61ee6-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ee6-137">System-Only</span></span>            | <span data-ttu-id="61ee6-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-138">False</span></span>                                                               |
| <span data-ttu-id="61ee6-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61ee6-139">Is-Single-Valued</span></span>       | <span data-ttu-id="61ee6-140">True</span><span class="sxs-lookup"><span data-stu-id="61ee6-140">True</span></span>                                                                |
| <span data-ttu-id="61ee6-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61ee6-141">Is Indexed</span></span>             | <span data-ttu-id="61ee6-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-142">False</span></span>                                                               |
| <span data-ttu-id="61ee6-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61ee6-143">In Global Catalog</span></span>      | <span data-ttu-id="61ee6-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-144">False</span></span>                                                               |
| <span data-ttu-id="61ee6-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61ee6-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ee6-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61ee6-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="61ee6-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ee6-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ee6-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-149">Search-Flags</span></span>           | <span data-ttu-id="61ee6-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ee6-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="61ee6-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-151">System-Flags</span></span>           | <span data-ttu-id="61ee6-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ee6-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="61ee6-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61ee6-153">Classes used in</span></span>        | [<span data-ttu-id="61ee6-154">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="61ee6-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="61ee6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61ee6-155">Windows Server 2003</span></span>



| <span data-ttu-id="61ee6-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-156">Entry</span></span> | <span data-ttu-id="61ee6-157">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="61ee6-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61ee6-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ee6-160">System-Only</span></span>            | <span data-ttu-id="61ee6-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-161">False</span></span>                                                               |
| <span data-ttu-id="61ee6-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61ee6-162">Is-Single-Valued</span></span>       | <span data-ttu-id="61ee6-163">True</span><span class="sxs-lookup"><span data-stu-id="61ee6-163">True</span></span>                                                                |
| <span data-ttu-id="61ee6-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61ee6-164">Is Indexed</span></span>             | <span data-ttu-id="61ee6-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-165">False</span></span>                                                               |
| <span data-ttu-id="61ee6-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61ee6-166">In Global Catalog</span></span>      | <span data-ttu-id="61ee6-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-167">False</span></span>                                                               |
| <span data-ttu-id="61ee6-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61ee6-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ee6-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61ee6-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="61ee6-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ee6-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ee6-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-172">Search-Flags</span></span>           | <span data-ttu-id="61ee6-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ee6-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="61ee6-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-174">System-Flags</span></span>           | <span data-ttu-id="61ee6-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ee6-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="61ee6-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61ee6-176">Classes used in</span></span>        | [<span data-ttu-id="61ee6-177">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="61ee6-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="61ee6-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="61ee6-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="61ee6-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-179">Entry</span></span> | <span data-ttu-id="61ee6-180">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="61ee6-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61ee6-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ee6-183">System-Only</span></span>            | <span data-ttu-id="61ee6-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-184">False</span></span>                                                               |
| <span data-ttu-id="61ee6-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61ee6-185">Is-Single-Valued</span></span>       | <span data-ttu-id="61ee6-186">True</span><span class="sxs-lookup"><span data-stu-id="61ee6-186">True</span></span>                                                                |
| <span data-ttu-id="61ee6-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61ee6-187">Is Indexed</span></span>             | <span data-ttu-id="61ee6-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-188">False</span></span>                                                               |
| <span data-ttu-id="61ee6-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61ee6-189">In Global Catalog</span></span>      | <span data-ttu-id="61ee6-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-190">False</span></span>                                                               |
| <span data-ttu-id="61ee6-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61ee6-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ee6-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61ee6-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="61ee6-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ee6-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ee6-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-195">Search-Flags</span></span>           | <span data-ttu-id="61ee6-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ee6-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="61ee6-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-197">System-Flags</span></span>           | <span data-ttu-id="61ee6-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ee6-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="61ee6-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61ee6-199">Classes used in</span></span>        | [<span data-ttu-id="61ee6-200">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="61ee6-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="61ee6-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61ee6-201">Windows Server 2008</span></span>



| <span data-ttu-id="61ee6-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-202">Entry</span></span> | <span data-ttu-id="61ee6-203">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="61ee6-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61ee6-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ee6-206">System-Only</span></span>            | <span data-ttu-id="61ee6-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-207">False</span></span>                                                               |
| <span data-ttu-id="61ee6-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61ee6-208">Is-Single-Valued</span></span>       | <span data-ttu-id="61ee6-209">True</span><span class="sxs-lookup"><span data-stu-id="61ee6-209">True</span></span>                                                                |
| <span data-ttu-id="61ee6-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61ee6-210">Is Indexed</span></span>             | <span data-ttu-id="61ee6-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-211">False</span></span>                                                               |
| <span data-ttu-id="61ee6-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61ee6-212">In Global Catalog</span></span>      | <span data-ttu-id="61ee6-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-213">False</span></span>                                                               |
| <span data-ttu-id="61ee6-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61ee6-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ee6-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61ee6-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="61ee6-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ee6-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ee6-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-218">Search-Flags</span></span>           | <span data-ttu-id="61ee6-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ee6-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="61ee6-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-220">System-Flags</span></span>           | <span data-ttu-id="61ee6-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ee6-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="61ee6-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61ee6-222">Classes used in</span></span>        | [<span data-ttu-id="61ee6-223">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="61ee6-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="61ee6-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61ee6-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="61ee6-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-225">Entry</span></span> | <span data-ttu-id="61ee6-226">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="61ee6-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61ee6-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ee6-229">System-Only</span></span>            | <span data-ttu-id="61ee6-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-230">False</span></span>                                                               |
| <span data-ttu-id="61ee6-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61ee6-231">Is-Single-Valued</span></span>       | <span data-ttu-id="61ee6-232">True</span><span class="sxs-lookup"><span data-stu-id="61ee6-232">True</span></span>                                                                |
| <span data-ttu-id="61ee6-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61ee6-233">Is Indexed</span></span>             | <span data-ttu-id="61ee6-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-234">False</span></span>                                                               |
| <span data-ttu-id="61ee6-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61ee6-235">In Global Catalog</span></span>      | <span data-ttu-id="61ee6-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-236">False</span></span>                                                               |
| <span data-ttu-id="61ee6-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61ee6-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ee6-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61ee6-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="61ee6-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ee6-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ee6-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-241">Search-Flags</span></span>           | <span data-ttu-id="61ee6-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ee6-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="61ee6-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-243">System-Flags</span></span>           | <span data-ttu-id="61ee6-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ee6-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="61ee6-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61ee6-245">Classes used in</span></span>        | [<span data-ttu-id="61ee6-246">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="61ee6-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="61ee6-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="61ee6-247">Windows Server 2012</span></span>



| <span data-ttu-id="61ee6-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="61ee6-248">Entry</span></span> | <span data-ttu-id="61ee6-249">Значение</span><span class="sxs-lookup"><span data-stu-id="61ee6-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="61ee6-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="61ee6-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="61ee6-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="61ee6-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="61ee6-252">System-Only</span></span>            | <span data-ttu-id="61ee6-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-253">False</span></span>                                                               |
| <span data-ttu-id="61ee6-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="61ee6-254">Is-Single-Valued</span></span>       | <span data-ttu-id="61ee6-255">True</span><span class="sxs-lookup"><span data-stu-id="61ee6-255">True</span></span>                                                                |
| <span data-ttu-id="61ee6-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="61ee6-256">Is Indexed</span></span>             | <span data-ttu-id="61ee6-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-257">False</span></span>                                                               |
| <span data-ttu-id="61ee6-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="61ee6-258">In Global Catalog</span></span>      | <span data-ttu-id="61ee6-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="61ee6-259">False</span></span>                                                               |
| <span data-ttu-id="61ee6-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="61ee6-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="61ee6-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="61ee6-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="61ee6-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="61ee6-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="61ee6-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="61ee6-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-264">Search-Flags</span></span>           | <span data-ttu-id="61ee6-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61ee6-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="61ee6-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="61ee6-266">System-Flags</span></span>           | <span data-ttu-id="61ee6-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="61ee6-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="61ee6-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="61ee6-268">Classes used in</span></span>        | [<span data-ttu-id="61ee6-269">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="61ee6-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





