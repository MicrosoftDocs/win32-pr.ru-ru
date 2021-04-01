---
title: Атрибут ГПК-Machine-Extension-Names
description: Используется объектом групповая политика для политик компьютера.
ms.assetid: a5e00bf6-d311-4ccd-a2cf-4f7506fec419
ms.tgt_platform: multiple
keywords:
- ГПК-Machine-Extension-имя схемы AD
- Схема AD атрибута Гпкмачиникстенсионнамес
topic_type:
- apiref
api_name:
- GPC-Machine-Extension-Names
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9d9c1ce435a017bfefe88d728004f619e193f9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989740"
---
# <a name="gpc-machine-extension-names-attribute"></a><span data-ttu-id="2fb58-105">Атрибут ГПК-Machine-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="2fb58-105">GPC-Machine-Extension-Names attribute</span></span>

<span data-ttu-id="2fb58-106">Используется объектом групповая политика для политик компьютера.</span><span class="sxs-lookup"><span data-stu-id="2fb58-106">Used by the Group Policy Object for computer policies.</span></span>



| <span data-ttu-id="2fb58-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-107">Entry</span></span> | <span data-ttu-id="2fb58-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-108">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2fb58-109">CN</span><span class="sxs-lookup"><span data-stu-id="2fb58-109">CN</span></span>                | <span data-ttu-id="2fb58-110">ГПК-Machine-Extension-Names</span><span class="sxs-lookup"><span data-stu-id="2fb58-110">GPC-Machine-Extension-Names</span></span>                                                     |
| <span data-ttu-id="2fb58-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2fb58-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2fb58-112">гпкмачиникстенсионнамес</span><span class="sxs-lookup"><span data-stu-id="2fb58-112">gPCMachineExtensionNames</span></span>                                                        |
| <span data-ttu-id="2fb58-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2fb58-113">Size</span></span>              | <span data-ttu-id="2fb58-114">Зависит от числа клиентских расширений, имеющих политику в этом объекте групповой политики.</span><span class="sxs-lookup"><span data-stu-id="2fb58-114">Depends on the number of client-side extensions that have a policy in this GPO.</span></span> |
| <span data-ttu-id="2fb58-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2fb58-115">Update Privilege</span></span>  | <span data-ttu-id="2fb58-116">Администратор домена или политики.</span><span class="sxs-lookup"><span data-stu-id="2fb58-116">Domain or policy administrator.</span></span>                                                 |
| <span data-ttu-id="2fb58-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2fb58-117">Update Frequency</span></span>  | <span data-ttu-id="2fb58-118">Каждый раз при обновлении объекта групповой политики с помощью ГПЕ.</span><span class="sxs-lookup"><span data-stu-id="2fb58-118">Whenever a GPO is updated through the GPE.</span></span>                                      |
| <span data-ttu-id="2fb58-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-119">Attribute-Id</span></span>      | <span data-ttu-id="2fb58-120">1.2.840.113556.1.4.1348</span><span class="sxs-lookup"><span data-stu-id="2fb58-120">1.2.840.113556.1.4.1348</span></span>                                                         |
| <span data-ttu-id="2fb58-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2fb58-121">System-Id-Guid</span></span>    | <span data-ttu-id="2fb58-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="2fb58-122">32ff8ecc-783f-11d2-9916-0000f87a57d4</span></span>                                            |
| <span data-ttu-id="2fb58-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fb58-123">Syntax</span></span>            | [<span data-ttu-id="2fb58-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="2fb58-124">**String(Unicode)**</span></span>](s-string-unicode.md)                                     |



## <a name="implementations"></a><span data-ttu-id="2fb58-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2fb58-125">Implementations</span></span>

-   [<span data-ttu-id="2fb58-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2fb58-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2fb58-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2fb58-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2fb58-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2fb58-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2fb58-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2fb58-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2fb58-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2fb58-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2fb58-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2fb58-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2fb58-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2fb58-132">Windows 2000 Server</span></span>



| <span data-ttu-id="2fb58-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-133">Entry</span></span> | <span data-ttu-id="2fb58-134">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-134">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2fb58-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2fb58-135">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-136">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fb58-137">System-Only</span></span>            | <span data-ttu-id="2fb58-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-138">False</span></span>                                                               |
| <span data-ttu-id="2fb58-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2fb58-139">Is-Single-Valued</span></span>       | <span data-ttu-id="2fb58-140">True</span><span class="sxs-lookup"><span data-stu-id="2fb58-140">True</span></span>                                                                |
| <span data-ttu-id="2fb58-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2fb58-141">Is Indexed</span></span>             | <span data-ttu-id="2fb58-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-142">False</span></span>                                                               |
| <span data-ttu-id="2fb58-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2fb58-143">In Global Catalog</span></span>      | <span data-ttu-id="2fb58-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-144">False</span></span>                                                               |
| <span data-ttu-id="2fb58-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2fb58-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fb58-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2fb58-146">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2fb58-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fb58-147">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fb58-148">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-149">Search-Flags</span></span>           | <span data-ttu-id="2fb58-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fb58-150">0x00000000</span></span>                                                          |
| <span data-ttu-id="2fb58-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-151">System-Flags</span></span>           | <span data-ttu-id="2fb58-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fb58-152">0x00000010</span></span>                                                          |
| <span data-ttu-id="2fb58-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2fb58-153">Classes used in</span></span>        | [<span data-ttu-id="2fb58-154">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2fb58-154">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2fb58-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2fb58-155">Windows Server 2003</span></span>



| <span data-ttu-id="2fb58-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-156">Entry</span></span> | <span data-ttu-id="2fb58-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-157">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2fb58-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2fb58-158">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-159">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fb58-160">System-Only</span></span>            | <span data-ttu-id="2fb58-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-161">False</span></span>                                                               |
| <span data-ttu-id="2fb58-162">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2fb58-162">Is-Single-Valued</span></span>       | <span data-ttu-id="2fb58-163">True</span><span class="sxs-lookup"><span data-stu-id="2fb58-163">True</span></span>                                                                |
| <span data-ttu-id="2fb58-164">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2fb58-164">Is Indexed</span></span>             | <span data-ttu-id="2fb58-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-165">False</span></span>                                                               |
| <span data-ttu-id="2fb58-166">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2fb58-166">In Global Catalog</span></span>      | <span data-ttu-id="2fb58-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-167">False</span></span>                                                               |
| <span data-ttu-id="2fb58-168">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2fb58-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fb58-169">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2fb58-169">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2fb58-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fb58-170">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fb58-171">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-172">Search-Flags</span></span>           | <span data-ttu-id="2fb58-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fb58-173">0x00000000</span></span>                                                          |
| <span data-ttu-id="2fb58-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-174">System-Flags</span></span>           | <span data-ttu-id="2fb58-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fb58-175">0x00000010</span></span>                                                          |
| <span data-ttu-id="2fb58-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2fb58-176">Classes used in</span></span>        | [<span data-ttu-id="2fb58-177">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2fb58-177">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2fb58-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2fb58-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2fb58-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-179">Entry</span></span> | <span data-ttu-id="2fb58-180">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-180">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2fb58-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2fb58-181">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-182">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fb58-183">System-Only</span></span>            | <span data-ttu-id="2fb58-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-184">False</span></span>                                                               |
| <span data-ttu-id="2fb58-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2fb58-185">Is-Single-Valued</span></span>       | <span data-ttu-id="2fb58-186">True</span><span class="sxs-lookup"><span data-stu-id="2fb58-186">True</span></span>                                                                |
| <span data-ttu-id="2fb58-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2fb58-187">Is Indexed</span></span>             | <span data-ttu-id="2fb58-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-188">False</span></span>                                                               |
| <span data-ttu-id="2fb58-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2fb58-189">In Global Catalog</span></span>      | <span data-ttu-id="2fb58-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-190">False</span></span>                                                               |
| <span data-ttu-id="2fb58-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2fb58-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fb58-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2fb58-192">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2fb58-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fb58-193">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fb58-194">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-195">Search-Flags</span></span>           | <span data-ttu-id="2fb58-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fb58-196">0x00000000</span></span>                                                          |
| <span data-ttu-id="2fb58-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-197">System-Flags</span></span>           | <span data-ttu-id="2fb58-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fb58-198">0x00000010</span></span>                                                          |
| <span data-ttu-id="2fb58-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2fb58-199">Classes used in</span></span>        | [<span data-ttu-id="2fb58-200">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2fb58-200">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2fb58-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fb58-201">Windows Server 2008</span></span>



| <span data-ttu-id="2fb58-202">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-202">Entry</span></span> | <span data-ttu-id="2fb58-203">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-203">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2fb58-204">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2fb58-204">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-205">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fb58-206">System-Only</span></span>            | <span data-ttu-id="2fb58-207">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-207">False</span></span>                                                               |
| <span data-ttu-id="2fb58-208">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2fb58-208">Is-Single-Valued</span></span>       | <span data-ttu-id="2fb58-209">True</span><span class="sxs-lookup"><span data-stu-id="2fb58-209">True</span></span>                                                                |
| <span data-ttu-id="2fb58-210">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2fb58-210">Is Indexed</span></span>             | <span data-ttu-id="2fb58-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-211">False</span></span>                                                               |
| <span data-ttu-id="2fb58-212">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2fb58-212">In Global Catalog</span></span>      | <span data-ttu-id="2fb58-213">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-213">False</span></span>                                                               |
| <span data-ttu-id="2fb58-214">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2fb58-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fb58-215">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2fb58-215">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2fb58-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fb58-216">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fb58-217">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-218">Search-Flags</span></span>           | <span data-ttu-id="2fb58-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fb58-219">0x00000000</span></span>                                                          |
| <span data-ttu-id="2fb58-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-220">System-Flags</span></span>           | <span data-ttu-id="2fb58-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fb58-221">0x00000010</span></span>                                                          |
| <span data-ttu-id="2fb58-222">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2fb58-222">Classes used in</span></span>        | [<span data-ttu-id="2fb58-223">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2fb58-223">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2fb58-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2fb58-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2fb58-225">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-225">Entry</span></span> | <span data-ttu-id="2fb58-226">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-226">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2fb58-227">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2fb58-227">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-228">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fb58-229">System-Only</span></span>            | <span data-ttu-id="2fb58-230">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-230">False</span></span>                                                               |
| <span data-ttu-id="2fb58-231">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2fb58-231">Is-Single-Valued</span></span>       | <span data-ttu-id="2fb58-232">True</span><span class="sxs-lookup"><span data-stu-id="2fb58-232">True</span></span>                                                                |
| <span data-ttu-id="2fb58-233">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2fb58-233">Is Indexed</span></span>             | <span data-ttu-id="2fb58-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-234">False</span></span>                                                               |
| <span data-ttu-id="2fb58-235">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2fb58-235">In Global Catalog</span></span>      | <span data-ttu-id="2fb58-236">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-236">False</span></span>                                                               |
| <span data-ttu-id="2fb58-237">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2fb58-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fb58-238">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2fb58-238">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2fb58-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fb58-239">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fb58-240">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-241">Search-Flags</span></span>           | <span data-ttu-id="2fb58-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fb58-242">0x00000000</span></span>                                                          |
| <span data-ttu-id="2fb58-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-243">System-Flags</span></span>           | <span data-ttu-id="2fb58-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fb58-244">0x00000010</span></span>                                                          |
| <span data-ttu-id="2fb58-245">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2fb58-245">Classes used in</span></span>        | [<span data-ttu-id="2fb58-246">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2fb58-246">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2fb58-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2fb58-247">Windows Server 2012</span></span>



| <span data-ttu-id="2fb58-248">Ввод</span><span class="sxs-lookup"><span data-stu-id="2fb58-248">Entry</span></span> | <span data-ttu-id="2fb58-249">Значение</span><span class="sxs-lookup"><span data-stu-id="2fb58-249">Value</span></span> |
|------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="2fb58-250">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2fb58-250">Link-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2fb58-251">MAPI-Id</span></span>                | \-                                                                  |
| <span data-ttu-id="2fb58-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="2fb58-252">System-Only</span></span>            | <span data-ttu-id="2fb58-253">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-253">False</span></span>                                                               |
| <span data-ttu-id="2fb58-254">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2fb58-254">Is-Single-Valued</span></span>       | <span data-ttu-id="2fb58-255">True</span><span class="sxs-lookup"><span data-stu-id="2fb58-255">True</span></span>                                                                |
| <span data-ttu-id="2fb58-256">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2fb58-256">Is Indexed</span></span>             | <span data-ttu-id="2fb58-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-257">False</span></span>                                                               |
| <span data-ttu-id="2fb58-258">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2fb58-258">In Global Catalog</span></span>      | <span data-ttu-id="2fb58-259">Неверно</span><span class="sxs-lookup"><span data-stu-id="2fb58-259">False</span></span>                                                               |
| <span data-ttu-id="2fb58-260">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2fb58-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="2fb58-261">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2fb58-261">O:BAG:BAD:S:</span></span>                                                        |
| <span data-ttu-id="2fb58-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2fb58-262">Range-Lower</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2fb58-263">Range-Upper</span></span>            | \-                                                                  |
| <span data-ttu-id="2fb58-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-264">Search-Flags</span></span>           | <span data-ttu-id="2fb58-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2fb58-265">0x00000000</span></span>                                                          |
| <span data-ttu-id="2fb58-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2fb58-266">System-Flags</span></span>           | <span data-ttu-id="2fb58-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2fb58-267">0x00000010</span></span>                                                          |
| <span data-ttu-id="2fb58-268">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2fb58-268">Classes used in</span></span>        | [<span data-ttu-id="2fb58-269">**Группа-Политика-контейнер**</span><span class="sxs-lookup"><span data-stu-id="2fb58-269">**Group-Policy-Container**</span></span>](c-grouppolicycontainer.md)<br/> |



 

 





