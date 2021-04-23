---
title: MS-TS-Initial-атрибут программы
description: Начальная программа сеанса служб терминалов указывает путь и имя файла приложения, которое пользователь хочет запустить автоматически при входе пользователя на сервер терминалов.
ms.assetid: c886209b-725b-4e49-a802-58be9ed5e92e
ms.tgt_platform: multiple
keywords:
- MS-TS-Initial-схема AD атрибута программы
- Схема AD атрибута Мстсинитиалпрограм
topic_type:
- apiref
api_name:
- ms-TS-Initial-Program
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2a4796a97722f2d26142a2ff374414ca3ca1cf2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104416253"
---
# <a name="ms-ts-initial-program-attribute"></a><span data-ttu-id="def75-105">MS-TS-Initial-атрибут программы</span><span class="sxs-lookup"><span data-stu-id="def75-105">ms-TS-Initial-Program attribute</span></span>

<span data-ttu-id="def75-106">Начальная программа сеанса служб терминалов указывает путь и имя файла приложения, которое пользователь хочет запустить автоматически при входе пользователя на сервер терминалов.</span><span class="sxs-lookup"><span data-stu-id="def75-106">Terminal Services Session Initial Program specifies the path and file name of the application that the user wants to start automatically when the user logs on to the Terminal Server.</span></span>



| <span data-ttu-id="def75-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="def75-107">Entry</span></span> | <span data-ttu-id="def75-108">Значение</span><span class="sxs-lookup"><span data-stu-id="def75-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="def75-109">CN</span><span class="sxs-lookup"><span data-stu-id="def75-109">CN</span></span>                | <span data-ttu-id="def75-110">MS-TS-Initial-программа</span><span class="sxs-lookup"><span data-stu-id="def75-110">ms-TS-Initial-Program</span></span>                       |
| <span data-ttu-id="def75-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="def75-111">Ldap-Display-Name</span></span> | <span data-ttu-id="def75-112">мстсинитиалпрограм</span><span class="sxs-lookup"><span data-stu-id="def75-112">msTSInitialProgram</span></span>                          |
| <span data-ttu-id="def75-113">Размер</span><span class="sxs-lookup"><span data-stu-id="def75-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="def75-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="def75-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="def75-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="def75-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="def75-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="def75-116">Attribute-Id</span></span>      | <span data-ttu-id="def75-117">1.2.840.113556.1.4.1990</span><span class="sxs-lookup"><span data-stu-id="def75-117">1.2.840.113556.1.4.1990</span></span>                     |
| <span data-ttu-id="def75-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="def75-118">System-Id-Guid</span></span>    | <span data-ttu-id="def75-119">9201ac6f-1d69-4dfb-802e-d95510109599</span><span class="sxs-lookup"><span data-stu-id="def75-119">9201ac6f-1d69-4dfb-802e-d95510109599</span></span>        |
| <span data-ttu-id="def75-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="def75-120">Syntax</span></span>            | [<span data-ttu-id="def75-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="def75-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="def75-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="def75-122">Implementations</span></span>

