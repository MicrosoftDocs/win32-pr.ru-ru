---
title: атрибут MS-TS-Profile-Path
description: 'Путь к профилю служб терминалов указывает перемещаемый или обязательный путь к профилю, который будет использоваться при входе пользователя на сервер терминалов. Путь к профилю указан в следующем сетевом пути: \\ \\ имя_сервера \\ профилесфолдернаме \\ имя пользователя.'
ms.assetid: 9b13f91d-c3ee-4862-800c-fda831dce859
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TS-Profile-Path
- Схема AD атрибута Мстспрофилепас
topic_type:
- apiref
api_name:
- ms-TS-Profile-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67243c2ef588bd1470a50417c0948b1ea4ea7fa9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989661"
---
# <a name="ms-ts-profile-path-attribute"></a><span data-ttu-id="bfb1c-106">атрибут MS-TS-Profile-Path</span><span class="sxs-lookup"><span data-stu-id="bfb1c-106">ms-TS-Profile-Path attribute</span></span>

<span data-ttu-id="bfb1c-107">Путь к профилю служб терминалов указывает перемещаемый или обязательный путь к профилю, который будет использоваться при входе пользователя на сервер терминалов.</span><span class="sxs-lookup"><span data-stu-id="bfb1c-107">Terminal Services Profile Path specifies a roaming or mandatory profile path to use when the user logs on to the terminal server.</span></span> <span data-ttu-id="bfb1c-108">Путь к профилю указан в следующем формате сетевого пути: **\\\\** _ServerName_ *_\\_* _профилесфолдернаме_ *_\\_* _имя пользователя_.</span><span class="sxs-lookup"><span data-stu-id="bfb1c-108">The profile path is in the following network path format: **\\\\**_ServerName_*_\\_*_ProfilesFolderName_*_\\_*_UserName_.</span></span>