-   [<span data-ttu-id="def75-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="def75-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="def75-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="def75-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="def75-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="def75-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="def75-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="def75-126">Windows Server 2008</span></span>



| <span data-ttu-id="def75-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="def75-127">Entry</span></span> | <span data-ttu-id="def75-128">Значение</span><span class="sxs-lookup"><span data-stu-id="def75-128">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="def75-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="def75-129">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="def75-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def75-130">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="def75-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="def75-131">System-Only</span></span>            | <span data-ttu-id="def75-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-132">False</span></span>                             |
| <span data-ttu-id="def75-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="def75-133">Is-Single-Valued</span></span>       | <span data-ttu-id="def75-134">True</span><span class="sxs-lookup"><span data-stu-id="def75-134">True</span></span>                              |
| <span data-ttu-id="def75-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="def75-135">Is Indexed</span></span>             | <span data-ttu-id="def75-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-136">False</span></span>                             |
| <span data-ttu-id="def75-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="def75-137">In Global Catalog</span></span>      | <span data-ttu-id="def75-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-138">False</span></span>                             |
| <span data-ttu-id="def75-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="def75-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="def75-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="def75-140">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="def75-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def75-141">Range-Lower</span></span>            | <span data-ttu-id="def75-142">0</span><span class="sxs-lookup"><span data-stu-id="def75-142">0</span></span>                                 |
| <span data-ttu-id="def75-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def75-143">Range-Upper</span></span>            | <span data-ttu-id="def75-144">32767</span><span class="sxs-lookup"><span data-stu-id="def75-144">32767</span></span>                             |
| <span data-ttu-id="def75-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def75-145">Search-Flags</span></span>           | <span data-ttu-id="def75-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def75-146">0x00000000</span></span>                        |
| <span data-ttu-id="def75-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def75-147">System-Flags</span></span>           | <span data-ttu-id="def75-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="def75-148">0x00000010</span></span>                        |
| <span data-ttu-id="def75-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="def75-149">Classes used in</span></span>        | [<span data-ttu-id="def75-150">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="def75-150">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="def75-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="def75-151">Windows Server 2008 R2</span></span>



| <span data-ttu-id="def75-152">Ввод</span><span class="sxs-lookup"><span data-stu-id="def75-152">Entry</span></span> | <span data-ttu-id="def75-153">Значение</span><span class="sxs-lookup"><span data-stu-id="def75-153">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="def75-154">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="def75-154">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="def75-155">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def75-155">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="def75-156">System-Only</span><span class="sxs-lookup"><span data-stu-id="def75-156">System-Only</span></span>            | <span data-ttu-id="def75-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-157">False</span></span>                             |
| <span data-ttu-id="def75-158">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="def75-158">Is-Single-Valued</span></span>       | <span data-ttu-id="def75-159">True</span><span class="sxs-lookup"><span data-stu-id="def75-159">True</span></span>                              |
| <span data-ttu-id="def75-160">Индексируется</span><span class="sxs-lookup"><span data-stu-id="def75-160">Is Indexed</span></span>             | <span data-ttu-id="def75-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-161">False</span></span>                             |
| <span data-ttu-id="def75-162">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="def75-162">In Global Catalog</span></span>      | <span data-ttu-id="def75-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-163">False</span></span>                             |
| <span data-ttu-id="def75-164">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="def75-164">NT-Security-Descriptor</span></span> | <span data-ttu-id="def75-165">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="def75-165">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="def75-166">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def75-166">Range-Lower</span></span>            | <span data-ttu-id="def75-167">0</span><span class="sxs-lookup"><span data-stu-id="def75-167">0</span></span>                                 |
| <span data-ttu-id="def75-168">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def75-168">Range-Upper</span></span>            | <span data-ttu-id="def75-169">32767</span><span class="sxs-lookup"><span data-stu-id="def75-169">32767</span></span>                             |
| <span data-ttu-id="def75-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def75-170">Search-Flags</span></span>           | <span data-ttu-id="def75-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def75-171">0x00000000</span></span>                        |
| <span data-ttu-id="def75-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def75-172">System-Flags</span></span>           | <span data-ttu-id="def75-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="def75-173">0x00000010</span></span>                        |
| <span data-ttu-id="def75-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="def75-174">Classes used in</span></span>        | [<span data-ttu-id="def75-175">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="def75-175">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="def75-176">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="def75-176">Windows Server 2012</span></span>



| <span data-ttu-id="def75-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="def75-177">Entry</span></span> | <span data-ttu-id="def75-178">Значение</span><span class="sxs-lookup"><span data-stu-id="def75-178">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="def75-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="def75-179">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="def75-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="def75-180">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="def75-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="def75-181">System-Only</span></span>            | <span data-ttu-id="def75-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-182">False</span></span>                             |
| <span data-ttu-id="def75-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="def75-183">Is-Single-Valued</span></span>       | <span data-ttu-id="def75-184">True</span><span class="sxs-lookup"><span data-stu-id="def75-184">True</span></span>                              |
| <span data-ttu-id="def75-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="def75-185">Is Indexed</span></span>             | <span data-ttu-id="def75-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-186">False</span></span>                             |
| <span data-ttu-id="def75-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="def75-187">In Global Catalog</span></span>      | <span data-ttu-id="def75-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="def75-188">False</span></span>                             |
| <span data-ttu-id="def75-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="def75-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="def75-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="def75-190">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="def75-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="def75-191">Range-Lower</span></span>            | <span data-ttu-id="def75-192">0</span><span class="sxs-lookup"><span data-stu-id="def75-192">0</span></span>                                 |
| <span data-ttu-id="def75-193">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="def75-193">Range-Upper</span></span>            | <span data-ttu-id="def75-194">32767</span><span class="sxs-lookup"><span data-stu-id="def75-194">32767</span></span>                             |
| <span data-ttu-id="def75-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="def75-195">Search-Flags</span></span>           | <span data-ttu-id="def75-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="def75-196">0x00000000</span></span>                        |
| <span data-ttu-id="def75-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="def75-197">System-Flags</span></span>           | <span data-ttu-id="def75-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="def75-198">0x00000010</span></span>                        |
| <span data-ttu-id="def75-199">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="def75-199">Classes used in</span></span>        | [<span data-ttu-id="def75-200">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="def75-200">**User**</span></span>](c-user.md)<br/> |



 

 