| <span data-ttu-id="bfb1c-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfb1c-109">Entry</span></span> | <span data-ttu-id="bfb1c-110">Значение</span><span class="sxs-lookup"><span data-stu-id="bfb1c-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="bfb1c-111">CN</span><span class="sxs-lookup"><span data-stu-id="bfb1c-111">CN</span></span>                | <span data-ttu-id="bfb1c-112">MS-TS-Profile-Path</span><span class="sxs-lookup"><span data-stu-id="bfb1c-112">ms-TS-Profile-Path</span></span>                          |
| <span data-ttu-id="bfb1c-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="bfb1c-113">Ldap-Display-Name</span></span> | <span data-ttu-id="bfb1c-114">мстспрофилепас</span><span class="sxs-lookup"><span data-stu-id="bfb1c-114">msTSProfilePath</span></span>                             |
| <span data-ttu-id="bfb1c-115">Размер</span><span class="sxs-lookup"><span data-stu-id="bfb1c-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="bfb1c-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="bfb1c-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="bfb1c-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="bfb1c-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="bfb1c-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="bfb1c-118">Attribute-Id</span></span>      | <span data-ttu-id="bfb1c-119">1.2.840.113556.1.4.1976</span><span class="sxs-lookup"><span data-stu-id="bfb1c-119">1.2.840.113556.1.4.1976</span></span>                     |
| <span data-ttu-id="bfb1c-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="bfb1c-120">System-Id-Guid</span></span>    | <span data-ttu-id="bfb1c-121">e65c30db-316c-4060-a3a0-387b083f09cd</span><span class="sxs-lookup"><span data-stu-id="bfb1c-121">e65c30db-316c-4060-a3a0-387b083f09cd</span></span>        |
| <span data-ttu-id="bfb1c-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfb1c-122">Syntax</span></span>            | [<span data-ttu-id="bfb1c-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="bfb1c-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="bfb1c-124">Implementations</span></span>

-   [<span data-ttu-id="bfb1c-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="bfb1c-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="bfb1c-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="bfb1c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfb1c-128">Windows Server 2008</span></span>



| <span data-ttu-id="bfb1c-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfb1c-129">Entry</span></span> | <span data-ttu-id="bfb1c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bfb1c-130">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfb1c-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfb1c-131">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfb1c-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfb1c-132">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfb1c-133">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfb1c-133">System-Only</span></span>            | <span data-ttu-id="bfb1c-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-134">False</span></span>                             |
| <span data-ttu-id="bfb1c-135">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfb1c-135">Is-Single-Valued</span></span>       | <span data-ttu-id="bfb1c-136">True</span><span class="sxs-lookup"><span data-stu-id="bfb1c-136">True</span></span>                              |
| <span data-ttu-id="bfb1c-137">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfb1c-137">Is Indexed</span></span>             | <span data-ttu-id="bfb1c-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-138">False</span></span>                             |
| <span data-ttu-id="bfb1c-139">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfb1c-139">In Global Catalog</span></span>      | <span data-ttu-id="bfb1c-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-140">False</span></span>                             |
| <span data-ttu-id="bfb1c-141">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfb1c-141">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfb1c-142">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfb1c-142">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfb1c-143">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfb1c-143">Range-Lower</span></span>            | <span data-ttu-id="bfb1c-144">0</span><span class="sxs-lookup"><span data-stu-id="bfb1c-144">0</span></span>                                 |
| <span data-ttu-id="bfb1c-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfb1c-145">Range-Upper</span></span>            | <span data-ttu-id="bfb1c-146">32767</span><span class="sxs-lookup"><span data-stu-id="bfb1c-146">32767</span></span>                             |
| <span data-ttu-id="bfb1c-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfb1c-147">Search-Flags</span></span>           | <span data-ttu-id="bfb1c-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfb1c-148">0x00000000</span></span>                        |
| <span data-ttu-id="bfb1c-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfb1c-149">System-Flags</span></span>           | <span data-ttu-id="bfb1c-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfb1c-150">0x00000010</span></span>                        |
| <span data-ttu-id="bfb1c-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfb1c-151">Classes used in</span></span>        | [<span data-ttu-id="bfb1c-152">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-152">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="bfb1c-153">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bfb1c-153">Windows Server 2008 R2</span></span>



| <span data-ttu-id="bfb1c-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfb1c-154">Entry</span></span> | <span data-ttu-id="bfb1c-155">Значение</span><span class="sxs-lookup"><span data-stu-id="bfb1c-155">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfb1c-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfb1c-156">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfb1c-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfb1c-157">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfb1c-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfb1c-158">System-Only</span></span>            | <span data-ttu-id="bfb1c-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-159">False</span></span>                             |
| <span data-ttu-id="bfb1c-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfb1c-160">Is-Single-Valued</span></span>       | <span data-ttu-id="bfb1c-161">True</span><span class="sxs-lookup"><span data-stu-id="bfb1c-161">True</span></span>                              |
| <span data-ttu-id="bfb1c-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfb1c-162">Is Indexed</span></span>             | <span data-ttu-id="bfb1c-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-163">False</span></span>                             |
| <span data-ttu-id="bfb1c-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfb1c-164">In Global Catalog</span></span>      | <span data-ttu-id="bfb1c-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-165">False</span></span>                             |
| <span data-ttu-id="bfb1c-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfb1c-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfb1c-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfb1c-167">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfb1c-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfb1c-168">Range-Lower</span></span>            | <span data-ttu-id="bfb1c-169">0</span><span class="sxs-lookup"><span data-stu-id="bfb1c-169">0</span></span>                                 |
| <span data-ttu-id="bfb1c-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfb1c-170">Range-Upper</span></span>            | <span data-ttu-id="bfb1c-171">32767</span><span class="sxs-lookup"><span data-stu-id="bfb1c-171">32767</span></span>                             |
| <span data-ttu-id="bfb1c-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfb1c-172">Search-Flags</span></span>           | <span data-ttu-id="bfb1c-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfb1c-173">0x00000000</span></span>                        |
| <span data-ttu-id="bfb1c-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfb1c-174">System-Flags</span></span>           | <span data-ttu-id="bfb1c-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfb1c-175">0x00000010</span></span>                        |
| <span data-ttu-id="bfb1c-176">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfb1c-176">Classes used in</span></span>        | [<span data-ttu-id="bfb1c-177">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-177">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="bfb1c-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bfb1c-178">Windows Server 2012</span></span>



| <span data-ttu-id="bfb1c-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="bfb1c-179">Entry</span></span> | <span data-ttu-id="bfb1c-180">Значение</span><span class="sxs-lookup"><span data-stu-id="bfb1c-180">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="bfb1c-181">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="bfb1c-181">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="bfb1c-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="bfb1c-182">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="bfb1c-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="bfb1c-183">System-Only</span></span>            | <span data-ttu-id="bfb1c-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-184">False</span></span>                             |
| <span data-ttu-id="bfb1c-185">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="bfb1c-185">Is-Single-Valued</span></span>       | <span data-ttu-id="bfb1c-186">True</span><span class="sxs-lookup"><span data-stu-id="bfb1c-186">True</span></span>                              |
| <span data-ttu-id="bfb1c-187">Индексируется</span><span class="sxs-lookup"><span data-stu-id="bfb1c-187">Is Indexed</span></span>             | <span data-ttu-id="bfb1c-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-188">False</span></span>                             |
| <span data-ttu-id="bfb1c-189">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="bfb1c-189">In Global Catalog</span></span>      | <span data-ttu-id="bfb1c-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="bfb1c-190">False</span></span>                             |
| <span data-ttu-id="bfb1c-191">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="bfb1c-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="bfb1c-192">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="bfb1c-192">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="bfb1c-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="bfb1c-193">Range-Lower</span></span>            | <span data-ttu-id="bfb1c-194">0</span><span class="sxs-lookup"><span data-stu-id="bfb1c-194">0</span></span>                                 |
| <span data-ttu-id="bfb1c-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="bfb1c-195">Range-Upper</span></span>            | <span data-ttu-id="bfb1c-196">32767</span><span class="sxs-lookup"><span data-stu-id="bfb1c-196">32767</span></span>                             |
| <span data-ttu-id="bfb1c-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="bfb1c-197">Search-Flags</span></span>           | <span data-ttu-id="bfb1c-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bfb1c-198">0x00000000</span></span>                        |
| <span data-ttu-id="bfb1c-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="bfb1c-199">System-Flags</span></span>           | <span data-ttu-id="bfb1c-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="bfb1c-200">0x00000010</span></span>                        |
| <span data-ttu-id="bfb1c-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="bfb1c-201">Classes used in</span></span>        | [<span data-ttu-id="bfb1c-202">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="bfb1c-202">**User**</span></span>](c-user.md)<br/> |



 

 





